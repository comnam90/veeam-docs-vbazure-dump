---
title: "cosmos_db_restore_from_repository_service_account"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/cosmos_db_restore_from_repository_service_account.html"
last_updated: "5/30/2025"
product_version: "8.0.1.202"
---


In this article

At the Account step of the wizard, select a service account whose permissions Veeam Backup for Microsoft Azure will use to perform the restore operation.

1. Click Choose account.
2. In the Choose account window, select the necessary account and click Apply. The specified service account must be assigned permissions listed in section [Cosmos DB Permissions](cosmos_db_permissions.md#restore).

For a service account to be displayed in the list of available accounts, it must be added to Veeam Backup for Microsoft Azure and assigned the Cosmos DB Restore operational role as described in section [Adding Service Accounts](service_account_add.md). If you have not added the necessary service account to Veeam Backup for Microsoft Azure beforehand, you can do it without closing the Cosmos DB Restore wizard. To do that, click Add and complete the Add Account wizard.

[![Selecting Service Account](images/cosmos_db_restore_from_repository_service_account.webp)](images/cosmos_db_restore_from_repository_service_account.webp "Selecting Service Account")

Page updated 5/30/2025

Page content applies to build 8.0.1.202
