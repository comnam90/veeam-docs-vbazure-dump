---
title: "Editing Storage Templates"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/storage_edit.html"
last_updated: "7/28/2025"
product_version: "8.0.1.202"
---

# Editing Storage Templates


|  |
| --- |
| Important |
| If a storage template is already assigned to at least one SLA-based backup policy, modifying its location settings will cause Veeam Backup for Microsoft Azure to start a new chain of restore points in the specified location. The old chain of restore points will be retained in the previous location until removed according to retention settings specified for the SLA template assigned to this SLA-based backup policy. |

For each storage template, you can modify settings configured while creating the template:

1. Switch to the Configuration page.
2. Navigate to Policy Templates > Storage and click Edit.
3. Complete the Edit Storage Template wizard:

1. To provide a new name and description for the template, follow the instructions provided in section [Adding Storage Templates](storage_name.md) (step 2).
2. To modify the configured location settings, follow the instructions provided in section [Adding Storage Templates](storage_location_settings.md) (step 3).
3. At the Summary step of the wizard, review configuration information and click Finish to confirm the changes.

|  |
| --- |
| Tip |
| After you click Finish, Veeam Backup for Microsoft Azure will update the timestamp in the Last Modified column on the Storage page, regardless of whether you have actually modified the template settings or not. If you want to simply view the configured settings without making any changes, click View Info. |

[![Editing Backup Policy Settings](images/storage_edit.webp)](images/storage_edit.webp "Editing Backup Policy Settings")


