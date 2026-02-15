---
title: "Deployment"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/deploying_vb.html"
last_updated: "2/13/2026"
product_version: "8.0.1.202"
---

# Deployment


To deploy Veeam Backup for Microsoft Azure, do the following:

1. Deploy the backup server as described in the Veeam Backup & Replication User Guide, sections [Installing Veeam Backup & Replication](https://helpcenter.veeam.com/docs/backup/vsphere/install_vbr.html?ver=120) and [Veeam Software Appliance Installation](https://helpcenter.veeam.com/docs/vbr/userguide/deployment_linux.html?ver=13).

Alternatively, you can use a backup server that already exists in your backup infrastructure if it meets the Veeam Plug-in for Microsoft Azure [system requirements](system_requirements.md).

1. [Install Veeam Plug-in for Microsoft Azure on the backup server](installing_plug_in.md).

This step applies only to Veeam Backup & Replication versions prior to 12. Version 12 (and later) comes with Veeam Plug-in for Microsoft Azure pre-installed by default.

1. [Deploy a backup appliance in Microsoft Azure](deploying_appliance.md).

|  |
| --- |
| Important |
| If you install the backup server as described in section Veeam Software Appliance Installation, you will not be able to access the Veeam Backup for Microsoft Azure functionality from the Veeam Backup & Replication Web UI. To work around the issue, [install a remote Veeam Backup & Replication console](https://helpcenter.veeam.com/docs/vbr/userguide/install_console.html?ver=13) — and then log in to the console using the name or IP address of the backup server. For more information, see the Veeam Backup & Replication User Guide, section [Logging in to Veeam Backup & Replication](https://helpcenter.veeam.com/docs/vbr/userguide/logon_to_console.html?ver=13). |

Related Topics

* [Failure and Recovery](failure_recovery.md)
* [Uninstalling Backup Appliances Deployed from Microsoft Azure Marketplace](uninstalling_vb.md)


