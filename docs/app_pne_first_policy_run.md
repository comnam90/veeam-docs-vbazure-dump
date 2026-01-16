---
title: "app_pne_first_policy_run"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/app_pne_first_policy_run.html"
last_updated: "3/25/2025"
product_version: "8.0.1.202"
---


In this article

To allow Veeam Backup for Microsoft Azure to protect Azure VMs in the private environment, create and launch a schedule-based backup policy as described in section [Performing VM Backup](performing_vm_backup.md).

Consider that the backup policy is launched at this step only to automatically create and configure Veeam storage accounts and private endpoints that will further be used for backup operations. As soon as Veeam Backup for Microsoft Azure performs the necessary configuration steps, the policy will fail as some additional manual configuration actions with the private endpoints will still be required. For more information, see [Configuring Private Endpoints](pne_dns_endpoints.md).

Page updated 3/25/2025

Page content applies to build 8.0.1.202
