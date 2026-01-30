---
title: "Glossary"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/glossary.html"
last_updated: "11/25/2025"
product_version: "8.0.1.202"
---

# Glossary


This section describes product-specific terms and abbreviations that appear in the User Guide.

A

* application-aware processing — a Veeam technology that enables quiescing applications on Azure VMs and creating a consistent view of application data. See also [Performing VM Backup](application_aware_processing.md).
* Availability Zone — a logical grouping of one or more physically separate datacenters within an Azure region that provides high availability for Azure resources in this region. See also [Performing Entire VM Restore](vm_restore_console_zone.md).
* Azure Key Vault — a cloud service in Azure that provides secure storage for secrets, keys and certificates. See also [Data Encryption](data_encryption.md).
* Azure region — a specific physical location where Azure resources are hosted. See also [Overview](overview.md).
* Azure services — cloud-based tools and Azure resources that are used for cloud computing, storage, networking and security purposes. See also [Azure Services](azure_services.md).
* Azure tag — a label (name-value pair) assigned to Azure resources that is used to organize and manage them. See also [Performing Backup Using Web UI](vm_sla_source_settings.md#resources).

B

* backup appliance — a Linux-based Azure VM that orchestrates backup and restore tasks, communicates with Azure services and stores configuration data. See also [Solution Architecture](backup_appliances.md).
* backup chain — a sequence of backups created by a backup policy. See also [Protecting Azure VMs](backup_chain_vm.md).
* backup copy — a Veeam Backup & Replication functionality that enables creating copies of backed-up data in different locations, providing additional data protection and disaster recovery options. See also [Creating Backup Copy Jobs](backup_copy_console.md).
* backup policy — a collection of settings that define the way backup operations are performed: what data to back up, which operations to perform, where to store backups, when to start the backup process, how to retain restore points and so on. See also [Performing VM Backup](vm_backup_retry_notifications.md#health).
* backup repository — a folder in a blob container where Veeam Backup for Microsoft Azure stores backups created by backup policies. See also [Solution Architecture](backup_repositories.md).
* backup server — a physical or virtual machine (Windows-based or Linux-based) that serves as the core component of the backup infrastructure. See also [Solution Architecture](backup_server.md).
* Block Generation — a Veeam technology that enables managing immutability periods for backed-up data stored in backup repositories. See also [Immutability](immutability.md).

C

* change block tracking (CBT) — a Veeam technology that enables tracking data block changes to reduce the amount of data read from processed Azure VMs, and to increase the speed and efficiency of incremental backups. See also [Changed Block Tracking](changed_block_tracking.md).
* cloud-native snapshot — a restore point that Veeam Backup for Microsoft Azure takes using native Microsoft Azure capabilities to capture a set of point-in-time snapshots created for virtual disks or share files of a processed Azure VM or file share. See also [Protecting Azure VMs](overview_vm.md).
* configuration database — a backup appliance component that stores data on backup policies, sessions, worker instance configurations, service accounts, Azure resources and so on. See also [Performing Configuration Backup Using Web UI](configuration_backup_ui.md).
* Cloud Credentials Manager — a configuration database where Veeam Backup & Replication stores credential records that are used to connect to components of the backup infrastructure (such as servers, virtual machines and cloud services). See also [Deploying Backup Appliance](deploying_appliance.md).

D

* database account — credentials that are used to access Azure database services such as Azure Cosmos DB or Azure SQL when performing backup and restore operations. See also [Managing SMTP and Database Accounts](accounts_smtp_database.md).

G

* gateway server — an auxiliary backup infrastructure component that provides access from the backup server to the repositories. See also [Connecting to Existing Appliances](connecting_appliance_console.md).
* guest scripting — a Veeam Backup for Microsoft Azure functionality that enables running custom scripts on Azure VMs before and after backup operations. See also [Performing VM Backup](vm_guest_processing.md).

H

* health check — a Veeam Backup for Microsoft Azure functionality that enables verifying the availability of data blocks in backup files and cyclic redundancy check (CRC) values of metadata to ensure its integrity. See also [Performing VM Backup](vm_backup_retry_notifications.md#health).

I

* image-level backup — a restore point that captures the whole image of the processed Azure VM (including OS data, application data and so on) at a specific point in time. See also [VM Backup](how_vm_backup_works.md).
* immutability — a Veeam Backup for Microsoft Azure functionality that enables protecting restore points stored in backup repositories from deletion or loss as a result of malware, ransomware or any other malicious actions. See also [Immutability](immutability.md).

M

* Veeam Plug-in for Microsoft Azure — an architecture component that extends the Veeam Backup & Replication functionality to enable integration of backup appliances into the backup infrastructure. See also [Integration with Veeam Backup & Replication](integration_vbr.md).
* Microsoft Entra ID — a Microsoft cloud-based identity and access management service formerly known as Azure Active Directory (Azure AD). Veeam integrates with Entra ID for authentication and authorization purposes. See also [Azure Services](azure_services.md).

P

* product updates — updates for Veeam Backup for Microsoft Azure components that deliver new features and improvements. See also [Updating Appliances Using Web UI](updating_ui.md).

R

* restore point — a point-in-time cloud-native snapshot, cloud-native backup and image-level backup that can be used to restore an Azure resource. See also [Snapshot Chain](snapshot_chain_vm.md).
* retention policy — a collection of settings that define how long Veeam Backup for Microsoft Azure keeps restore points produced by backup policies. See also [Retention Policies](understanding_retention_policy.md).

S

* service account — an identity associated with a Microsoft Entra ID whose permissions Veeam Backup for Microsoft Azure uses to access Azure services and resources. See also [Service Account Permissions](service_account_permissions.md).
* schedule-based backup policy — a collection of settings that define the way backup operations are performed: what data to back up, which operations to perform, where to store backups, when to start the backup process, how to retain restore points, and so on. See also [Protecting Azure VMs](overview_vm.md).
* SLA-based backup policy — a collection of settings that automate the way backup operations are performed: what data to back up, how frequently to run the backup process, what region-specific repositories to use to store backups, how many restore points should be created in time to meet SLA requirements, and so on. See also [Protecting Azure VMs](overview_vm.md).
* software package updates — updates for Veeam Backup for Microsoft Azure software components such as .NET, PostgreSQL, and other third-party packages required for proper operation. See also [Updating Veeam Backup for Microsoft Azure](updating_vb.md).

* storage vault — a folder in an immutable blob container in the Cool access tier where Veeam Backup for Microsoft Azure stores backups created by backup policies. See also [Solution Architecture](vdc_vaults.md).

T

* tape device — a hardware component that records and reads data sequentially, commonly used for long-term backup archiving. See also [Additional Repositories and Tape Devices](additional_repositories_and_tape_devices.md).
* traffic throttling — a mechanism to control the bandwidth used by backup operations. Veeam allows configuring traffic throttling to minimize the impact on network performance. See also [Sizing and Scalability Guidelines](sizing_guidelines.md).

V

* Veeam Backup for Microsoft Azure REST API service — a service that allows users to perform operations with Veeam Backup for Microsoft Azure entities using HTTP requests and standard HTTP methods. See also [Ports](ports.md).

* Veeam Backup for Microsoft Azure Web UI — a client-side component that is used to access and manage backup appliances through a web browser. See also [Accessing Web UI from Workstation](accessing_vb_workstation.md).
* Veeam Backup & Replication console — a client-side component that provides access to the backup server. See also [Integration with Veeam Backup & Replication](integration_vbr.md).
* Veeam Data Mover — a service that is responsible for data processing and transfer. It optimizes backup performance by compressing, encrypting and transporting data between source and target locations. See also [Solution Architecture](backup_repositories.md).
* Veeam File-Level Recovery (FLR) service — a service that enables restoring individual files and folders of protected Azure VMs and file shares. See also [Performing File-Level Recovery](performing_flr.md).
* Veeam Updater service — a service that enables checking, viewing and installing product and software package updates. See also [Installing Updates](updates_install.md).

W

* worker configuration — a group of network settings that Veeam Backup for Microsoft Azure uses to deploy worker instances in a specific Azure region to perform data protection and disaster recovery operations. See also [Managing Worker Configurations](worker_configurations.md).
* worker instance — a temporary Linux-based Azure VM that is responsible for the interaction between the backup appliance, Azure services and other Veeam Backup for Microsoft Azure components. See also [Worker Instances](worker_instances.md).
* worker profile — a VM size of a worker instance that Veeam Backup for Microsoft Azure launches in a specific Azure region to perform data protection and disaster recovery operations. See also [Managing Worker Profiles](worker_profiles.md).
* workload — any Azure resource (for example, a VM, a SQL database, a file share and so on) that can be protected by Veeam Backup for Microsoft Azure. See also [Managing Backed-Up Data](managing_backups.md).


