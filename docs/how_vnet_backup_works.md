---
title: "Virtual Network Configuration Backup"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/how_vnet_backup_works.html"
last_updated: "8/23/2024"
product_version: "8.0.1.202"
---

# Virtual Network Configuration Backup


Veeam Backup for Microsoft Azure performs virtual network configuration backup in the following way:

1. Sends API requests to Microsoft Azure to retrieve the virtual network configuration data, and saves this data in the configuration database.

To back up virtual network configurations of Azure subscriptions added to backup policies, Veeam Backup for Microsoft Azure uses permissions of service accounts specified in the backup policy settings. The virtual network configuration data is collected for the Microsoft Entra tenants to which the specified service accounts belong.

1. Creates a configuration record for each pair of an Microsoft Entra tenant and an Azure subscription whose virtual network configuration data is being backed up. Every time the Virtual Network Configuration Backup policy runs, Veeam Backup for Microsoft Azure updates the record to create a new restore point for each protected virtual network configuration.
2. If you [enable additional backup copy](vnet_backup_copies.md) for the Virtual Network Configuration Backup policy, Veeam Backup for Microsoft Azure launches the Veeam Data Mover service on the backup appliance to copy the restore points from the configuration database to the target repository, creating an individual folder for each Azure subscription whose virtual network configuration data is protected by the policy.


