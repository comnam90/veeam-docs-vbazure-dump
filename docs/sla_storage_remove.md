---
title: "Removing SLA and Storage Templates"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/sla_storage_remove.html"
last_updated: "3/25/2025"
product_version: "8.0.1.202"
---

# Removing SLA and Storage Templates


Veeam Backup for Microsoft Azure allows you to permanently remove a policy template from the configuration database if you no longer need it:

1. Switch to the Configuration page.
2. Navigate to Policy Templates.
3. Switch to the necessary tab and select the template.
4. Click Remove.

|  |
| --- |
| Important |
| You cannot remove a template that is used by any SLA-based backup policy. [Modify the settings of all the related policies](backup.md) to remove references to the template — and then try removing the template again. |

[![Removing Accounts](images/sla_storage_remove.webp)](images/sla_storage_remove.webp "Removing Accounts")


