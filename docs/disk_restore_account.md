---
title: "Step 3. Select Service Account"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/disk_restore_account.html"
last_updated: "1/27/2025"
product_version: "8.0.1.202"
---

# Step 3. Select Service Account


At the Account step of the wizard, select a service account whose permissions Veeam Backup for Microsoft Azure will use to perform the restore operation.

1. Click Select account.
2. In the Choose account window, select the necessary account and click Apply. The specified service account must be assigned permissions listed in section [Azure VM Permissions](vm_permissions.md#restore).

For a service account to be displayed in the list of available accounts, it must be added to Veeam Backup for Microsoft Azure and assigned the Azure VMs Restore operational role as described in section [Adding Service Accounts](service_account_add.md). If you have not added the necessary service account to Veeam Backup for Microsoft Azure beforehand, you can do it without closing the Restore Disks wizard. To do that, click Add and complete the Add Account wizard.

[![Performing Disk Restore](images/restoring_disk_account.webp)](images/restoring_disk_account.webp "Performing Disk Restore")


