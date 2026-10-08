# Shell Commands

## Finding Commands and Files

* **which:** Locates the full path to an executable file on your system. It's helpful for finding the exact location of a command you want to run.
  * Example: `which ls` (might output something like `/bin/ls`)
* **locate:** Quickly finds files based on names or patterns using a pre-built database. This can be faster than `find` for simple searches.
  * Example: `locate demo*` (finds all files starting with "demo")
  * **Important:** The `locate` database needs to be updated periodically using `updatedb` to ensure it reflects the latest file system changes.
* **updatedb:** Updates the database used by the `locate` command. This should be run regularly to keep the file location information accurate.
* **find:** Searches for files and directories based on various criteria, offering more flexibility than `locate`.
  * Example: `find / -name demo*` (finds all files starting with "demo" anywhere on the system)

## User Management

* **passwd:** Changes a user's password. It prompts you for the current password and then the new password you want to set.

## System Service Management (Systemd)

* **systemctl start ssh:** Starts the SSH (Secure Shell) service, allowing remote logins to the system.
* **systemctl enable ssh:** Enables the SSH service to start automatically when the system boots.

## Network Tools

* **netstat -antp | grep ssh:** Shows network connections, including those related to SSH (port 22 by default). The options used (`-antp`) provide detailed information about connections, including listening ports and processes using the connections.

## Downloading Files

* **wget:** Downloads a file from the internet.
  * Example: `wget https://example.com/file.txt` (downloads the file "file.txt" from the specified URL)

## Extracting Script Names from HTML (Not recommended for security reasons)

* The provided command pipe (`grep -o '<script[^>]src="[^"].js"' index.html | grep -o '"[^"]*.js"'`) attempts to extract script filenames from an HTML file (`index.html`) using regular expressions (grepping). However, it's generally not recommended to parse HTML with shell commands due to security risks and potential for errors. Consider using a safer approach like a programming language library designed for HTML parsing.

Here's a breakdown of the commands you requested:

## File Permissions

* **Chown:** Changes the ownership of a file or directory.
  * Syntax: `chown [owner][:group] file/directory`
  * Example: `chown john:users myfile.txt` (changes owner to "john" and group to "users")
* **Chmod:** Modifies file or directory permissions.
  * Syntax: `chmod [ugo][+-=][rwxX] file/directory`
    * `u` (user), `g` (group), `o` (others)
    * `+` (add permission), `-` (remove permission), `=` (set exact permissions)
    * `r` (read), `w` (write), `x` (execute), `X` (execute for directories)
  * Example: `chmod 754 myfile.txt` (sets full access for owner, read/execute for group and others)
* **Setuid:** Sets the owner's user ID for the process started by the file, regardless of the user who executes it (often used for security purposes).
  * Syntax: `chmod u+s file` (gives setuid permission to the owner)
* **Setgid:** Sets the group ID for the process started by the file, regardless of the user who executes it (used for group-specific actions).
  * Syntax: `chmod g+s file` (gives setgid permission to the group)

## Basic Commands

* **Echo:** Displays a line of text on the terminal.
  * Syntax: `echo "This is some text"`

## Network Tools

* **Nmap:** A powerful network scanner used for discovering hosts and services on a network.
  * Example: `nmap scanme.example.com` (scans the host "scanme.example.com")
* **Arping:** Sends ARP (Address Resolution Protocol) requests to identify MAC addresses associated with IP addresses on a network.
  * Example: `arping -a 192.168.1.0/24` (sends ARP requests to all devices on the 192.168.1.0 subnet)
* **Dig:** Queries DNS (Domain Name System) servers to look up domain name information.
  * `dig microsoft.com mx`: Retrieves mail exchange (MX) records for microsoft.com
  * `dig microsoft +short`: Performs a quick lookup and displays only the answer
* **Whois:** Looks up information about a domain name registrant.
  * Example: `whois google.com`
* **W:** Displays logged-in users and their terminals.
* **Lastlog:** Shows the last login time for all users.

## File Viewing and Management

* **Cat:** Displays the contents of a file.
  * Example: `cat /etc/passwd` (shows the system password file)

**Caution:** Be careful when using `cat` with sensitive files like `/etc/passwd` as it might display usernames and password hashes.

* **Less/More:** Similar to `cat` but allow page-by-page navigation for large files.

## Permissions and Processes

* **/etc/group:** This system file stores information about groups on the system.
* **/etc/sudoers:** This sensitive file defines which users have administrative privileges (sudo) and what commands they can run.

**Caution:** Never modify `/etc/sudoers` without a clear understanding of its implications, as it can compromise system security.

* **Lsof:** Lists open files and the processes that have them open.
  * `lsof -u <username>`: Shows files opened by a specific user.

## Package Management (Debian/Ubuntu)

* **apt-get install net-tools:** Installs the `net-tools` package, which provides basic networking utilities. Note that some newer systems may use `apt` instead of `apt-get`.

## Finding Files

* **which:** Locates the full path to an executable file.
  * Example: `which ls` (shows the location of the `ls` command)
* **locate:** Quickly finds files based on names or patterns in a pre-built database (update the database with `updatedb`).
  * Example: `locate demo*` (finds all files starting with "demo")
* **find:** Searches for files and directories based on various criteria (more powerful than `locate`).
  * Example: `find / -name demo*` (finds all files starting with "demo" anywhere on the system)

## User Management

* **passwd:** Changes a user's password (prompts for the current and new password
