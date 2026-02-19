---
title: "Specifying Weekly Schedule"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/vm_schedule_weekly.html"
last_updated: "2/17/2026"
product_version: "8.0.1.202"
---

# Specifying Weekly Schedule


To create a weekly schedule for the backup policy, do the following at the Schedule step of the wizard:

1. Set the Weekly retention toggle to On and click Edit Weekly Settings.
2. In the Weekly schedule window, select days of the week when the backup policy will create cloud-native snapshots and image-level backups. Use the Create restore points at drop-down list to schedule a specific time for the backup policy to run.

|  |
| --- |
| Note |
| Veeam Backup for Microsoft Azure does not create image-level backups independently from cloud-native snapshots. That is why when you select days for image-level backups, the same days are automatically selected for cloud-native snapshots. To learn how Veeam Backup for Microsoft Azure performs backup operations, see [Protecting Azure VMs](overview_vm.md). |

1. In the Weekly retention section, configure retention policy settings for the weekly schedule:

* For cloud-native snapshots, specify the number of restore points that you want to keep in a snapshot chain.

If the restore point limit is exceeded, Veeam Backup for Microsoft Azure removes the earliest restore point from the chain. For more information, see [VM Snapshot Retention](vm_snapshot_retention.md).

* For image-level backups, specify the number of days (or months) for which you want to keep restore points in a backup chain.

If a restore point is older than the specified time limit, Veeam Backup for Microsoft Azure removes the restore point from the chain. For more information, see [VM Backup Retention](vm_backup_retention.md).

1. In the Repository section, select a repository where the created image-level backups will be stored.

For a repository to be displayed in the Repository list, it must be added to Veeam Backup for Microsoft Azure as described in section [Adding Backup Repositories](repository_add_ui.md) or [Adding Storage Vaults](repository_vdc_add_ui.md).

1. To save changes made to the backup policy settings, click Apply.

|  |
| --- |
| Tip |
| Veeam Backup for Microsoft Azure will start applying the configured retention settings as soon as the backup policy produces restore points. Even if you disable the daily schedule after the restore points are created, the retention policy will still be applied to these restore points. As a workaround, you can modify the configured retention settings. |

Considerations and Limitations

When you configure retention policy settings, consider the following:

* For Veeam Backup for Microsoft Azure to be able to use the [Changed Block Tracking](changed_block_tracking.md) (CBT) mechanism when processing Azure VM data, you must keep at least one cloud-native snapshot in the snapshot chain.

To learn how the CBT mechanism works, see [Changed Block Tracking](changed_block_tracking.md).

* Regardless of the number of restore points that you specify, Veeam Backup for Microsoft Azure permanently retains an additional cloud-native snapshot in the chain by design, which is required for proper CBT functioning.
* Veeam Backup for Microsoft Azure prioritizes [global retention settings](configuring_global_retention.md) over retention settings configured for backup policies. If snapshots produced by a backup policy are older than the global retention period, these snapshots will be removed anyway.

[![Adding Backup Policy](images/policy_weekly.webp)](images/policy_weekly.webp "Adding Backup Policy")


