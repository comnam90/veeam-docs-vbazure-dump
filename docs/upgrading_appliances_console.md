---
title: "upgrading_appliances_console"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/upgrading_appliances_console.html"
last_updated: "5/30/2025"
product_version: "8.0.1.202"
---


In this article

To upgrade Veeam Backup for Microsoft Azure to version 6.0 or 7.0, a backup appliance must be running version 3.0 or later. To upgrade the appliance, check the [prerequisites](#prerequisites) and follow the instructions provided in section [Updating Appliances Using Console](updating_console.md).

When you perform upgrade to Veeam Backup for Microsoft Azure version 6.0 or 7.0 from Veeam Backup for Microsoft Azure version 5.0 or earlier, the backup appliance operating system is upgraded from Ubuntu 18.04 LTS to Ubuntu 22.04 LTS, and the configuration database is upgraded to PostgreSQL 15.5. Consider that the upgrade procedure includes re-deployment of the backup appliance on a new Azure VM and attachment of data disks from the previous appliance to this new Azure VM.

How Upgrade to Version 6.0 or 7.0 Works

When upgrading backup appliances to version 6.0 or 7.0 from Veeam Backup for Microsoft Azure version 5.0 or earlier, Veeam Backup & Replication performs the following steps:

1. Instructs Veeam Backup for Microsoft Azure to create a cloud-native snapshot of the original appliance. If the upgrade process fails, the appliance will be reverted to the created snapshot.

Consider that this snapshot will not be automatically removed by Veeam Backup & Replication from Microsoft Azure after the upgrade operation completes successfully. You can remove this snapshot manually if you no longer need it, or keep it in case you will need to roll back the appliance to the previous state.

1. Upgrades version of the appliance configuration database to PostgreSQL 15.5: creates a new PostgreSQL database on the virtual data disk of the original appliance, copies all configuration data to this database and removes the old database.
2. Saves the following configuration files and settings to the virtual data disk of the original appliance: the appliance configuration file (/etc/veeam/azurebackup/Config.ini), users, MFA and time zone settings, and Linux environment (/etc/ssh/, /root/, /home/).
3. Detaches the virtual data disk from the original Azure VM and removes the VM from Microsoft Azure.
4. Launches a new Azure VM with the same name and network configuration from the Veeam Backup for Microsoft Azure version 6.0 or 7.0 image. By default, the launched VM will have 2 disks attached: one OS disk containing Ubuntu 22.04 LTS as an operating system and one empty virtual data disk.
5. Attaches the virtual data disk of the original appliance to the newly created appliance.
6. Restores the configuration files and settings saved at step 3 to the new OS disk.
7. Detaches the default virtual data disk from the newly created appliance and removes the disk from Microsoft Azure.
8. Removes the OS disk of the original Azure VM from Microsoft Azure.

Limitations and Prerequisites

Before you start the upgrade process, consider the following requirements and limitations:

* The Microsoft Azure compute account (service account) specified when [deploying a backup appliance](deploying_appliance_account.md) or [connecting to the appliance](adding_appliance_account.md) must be assigned permissions required to perform upgrade. For the list of required permissions, see [Plug-In Permissions](plugin_permissions.md).

* Outbound internet access must be allowed from the backup appliance to the PostgreSQL APT repository (apt.postgresql.org, apt-archive.postgresql.org) through port 80 over the HTTP protocol.

* Outbound internet access must be allowed from the backup appliance to the PostgreSQL website (postgresql.org) through port 443 over the HTTPS protocol to download the repository key <https://www.postgresql.org/media/keys/ACCC4CF8.asc>.
* Outbound internet access must be allowed from the backup appliance to the [Veeam Update Notification Server](https://repository.veeam.com/) through port 443 over the HTTPS protocol.
* Outbound internet access must be allowed from the backup appliance to the [Ubuntu Security Repository](https://ubuntu.com/security/notices) through port 80 over the HTTP protocol.

* During upgrade, the data disk of the backup appliance will temporarily contain files of 2 databases. That is why the size of the data disk must be twice the total amount of storage space used by the configuration database.

* During upgrade, Veeam Backup & Replication will create the new root virtual disk with the default settings. That is why if you have modified root disk settings, for example have increased disk size, these settings will not be transferred, and custom 3rd-party software installed on the backup appliance will not be migrated.

Page updated 5/30/2025

Page content applies to build 8.0.1.202
