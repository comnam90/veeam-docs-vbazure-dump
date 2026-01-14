---
title: "sql_restore_ui_service_account"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/sql_restore_ui_service_account.html"
last_updated: "1/28/2025"
product_version: "8.0.1.202"
---


In this article

At the Account step of the wizard, select a service account whose permissions Veeam Backup for Microsoft Azure will use to perform the restore operation.

1. Click Choose account.
2. In the Choose service account window, select the necessary account and click Apply. The specified service account must be assigned permissions listed in section [Azure SQL Permissions](sql_permissions.md#restore).

For a service account to be displayed in the list of available accounts, it must be added to Veeam Backup for Microsoft Azure and assigned the Azure SQL Restore operational role as described in section [Adding Service Accounts](service_account_add.md). If you have not added the necessary service account to Veeam Backup for Microsoft Azure beforehand, you can do it without closing the SQL Database Restore wizard. To do that, click Add and complete the Add Account wizard.

[![Performing SQL Restore](images/sql_restore_account.webp)](images/sql_restore_account.webp "Performing SQL Restore")

Page updated 1/28/2025

Page content applies to build 8.0.1.202
