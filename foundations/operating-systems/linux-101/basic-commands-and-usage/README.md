---
description: "Linux, with its robust set of commands, is a playground for those who crave control over their computing environment."
---

# Basic Commands and Usage

Linux, with its robust set of commands, is a playground for those who crave control over their computing environment. Whether you are a system administrator, a developer, or a cybersecurity enthusiast, mastering Linux commands is an essential skill. Let's delve into some of the fundamental commands and their usage in various scenarios, including network communication, file manipulation, system management, and security testing.

Certainly, let's go through each of the Linux commands listed and explain their basic usage:

1. **`ls`**: This command lists the contents of a directory. If no directory is specified, it lists the contents of the current directory. For example, `ls /home` will list all files and directories in the `/home` directory.
2. **`pwd`**: Stands for "print working directory". This command prints the full pathname of the current working directory.
3. **`cd`**: Stands for "change directory". This command changes the current directory to another one. For example, `cd /var/www` changes the current directory to `/var/www`.
4. **`man`**: This command displays the user manual of any command that we can run on the terminal. For example, `man ls` shows the manual pages for the `ls` command.
5. **`adduser`**: The `adduser` command is used to create a new user. For example, `adduser moha` would create a new user named moha.
6.  To add a user to the sudoers group, the command should be `usermod -aG sudo moha`, where `moha` is the username.
7. **`touch`**: This command is used to create a new empty file. For example, `touch filename` will create a new file named `filename` in the current directory.
8. **`cp`**: This command is used to copy files and directories. For example, `cp source destination` will copy the file from source to destination.
9. **`rm`**: This command is used to remove files or directories. For example, `rm filename` will delete the file named `filename`. It is a command that must be used with caution.
10. **`echo`**: This command is used to display a line of text/string that are passed as an argument. For example, `echo hello > demo` creates a file named `demo` and writes "hello" to it.
11. **`echo hello >> demo`**: Appends "hello" to the file `demo`. If `demo` does not exist, it will be created.
12. **File Permissions**:

    * **Read (4)**: Permission to read the file.
    * **Write (3)**: Permission to modify the file.
    * **Execute (1)**: Permission to execute the file as a program/script.

    File permissions are denoted as a three-digit number, with each digit corresponding to the user, group, and others, respectively.
13. **`chmod`**: This command changes the file permissions. For example, `chmod 755 filename` sets the read, write, and execute permissions for the user, and read and execute permissions for the group and others for `filename`.
14. **Editors (`vi` and `nano`)**:
    * **`vi`**: A text editor in the Unix systems, `vi filename` opens the file in the `vi` editor.
    * **`nano`**: A simpler, user-friendly text editor, `nano filename` opens the file in the `nano` editor.
15. **`cat`**: Concatenate files and print on the standard output. For example, `cat filename` will display the contents of `filename`.
16. **`grep`**: Used to search text or searches the given file for lines containing a match to the given strings or words. For example, `grep 'pattern' filename` will search for 'pattern' in `filename`.
17. **`cut`**: Removes sections from each line of files. For example, `cut -d':' -f1 filename` will cut the first field from each line in `filename`.
18. **`sed`**: Stands for "stream editor", it is used to perform basic text transformations on an input stream. For example, `sed 's/old/new/g' filename` will replace all occurrences of 'old' with 'new' in `filename`.
19. **`awk`**: A programming language and utility that excels at text processing and is often used for data extraction and reporting. For example, `awk '{print $1}' filename` will print the first column in `filename`.
20. whoami

Each of these commands can be very powerful and are often combined in scripts or command lines to perform complex tasks. Always ensure you understand the commands and use them carefully, especially when modifying or deleting files.

#### File and Text Manipulation Commands

* **`wget`**: This network downloader can retrieve files from the web and is often used to download packages or files from a specified URL.
* **`cat`**: Short for concatenate, `cat` reads file contents and outputs them in the terminal. It’s often piped with other commands for file creation and merging.
* **`grep`**: The global regular expression print command is used to search for text patterns within files. For example, `grep "cisco\.com"` would search for instances of 'cisco.com'.
* **`cut`**: This command is used to extract sections from each line of files, often combined with delimiters to parse data.
* **`sort -u`**: Sorts the input data and `-u` flag ensures that the output is unique, removing duplicate lines.
* **`find`**: A powerful command to search for files in a directory hierarchy, capable of running commands on the files found.
* **`locate`**: Quickly searches for files by name, leveraging a database updated by `updatedb`.

#### Network Communication with Netcat

* **`netcat` (nc)**: A versatile networking tool used for reading from and writing to network connections using TCP or UDP. It's used for creating server-client setups, port scanning, and transferring files.
  * **Listening mode**: `nc -nlvp 444` sets up a listener on port 444, which can be used to receive data.
  * **Connecting mode**: `nc -nc victim_ip 444` initiates a connection to a listening port, enabling data transfer.

#### System Services Management

