---
title: "Copying Backups to Tapes"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/copy_to_tape_console.html"
last_updated: "8/26/2025"
product_version: "8.0.1.202"
---

# Copying Backups to Tapes


Veeam Backup & Replication allows you to automate copying of image-level backups of Azure VMs to tape devices and lets you specify scheduling, archiving and media automation options. For more information on the supported tape libraries, see the Veeam Backup & Replication User Guide, section [Tape Devices Support](https://helpcenter.veeam.com/docs/vbr/userguide/tape_device_support.html?ver=13).

Before you start copying backup to tapes:

* Copy Azure VM backups to on-premises backup repositories. To learn how to copy backups, see the instructions provided in [Creating Backup Copy Jobs](backup_copy_console.md).

* Connect tape devices to Veeam Backup & Replication as described in the Veeam Backup & Replication User Guide, section [Tape Devices Deployment](https://helpcenter.veeam.com/docs/vbr/userguide/tape_deployment.html?ver=13).
* Configure the tape infrastructure as described in the Veeam Backup & Replication User Guide, section [Getting Started with Tapes](https://helpcenter.veeam.com/docs/vbr/userguide/getting_started_with_tapes.html?ver=13) (steps 1–3).

To copy Azure VM backups to tapes, create a backup to tape job as described in the Veeam Backup & Replication User Guide, section [Creating Backup to Tape Jobs](https://helpcenter.veeam.com/docs/vbr/userguide/creating_backup_to_tape_jobs.html?ver=13).

[![Copy backups to tape](images/backup_to_tape.webp)](images/backup_to_tape.webp "Copy backups to tape")


