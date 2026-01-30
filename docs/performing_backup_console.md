---
title: "Performing Backup Using Console"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/performing_backup_console.html"
last_updated: "9/9/2025"
product_version: "8.0.1.202"
---

# Performing Backup Using Console


Veeam Backup for Microsoft Azure runs backup policies for every data protection operation. A backup policy is a collection of settings that define the way backup operations are performed: what data to back up, where backups will be stored, when the backup process will start, and so on.

You can create multiple backup policies for Azure resources. One backup policy can be used to process multiple resources within different regions, but you can back up each resource with one backup policy at a time. For example, if an instance is added to more than one backup policy, it will be processed only by a backup policy that has the highest priority. Other backup policies will skip this instance from processing. For information on how to set a priority for a backup policy, see section [Setting Backup Policy Priority](backup_policy_priority.md).

After you install Veeam Plug-in for Microsoft Azure and add backup appliances to the backup infrastructure, you can manage backup policies directly from the Veeam Backup & Replication console.


