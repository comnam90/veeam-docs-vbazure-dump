---
title: "Step 5. Create and Launch Backup Policy"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/app_pne_first_policy_run.html"
last_updated: "3/25/2025"
product_version: "8.0.1.202"
---

# Step 5. Create and Launch Backup Policy


To allow Veeam Backup for Microsoft Azure to protect Azure VMs in the private environment, create and launch a schedule-based backup policy as described in section [Performing VM Backup](performing_vm_backup.md).

Consider that the backup policy is launched at this step only to automatically create and configure Veeam storage accounts and private endpoints that will further be used for backup operations. As soon as Veeam Backup for Microsoft Azure performs the necessary configuration steps, the policy will fail as some additional manual configuration actions with the private endpoints will still be required. For more information, see [Configuring Private Endpoints](pne_dns_endpoints.md).


