---
title: "Performing File-Level Recovery"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/performing_flr.html"
last_updated: "3/13/2026"
product_version: "8.0.1.202"
---

# Performing File-Level Recovery


In case a disaster strikes, you can recover corrupted or missing files of an Azure VM from a cloud-native snapshot or image-level backup. Veeam Backup for Microsoft Azure allows you to download the necessary files and folders to a local machine, or restore the files and folders of the source Azure VM to the original location, using the [File-level recovery browser](flr_download.md).

To recover files and folders of a protected Azure VM, do the following:

1. [Launch the File-Level Recovery wizard](flr_wizard.md).
2. [Select a restore point](flr_restore_point.md).
3. [Configure restore settings](flr_restore_settings.md).
4. [Specify a restore reason](flr_reason.md).
5. [Finish working with the wizard — start a recovery session](flr_restore_session.md).
6. [Choose files and folders to recover](flr_download.md).
7. [Stop the recovery session](flr_stop_session.md).


