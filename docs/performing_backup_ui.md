---
title: "performing_backup_ui"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/performing_backup_ui.html"
last_updated: "2/18/2025"
product_version: "8.0.1.202"
---


In this article

Veeam Backup for Microsoft Azure runs backup policies for every data protection operation. A backup policy is a collection of settings that define the way backup operations are performed: what data to back up, where to store backups, when to start the backup process, and so on.

One backup policy can be used to process multiple resources within different regions, but you can back up each resource with one backup policy at a time. For example, if an instance is added to more than one backup policy, it will be processed only by a backup policy that has the highest priority. For information on how to set a priority for a backup policy, see section [Setting Backup Policy Priority](backup_policy_priority.md). Other backup policies will skip this instance from processing.

Page updated 2/18/2025

Page content applies to build 8.0.1.202
