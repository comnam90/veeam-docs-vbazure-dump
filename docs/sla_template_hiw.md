---
title: "sla_template_hiw"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/sla_template_hiw.html"
last_updated: "1/13/2026"
product_version: "8.0.1.202"
---


In this article

An SLA template is a collection of settings that allows you to protect your data according to a periodic backup schedule in a way the data protection complies with SLA standards in your company. These standards are defined by a specific target SLA value that indicates how much data you can afford to lose in case a disaster strikes, which allows you to troubleshoot backup issues and facilitate backup infrastructure audit.

The target SLA value is a percentage of successfully created restore points out of the total number of restore points expected to be produced by an SLA-based backup policy. Based on this percentage, Veeam Backup for Microsoft Azure estimates the SLA compliance ratio for all SLA-based backup policies that have the related SLA template assigned. For more information, see [How Veeam Backup for Microsoft Azure Estimates SLA Compliance](sla_calculation.md).

One SLA template can be assigned to one or more SLA-based backup policies. When configuring an SLA template, you can create separate independent schedules for cloud-native snapshots, image-level backups and archived backups. For more information on how Veeam Backup for Microsoft Azure builds snapshot, backup and archive backup chains, see sections [Snapshot Chain](snapshot_chain_vm.md), [Backup Chain](backup_chain_vm.md) and [Archive Backup Chain](archive_chain.md).

|  |
| --- |
| Note |
| Cloud-native snapshots created according to snapshot schedules do not participate in the process of producing backups. To produce image-level backups according to backup schedules, Veeam Backup for Microsoft Azure takes temporary snapshots but then removes these snapshots based on their own [retention settings](temporary_restore_points.md#temporary_snapshots). |

Related Topics

* [Data Protection Windows](snapshot_backup_window.md)
* [Monitoring SLA-Based Policy Performance](sla_monitoring.md)

Page updated 1/13/2026

Page content applies to build 8.0.1.202
