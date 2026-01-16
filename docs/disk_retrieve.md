---
title: "disk_retrieve"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/disk_retrieve.html"
last_updated: "1/27/2025"
product_version: "8.0.1.202"
---


In this article

[This step applies only if you have selected a restore point stored in an archive repository at the Restore Point step of the wizard]

At the Data retrieval step of the wizard, choose a retrieval mode and specify a period for which you want to keep the data available.

1. In the Retrieval Mode section, select the retrieval mode that Veeam Backup for Microsoft Azure will use to retrieve the archived data. For more information on data retrieval modes, see [Retrieving Data From Archive](retrieving_vm_data.md).

1. In the Availability Period section, specify the number of days for which you want to keep the data available for restore operations. You can [manually extend the availability period](retrieving_vm_data.md) later if required.

|  |
| --- |
| Tip |
| If you want to receive an email notification when data availability period is about to expire, select the Send notification email check box and choose when you want to be notified (that is, the number of hours remaining until data expiration). |

[![Performing Disk Restore](images/restoring_disk_retrieve.webp)](images/restoring_disk_retrieve.webp "Performing Disk Restore")

Page updated 1/27/2025

Page content applies to build 8.0.1.202
