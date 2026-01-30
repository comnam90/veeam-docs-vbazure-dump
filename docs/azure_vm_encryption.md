---
title: "Azure VM Disk Encryption"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/azure_vm_encryption.html"
last_updated: "5/20/2025"
product_version: "8.0.1.202"
---

# Azure VM Disk Encryption


Veeam Backup for Microsoft Azure allows you to back up and restore data of Azure VMs whose disks are encrypted using the following native Microsoft Azure encryption mechanisms:

* Server-side encryption (SSE) of Azure Disk Storage — leverages the 256-bit Advanced Encryption Standard (AES) to encrypt managed disks of Azure VMs using platform-managed keys, customer-managed keys or a combination of these key management options. For more information, see [Microsoft Docs](https://learn.microsoft.com/en-us/azure/virtual-machines/disk-encryption).
* Azure Disk Encryption (ADE) — leverages the BitLocker feature (for Windows-based Azure VMs) or the DM-Crypt feature (for Linux-based Azure VMs) to encrypt OS and data disks of Azure VMs using Azure Key Vault keys. For more information, see [Microsoft Docs](https://learn.microsoft.com/en-us/azure/virtual-machines/windows/disk-encryption-overview).

In This Section

* [Protecting VM Disk Data](encryption_vm_backup.md)
* [Restoring VM Disk Data](encryption_vm_restore.md)


