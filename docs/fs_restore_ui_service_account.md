---
title: "fs_restore_ui_service_account"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/fs_restore_ui_service_account.html"
last_updated: "8/12/2024"
product_version: "8.0.1.202"
---


In this article

At the Account step of the wizard, select a service account whose permissions Veeam Backup for Microsoft Azure will use to perform the restore operation.

1. Click Choose account.
2. In the Choose service account window, select the necessary account and click Apply. The specified service account must be assigned permissions listed in section [Azure Files Permissions](fs_permissions.md).

For a service account to be displayed in the list of available accounts, it must be added to Veeam Backup for Microsoft Azure and assigned the Azure Files Snapshot and Restore operational role as described in section [Adding Service Accounts](service_account_add.md). If you have not added the necessary service account to Veeam Backup for Microsoft Azure beforehand, you can do it without closing the Azure Files File-Level Recovery wizard. To do that, click Add and complete the Add Account wizard.

[![Performing File Share Restore](images/fs_restore_account.webp)](images/fs_restore_account.webp "Performing File Share Restore")

Page updated 8/12/2024

Page content applies to build 8.0.1.202
