---
title: "app_pne_second_policy_run"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/app_pne_second_policy_run.html"
last_updated: "5/7/2025"
product_version: "8.0.1.202"
---


In this article

[This step applies only if you chose to create and manage the private DNS zones manually at [step 1](app_pne_dns_zones.md)]

To allow Veeam Backup for Microsoft Azure to finalize the private network deployment configuration, run the schedule-based backup policy created at [step 5](app_pne_first_policy_run.md) once again.

Consider that the backup policy is launched at this step only to automatically create and configure Veeam disk access resources that will further be used for backup operations. As soon as Veeam Backup for Microsoft Azure performs the necessary configuration steps, the policy will fail as some additional manual configuration actions with the disk access resources will still be required. For more information, see [Configuring Disk Access Settings](app_pne_disk_access.md).

Related Topics

[Performing VM Backup](performing_vm_backup.md)

Page updated 5/7/2025

Page content applies to build 8.0.1.202
