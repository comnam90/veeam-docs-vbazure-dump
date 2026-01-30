---
title: "Performing VM Backup"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/performing_vm_backup.html"
last_updated: "1/13/2026"
product_version: "8.0.1.202"
---

# Performing VM Backup


One backup policy can be used to process one or more Azure VMs within one Microsoft Entra tenant. The scope of data that you can protect in a tenant is limited by permissions of a service account that is specified in the backup policy settings.

Before you create an Azure VM backup policy, keep in mind the following considerations:

* If you plan to create image-level backups of Azure VMs, backup infrastructure components that will take part in the backup process must be added to the backup infrastructure and configured properly. These include [repositories](repositories.md) and [worker instances](workers.md).

* If you plan to create transactionally consistent snapshots of Azure VMs, make sure these VMs have the [Azure Windows VM Agent](https://learn.microsoft.com/en-us/azure/virtual-machines/extensions/agent-windows) (for Windows-based VMs) or [Azure Linux VM Agent](https://learn.microsoft.com/en-us/azure/virtual-machines/extensions/agent-linux) (for Linux-based VMs) installed. The same applies if you plan to use any restore points produced for these VMs to perform file-level recovery to the original location.

* If you plan to receive email notifications on backup policy results, configure email notification settings first. For more information, see [Configuring Global Notification Settings](configuring_notification_settings.md).
* Configure policy templates that will be used by SLA-based backup policies. For more information, see [Managing SLA and Storage Templates](sla_storage_manage.md).

To schedule data protection tasks to run automatically, create backup policies. For each protected Azure VM, you can also [take a cloud-native snapshot manually](creating_vm_snapshots_manually.md) when needed.


