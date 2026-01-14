---
title: "backup_policy_priority"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/backup_policy_priority.html"
last_updated: "3/25/2025"
product_version: "8.0.1.202"
---


In this article

By default, Veeam Backup for Microsoft Azure runs backup policies in the order you create them. However, you can set the backup policy priority manually:

1. Navigate to Policies.
2. Switch to the necessary tab and click Priority.
3. In the Priority Order window, do the following:

1. Select a backup policy in the list of existing policies.
2. To move the policy up or down the list, use the Up and Down arrows.
3. To save changes made to the priority order, click Apply.

|  |
| --- |
| Note |
| If an Azure resource is included into multiple backup policies, it will be processed only by the backup policy that has the highest priority. |

[![Setting Backup Policy Priority](images/policy_priority.webp)](images/policy_priority.webp "Setting Backup Policy Priority")

Page updated 3/25/2025

Page content applies to build 8.0.1.202
