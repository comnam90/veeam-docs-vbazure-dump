---
title: "configuration_restore_ui"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/configuration_restore_ui.html"
last_updated: "3/24/2025"
product_version: "8.0.1.202"
---


In this article

To restore the configuration database of a backup appliance using the Veeam Backup for Microsoft Azure Web UI, do the following:

1. [Launch the Configuration Restore wizard](configuration_restore_ui_wizard.md).
2. [Choose a backup file](configuration_restore_ui_file.md).
3. [Review the backup file info](configuration_restore_ui_info.md).
4. [Choose restore options](configuration_restore_ui_options.md).
5. [Track the restore progress](configuration_restore_ui_progress.md).
6. [View the results of verification steps](configuration_restore_ui_check.md).
7. [Finish working with the wizard](configuration_restore_ui_finish.md).

|  |
| --- |
| Important |
| * Before you start the restore process, stop all policies that are currently running.  * If the backup appliance to which you plan to restore the configuration database is managed by a Veeam Backup & Replication server, you will not be able to restore the configuration of Veeam Backup for Microsoft Azure from the Web UI. In this case, you can perform configuration restore using the Veeam Backup & Replication console as described in section [Restoring Configuration Data Using Console](configuration_restore_console.md). * If the backup appliance whose configuration database you plan to restore used the Azure Service Bus messaging service, you must switch to the Azure Queue Storage service immediately after the restore operation is complete. For more information, see [Configuring Deployment Mode](deployment_mode.md). |

After Veeam Backup for Microsoft Azure performs configuration restore, it rescans the whole infrastructure to detect obsolete snapshots. These snapshots are then removed from the configuration database according to the specified [global retention settings](configuring_global_retention_settings.md).

Page updated 3/24/2025

Page content applies to build 8.0.1.202
