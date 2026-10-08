# Active Recon

TCP and UDP are fundamental protocols that govern communication across networks, but they differ in their approach:

## TCP (Transmission Control Protocol)

* **Connection-oriented:** Establishes a virtual connection between two devices before data transmission, ensuring reliable and ordered delivery.
* **Reliable:** Uses error checking and retransmission mechanisms to guarantee data arrives correctly and in sequence.
* **Slower:** The connection setup and error checking introduce some overhead, making it slightly slower than UDP.
* **Suitable for:** Applications that require reliable data transfer, like web browsing, file transfer, and email.

## UDP (User Datagram Protocol)

* **Connectionless:** Sends data packets (datagrams) directly without establishing a connection, making it faster and simpler.
* **Unreliable:** Doesn't guarantee delivery or order of packets. Applications need to implement their own error checking if needed.
* **Faster:** Lower overhead due to the lack of connection setup and error checking.
* **Suitable for:** Applications that prioritize speed over reliability, like online gaming, live streaming, and DNS lookups.

## Scanning TCP and UDP Ports

Port scanning involves sending packets to specific ports on a target device to see if they are open (listening for connections) or closed (not accepting connections). Here's how it works:

1. **Specify Target:** You provide the IP address of the target device.
2. **Select Ports:** Define the range of ports you want to scan (common ports or custom ranges).
3. **Protocol Choice:** Choose between TCP or UDP scan depending on the type of service you're looking for.
4. **Scan Initiated:** The scanning tool sends packets to each port on the target device.
5. **Response Analysis:** The tool analyzes the response from the target device to determine if the port is open, closed, or filtered (firewalls might block the scan attempt).

## Tools for Port Scanning

Several tools are available for scanning TCP and UDP ports. Here are a few popular options:

* **Nmap (Network Mapper):** A free and open-source network security scanner with a vast array of features, including TCP and UDP port scanning. It offers various scan types, customization options, and powerful reporting capabilities. <https://nmap.org/>
* **Nessus:** A commercial vulnerability scanner with a comprehensive set of features, including TCP and UDP port scanning. It goes beyond basic port scanning to identify potential vulnerabilities on the target device. <https://www.tenable.com/products/nessus/nessus-professional>
* **Angry IP Scanner:** A free and easy-to-use tool for basic TCP and UDP port scanning. It provides a quick overview of open ports on a target device. <https://angryip.org/download/>
* **Netcat (nc):** A versatile command-line networking tool that can be used for various purposes, including basic TCP and UDP port scanning. <https://docs.oracle.com/cd/E86824_01/html/E54763/netcat-1.html>

## Network Scanning and Host Discovery

1. **Nmap:**
   * Nmap is a versatile open-source tool used for network scanning and host discovery. It can identify open ports, services, and OS details. Usage example: `nmap -sS -p 1-65535 -T4 -A target_ip`.
2. **Masscan:**
   * Masscan is a high-speed network scanner that can scan the entire internet in under six minutes. Usage example: `masscan -p1-65535 target_ip`.
3. **Angry IP Scanner:**
   * Angry IP Scanner is a lightweight and cross-platform network scanner for discovering active hosts. Usage example: Enter the target IP range and click "Start."
4. **Sparta:**
   * Sparta is a Python tool that combines multiple scanning and enumeration tools to simplify the information-gathering process.

## In this section

* ✅ [Tools](tools/README.md) · 3/16 pages written
