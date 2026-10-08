---
description: "Shell scripting is a powerful method to automate tasks on Unix-like operating systems."
---

# Shell Scripting

Shell scripting is a powerful method to automate tasks on Unix-like operating systems. A shell script is a text file with a series of commands that the shell can execute. It is often used for repetitive tasks, for instance, backups, system monitoring, and file manipulation, so that you don't have to enter each command manually.

**Variables:** In shell scripting, variables are placeholders or references to data that can change. Variables in shell scripts don't need to be declared and can store strings, integers, or the output of commands.

```sh
MY_VARIABLE="Hello, World!"
echo $MY_VARIABLE
```

**Accepting Input from User:** You can accept input from the user using the `read` command.

```sh
echo "Enter your name:"
read USER_NAME
echo "Hello, $USER_NAME!"
```

**Showing Output:** To show output in shell scripting, you typically use the `echo` or `printf` commands.

```sh
echo "This will display on the console."
printf "This will %s on the console.\n" "also display"
```

## Standard Streams

* `stdin` (standard input) is the stream where a program reads its input data. It's typically connected to the keyboard, but can also be redirected to read from a file or another command.
* `stdout` (standard output) is the stream where a program writes its output data. It's typically displayed on the screen but can be redirected to files or other programs.
* `stderr` (standard error) is the stream where a program writes its error messages. It's separate from stdout to allow users to separate regular output from error messages.

## Redirecting Streams

* `>` redirects stdout to a file, overwriting the file.
* `>>` redirects stdout to a file, appending to the file.
* `2>` redirects stderr to a file.
* `<` redirects a file to stdin.

**Conditions:** Conditional statements allow you to perform different actions based on conditions.

```sh
if [ $USER_NAME == "admin" ]; then
    echo "Welcome, admin."
else
    echo "Access denied."
fi
```

**Loops:** Loops are used for executing a series of commands repeatedly.

* For loop:

```sh
for i in 1 2 3; do
    echo "Number $i"
done
```

* While loop:

```sh
while [ $i -lt 5 ]; do
    echo "i is less than 5"
    i=$((i+1))
done
```

* Until loop:

```sh
until [ $i -ge 5 ]; do
    echo "i is less than 5"
    i=$((i+1))
done
```

Shell scripting is versatile and can include advanced features like functions, arrays, and signal trapping. It's a critical skill for system administrators and developers working in a Unix-like environment.\
Below is an example of a shell script that demonstrates core features of shell scripting in the context of a cybersecurity assessment scenario. This script will simulate the following:

1. Check if a list of domains is accessible.
2. Download the homepage of each domain.
3. Search for a specific pattern within the downloaded page that may indicate a security vulnerability (like an exposed admin panel or a specific software version).
4. Log the results and errors for review.

Please note that this script is for educational purposes only and should not be used without permission on any domain.

```sh
#!/bin/bash

# Define a list of domains to check
DOMAINS=("example.com" "testsite.com" "demo.org")

# Pattern to search for in the downloaded content
PATTERN="AdminPanel"

# Directory where we will store the results
RESULT_DIR="scan_results"
mkdir -p "$RESULT_DIR"

# Function to check domain availability and search for a pattern
check_domain() {
    local domain=$1

    # Use wget to download the homepage
    if wget -q -O - "$domain" > "$RESULT_DIR/$domain.html"; then
        echo "[+] Successfully downloaded homepage for $domain"
        
        # Use grep to search for the pattern
        if grep -q "$PATTERN" "$RESULT_DIR/$domain.html"; then
            echo "[!] Found the pattern '$PATTERN' in $domain!"
            echo "$domain" >> "$RESULT_DIR/pattern_found.txt"
        else
            echo "[-] Pattern not found in $domain."
        fi
    else
        echo "[!] Failed to download the homepage for $domain" >&2
        echo "$domain" >> "$RESULT_DIR/errors.txt"
    fi
}

# Loop through the list of domains and call the check_domain function
for domain in "${DOMAINS[@]}"; do
    echo "Checking $domain..."
    check_domain "$domain"
done

echo "Scan completed. Results and errors stored in $RESULT_DIR directory."
```

