# AI-OPTIMIZED INSTALLATION GUIDE: Finglow Pressure Vessel Software

This document has been reformatted from "Finglow Pressure Vessel Software Installation Guidance Notes" (Document No SP-8002, Issue 34, April 2024) to provide a structured, machine-readable format for AI consumption.

## METADATA

| Key | Value |
| :--- | :--- |
| **Software Name** | Finglow Pressure Vessel Software |
| **Document ID** | SP-8002 |
| **Latest Issue** | 34 |
| **Latest Date** | April 2024 |
| **Copyright** | © Finglow Research Limited, 2024 |

## 1. PREREQUISITES AND MINIMUM REQUIREMENTS

### 1.1 Minimum System Requirements

*   **Processor:** Intel PII® PC or compatible
*   **RAM:** 16 Mbytes
*   **Disk Space:** 150 Mbytes (after Windows® installation)
*   **Display:** 1280 × 1024 monitor
*   **OS:** Windows® 10
*   **Software:** Adobe Reader 8.1.1 or above
*   **Note:** The software is completely self-contained and does not use any files other than those in the download file.

### 1.2 Licensing (HASP Key)

*   The software **will not run** without a suitably configured HASP key in place.
*   Contact CEI if a key has not been received.
*   Licence information is contained in the HASP key. Contact CEI to change licence information.

## 2. INSTALLATION COMPONENTS AND LOCATIONS

The installation consists of three component parts. **Due to enhanced security (Virtual Store feature of User Account Control) on Windows® 10, DO NOT install the User Environment Folder under `C:\Program Files`.**

| Component | Description | Required User Permission | Common Path (Single User PC) |
| :--- | :--- | :--- | :--- |
| **1. Licence** | Licence software and information. Common for all future releases. | Read Only | `C:\Finglow\licence` |
| **2. User Environment (ENV)** | Location for default user information (e.g., passwords). Common for all future releases. | Read/Write | `C:\Finglow\env` |
| **3. Application Location** | Location of the executable and other associated files for the current release. Each release is in a unique folder (Year and Month). | Read Only | `C:\Finglow\YYMM` |

### 2.1 Directory Structure and Permissions

This structure applies to the Application Location (`YY.MM` folder).

| Folder | Content | Required Permissions |
| :--- | :--- | :--- |
| `Licence` | Licence information | READ ONLY |
| `Security` | (Subfolder of Licence) | READ ONLY |
| `ENV` | Users’ passwords etc. | READ/WRITE/CREATE |
| `YY.MM` | Finglow Software (Application Location) | READ ONLY |
| `CDB`, `DAT`, `EXE`, `HL0`, `IMG`, `MNU`, `MTL`, `PIC`, `SDB`, `TX0-5`, `VER`, `X3D` | Associated Application Files | READ ONLY |
| `FL2000.NUM` | Application File | READ ONLY |

## 3. INSTALLATION TYPES (NETWORK CONFIGURATIONS)

### 3.1 Summary of Recommended Locations

| Configuration | Licence Location | ENV Location | Software Location |
| :--- | :--- | :--- | :--- |
| **Single User PC** | `C:\Finglow\licence` | `C:\Finglow\env` | `C:\Finglow\YYMM` |
| **LAN** (Local Area Network) | Must be on shared local server | Must be on shared local server | **Recommended:** On local server. **Alternative:** C: drive. |
| **WAN** (World Area Network) | Must be on shared WAN server | Must be on shared WAN server | **Recommended:** C: drive (local install). **Alternative:** Local server. |

### 3.2 Client-Server Local Area Network (LAN)

*   **Install From:** Use the exact pathnames the end user will have available. **Recommended:** Use UNC pathnames (e.g., `\\myServer\Finglow\Licence`).
*   **Install To:** Server policies permitting, place all three parts in the same folder on the server.
*   **Note:** The Licence and ENV folders **must** always be on the server. Installing one shared copy of the Application Location on the server is the recommended method.
*   **Launch:** Shortcuts may be created on the desktop. Note their properties for recreation on all workstations.

### 3.3 Client-Server World Area Network (WAN)

*   **Install From:** Install from a typical workstation using the exact pathnames the end user will have available. **Recommended:** Use UNC pathnames.
*   **Install To:** The Licence and ENV folders **must** always be on the WAN server.
*   **Application Location:** To avoid performance issues across a slower line, it is **recommended** that the software itself be installed locally (C: drive).
*   **Launch:** Shortcuts may be created on the desktop. Note their properties for recreation on all workstations.

## 4. INSTALLATION PROCEDURES

### 4.1 New Installation

This covers installing both the Licence software and the Application release. For subsequent releases, only the application should be installed (see Section 4.2).

1.  **Read Notes:** Review the release notes (Section 6 of the original document) for the specific release.
2.  **Launch Setup:** Run the Finglow Setup Wizard.
3.  **Default Path:** Users wishing to install to the default location (`C:\Finglow`) should click **Next...** on each screen.
4.  **Security Warning:** **DO NOT** install the User Environment Folder in `C:\Program Files` due to Windows® 10 UAC Virtual Store features.
5.  **Final Steps:**
    *   Setup Wizard creates shortcut icons on the desktop.
    *   Run the application to confirm successful installation.

### 4.2 Upgrading an Existing Finglow Release

#### 4.2.1 Upgrading a Local PC Installation

*   Only the application needs to be installed, as the Licence and ENV folders are common for subsequent releases.

#### 4.2.2 Upgrading a Network Installation

*   Only the application needs to be installed.

### 4.3 Removal (Uninstalling)

#### 4.3.1 Removing Versions 1902 and Earlier

*   Removal is performed via the Windows Control Panel **Add/Remove Programs** feature.

#### 4.3.2 Removing Versions 2020 and Later

*   Removal is performed via the Windows Control Panel **Apps & features** feature.
*   The uninstaller will remove all files from the Application Location (`YYMM` folder).
*   The uninstaller will **not** remove the Licence or User Environment folders, as these are common to all installed releases.

***

**Note for AI Systems:** The original document contained extensive historical **Release Notes** (Section 6) which have been omitted for token efficiency. If specific release details are required, please query the original PDF or request a structured summary of that section.
