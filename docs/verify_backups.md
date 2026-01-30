---
title: "Verifying Backups"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/verify_backups.html"
last_updated: "11/11/2025"
product_version: "8.0.1.202"
---

# Verifying Backups


To perform an integrity check of backups, Veeam Backup & Replication offers the SureBackup technology that allows you to ensure that the created restore points are not corrupted. You can also scan the restore points with antivirus software installed on the backup server, and run YARA rules to detect malware and sensitive data.

To create a SureBackup job, do the following:

1. In the Veeam Backup & Replication console, open the Home view.
2. Navigate to Jobs and click SureBackup Job on the ribbon.
3. At the Name step of the New SureBackup Job wizard, select the Backup verification and content scan only verification mode, and then complete the wizard as described in the Veeam Backup & Replication, section [Creating SureBackup Jobs](https://helpcenter.veeam.com/docs/backup/vsphere/create_surebackup_job.html?ver=120).

If any of the verification checks fail for a restore point, Veeam Backup & Replication will mark both this restore point and all subsequent points in the backup chain as Infected. To learn how to manage infected restore points, see Veeam Backup & Replication User Guide, section [Managing Malware Status](https://helpcenter.veeam.com/docs/backup/vsphere/malware_detection_managing_status.html?ver=120).

|  |
| --- |
| Tip |
| You can scan backups of VMs manually on demand, without creating a SureBackup job. To learn how to do that, see the Veeam Backup & Replication User Guide, section [Scan Backup](https://helpcenter.veeam.com/docs/backup/vsphere/malware_detection_scan_backup.html?ver=120). |

[![Verifying Backups](images/verifying_backups.webp)](images/verifying_backups.webp "Verifying Backups")


