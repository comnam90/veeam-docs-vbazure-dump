---
title: "backup_policy_start_stop_console"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/backup_policy_start_stop_console.html"
last_updated: "7/11/2025"
product_version: "8.0.1.202"
---


In this article

You can start a backup policy manually, for example, if you want to create an additional restore point in the snapshot or backup chain and do not want to modify the configured backup policy schedule. You can also stop a running backup policy if processing of a workload is about to take too long, and you do not want the policy to produce heavy load on the production environment during business hours.

To start or stop a backup policy, do the following:

1. In the Veeam Backup & Replication console, open the Home view.
2. Navigate to Jobs.
3. Select the necessary backup policy and click Start or Stop on the ribbon.

Alternatively, you can right-click the selected backup policy and select Start or Stop.

[![Start and stop Azure policy](images/azure_policy_start.webp)](images/azure_policy_start.webp "Start and stop Azure policy")

Page updated 7/11/2025

Page content applies to build 8.0.1.202
