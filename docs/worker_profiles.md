---
title: "worker_profiles"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/worker_profiles.html"
last_updated: "10/24/2025"
product_version: "8.0.1.202"
---


In this article

A profile is the VM size of a worker instance that Veeam Backup for Microsoft Azure launches in a specific Azure region to perform a backup, restore, retention, archive, file share indexing, repository synchronization or health check operation. Veeam Backup for Microsoft Azure launches one worker instance per each Azure resource added to a backup policy or restore task.

Out of the box, Veeam Backup for Microsoft Azure comes with the default set of worker profiles where the primary profile is Standard\_F2s\_v2 and the archive profile is Standard\_E2\_v5. However, to boost operational performance, you can add custom sets of worker profiles to specify VM sizes of worker instances that will operate in different regions. When configuring worker profiles, you can choose the profile of each launched worker instance depending on the performed operation and the total size of the processed data:

| Worker Profile | Default Azure VM Size | Usage |
| --- | --- | --- |
| Small | Standard\_F2s\_v2 | * Backup and restore of the following workloads:  * Azure VMs whose total disk size is less than 100 GB * Azure SQL databases whose total size is less than 1 GB * Cosmos DB for PostgreSQL clusters whose total size is less than 22 GB  * File-level recovery of Azure VMs * Retention of backup chains whose total size is less than 100 GB, or whose length is less than 100 restore points * Repository synchronization, file share indexing and health check |
| Medium | Standard\_F4s\_v2 | * Backup and restore of the following workloads:  * Azure VMs whose total disk size is between 100 GB and 1 TB * Azure SQL databases whose total size is between 1 GB and 50 GB * Cosmos DB for PostgreSQL clusters whose total size is between 22 GB and 112 GB  * Retention of backup chains whose total size is between 100 GB and 1024 GB, or whose length is between 100 and 250 restore points |
| Large | Standard\_F8s\_v2 | * Backup and restore of the following workloads:  * Azure VMs whose total disk size is more than 1 TB * Azure SQL databases whose total size is more than 50 GB * Cosmos DB for PostgreSQL clusters whose total size is more than 112 GB  * Retention of backup chains whose total size is more than 1024 GB, or whose length is more than 250 restore points |
| Archiving | Standard\_E2\_v5 | * Backup archiving * Data retrieval operations |

In This Section

* [Adding Worker Profiles](worker_profile_add.md)
* [Editing Worker Profiles](worker_profile_edit.md)
* [Removing Worker Profiles](worker_profile_remove.md)

Page updated 10/24/2025

Page content applies to build 8.0.1.202
