# Windows 101

## Key Features and Architecture

* **Graphical User Interface (GUI):** Windows is known for its user-friendly graphical interface with a desktop, icons, windows, and a taskbar. This makes it more intuitive for less technical users.
* **Windows Kernel:** The core of the operating system, responsible for resource management, process scheduling, memory management, and hardware interaction.
* **Hybrid Kernel:** The Windows kernel combines aspects of monolithic and microkernel architectures, attempting to balance performance and stability.
* **Hardware Abstraction Layer (HAL):** Provides an interface between the kernel and the underlying hardware, enhancing compatibility across different hardware platforms.
* **Device Drivers:** Software that enables communication between hardware devices and the operating system.
* **System Services and APIs:** Provides a layer for developers to create applications that interact with the operating system and its features.

## File System

* **NTFS (New Technology File System):** The primary file system used in modern Windows versions. It offers features like:
  * File and folder permissions
  * File compression
  * Encryption
  * Journaling (for enhanced fault tolerance)
  * Quotas
* **FAT32 (File Allocation Table):** An older file system often used for compatibility with removable drives like USB sticks.

## User Accounts and Security

* **User Profiles:** Stores user-specific settings, files and preferences.
* **User Account Control (UAC):** A security feature that prompts for administrator permission before allowing certain changes, helping prevent malware.
* **Windows Defender:** Built-in antivirus and antimalware protection.
* **Windows Firewall:** Helps to protect from network-based attacks.

## Common Directories

* **C:\Windows:** Contains the Windows system files.
* **C:\Program Files:** Default location for installed programs.
* **C:\Users\[Username]:** Stores user profiles, including personal documents, settings, and data.

## Key Windows Tools and Settings

* **Control Panel:** Provides access to system settings like hardware configuration, user accounts, and display settings.
* **Settings app:** A modern interface for managing many of the same settings as the Control Panel.
* **Registry:** A hierarchical database that stores system-wide and application-specific configuration settings.
* **Task Manager:** Provides information on running processes, performance statistics, and allows you to manage processes.
* **Windows Update:** Handles the download and installation of security patches and software updates.

## Networking

* **TCP/IP:** Standard networking protocol suite used by Windows.
* **Network connections settings:** Allows configuration of network adapters, Wi-Fi connections, VPNs, and more.
* **File and printer sharing:** Allows sharing of resources across a network.

## Windows Editions

* **Windows Home:** Designed for consumer use.
* **Windows Pro:** Adds features for business users, such as domain joining, BitLocker encryption, and Group Policy management.
* **Windows Enterprise:** Includes even more advanced features for large organizations.
* **Windows Server:** Designed for servers, with roles like web server, file server, and domain controller.

Windows file system:

## Key Concepts

* **Hierarchical Structure:** Like other operating systems, Windows organizes everything into a tree-like structure. The top-level is represented by drive letters (usually C:). Files and folders are arranged in directories under these drives.
* **File and Folder Organization:** Each file and folder has attributes like name, timestamps (creation, modification), size, and permissions.
* **Drive Letters:** Windows assigns a letter (e.g., C:, D:) to physical drives, network drives, and partitions.

## NTFS: The Primary File System

NTFS (New Technology File System) is the default and most robust file system for modern Windows installations. Key features:

* **Security:**
  * **Permissions:** Fine-grained control over file and folder access (read, write, modify, etc.) for users and groups.
  * **Encryption (EFS):** Protects individual files and folders from unauthorized access.
* **Reliability:**
  * **Journaling:** Logs file changes, aiding recovery in case of crashes.
  * **Self-healing:** Can detect and repair some file system errors.
* **Efficiency:**
  * **Compression:** Option to reduce file size on disk.
  * **Disk Quotas:** Allows setting storage limits for individual users.
  * **Support for large files and volumes**

## Legacy File Systems

* **FAT32:** Older file system, often used for USB drives and compatibility with older devices. Limitations include:
  * No built-in security features
  * Maximum file size of 4GB
  * Maximum volume size limits
* **exFAT:** A newer file system designed for flash drives, overcoming some of the limitations of FAT32.

## Standard Folders

Windows has standard folders for organizing common file types:

* **C:\Windows:** Contains Windows system files.
* **C:\Program Files:** Default location for installed programs.
* **C:\Users\[Username]\Documents:** User's documents (text files, spreadsheets, etc.).
* **C:\Users\[Username]\Pictures:** User's image files.
* **C:\Users\[Username]\Desktop:** Files and shortcuts placed on the desktop.

## File System Management

* **File Explorer:** The primary interface for browsing files and directories.
* **Disk Management:** A tool for managing partitions, formatting drives, and assigning drive letters.
* **Command Prompt and PowerShell:** Command-line interfaces for file manipulation and advanced tasks.

## Important Notes

* You'll mainly encounter NTFS on most modern Windows systems.
* FAT32 is still common for external USB drives due to compatibility with non-Windows devices.

## Windows Folder

## C:\Windows

* **The Heart of Windows:** Houses the core operating system files. This includes essential components, drivers, DLL files, and system applications and utilities.
* **Why It's Critical:** Tampering with files within C:\Windows can render your operating system unstable or completely unusable.
* **Examples of Key Files:**
  * `explorer.exe` (Windows Shell/File Explorer)
  * `cmd.exe` (Command Prompt)
  * `winlogon.exe` (Handles the login process)
  * Many `.dll` files (Dynamic Link Libraries containing shared code)
* **Rule of Thumb:** Unless you *absolutely* know what you're doing, it's generally best to leave files in this directory undisturbed to avoid breaking the system.

## C:\Program Files and C:\Program Files (x86)

* **Home of Installed Applications:** These are the default locations for most programs you install.
  * **C:\Program Files:** Usually stores 64-bit applications.
  * **C:\Program Files (x86):** Usually stores 32-bit applications.
* **Why They're Critical:** These folders contain the executable files, configurations, libraries, and data needed for your applications to run. Deleting them carelessly will break the corresponding programs.
* **Contents:**
  * Program executables (`.exe` files)
  * Support libraries and data files
  * Configuration files
* **Note:** Manually messing with program files is rarely necessary; uninstallation should be handled through the Control Panel or the app's dedicated uninstaller.

## C:\Windows\System32

* **The Engine Room:** This directory holds a vast collection of files critical for the proper functioning of your Windows system.
* **Why It's Extra Critical:** Files in this folder are especially vital. Any accidental or intentional modification can have widespread consequences, potentially leading to system crashes or instability.
* **Key Contents:**
  * System-critical `.dll` files
  * Core system executables (e.g., `taskmgr.exe` for Task Manager, `regedit.exe` for the Registry Editor)
  * System configuration files
* **Best Practice:** Extreme caution is required when interacting with this folder.

## Important Considerations

* **System Protection:** Windows often has built-in mechanisms to prevent accidental modification of critical folders.
* **Malware Targets:** Malware sometimes tries to hide in these critical folders. Therefore, be wary of files you didn't place there yourself.
* **Backups:** Creating system backups is essential before major changes, providing a way to restore in case of issues.

## In this section

* ✅ [Windows system calls](windows-system-calls.md)
* ✅ [Windows Event Logs and IDs](windows-event-logs-and-ids.md)
* ✅ [Windows UAC](windows-uac.md)
* ✅ [Windows Registry](windows-registry.md)
* ✅ [Windows Bit Locker](windows-bit-locker.md)
* ✅ [Volume Shadow Copy Service](volume-shadow-copy-service.md)
* ✅ [Windows OS API's](windows-os-apis.md)
