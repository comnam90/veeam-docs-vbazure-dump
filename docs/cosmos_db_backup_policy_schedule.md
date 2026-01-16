---
title: "cosmos_db_backup_policy_schedule"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/cosmos_db_backup_policy_schedule.html"
last_updated: "3/19/2025"
product_version: "8.0.1.202"
---


In this article

[This step applies only if you set the Backup to repository toggle on the Targets step of the wizard to On]

You can instruct Veeam Backup for Microsoft Azure to start the backup policy automatically according to a specific backup schedule. The backup schedule defines how often data of the Cosmos DB for PostgreSQL and Cosmos DB for MongoDB accounts added to the backup policy will be backed up.

To help you implement a comprehensive backup strategy, Veeam Backup for Microsoft Azure allows you to create schedules of the following types:

* [Daily](cosmos_db_schedule_daily.md) — the backup policy will create restore points repeatedly throughout a day on specific days.
* [Weekly](cosmos_db_schedule_weekly.md) — the backup policy will create restore points once a day on specific days.
* [Monthly](cosmos_db_schedule_monthly.md) — the backup policy will create restore points once a month on a specific day.
* [Yearly](cosmos_db_schedule_yearly.md) — the backup policy will create restore points once a year on a specific day.

Combining multiple schedule types together allows you to retain restore points for longer periods of time — for more information, see [Enabling Harmonized Scheduling](cosmos_db_harmonized_scheduling.md). Combining multiple schedule types together also allows you to archive backups — for more information, see [Enabling Backup Archiving](cosmos_db_backup_archiving.md).

|  |
| --- |
| Note |
| When scheduling backup policies, it is recommended that you take into account the load in your Cosmos DB clusters since a large number of backup operations may affect the overall cluster performance. |

Page updated 3/19/2025

Page content applies to build 8.0.1.202
