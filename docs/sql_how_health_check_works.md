---
title: "sql_how_health_check_works"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/sql_how_health_check_works.html"
last_updated: "9/16/2025"
product_version: "8.0.1.202"
---


In this article

When Veeam Backup for Microsoft Azure saves a new backup restore point to a repository, it calculates CRC values for metadata in the backup chain and saves these values to the chain metadata, together with the instance data. When performing a health check, Veeam Backup for Microsoft Azure verifies the availability of data blocks and uses the saved values to ensure that the restore points being verified are consistent.

If you have enabled health checks for the backup policy, Veeam Backup for Microsoft Azure performs the following operations at the day scheduled for a health check to run:

1. As soon as a backup policy session completes successfully, Veeam Backup for Microsoft Azure starts the health check as a new session. For each restore point in the standard backup chain, Veeam Backup for Microsoft Azure calculates CRC values for backup metadata and compares them with the CRC values that were previously saved to the restore point. Veeam Backup for Microsoft Azure also checks whether data blocks that are required to rebuild the restore point are available.

If the backup policy session completes with an error, Veeam Backup for Microsoft Azure tries to run the backup policy again, taking into account the maximum number of retries specified in the [automatic retry settings](sql_backup_retry_notifications.md#retry). After the first successful retry (or after the last one out of the maximum number of retries), Veeam Backup for Microsoft Azure starts the health check.

1. If Veeam Backup for Microsoft Azure does not detect data inconsistency, the health check session completes successfully. Otherwise, the session completes with an error.

Depending on the detected data inconsistency, Veeam Backup for Microsoft Azure performs the following operations:

* If the health check detects corrupted metadata in a full or incremental restore point, Veeam Backup for Microsoft Azure marks the backup chain as corrupted in the configuration database. During the next backup policy session, Veeam Backup for Microsoft Azure copies the full instance image, creates a full restore point in the repository and starts a new backup chain in the repository.

|  |
| --- |
| Note |
| Veeam Backup for Microsoft Azure does not support metadata check for encrypted backup chains. |

* If the health check detects corrupted disk blocks in a full or an incremental restore point, Veeam Backup for Microsoft Azure marks the restore point that includes the corrupted data blocks and all subsequent incremental restore points as incomplete in the configuration database. During the next backup policy session, Veeam Backup for Microsoft Azure copies not only those data blocks that have changed since the previous backup session but also data blocks that have been corrupted, and saves these data blocks to the latest restore point that has been created during the current session.

Page updated 9/16/2025

Page content applies to build 8.0.1.202
