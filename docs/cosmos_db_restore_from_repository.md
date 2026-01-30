---
title: "Performing Restore From Repository"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/cosmos_db_restore_from_repository.html"
last_updated: "3/25/2025"
product_version: "8.0.1.202"
---

# Performing Restore From Repository


In case a disaster strikes, you can restore the database of a Cosmos DB for PostgreSQL account or databases and collections of a Cosmos DB for MongoDB account from a backup stored in a repository. Veeam Backup for Microsoft Azure allows you to restore one database at a time, to the original or to a new location.

Before You Begin

Consider the following prerequisites:

* To restore a database from a backup that is stored in an archive repository, you must retrieve the archived data first. You can either retrieve the archived data manually before you begin the restore operation, or launch the data retrieval process right from the restore wizard. To learn how to retrieve data manually, see [Retrieving Data from Archive](retrieving_cosmos_db_data.md).
* If you plan to restore databases and collections of a Cosmos DB for MongoDB account, make sure that the MongoDB version of the target account to which you want to restore the data is not earlier than the MongoDB version of the source account that originally managed these databases and collections.

How to Perform Cosmos DB Restore

To restore the database of a Cosmos DB for PostgreSQL account or databases and collections of a Cosmos DB for MongoDB account, do the following:

1. [Launch the Cosmos DB Restore wizard](cosmos_db_restore_from_repository_wizard.md).
2. [Select a restore point](cosmos_db_restore_from_repository_point.md).
3. [Select a service account](cosmos_db_restore_from_repository_service_account.md).
4. [Specify data retrieval settings](cosmos_db_restore_from_repository_retrieve.md).
5. [Configure restore settings](cosmos_db_restore_from_repository_settings.md).
6. [Specify a restore reason](cosmos_db_restore_from_repository_reason.md).
7. [Finish working with the wizard](cosmos_db_restore_from_repository_finish.md).


