# Finglow PDF Manual 2

This document is a machine-readable reformat of "Finglow Pressure Vessel Software Installation Guidance Notes" (Document No SP-8002, Issue 34, April 2024).

## METADATA

| Key               | Value                            |
| ----------------- | -------------------------------- |
| **Software Name** | Finglow Pressure Vessel Software |
| **Document ID**   | SP-8002                          |
| **Latest Issue**  | 34                               |
| **Latest Date**   | April 2024                       |
| **Copyright**     | © Finglow Research Limited, 2024 |

## 1. PREREQUISITES AND MINIMUM REQUIREMENTS

### 1.1 Minimum System Requirements

* Processor: Intel PII® PC or compatible
* RAM: 16 Mbytes
* Disk Space: 150 Mbytes (after Windows® installation)
* Display: 1280 × 1024 monitor
* OS: Windows® 10
* Software: Adobe Reader 8.1.1 or above

{% hint style="info" %}
The software is completely self-contained and does not use any files other than those in the download file.
{% endhint %}

### 1.2 Licensing (HASP Key)

{% hint style="danger" %}
The software will not run without a suitably configured HASP key in place.
{% endhint %}

* Contact CEI if a key has not been received.
* Licence information is contained in the HASP key. Contact CEI to change licence information.

## 2. INSTALLATION COMPONENTS AND LOCATIONS

Due to enhanced security (Virtual Store feature of User Account Control) on Windows® 10, DO NOT install the User Environment Folder under C:\Program Files.

The installation consists of three component parts.

| Component              | Description                                                                                                                         | Required User Permission | Common Path (Single User PC) |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ------------------------ | ---------------------------- |
| Licence                | Licence software and information. Common for all future releases.                                                                   | Read Only                | `C:\Finglow\licence`         |
| User Environment (ENV) | Location for default user information (e.g., passwords). Common for all future releases.                                            | Read/Write               | `C:\Finglow\env`             |
| Application Location   | Location of the executable and other associated files for the current release. Each release is in a unique folder (Year and Month). | Read Only                | `C:\Finglow\YYMM`            |

### 2.1 Directory Structure and Permissions

This structure applies to the Application Location (`YY.MM` folder).

| Folder                                                                               | Content                                 | Required Permissions |
| ------------------------------------------------------------------------------------ | --------------------------------------- | -------------------- |
| `Licence`                                                                            | Licence information                     | READ ONLY            |
| `Security`                                                                           | (Subfolder of Licence)                  | READ ONLY            |
| `ENV`                                                                                | Users’ passwords etc.                   | READ/WRITE/CREATE    |
| `YY.MM`                                                                              | Finglow Software (Application Location) | READ ONLY            |
| `CDB`, `DAT`, `EXE`, `HL0`, `IMG`, `MNU`, `MTL`, `PIC`, `SDB`, `TX0-5`, `VER`, `X3D` | Associated Application Files            | READ ONLY            |
| `FL2000.NUM`                                                                         | Application File                        | READ ONLY            |

## 3. INSTALLATION TYPES (NETWORK CONFIGURATIONS)

### 3.1 Summary of Recommended Locations

| Configuration            | Licence Location               | ENV Location                   | Software Location                                                 |
| ------------------------ | ------------------------------ | ------------------------------ | ----------------------------------------------------------------- |
| Single User PC           | `C:\Finglow\licence`           | `C:\Finglow\env`               | `C:\Finglow\YYMM`                                                 |
| LAN (Local Area Network) | Must be on shared local server | Must be on shared local server | Recommended: On local server. Alternative: C: drive.              |
| WAN (World Area Network) | Must be on shared WAN server   | Must be on shared WAN server   | Recommended: C: drive (local install). Alternative: Local server. |

### 3.2 Client-Server Local Area Network (LAN)

* Install From: Use the exact pathnames the end user will have available. Recommended: Use UNC pathnames (e.g., `\\myServer\Finglow\Licence`).
* Install To: Server policies permitting, place all three parts in the same folder on the server.
* Note: The Licence and ENV folders must always be on the server. Installing one shared copy of the Application Location on the server is the recommended method.
* Launch: Shortcuts may be created on the desktop. Note their properties for recreation on all workstations.

### 3.3 Client-Server World Area Network (WAN)

* Install From: Install from a typical workstation using the exact pathnames the end user will have available. Recommended: Use UNC pathnames.
* Install To: The Licence and ENV folders must always be on the WAN server.
* Application Location: To avoid performance issues across a slower line, it is recommended that the software itself be installed locally (C: drive).
* Launch: Shortcuts may be created on the desktop. Note their properties for recreation on all workstations.

## 4. INSTALLATION PROCEDURES

### 4.1 New Installation

This covers installing both the Licence software and the Application release. For subsequent releases, only the application should be installed (see Section 4.2).

{% stepper %}
{% step %}
### Read release notes

Review the release notes for the specific release (see the original document's Section 6).
{% endstep %}

{% step %}
### Launch Setup

Run the Finglow Setup Wizard.
{% endstep %}

{% step %}
### Default Path

If installing to the default location (`C:\Finglow`), click Next on each screen.
{% endstep %}

{% step %}
### Security warning

DO NOT install the User Environment Folder in `C:\Program Files` due to Windows® 10 UAC Virtual Store features.
{% endstep %}

{% step %}
### Final steps

* Setup Wizard creates shortcut icons on the desktop.
* Run the application to confirm successful installation.
{% endstep %}
{% endstepper %}

### 4.2 Upgrading an Existing Finglow Release

#### Upgrading a Local PC Installation

* Only the application needs to be installed, as the Licence and ENV folders are common for subsequent releases.

#### Upgrading a Network Installation

* Only the application needs to be installed.

### 4.3 Removal (Uninstalling)

#### Removing Versions 1902 and Earlier

* Removal is performed via the Windows Control Panel Add/Remove Programs feature.

#### Removing Versions 2020 and Later

* Removal is performed via the Windows Control Panel Apps & features feature.
* The uninstaller will remove all files from the Application Location (`YYMM` folder).
* The uninstaller will not remove the Licence or User Environment folders, as these are common to all installed releases.

<details>

<summary>Release Notes (historical)</summary>

The original document contained extensive historical Release Notes (Section 6) that have been omitted here for token efficiency. If you require specific release details, please provide the original PDF or request a structured summary of that section.

</details>
