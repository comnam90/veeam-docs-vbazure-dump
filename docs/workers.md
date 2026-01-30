---
title: "Managing Worker Instances"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/workers.html"
last_updated: "8/20/2025"
product_version: "8.0.1.202"
---

# Managing Worker Instances


To perform most data protection and disaster recovery operations (such as creating backups in repositories and restoring backed-up data), Veeam Backup for Microsoft Azure uses worker instances. A worker instance is an auxiliary Linux-based virtual machine that is responsible for the interaction between the backup appliance and other Veeam Backup for Microsoft Azure components. Worker instances process backup workload and distribute backup traffic when transferring data to repositories.

Each worker instance is launched in a specific Azure region and keeps running for the duration of the backup or restore process. For more information on regions in which Veeam Backup for Microsoft Azure launches worker instances, see [Worker Instances](worker_instances.md).

|  |
| --- |
| Note |
| You can tell worker instances from other Azure VMs running in your environment — all worker instances launched by Veeam Backup for Microsoft Azure will have the word VBA in their names, and the Veeam backup appliance ID tag. To learn how to assign custom tags to worker instances, see [Adding Worker Instance Tags](worker_instance_tags.md). |

In This Section

* [Managing Worker Configurations](worker_configurations.md)
* [Managing Worker Profiles](worker_profiles.md)
* [Adding Tags to Worker Instances](worker_instance_tags.md)
* [Removing Worker Instances](worker_instance_remove.md)


