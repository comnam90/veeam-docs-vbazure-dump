---
title: "data_encryption"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/data_encryption.html"
last_updated: "1/13/2026"
product_version: "8.0.1.202"
---


In this article

By default, Azure Storage uses service-side encryption (SSE) to automatically encrypt data with 256-bit AES keys. For more information on Azure Storage encryption, see [Microsoft Docs](https://learn.microsoft.com/en-us/azure/storage/common/storage-service-encryption?toc=%2Fazure%2Fstorage%2Fblobs%2Ftoc.json&bc=%2Fazure%2Fstorage%2Fblobs%2Fbreadcrumb%2Ftoc.json).

For enhanced data security, Veeam Backup for Microsoft Azure allows you to encrypt backed-up data in repositories using Veeam encryption mechanisms. Additionally, Veeam Backup for Microsoft Azure supports native Microsoft Azure encryption of Azure VMs.

|  |
| --- |
| Note |
| Sensitive customer data (credentials of user accounts required to connect to virtual servers and other systems, cloud credentials, and so on) is stored in the configuration database in the encrypted format. |

Page updated 1/13/2026

Page content applies to build 8.0.1.202
