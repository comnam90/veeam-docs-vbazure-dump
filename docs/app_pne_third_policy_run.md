---
title: "Step 9. Launch Test Backup Policy"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/app_pne_third_policy_run.html"
last_updated: "3/25/2025"
product_version: "8.0.1.202"
---

# Step 9. Launch Test Backup Policy


To make sure that you have configured all the required settings correctly, launch the schedule-based backup policy created at [step 5](app_pne_first_policy_run.md).

Consider that as soon as the backup policy completes successfully, Veeam Backup for Microsoft Azure will start regularly updating the worker instances. However, for Veeam Backup for Microsoft Azure to be able to install the updates, your worker instances will require public access to the online Ubuntu repositories listed in section [Ports](ports.md). If you do not want Veeam Backup for Microsoft Azure to update the worker instances, open a [support case](support_information.md).

Related Topics

[Performing VM Backup](performing_vm_backup.md)


