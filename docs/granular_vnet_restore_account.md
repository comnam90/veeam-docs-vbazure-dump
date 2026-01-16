---
title: "granular_vnet_restore_account"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/granular_vnet_restore_account.html"
last_updated: "9/11/2024"
product_version: "8.0.1.202"
---


In this article

At the Account step of the wizard, choose a service account whose permissions will be used to perform the restore operation. To do that, click the link to the right of Service account and choose the necessary account from the list. The specified service account must be assigned permissions listed in section [Virtual Network Configuration Permissions](vnet_permissions.md#restore).

For a service account to be displayed in the list of available accounts, it must be added to Veeam Backup for Microsoft Azure and assigned the Virtual Network Restore operational role as described in section [Adding Service Accounts](service_account_add.md).

|  |
| --- |
| Important |
| It is recommended that you check whether the selected service account has all the permissions required to perform the operation. If the service account permissions are insufficient, the restore operation will fail to complete successfully. To run the service account permission check, follow the instructions provided in section [Checking Service Account Permissions](service_account_check.md). |

[![Selecting Service Account for Virtual Network Configuration Granular Restore](images/vnet_restore_granular_account.webp)](images/vnet_restore_granular_account.webp "Selecting Service Account for Virtual Network Configuration Granular Restore")

Page updated 9/11/2024

Page content applies to build 8.0.1.202
