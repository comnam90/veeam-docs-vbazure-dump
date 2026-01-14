---
title: "sla_calculation"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/sla_calculation.html"
last_updated: "10/20/2025"
product_version: "8.0.1.202"
---


In this article

To estimate SLA compliance for an SLA-based backup policy, Veeam Backup for Microsoft Azure performs the following steps:

1. Calculates the SLA compliance ratio individually for each Azure VM added to the backup scope. The SLA compliance ratio equals a percentage of restore points successfully created for the VM out of the total number of restore points expected to be produced by the SLA-based backup policy for this VM.

When calculating the SLA compliance ratio for daily, weekly and monthly restore points, Veeam Backup for Microsoft Azure takes into account [snapshot and backup settings](sla_add.md) configured while creating the SLA template that is assigned to the SLA-based backup policy.

1. Uses the ratios calculated at step 1 to determine the average SLA compliance ratio for the policy.
2. Compares the average SLA compliance ratio calculated at step 2 and the target SLA value configured for the policy. If the average SLA compliance ratio equals or is greater than the target SLA value, Veeam Backup for Microsoft Azure marks this policy as meeting SLA standards.

Impact of Backup Scope Changes on SLA Compliance Estimation

When calculating the SLA compliance ratio for each Azure VM added to the backup scope of an SLA-based backup policy, Veeam Backup for Microsoft Azure estimates the total number of restore points expected to be produced for this VM based on the number of policy sessions remaining at the time when the VM was added to the backup scope. This means that when a [new Azure VM is added](vm_sla_source_settings.md#resources) to the backup scope (either manually or automatically) during the time period between the currently selected and the next entry on the SLA Compliance Overview chart, Veeam Backup for Microsoft Azure considers all the preceding policy sessions as completed successfully for this VM.

Consider the following example. You configure an SLA-based backup policy to create daily backups every 1 hour between 10:00 AM and 6:00 PM, meaning that the total number of backups expected to be produced for all Azure VMs already included in the backup scope equals 8 per day. At 12:30 PM (after the 3rd backup session ends), you add a new VM to the backup scope, while the remaining number of backups expected to be produced equals 5. As soon as Veeam Backup for Microsoft Azure finalizes the [backup window](snapshot_backup_window.md) in all the protected regions, 3 backups that were to be produced during the first 3 backup sessions will be considered as created successfully — and the SLA compliance ratio for the newly added VM will be calculated depending on the results of the last 5 sessions:

* If Veeam Backup for Microsoft Azure successfully creates 5 backups (one per each of these 5 sessions), the SLA compliance ratio will equal (3 + 5) / 8 \* 100% = 100% for the VM.
* If Veeam Backup for Microsoft Azure successfully creates only 3 backups (meaning that 2 out of these 5 sessions fail to complete successfully), the SLA compliance ratio will equal (3 + 3) / 8 \* 100% = 75% for the VM.

Impact of SLA Template Changes on SLA Compliance Estimation

Veeam Backup for Microsoft Azure estimates SLA compliance for each SLA-based backup policy based on the schedule settings configured for the SLA template that is assigned to this policy. When you modify snapshot or backup settings for an SLA template or assign another template to an SLA-based backup policy, this affects the SLA compliance ratio retrospectively — meaning that Veeam Backup for Microsoft Azure recalculates the SLA compliance ratio for all entries on the SLA Compliance Overview chart.

For example, if an SLA-based backup policy configured to produce daily snapshots every 2 hours between 10:00 AM and 2:00 PM successfully creates 2 snapshots on time, this means that the SLA compliance ratio will be 100%. If you reconfigure the policy to produce daily snapshots every 1 hour between 10:00 AM and 2:00 PM, and if the policy successfully creates 4 snapshots on time, this means that the SLA compliance ratio will change to 50% on the SLA Compliance Overview chart.

|  |
| --- |
| Important |
| Modifying snapshot or backup settings for an SLA template or assigning another template to an SLA-based backup policy may cause Veeam Backup for Microsoft Azure to incorrectly calculate the SLA compliance ratio for the policy on the day when this modification is made. To learn how to edit SLA template settings, see [Managing SLA Templates](sla_edit.md). |

Page updated 10/20/2025

Page content applies to build 8.0.1.202
