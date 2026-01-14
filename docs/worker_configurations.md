---
title: "worker_configurations"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/worker_configurations.html"
last_updated: "9/27/2024"
product_version: "8.0.1.202"
---


In this article

A configuration is a group of network settings that Veeam Backup for Microsoft Azure uses to launch worker instances in a specific Azure region to perform data protection and disaster recovery operations. Veeam Backup for Microsoft Azure launches one worker instance per each Azure resource added to a backup policy or restore task.

By default, Veeam Backup for Microsoft Azure automatically creates a new network configuration for each Azure region in which it launches worker instances. However, you can add custom worker configurations to provide network settings that will be used to launch worker instances in a specific region.

|  |
| --- |
| Important |
| Consider the following:   * For each automatically created worker configuration, Veeam Backup for Microsoft Azure creates a virtual network, a subnet and a network security group. * It is not recommended that you manually change settings of automatically created configurations. If you want to use a specific worker configuration, add it manually as described in section [Adding Worker Configurations](worker_configuration_add.md). |

In This Section

* [Specifying Destination for Worker Instances](worker_service_account.md)
* [Adding Worker Configurations](worker_configuration_add.md)
* [Editing Worker Configurations](worker_configuration_edit.md)
* [Removing Worker Configurations](worker_configuration_remove.md)

Page updated 9/27/2024

Page content applies to build 8.0.1.202
