---
title: "Step 2. Specify Repository Details"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/repository_console_appliance.html"
last_updated: "2/4/2026"
product_version: "8.0.1.202"
---

# Step 2. Specify Repository Details


At the Backup Appliance step of the wizard, do the following:

1. From the Appliance drop-down list, select a backup appliance that will manage the repository.

For an appliance to be displayed in the Appliance drop-down list, it must be added to the backup infrastructure as described in section [Adding Appliances](adding_appliance_console.md).

1. Use the Repository name and Description fields to enter a name for the new repository and to provide a description for future reference. The maximum length of the name is 127 characters; the following characters are not supported: \ / " ' [ ] : | < > + = ; , ? \* @ & \_ .

Veeam Backup & Replication will create a folder with the specified name in the blob container that you will specify at [step 5](repository_console_container.md). This folder will be used to store backed-up data.

![Step 2. Specify Repository Details](images/add_repo_specify_appliance.webp)


