---
title: "azure_services"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/azure_services.html"
last_updated: "10/24/2025"
product_version: "8.0.1.202"
---


In this article

To perform backup and restore operations in both public and private environments, [Veeam Plug-in for Microsoft Azure](plug_in.md), [backup appliance](backup_appliances.md) and [worker instances](worker_instances.md) must have outbound network access to the following Microsoft Azure services.

Azure Services Required for Veeam Plug-in for Microsoft Azure

* [Microsoft Entra ID](https://learn.microsoft.com/en-us/entra/fundamentals/whatis)
* [Azure Resource Manager](https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/overview)
* [Azure Storage](https://learn.microsoft.com/en-us/azure/storage/common/storage-introduction)

Azure Services Required for Backup Appliance

* [Microsoft Entra ID](https://learn.microsoft.com/en-us/entra/fundamentals/whatis)
* [Azure Cost Management](https://docs.microsoft.com/en-us/azure/cost-management-billing/cost-management-billing-overview)
* [Azure Instance Metadata Service](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/instance-metadata-service?tabs=windows)
* [Azure Key Vault](https://docs.microsoft.com/en-us/azure/key-vault/)
* [Azure Queue Storage](https://learn.microsoft.com/en-us/azure/storage/queues/storage-queues-introduction)
* [Azure Resource Manager](https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/overview)
* [Azure Storage](https://learn.microsoft.com/en-us/azure/storage/common/storage-introduction)
* [Azure Virtual Network](https://learn.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview), for Azure resources that operate in private environments only
* [Microsoft Identity Platform](https://docs.microsoft.com/en-us/azure/active-directory/develop/v2-overview)

Azure Services Required for Worker Instances

* [Azure Storage](https://learn.microsoft.com/en-us/azure/storage/common/storage-introduction)
* [Azure SQL Database](https://learn.microsoft.com/en-us/azure/azure-sql/database/sql-database-paas-overview?view=azuresql)
* [Azure Cosmos DB for PostgreSQL](https://learn.microsoft.com/en-us/azure/cosmos-db/postgresql/introduction)
* [Azure Cosmos DB for MongoDB](https://learn.microsoft.com/en-us/azure/cosmos-db/mongodb/introduction)

|  |
| --- |
| Important |
| Consider the following:   * To allow access to the services, you must open all the required network ports using either Azure network security groups or firewall rules. For the list of required network ports, see [Ports](ports.md). * If your backup appliance used the Azure Service Bus messaging service in versions prior to version 8.1, you must switch to the Azure Queue Storage service immediately after you upgrade to version 8.1. Otherwise, Veeam Backup for Microsoft Azure will no longer be able to perform backup and restore operations. For more information, see [Configuring Deployment Mode](deployment_mode.md#messaging). |

[![Backup Infrastructure](images/architecture_services_v7.webp)](images/architecture_services_v7.webp "Backup Infrastructure")

Page updated 10/24/2025

Page content applies to build 8.0.1.202