To run this script:

1. Save the script to a file, for example, `domain_check.sh`.
2. Make the script executable with `chmod +x domain_check.sh`.
3. Run the script with `./domain_check.sh`.

This script showcases variable usage, function definitions, conditional statements, loops, pattern searching with `grep`, and network communication with `wget`. The logging is split into standard output for successful checks and standard error for issues, demonstrating stream redirection.

Port Scanning Script

Below is a shell script that accepts an IP range as input and scans for open ports 21 (FTP), 22 (SSH), 80 (HTTP), and 443 (HTTPS) using `nc` (Netcat). This script assumes that Netcat is installed on the system where it's executed. It uses a simple loop and timeout strategy to quickly check if the ports are open.

```sh
#!/bin/bash

# Function to scan ports using Netcat
scan_ports() {
    local ip=$1
    local ports=(21 22 80 443)
    for port in ${ports[@]}; do
        nc -zv -w 1 $ip $port 2>&1 | grep succeeded
    done
}

# Read the IP range from the user
read -p "Enter the IP range (e.g., 192.168.1.1-192.168.1.255): " ip_range

# Validate IP range input
if [[ ! $ip_range =~ ^[0-9]+\.[0-9]+\.[0-9]+\.[0-9]+-[0-9]+\.[0-9]+\.[0-9]+\.[0-9]+$ ]]; then
    echo "Invalid IP range format."
    exit 1
fi

# Extract start and end IP from the range
IFS='-' read -r start_ip end_ip <<< "$ip_range"
IFS='.' read -r s1 s2 s3 s4 <<< "$start_ip"
IFS='.' read -r e1 e2 e3 e4 <<< "$end_ip"

# Convert IPs to integers for comparison
start_ip_int=$(printf "%03d%03d%03d%03d" $s1 $s2 $s3 $s4)
end_ip_int=$(printf "%03d%03d%03d%03d" $e1 $e2 $e3 $e4)

if [[ $start_ip_int -gt $end_ip_int ]]; then
    echo "Start IP cannot be greater than end IP."
    exit 1
fi

# Begin the scanning loop
current_ip=$start_ip
while [[ $start_ip_int -le $end_ip_int ]]; do
    echo "Scanning $current_ip..."
    scan_ports $current_ip

    # Increment IP
    ((s4++))
    if [ $s4 -gt 255 ]; then
        s4=0
        ((s3++))
    fi
    if [ $s3 -gt 255 ]; then
        s3=0
        ((s2++))
    fi
    if [ $s2 -gt 255 ]; then
        s2=0
        ((s1++))
    fi
    if [ $s1 -gt 255 ]; then
        echo "Finished scanning the IP range."
        break
    fi

    current_ip="$s1.$s2.$s3.$s4"
    start_ip_int=$(printf "%03d%03d%03d%03d" $s1 $s2 $s3 $s4)
done

echo "Port scanning completed."
```

To use this script:

1. Save the script to a file, for instance, `port_scan.sh`.
2. Make the script executable: `chmod +x port_scan.sh`.
3. Run the script and enter the IP range when prompted: `./port_scan.sh`.

The script prompts for an IP range, calculates the integer equivalents of the start and end IPs for iteration, and uses a `while` loop to scan each IP address in the range. The `nc` (Netcat) command is used with the `-z` flag to scan without sending data, and the `-w 1` flag to set a timeout of 1 second for faster scans. The results will show only the connections that succeeded.

References:

{% embed url="<https://devhints.io/bash>" %}

{% embed url="<https://www.hostinger.com/tutorials/bash-script-example>" %}

{% embed url="<https://linuxcommand.org/lc3_writing_shell_scripts.php>" %}

{% embed url="<https://www.tutorialspoint.com/unix/unix-system-logging.htm>" %}
