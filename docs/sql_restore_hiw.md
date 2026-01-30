---
title: "SQL Restore"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/sql_restore_hiw.html"
last_updated: "9/5/2024"
product_version: "8.0.1.202"
---

# SQL Restore


To restore an Azure SQL database from a backup, Veeam Backup for Microsoft Azure performs the following steps:

1. [Applies only if you perform restore from an archived backup] Retrieves data from the archived restore point.
2. Launches a worker instance in the Azure region where the SQL Server that will host the restored database resides.
3. Creates an empty database on the target SQL Server using the Azure REST API.
4. Restores backed-up data to a BACPAC file on the worker instance.
5. Imports data from the BACPAC file to the created database.
6. Performs consistency checks for the restored database.
7. Deallocates the worker instance.

1. [Applies only if you perform restore to the original location and if the source database is still present in the location] Renames the restored database and then removes the source database from the SQL Server.

To learn how to restore an entire Azure SQL database from a backup, see [SQL Restore](sql_restore.md).


