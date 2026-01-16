---
title: "app_pne_storage_endpoints"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/app_pne_storage_endpoints.html"
last_updated: "8/27/2024"
product_version: "8.0.1.202"
---


In this article

If the backup appliance resides in another region than the resources that you want to back up, or you do not want to add firewall rules, you can create private endpoints for your storage account to allow Veeam Backup for Microsoft Azure access to the resources.

You must create a separate private endpoint for every VNet to which the backup appliance or worker instances are connected. To create a private endpoint, perform the following steps:

1. [Launch the Create a private endpoint wizard](app_pne_storage_wizard.md).
2. [Configure general settings for the private endpoint](app_pne_storage_endpoint.md).
3. [Specify resource settings](app_pne_storage_resource.md).
4. [Specify virtual network settings](app_pne_storage_configuration.md).
5. [Specify DNS settings](app_pne_storage_dns.md).
6. [Assign tags](app_pne_storage_tags.md).
7. [Finish working with the wizard](app_pne_storage_finish.md).
8. [Configure network settings of the newly created private endpoint](pne_storage_peering.md).

Page updated 8/27/2024

Page content applies to build 8.0.1.202