* **SSH**: `ssh` command is used for secure remote logins to other systems. Managing the SSH service involves starting (`service ssh start`) and stopping (`service ssh stop`) the daemon, as well as enabling persistence across reboots (`update-rc.d ssh enable`).
* **Apache**: Managing the Apache web server often involves starting (`service apache2 start`) and stopping (`service apache2 stop`) the service, as well as enabling it at boot (`update-rc.d apache2 enable`).

#### Cybersecurity and Penetration Testing Commands

* **`chmod +x` and `chmod 777`**: These commands change the file permissions to make scripts executable or universally accessible, a necessary step in many penetration testing tasks.
* **`ping sweep`**: A basic network scanning technique to discover active hosts on a network.
* **`bindshell` and `reverse shell`**: Techniques used to maintain access to a compromised system. The bind shell opens a new service on the victim, while the reverse shell makes the victim connect to the attacker's system.
* **`ncat`**: An advanced version of `netcat` that provides additional features like SSL encryption for secure communication.

#### Regular Expressions and Scripting

* **Bash Script**: A bash script can automate the process of finding subdomains and IP addresses. For example, a loop like \`for url in $(file.txt); do ...; done

\` can iterate through a list of URLs in a file and perform actions on each.

* **Regular expressions**: Used with commands like `grep`, they allow for pattern matching and data extraction from text files.

#### Monitoring and Diagnostics Tools

* **Wireshark**: A GUI-based network protocol analyzer that can capture and interactively browse the traffic running on a computer network. It's used extensively in network troubleshooting and analysis.
* **Remote Desktop**: `rdesktop` is a command-line utility that allows you to create a remote desktop session with another system.

#### System Update and Upgrade

* **Apt-get Commands**: On Debian-based systems, `apt-get update`, `apt-get upgrade`, and `apt-get dist-upgrade` are used to update the package index and then upgrade all the installed packages to their latest versions.

#### Using Linux Commands in Penetration Testing

The aforementioned Linux commands are not only useful for regular system administration tasks but are also crucial in the context of cybersecurity and penetration testing. Here's a brief overview of how some of these commands can be used in a penetration testing scenario:

* **Ping Sweep**: Used to identify which IP addresses are active on a network.
* **Netcat**: A Swiss army knife for networkers which can be used to set up ad-hoc servers to catch or send data. It can also be used for port scanning and is frequently employed in the creation of backdoors and reverse shells.
* **Bind Shell and Reverse Shell**: Creating a command-line interface on the victim's system that can be accessed remotely by an attacker, allowing them to execute commands as if they were physically present.
* **Firewall Bypassing with Ncat**: By using SSL with Ncat, attackers can attempt to bypass firewall restrictions on a network to establish a secure and hidden channel.

## Shell Scripting

* **Definition:** Shell scripting is a way to automate tasks and create programs within a command-line interface (CLI) environment like Bash, Zsh, or PowerShell.
* **Uses:**
  * System administration: Automating repetitive tasks like backups, updates, and file management.
  * Data processing: Manipulating files, text, and data within the CLI.
  * Creating custom tools: Building small programs to enhance command-line workflows.
* **Components:** shell scripts are composed of:
  * **Commands:** Standard commands you'd normally type at the command prompt (like `ls`, `cd`, `grep`)
  * **Variables:** Placeholders for storing data.
  * **Control flow structures:**
    * Conditional statements (if, else)
    * Loops (for, while)
  * **Functions:** Reusable blocks of code

## Shell Operators

Shell operators are special symbols used within shell scripts to perform various operations. Here are some main categories:

* **Arithmetic Operators**
  * **+** (addition)
  * **-** (subtraction)
  * **\*** (multiplication)
  * \*\*/ \*\* (division)
  * **%** (modulo: remainder after division)
* **Comparison Operators**
  * **-eq** (equal to)
  * **-ne** (not equal to)
  * **-gt** (greater than)
  * **-lt** (less than)
  * **-ge** (greater than or equal to)
  * **-le** (less than or equal to)
* **Logical Operators**
  * **!** (NOT)
  * **&&** (AND)
  * **||** (OR)
* **File Test Operators**
  * **-e** (file exists)
  * **-d** (directory exists)
  * **-f** (regular file exists)
  * **-r** (file is readable)
  * **-w** (file is writable)
* **String Operators**
  * **=** (string equality)
  * **!=** (string inequality)
  * **-z** (string is empty)

## Example

A simple shell script to check if a file exists and is readable:

Bash

```bash
#!/bin/bash
filename="my_file.txt"

if [ -f $filename ] && [ -r $filename ]; then
    echo "The file exists and is readable."
else
    echo "The file does not exist or is not readable."
fi
```

#### Conclusion

In the realm of Linux, the command line is the gateway to a world of powerful functionalities. From managing files and processes to securing and diagnosing network systems, the knowledge of these basic commands is invaluable. Whether you're scripting a quick one-liner to find a subdomain or leveraging Netcat for complex network interactions, each command holds the potential to unlock a deeper understanding of the Linux operating system. As Linux continues to evolve and be adopted in various sectors, these commands serve as the foundational tools for anyone looking to harness the full potential of this open-source powerhouse.

## In this section

* ✅ [Shell Commands](shell-commands.md)
