---
title: "system_requirements"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/system_requirements.html"
last_updated: "12/9/2025"
product_version: "8.0.1.202"
---


In this article

When you plan to install Veeam Plug-in for Microsoft Azure, consider the following hardware and software requirements.

Backup Server

The machine where Veeam Plug-in for Microsoft Azure will run must meet system requirements described in the Veeam Backup & Replication User Guide, section [System Requirements](https://helpcenter.veeam.com/docs/vbr/userguide/system_requirements.html?ver=13). Additionally, the following software must be installed:

* Microsoft .NET Core Runtime 8.0
* Microsoft ASP.NET Core Shared Framework 8.0

|  |
| --- |
| Important |
| If the version of Microsoft .NET Core Runtime differs from the version of Microsoft ASP.NET Core Shared Framework, Veeam Plug-in for Microsoft Azure services will not be able to start. |

Azure Services

The backup appliance and worker instances must have outbound internet access to a number of Microsoft Azure services. For the list of services, see [Azure Services](azure_services.md).

Web Browsers

Internet Explorer is not supported. To access Veeam Backup for Microsoft Azure, use Microsoft Edge (latest version), Mozilla Firefox (latest version) or Google Chrome (latest version).

Version Compatibility

|  |
| --- |
| Note |
| On February 1, 2025, the Azure AD Graph API service was [retired in Microsoft Azure](https://www.veeam.com/kb4714). As a result, Microsoft Entra applications using Azure AD Graph are no longer able to send requests to Azure AD Graph APIs. That is why Veeam Backup for Microsoft Azure versions prior to version 6.0 are not supported, as these versions use Azure AD Graph. |

The following table lists compatible versions of Veeam Backup & Replication, Veeam Plug-in for Microsoft Azure and Veeam Backup for Microsoft Azure.

| Veeam Backup & Replication Build | Veeam Plug-in for Microsoft Azure Build | Veeam Backup for Microsoft Azure Build |
| --- | --- | --- |
| 13.0.1.180 | 13.8.2.230 | 8.0.1.202 |
| 13.0.0.4967 | 13.8.1.207 |
| 12.3.2.3617 | 12.8.0.293 |
| 12.3.1.1139 | 8.0.0.334 |
| 12.1.2.172 | 12.7.1.18 | 7.1.0.59 |
| 7.1.0.22 |
| 12.7.0.218 | 7.0.0.467 |
| 12.1.0.2131 | 12.6.0.1009 | 6.0.0.234 |
| 12.0.0.1420 | 12.1.5.99 | 5.1.0.75 |
| 12.0.5.740 | 5.0.0.579 |

Page updated 12/9/2025

Page content applies to build 8.0.1.202
