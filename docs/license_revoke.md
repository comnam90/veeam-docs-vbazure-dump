---
title: "license_revoke"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/license_revoke.html"
last_updated: "8/27/2025"
product_version: "8.0.1.202"
---


In this article

By default, Veeam Backup for Microsoft Azure automatically revokes a license unit from a protected instance if no new restore points have been created by the backup policy during the past 31 days. However, you can manually revoke license units from protected instances — this can be helpful, for example, if you remove a number of instances from a backup policy and do not want to protect them anymore.

Revoking License Units Using Veeam Backup & Replication Console

You can revoke license units from a protected instance in the Veeam Backup & Replication console, do the following:

1. In the Veeam Backup & Replication console, open the main menu and select License.
2. In the License Information window, switch to the Instances tab and click Manage.

1. In the Licensed Instances window, select a protected workload and click Revoke. Veeam Backup & Replication will revoke a license unit from the selected workload.

[![Revoke licensed VMs](images/license_revoke_integr.webp)](images/license_revoke_integr.webp "Revoke licensed VMs")

Revoking License Units Using Veeam Backup for Microsoft Azure Web UI

To revoke a license unit from a protected instance in the Veeam Backup for Microsoft Azure Web UI, do the following:

1. Switch to the Configuration page.
2. Navigate to Licensing > License Usage.
3. Select the instance that you no longer want to protect.
4. Click Revoke License.

[![Revoking License Units](images/license_revoke.webp)](images/license_revoke.webp "Revoking License Units")

Page updated 8/27/2025

Page content applies to build 8.0.1.202
