---
title: "backup_chain_cosmos_db"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/backup_chain_cosmos_db.html"
last_updated: "3/19/2025"
product_version: "8.0.1.202"
---


In this article

If you enable backup to a repository for a backup policy, Veeam Backup for Microsoft Azure creates a new backup for the database of each processed Cosmos DB for PostgreSQL or Cosmos DB for MongoDB account in a standard repository during every backup session. A sequence of backups created during a set of backup sessions makes up a regular backup chain.

Each Cosmos DB for PostgreSQL or Cosmos DB for MongoDB backup in the backup chain contains metadata that stores information about the protected instance, the backup policy that created the backup, as well as the date, time and configured retention settings. Veeam Backup for Microsoft Azure uses metadata to identify outdated backups, to retrieve information on the source database configuration during recovery operations, and so on.

|  |
| --- |
| Note |
| The [forever forward incremental backup](backup_chain_vm.md) method is not implemented for Cosmos DB for PostgreSQL and Cosmos DB for MongoDB accounts — during every backup session, Veeam Backup for Microsoft Azure creates a full backup in the regular backup chain. |

The period of time during which Cosmos DB for PostgreSQL and Cosmos DB for MongoDB backups are kept in the backup chain is defined by retention policy settings. For details, see [Cosmos DB Backup Retention](cosmos_db_backup_retention.md).

Related Topics

* [Archive Backup Chain](archive_chain_cosmos_db.md)
* [Cosmos DB Backup Retention](cosmos_db_backup_retention.md)

Page updated 3/19/2025

Page content applies to build 8.0.1.202
