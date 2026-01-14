---
title: "backup_appliances"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/backup_appliances.html"
last_updated: "11/26/2025"
product_version: "8.0.1.202"
---


In this article

A backup appliance is a Linux-based Azure VM where Veeam Backup for Microsoft Azure is installed.

If you have multiple backup appliances in Microsoft Azure, you can add the appliances to Veeam Backup & Replication, and then use the Veeam Backup & Replication console as the central management console for Veeam Backup for Microsoft Azure operations. For more information on the Veeam Backup & Replication console, see the [Veeam Backup & Replication User Guide](https://helpcenter.veeam.com/docs/vbr/userguide/backup_console.html?ver=13).

Backup Appliance Software

The Azure VM running Veeam Backup for Microsoft Azure is deployed with the pre-installed set of software components:

* Ubuntu 22.04 LTS
* ASP.NET Core Runtime 8.0
* PostgreSQL 15
* nginx 1.18
* libpam-google-authenticator 20191231-2
* Veeam Backup for Microsoft Azure installation packages

In case any software updates become available for the backup appliance, these updates can be installed using the Veeam Updater service as described in section [Updating Veeam Backup for Microsoft Azure](updating_vb.md).

Backup Appliance Functionality

The backup appliance performs the following administrative activities:

* Manages architecture components.
* Coordinates snapshot creation, backup and recovery tasks.
* Controls backup policy scheduling.
* Generates daily reports and email notifications.

Backup Appliance Components

The backup appliance uses the following components:

* Backup service — coordinates data protection and disaster recovery operations.

* Configuration database — stores data on the existing backup policies, worker instance configurations, connected Microsoft Azure accounts and so on, as well as information on the available and protected resources collected from Microsoft Azure.
* Configuration restore service — allows users to back up and restore the configuration database of the backup appliance.
* Web UI — provides a web interface that allows users to access the Veeam Backup for Microsoft Azure functionality.
* Veeam Updater service — allows Veeam Backup for Microsoft Azure to check and install product and software software package updates.

* Veeam File-Level Recovery (FLR) service — allows users to restore individual files and folders of protected Azure VMs and file shares.

* REST API service — allows users to perform operations with Veeam Backup for Microsoft Azure entities using HTTP requests and standard HTTP methods. For more information, see the [Veeam Backup for Microsoft Azure REST API Reference](https://helpcenter.veeam.com/references/vbazure/8.1/rest/main/tag/SectionAbout).

Page updated 11/26/2025

Page content applies to build 8.0.1.202
