# Linux File System

![](https://lh7-us.googleusercontent.com/_UolDzov4oHsp7lys2ZKdN55wPgXhOXbZgTnHdcbIsFvgS754O6KV4_4843pJJz-jxIEVhMOE_iPIWcLNnXVJXW2ySRR5ZJj-HOlSzrLiNhxvsqoFO-zJiNDtWmcKfOklVbebBwvg74slzZPq8nMSyU)

## Key Concepts

* **Hierarchical Structure:** Linux organizes everything into a single, tree-like structure starting with the root directory (`/`). All files and directories are branches on this tree.
* **File Types:** Linux doesn't rely on file extensions as heavily as some other operating systems. It supports several file types:
  * **Ordinary files:** Contain data (text, binaries, images, etc.)
  * **Directories:** Contain files and other directories.
  * **Links:** Pointers to other files
  * **Device Files:** Represent hardware devices.
  * **Sockets:** Provide inter-process communication channels.
  * **Named pipes:** Used for one-directional communication between processes.

## Standard Directories

The Filesystem Hierarchy Standard (FHS) defines a common structure for most Linux distributions. Here are key directories:

* `/` (Root):The top-level directory containing everything.
* **`/bin`:** Essential user commands (ls, cat, etc.).
* **`/sbin`:** System administration commands.
* **`/boot`:** Bootloader files.
* **`/etc`:** System-wide configuration files.
* **`/home`:** Users' home directories.
* **`/lib`:** Shared libraries for programs
* **`/tmp`:** Temporary files
* **`/usr`:** Secondary hierarchy (user programs, libraries, etc).
* **`/var`:** Variable data like log files.

## Inodes and File Permissions

* **Inodes:** Each file and directory has an inode – a data structure storing file metadata:
  * Permissions (read, write, execute)
  * Owner and group
  * File size, timestamps
  * Pointers to the file's data blocks
* **Permissions:** Linux uses a fine-grained permission system for access control:
  * **User (u):** The file's owner
  * **Group (g):** A group the file belongs to
  * **Others (o):** Everyone else
  * **Read (r), Write (w), Execute (x):** Permissions for each category

![](https://lh7-us.googleusercontent.com/jKp8a_qT7XHA_PsjFpAsB1ic-LIDnpOn1XO-U3mqz62q2L1Hrqu_gKDS2PP-GXMnupE1sLpYmeGBbgYDK7TSP41JupGzdLsN4UU2_ihsSIogGWrRMaZKWRnj-yZSiyzTQ1XEWGbJ7akdat1382LQVoE)

## Mounting and Unmounting

* **Mounting:** Attaching additional filesystems (e.g., hard drives, USB sticks) to the main filesystem hierarchy, making them accessible from a "mount point" (directory).
* **Unmounting:** Detaching a filesystem.

## Common File System Tools

* **Navigation:** `cd` (change directory), `ls` (list), `pwd` (working directory).
* **Manipulation:** `cp` (copy), `mv` (move/rename), `rm` (delete), `mkdir` (create directory), `touch` (create a file)
* **Searching:** `find` (flexible search), `grep` (search within files)
* **Permissions:** `chmod` (change permissions), `chown` (change owner)

## File Systems Types

Linux supports various file systems designed for different use cases:

* **ext4:** The standard for many Linux distros. Reliable and efficient.
* **Btrfs:** Modern file system with copy-on-write, snapshots, etc.
* **XFS:** High-performance, optimized for large files.
* **JFS:** Designed for journaling to improve reliability.
* **ZFS:** Advanced features like pooling, snapshots, and compression.
