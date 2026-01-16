---
title: "sql_backup_policy_schedule"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/sql_backup_policy_schedule.html"
last_updated: "2/18/2025"
product_version: "8.0.1.202"
---


In this article

You can instruct Veeam Backup for Microsoft Azure to start the backup policy automatically according to a specific backup schedule. The backup schedule defines how often data of the Azure SQL databases added to the backup policy will be backed up.

To help you implement a comprehensive backup strategy, Veeam Backup for Microsoft Azure allows you to create schedules of the following types:

* [Daily](sql_schedule_daily.md) — the backup policy will create restore points repeatedly throughout a day on specific days.
* [Weekly](sql_schedule_weekly.md) — the backup policy will create restore points once a day on specific days.
* [Monthly](sql_schedule_monthly.md) — the backup policy will create restore points once a month on a specific day.
* [Yearly](sql_schedule_yearly.md) — the backup policy will create restore points once a year on a specific day.

Combining multiple schedule types together allows you to retain restore points for longer periods of time — for more information, see [Enabling Harmonized Scheduling](sql_harmonized_scheduling.md). Combining multiple schedule types together also allows you to archive backups — for more information, see [Enabling Backup Archiving](sql_backup_archiving.md).

Page updated 2/18/2025

Page content applies to build 8.0.1.202
