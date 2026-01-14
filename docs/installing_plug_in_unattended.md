---
title: "installing_plug_in_unattended"
source_url: "https://helpcenter.veeam.com/docs/vbazure/guide/installing_plug_in_unattended.html"
last_updated: "8/19/2025"
product_version: "8.0.1.202"
---


In this article

You can install or uninstall Veeam Plug-in for Microsoft Azure in the unattended mode using the command line interface. The unattended mode does not require user interaction — the installation runs automatically in the background, and you do not have to respond to the installation wizard prompts. You can use it to automate processes in large-scale environments.

To install Veeam Plug-in for Microsoft Azure in unattended mode, use either of the following options:

* If Veeam Plug-in for Microsoft Azure is a part of Veeam Backup & Replication installation package, follow the instructions provided in the Veeam Backup & Replication User Guide, section [Installing Veeam Backup & Replication in Silent Mode](https://helpcenter.veeam.com/docs/backup/vsphere/install_vbr_answer_file.html?ver=120).
* If Veeam Plug-in for Microsoft Azure is delivered as a separate .EXE file, use the instructions from this subsection.

Before You Begin

Before you start unattended installation, do the following:

1. Download the Veeam Plug-in for Microsoft Azure .EXE file as described in section [Installing Plug-In](installing_plug_in.md) (steps 1–4).
2. Check compatibility of Veeam Plug-in for Microsoft Azure and Veeam Backup & Replication versions. For more information, see [System Requirements](system_requirements.md#compatibility).

Installation Command-Line Syntax

Open the command prompt and run the .EXE file using the following parameters:

|  |
| --- |
| %path% /silent /accepteula /acceptlicensingpolicy /acceptthirdpartylicenses /acceptrequiredsoftware [/uninstall] |

The following command-line parameters are used to run the setup file:

| Parameter | Required | Description |
| --- | --- | --- |
| %path% | Yes | Specifies a path to the installation .EXE file on the backup server or in a network shared folder. |
| /silent | Yes | Sets the user interface level to None, which means no user interaction is needed during installation. |
| /accepteula | Yes | Confirms that you accept the terms of the Veeam license agreement. |
| /acceptlicensingpolicy | Yes | Confirms that you accept the Veeam licensing policy. |
| /acceptthirdpartylicenses | Yes | Confirms that you accept the license agreement for 3rd party components that Veeam incorporates. |
| /acceptrequiredsoftware | Yes | Confirms that you accept the license agreements for each required software that Veeam will install. |
| /uninstall | No | Uninstalls the plug-in.  Example: ”AzurePlugin\_12.8.0.293.exe /silent /accepteula /acceptlicensingpolicy /acceptthirdpartylicenses /acceptrequiredsoftware /uninstall” |

Page updated 8/19/2025

Page content applies to build 8.0.1.202
