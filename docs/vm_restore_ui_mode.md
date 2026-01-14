---
title: "vm_restore_ui_mode"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/vm_restore_ui_mode.html"
last_updated: "8/20/2025"
product_version: "8.0.1.202"
---


In this article

At the Restore Mode step of the wizard, choose whether you want to restore the selected Azure VM to the original or to a custom location.

If you select the Restore to a new location, or with different settings option, you must also select an Azure subscription and an Azure region in which the restored Azure VM will reside:

1. Click the link in the Subscription field. Then, select the necessary subscription in the Choose subscription window.

For a subscription to be displayed in the list of available subscriptions, it must be [created in Microsoft Azure](https://learn.microsoft.com/en-us/azure/cost-management-billing/manage/create-subscription) and [associated with the Microsoft Entra tenant](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/active-directory-how-subscriptions-associated-directory) to which the service account specified at [step 3](vm_restore_ui_service_account.md) belongs.

1. Click the link in the Region field. Then, select the necessary Azure region in the Choose region window.

|  |
| --- |
| Note |
| Data transfer to a new location may require additional costs and may take more time to complete. |

[![Restoring Azure VM](images/restore_vm_mode.webp)](images/restore_vm_mode.webp "Restoring Azure VM")

Page updated 8/20/2025

Page content applies to build 8.0.1.202
