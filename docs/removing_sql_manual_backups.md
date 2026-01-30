---
title: "Removing SQL Backups Created Manually"
product: "vbazure"
doc_type: "guide"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/removing_sql_manual_backups.html"
last_updated: "3/14/2025"
product_version: "8.0.1.202"
---

# Removing SQL Backups Created Manually


To remove all backups created for a SQL database manually, follow the instructions provided in [Removing SQL Backups](removing_sql_backups.md). If you want to remove a specific image-level backup created manually, do the following:

1. Navigate to Protected Data > Databases > Azure SQL.
2. Select the check box next to the necessary Azure SQL database, and click the link in the Restore Points column.
3. In the Available Restore Points window, select the necessary restore point and click Remove Manual Backup.

[![Removing SQL Backups Created Manually](images/removing_manual_backups.webp)](images/removing_manual_backups.webp "Removing SQL Backups Created Manually")

Related Topics

[Creating SQL Backups Manually](creating_sql_backups_manually.md)


