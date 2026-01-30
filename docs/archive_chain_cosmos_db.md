---
title: "Archive Backup Chain"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/archive_chain_cosmos_db.html"
last_updated: "3/19/2025"
product_version: "8.0.1.202"
---

# Archive Backup Chain


If you enable backup archiving for a backup policy, Veeam Backup for Microsoft Azure creates a new backup in an archive repository during every archive session. A sequence of backups created during a set of archive sessions makes up an archive backup chain.

|  |
| --- |
| Note |
| The forever forward incremental backup method is not implemented for Cosmos DB for PostgreSQL and Cosmos DB for MongoDB accounts — during every archive session, Veeam Backup for Microsoft Azure creates a full backup in the regular backup chain (that is, every incremental backup contains the full database data set). |

The period of time during which Cosmos DB for PostgreSQL and Cosmos DB for MongoDB backups are kept in the archive backup chain is defined by retention policy settings. For details, see [Cosmos DB Backup Retention](cosmos_db_backup_retention.md).


