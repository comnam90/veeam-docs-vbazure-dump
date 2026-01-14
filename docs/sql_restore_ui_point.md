---
title: "sql_restore_ui_point"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/sql_restore_ui_point.html"
last_updated: "1/28/2025"
product_version: "8.0.1.202"
---


In this article

At the Databases step of the wizard, select a restore point that will be used to restore the selected Azure SQL database. By default, Veeam Backup for Microsoft Azure uses the most recent valid restore point. However, you can restore the database data to an earlier state.

|  |
| --- |
| Important |
| If you select a restore point stored in an archive repository and the same restore point is also available in a regular repository, Veeam Backup for Microsoft Azure will display the confirmation window where you must choose whether you want to use the archived or regular restore point to perform the restore operation. |

To select a restore point, do the following:

1. Select the Azure SQL database and click Restore Point.
2. In the Specify restore point window, select the necessary restore point and click Apply.

To help you choose a restore point, Veeam Backup for Microsoft Azure provides the following information on each available restore point:

* Date — the date when the restore point was created.
* Access Tier — the storage tier of a backup repository where the restore point is stored.

[![Performing SQL Restore](images/sql_specify_point.webp)](images/sql_specify_point.webp "Performing SQL Restore")

Page updated 1/28/2025

Page content applies to build 8.0.1.202
