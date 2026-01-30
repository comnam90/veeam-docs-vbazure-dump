---
title: "Step 4. Configure Retention Settings"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/vnet_backup_retention.html"
last_updated: "1/24/2025"
product_version: "8.0.1.202"
---

# Step 4. Configure Retention Settings


At the Retention step of the wizard, specify retention settings for virtual network configuration backups.

1. Click the Collect data link.
2. In the Daily retention window, specify how often the data will be backed up and for how long the backups will be stored in the Veeam Backup for Microsoft Azure configuration database.

If a restore point is older than the specified time limit, Veeam Backup for Microsoft Azure removes the restore point from the backup chain. For more information, see [Virtual Network Configuration Backup Retention](retention_backup_vnet.md).

[![VNet Policy Retention Settings](images/vnet_backup_retention.webp)](images/vnet_backup_retention.webp "VNet Policy Retention Settings")


