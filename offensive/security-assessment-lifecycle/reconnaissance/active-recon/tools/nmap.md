---
description: "Conducting asset scanning using various network scanning tools can help you discover devices and services on a network."
---

# Nmap

Conducting asset scanning using various network scanning tools can help you discover devices and services on a network. Here are examples of how to conduct asset scanning using Nmap, Masscan, network scanning via TOR nodes, network scanning via a VPS (Virtual Private Server), and network scanning via VPN (Virtual Private Network):

## Asset Scanning with Nmap

[Nmap](https://nmap.org/) is a versatile and widely used open-source network scanning tool. It offers various scan types and commands to discover devices and services on a network.

* **Ping Scan (Discover Live Hosts):**

  ```bash
  nmap -sn <target>
  ```
* **Basic Service Discovery:**

  ```bash
  nmap -sV <target>
  ```
* **Port Scan (TCP SYN Scan):**

  ```bash
  nmap -sS -p <ports> <target>
  ```
* **Full Port Scan:**

  ```bash
  nmap -p- <target>
  ```
* **OS Detection:**

  ```bash
  nmap -O <target>
  ```
* Protocol Scanning
  * TCP
  * UDP

For more advanced scanning options and customizations, refer to the [Nmap documentation](https://nmap.org/book/man-briefoptions.html).
