---
title: "fs_backup_policy_schedule"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/fs_backup_policy_schedule.html"
last_updated: "2/23/2024"
product_version: "8.0.1.202"
---


In this article

You can instruct Veeam Backup for Microsoft Azure to start the backup policy automatically according to a specific backup schedule. The backup schedule defines how often data stored in file systems added to the backup policy will be backed up.

To help you implement a comprehensive backup strategy, Veeam Backup for Microsoft Azure allows you to create schedules of the following types:

* [Daily](fs_schedule_daily.md) — the backup policy will create restore points repeatedly throughout a day on specific days.
* [Weekly](fs_schedule_weekly.md) — the backup policy will create restore points once a day on specific days.
* [Monthly](fs_schedule_monthly.md) — the backup policy will create restore points once a month on a specific day.

Combining multiple schedule types together allows you to keep restore points for longer periods of time. For more information, see [Enabling Harmonized Scheduling](fs_harmonized_scheduling.md).

Page updated 2/23/2024

Page content applies to build 8.0.1.202
