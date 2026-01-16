---
title: "pne_cosmos_db_endpoints"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/pne_cosmos_db_endpoints.html"
last_updated: "1/27/2025"
product_version: "8.0.1.202"
---


In this article

To allow Veeam Backup for Microsoft Azure access to the databases that you want to protect, you must create private endpoints for your Cosmos DB for PostgreSQL account.

You must create a separate private endpoint for every VNet to which worker instances are connected. To create a private endpoint, complete the following steps:

1. [Launch the Create a private endpoint wizard](pne_cosmos_db_wizard.md).
2. [Configure private endpoint settings](pne_cosmos_db_endpoint.md).
3. [Specify resource settings](pne_cosmos_db_resource.md).
4. [Specify network settings](pne_cosmos_db_configuration.md).
5. [Specify DNS settings](pne_cosmos_db_dns.md).
6. [Assign tags](pne_cosmos_db_tags.md).
7. [Finish working with the wizard](pne_cosmos_db_finish.md).

Page updated 1/27/2025

Page content applies to build 8.0.1.202
