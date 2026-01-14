---
title: "managing_permissions"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/managing_permissions.html"
last_updated: "8/20/2025"
product_version: "8.0.1.202"
---


In this article

Veeam Backup for Microsoft Azure controls access to its functionality with the help of user roles. A role defines what operations users can perform and what range of data is available to them in the Veeam Backup for Microsoft Azure UI.

There are 3 user roles that you can assign to users working with Veeam Backup for Microsoft Azure:

* Portal Administrator — can perform all configuration actions, and can also act as a Portal Operator and Restore Operator.
* Portal Operator — can create and edit backup policies, perform backup and restore operations, manage protected data and track session statistics.
* Restore Operator — can only perform restore operations and track session statistics.
* Read-Only User — can only view backup policies, monitor protected data and track session statistics.

|  |
| --- |
| Important |
| The list of portal users may display user accounts with the Company Administrator role assigned — these accounts are intended to be used for the integration of Veeam Backup for Microsoft Azure and Veeam Service Provider Console, and are created using the [Veeam Service Provider Console plug-in](https://helpcenter.veeam.com/docs/vac/provider_admin/integration_clouds.html?ver=80). It is not recommended that you perform any actions with these users. |

The following table describes the functionality available to users with different roles in the Veeam Backup for Microsoft Azure UI.

| Tab | Functionality | Portal Administrator | Portal Operator | Restore Operator | Read-Only User |
| --- | --- | --- | --- | --- | --- |
| Overview | Dashboard | Full | Full | N/A | Full |
| Resources | Infrastructure | Full | Full | N/A | N/A |
| Policies | Backup policies | Full | Full | N/A | Read-only |
| Protected Data | Protected resources list | Full | Full | Full | Read-only |
| Restore | Full | Full | Full | N/A |
| File-level restore | Full | Full | Full | N/A |
| Remove | Full | Full | N/A | N/A |
| Session Log | Session logs | Full | Full | Full | Full |
| Stop session execution | Full | Full | Full | N/A |
| Configuration | | | | |  |
| Accounts | Service accounts, SQL Server and SMTP accounts, portal users | Full | N/A | N/A | N/A |
| Repositories | Backup repositories and storage vaults | Full | N/A | N/A | N/A |
| Worker Instances | Worker instances | Full | N/A | N/A | N/A |
| Policy Templates | SLA and storage templates | Full | Full | N/A | N/A |
| Settings | General settings | Full | N/A | N/A | N/A |
| Licensing | Licensing | Full | N/A | N/A | N/A |
| Support Information | Updates and logs | Full | N/A | N/A | N/A |

In This Section

* [Adding User Accounts](user_account_add.md)
* [Editing User Accounts](user_account_edit.md)
* [Changing User Passwords](changing_password.md)
* [Changing Default Admin Password](changing_default_admin_password.md)
* [Enabling Multi-Factor Authentication](configuring_mfa_settings.md)

Page updated 8/20/2025

Page content applies to build 8.0.1.202
