---
title: "exporting_configuration_data"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/exporting_configuration_data.html"
last_updated: "2/5/2024"
product_version: "8.0.1.202"
---


In this article

Once Veeam Backup for Microsoft Azure creates a successful configuration backup, you can export the configuration backup file and use it to [restore configuration data](configuration_restore_ui.md) on another backup appliance.

To export the configuration backup file, do the following:

1. Switch to the Configuration page.
2. Navigate to Configuration Backup.
3. Use either of the following options:

* To export the last successful configuration backup:

1. In the Overview section, click Export Last Backup.
2. In the Export Last Backup window, specify a password that will be used to encrypt the exported file, provide a hint for the specified password, and click Export.

* To export a specific configuration backup file:

1. In the Configuration restore section, click Available Restore Points.
2. In the Available Restore Points window, select the necessary backup and click Export Backup.
3. In the Export Backup window, specify a password that will be used to encrypt the exported file, provide a hint for the specified password, and click Export.

As soon as you click Export, Veeam Backup for Microsoft Azure will save the exported backup file to the default download directory on the local machine.

[![Exporting Configuration Backup Data](images/config_backup_export.webp)](images/config_backup_export.webp "Exporting Configuration Backup Data")

Page updated 2/5/2024

Page content applies to build 8.0.1.202
