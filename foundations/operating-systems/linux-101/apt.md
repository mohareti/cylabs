---
description: "The apt command is a powerful command-line tool used for handling packages in Linux distributions that are based on Debian."
---

# apt

The `apt` command is a powerful command-line tool used for handling packages in Linux distributions that are based on Debian. It provides functions to search for, install, manage, and remove software packages, and it is commonly used in distributions like Ubuntu.

Here's a detailed explanation of each of the commands you've listed:

1. `sudo apt update`:
   * This command updates the list of available packages and their versions, but it does not install or upgrade any packages.
   * It retrieves new lists of packages from the repositories defined in `/etc/apt/sources.list` and `/etc/apt/sources.list.d/`.
   * The package index files from the sources are fetched and "Updated" in the local repository to know what new versions of packages are available.
2. `sudo apt dist-upgrade`:
   * This command, in addition to performing the function of `upgrade`, also intelligently handles changing dependencies with new versions of packages.
   * `dist-upgrade` will attempt to upgrade the most important packages at the expense of less important ones if necessary.
   * It is used to perform upgrades that may include adding or removing new packages or upgrading to a completely new version of the operating system.
3. `sudo apt auto-remove`:
   * This command is used to remove packages that were automatically installed to satisfy dependencies for some package and that are no more needed.
   * When you remove a package using `apt remove`, the package is removed but not necessarily the dependencies that were installed with it.
   * `auto-remove` will clean up these unneeded packages.
4. `updatedb`:
   * This command is not part of the `apt` package system. It's related to the `locate` command which is a fast way to search for files by filename on the system.
   * `updatedb` updates the database that is used by `locate`. It scans the file system to create a fresh database of all the file paths.
   * The updated database allows `locate` to quickly find the path to a file without having to scan the file system when the search is performed.

In summary:

* `sudo apt update` refreshes the local package index with the latest changes made in the repositories.
* `sudo apt dist-upgrade` upgrades all of the installed packages, and may install or remove packages in the process.
* `sudo apt auto-remove` removes any packages that were installed as dependencies and are no longer required by installed packages.
* `updatedb` creates or updates a database used by `locate` to find files quickly.

example

sudo apt install wireshark
