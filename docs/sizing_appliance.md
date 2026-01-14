---
title: "sizing_appliance"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/sizing_appliance.html"
last_updated: "12/9/2025"
product_version: "8.0.1.202"
---


In this article

You can choose the size of the Azure VM running Veeam Backup for Microsoft Azure during the deployment, or change it later as the environment grows.

|  |
| --- |
| Note |
| In Veeam Backup for Microsoft Azure version 8.1, you can only choose the B2s, D4s\_v3 or D8s\_v3 VM size. |

General Recommendations

The following recommendations and examples apply to the latest Veeam Backup for Microsoft Azure builds.

| Azure VM Size | Recommended Maximum Number of Protected Workloads | Recommended Maximum Number of Launched Worker Instances |
| --- | --- | --- |
| B2s (2 vCPU, 4 GB RAM)  Note: The minimum amount of system RAM recommended to perform [Virtual Network configuration backup](overview_vnet.md) is 8 GB. If you plan to protect Azure Virtual Network configuration components, it is not recommended that you choose the B2s Azure VM size — consider choosing larger sizes. | * 500 * 300 (if backed up simultaneously) | 20 |
| D4s\_v3 (4 vCPU, 16 GB RAM) | * 1,500 * 500 (if backed up simultaneously) | 150 |
| D8s\_v3 (8 vCPU, 32 GB RAM) | * 3,000 * 1,500 (if backed up simultaneously) | 300 |

|  |
| --- |
| Note |
| For product deployments running on Azure VMs whose size is larger than D4s\_v3, Veeam Backup for Microsoft Azure may simultaneously launch 100 worker instances per region — however, this can trigger throttling issues in Microsoft Azure. If you are facing these issues, it is recommended that you use a maximum of 70 worker instances per region at a time. Alternatively, consider reducing the number of worker instances launched simultaneously by configuring different schedules for your backup policies or by specifying different target regions. For more information, see [Performing Backup](backup.md). |

Veeam Backup & Replication Integration

When you connect a backup appliance to the backup infrastructure, its backup policies, cloud-native snapshots, image-level backups, backup repositories and sessions are imported into the Veeam Backup & Replication database.

You can connect multiple backup appliances to a single Veeam Backup & Replication server. However, when working in an Azure subscription with cross-region data transfer, it is recommended that you use one Veeam Backup & Replication server per region, to help you avoid latency issues and meet potential data residency regulations.

Page updated 12/9/2025

Page content applies to build 8.0.1.202
