---
title: "Protecting Virtual Network Configurations"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/overview_vnet.html"
last_updated: "2/13/2026"
product_version: "8.0.1.202"
---

# Protecting Virtual Network Configurations


To protect Azure virtual network configurations, Veeam Backup for Microsoft Azure retrieves configuration data through API and saves this data to the configuration database. For more information on how virtual network configuration backup works, see [Virtual Network Configuration Backup](how_vnet_backup_works.md).

How To Protect Virtual Network Configurations

To modify the virtual network configuration backup policy settings, perform the following steps:

1. [Check limitations and prerequisites](limitations.md#backup).
2. [Specify service accounts to access Azure services and resources](service_accounts.md).
3. [Add backup repositories to save additional virtual network configuration backup copies](repositories.md).
4. [[Optional] Configure global retention settings for obsolete snapshots and session records](configuring_global_retention.md).
5. [[Optional] Configure email notification settings for automated delivery of backup policy results and daily reports](configuring_notification_settings.md).
6. [Complete the Edit Virtual Network Configuration Backup Policy wizard](vnet_backup_edit.md).

Related Topics

[Virtual Network Configuration Restore](vnet_restore_hiw.md)


