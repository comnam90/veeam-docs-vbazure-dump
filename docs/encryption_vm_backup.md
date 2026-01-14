---
title: "encryption_vm_backup"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/encryption_vm_backup.html"
last_updated: "8/19/2025"
product_version: "8.0.1.202"
---


In this article

The process of creating cloud-native snapshots and image-level backups of an Azure VM whose disks are encrypted with SSE or ADE does not differ from the same process for a VM with unencrypted disks. The service account used to create restore points does not require any additional permissions — Veeam Backup for Microsoft Azure saves these restore points to backup repositories as is, without applying any additional encryption mechanisms. However, you can enable encryption at the repository level; for more information, see [Backup Repository Encryption](repo_encryption.md).

Page updated 8/19/2025

Page content applies to build 8.0.1.202
