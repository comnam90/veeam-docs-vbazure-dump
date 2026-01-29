---
title: "Step 7. Specify Mount Server Settings"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/repository_console_mount_server.html"
last_updated: "1/28/2026"
product_version: "8.0.1.202"
---

# Step 7. Specify Mount Server Settings


To perform guest OS file restore and application restore operations, Veeam Backup & Replication uses [mount servers](mount_servers.md). By default, these servers are selected automatically depending on the operating system of the processed VM.

If Veeam Backup & Replication fails to choose a mount servers automatically or you want to specify a server manually, do the following:

1. To perform restore operations on Windows-based VMs, select the necessary server from the Windows mount server list. For a server to be displayed in the list of available servers, it must be added to the backup infrastructure as described in Veeam Backup & Replication User Guide, section [Adding Microsoft Windows Servers](https://helpcenter.veeam.com/docs/vbr/userguide/add_windows_server_console.html?ver=13). If you have not added the server to Veeam Backup & Replication beforehand, you can do it without closing the Add External Repository wizard. To do that, click Add and complete the New Windows Server wizard.
2. To perform restore operations on Linux-based VMs, select the necessary server from the Linux mount server list. For a server to be displayed in the list of available servers, it must be added to the backup infrastructure as described in Veeam Backup & Replication User Guide, section [Adding Linux Servers](https://helpcenter.veeam.com/docs/vbr/userguide/add_linux_server_console.html?ver=13). If you have not added the necessary server to Veeam Backup & Replication beforehand, you can do it without closing the Add External Repository wizard. To do that, click Add and complete the New Linux Server wizard.
3. To perform Instant Recovery or scan backups with SureBackup in VMware vSphere environments, click Configure settings. In the Mount Server Settings window, do the following:

1. Select the Enable vPower NFS service on the mount server check box to make the backup repository accessible by the [Veeam vPower NFS Service](https://helpcenter.veeam.com/docs/vbr/userguide/vpower_nfs_service.html?ver=13).

|  |
| --- |
| Important |
| It is not recommended that you enable Microsoft Windows NFS services on the same VM that runs Veeam vPower NFS Service. Otherwise, both services may fail to work properly. |

1. Click Ports to customize network ports used by the Veeam vPower NFS Service. By default, Veeam vPower NFS Service uses port 1058 to mount the vPower NFS datastore to the ESXi host and port 2049 to connect to the target NFS share.
2. In the Instant recovery write cache folder field, specify a folder that will be used for storing cache files.

![Step 7. Specify Mount Server Settings](images/add_repo_encryption.webp)

Related Topics

* [Verifying Backups](verify_backups.md)
* [Instant Recovery](performing_instant_recovery.md)
* [Performing Guest OS File Recovery](guest_file_recovery.md)
* [Performing Application Item Restore](application_items_restore.md)


