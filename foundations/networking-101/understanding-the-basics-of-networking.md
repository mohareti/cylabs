---
description: "Networking is a cornerstone of modern technology, connecting devices and facilitating communication across the globe."
---

# Understanding the Basics of Networking

Networking is a cornerstone of modern technology, connecting devices and facilitating communication across the globe. In this blog post, we'll dive into the foundational elements of networking that allow computers to interact seamlessly and securely.

#### TCP/IP: The Language of the Internet

TCP/IP, which stands for Transmission Control Protocol/Internet Protocol, is essentially the language that computers on the internet use to communicate. It is a suite of communication protocols that orchestrate the flow of data across networks. TCP/IP guides how data should be packaged, addressed, transmitted, routed, and received at the destination. These protocols are divided into four abstraction layers:

1. **Link Layer**: This is where data packets are encoded and decoded into bits.
2. **Internet Layer**: IP operates here, routing the data packets independently of the route they take.
3. **Transport Layer**: TCP operates at this layer, ensuring the data packets are reliable and in sequence.
4. **Application Layer**: This is where network applications operate, using the networking services to send and receive data.

#### OSI Layer: The Seven Layers of Network Communication

The Open Systems Interconnection (OSI) model is a conceptual framework used to understand network interactions in seven distinct layers. Each layer serves a specific function and communicates with the layers directly above and below it:

1. **Physical Layer**: Deals with the physical connection between devices, transmitting raw bit streams over a physical medium.
2. **Data Link Layer**: Responsible for node-to-node data transfer and error correction from the physical layer.
3. **Network Layer**: Manages device addressing, tracks the location of devices on the network, and determines the best way to move data.
4. **Transport Layer**: Coordinates data transfer between end systems and hosts.
5. **Session Layer**: Establishes, manages, and terminates connections between local and remote applications.
6. **Presentation Layer**: Transforms data into a format that the application layer can accept.
7. **Application Layer**: Provides network services to applications software such as email, file transfer, and web browsing.

#### TCP vs UDP: Reliable vs Speed

TCP (Transmission Control Protocol) and UDP (User Datagram Protocol) are two protocols that operate at the Transport Layer (Layer 4) of the OSI model. They have different characteristics and uses:

* **TCP** is connection-oriented, meaning a connection is established and maintained until the application programs at each end have finished exchanging messages. It ensures that data is received accurately and in the same order it was sent, which is crucial for applications where reliability is important, like web browsing and email.
* **UDP** is connectionless, meaning it doesn't establish a connection before sending data, and there's no guarantee the data you send will reach its destination. Its simplicity provides a faster, albeit less reliable, form of communication used in streaming media or online gaming where speed is more critical than reliability.

The three-way handshake is a fundamental process used in the Transmission Control Protocol (TCP) to establish a reliable connection between two devices on a network. It ensures both sides are ready to communicate and synchronizes their data transmission before any actual data is sent. Here's a breakdown of the three steps involved:

## 1. SYN (Synchronize)

* The **client** initiates the connection by sending a segment with the SYN flag set. This flag indicates that the client is requesting to start a new connection and includes a **randomly chosen sequence number**. This sequence number acts like a starting point for keeping track of the order of data packets that will be exchanged during the communication.

## 2. SYN-ACK (Synchronize Acknowledgement)

* The **server**, upon receiving the SYN packet from the client, responds with a segment that has both the SYN and ACK (Acknowledge) flags set.
  * The **SYN flag** in the server's response acknowledges the client's synchronization request.
  * The **ACK flag** carries a value equal to one plus the client's sequence number. This acknowledges the client's initial sequence number and informs the client about the starting sequence number the server will use for its data transmissions.

## 3. ACK (Acknowledge)

* Finally, the **client** sends another segment with just the ACK flag set. This acknowledges the server's SYN-ACK segment and indicates that the client is ready to begin data transfer.

## Importance of the Three-Way Handshake

* **Reliable Connection Establishment:** The handshake ensures both parties agree to establish a connection and are prepared to exchange data.
* **Synchronization:** The sequence numbers exchanged during the handshake allow both sides to keep track of the order in which data packets are received and ensure proper reassembly at the destination.
* **Preventing Old Connections:** By using randomly chosen sequence numbers, the handshake helps prevent accidentally connecting to a lingering half-closed connection from a previous session.

## Analogy

Imagine the three-way handshake like a handshake between two people before a dance.

1. **Client:** "Hi, I'd like to dance. Here's a starting step I came up with (sequence number)."
2. **Server:** "Great! I'm ready too (SYN). Here's my starting step for you to follow (ACK based on your step)."
3. **Client:** "Acknowledged, let's dance!" (ACK)

Once the three-way handshake is complete, the connection is established, and data exchange can begin reliably using the synchronized sequence numbers.

#### IP Addresses and Ranges: The Addressing System of the Internet

An IP address is a unique identifier assigned to every device connected to a network that uses the IP for communication. IP addresses have two formats:

* **IPv4**: Comprises four numbers separated by dots, e.g., 192.168.1.1.
* **IPv6**: Uses eight groups of four hexadecimal digits, e.g., 2001:0db8:85a3:0000:0000:8a2e:0370:7334.

IP ranges refer to a succession of contiguous IP addresses. They are crucial for managing and allocating addresses within networks and across the internet.

There are five classes of IP addresses defined in the IPv4 addressing scheme. Each class is designated by a specific range of IP addresses and is used to accommodate networks of varying sizes. The classes are differentiated based on the leading octet (the first eight bits) of the IP address.

* **Class A:** Class A networks were designed for very large organizations with a massive number of hosts. The range of Class A addresses is from 1.0.0.0 to 127.0.0.0. Since only the first octet is used for the network address, a significant portion of the remaining address space is available for assignable host addresses within the network. However, due to the depletion of IPv4 addresses, Class A allocations are no longer available.
* **Class B:** Class B networks are intended for medium-sized organizations with a moderate number of hosts. The range of Class B addresses is from 128.0.0.0 to 191.255.0.0. Class B addresses provide a balance between the number of networks and the number of assignable hosts per network.
* **Class C:** Class C networks are suitable for small organizations or home networks with a limited number of hosts. The range of Class C addresses is from 192.0.0.0 to 223.255.255.0. Class C addresses offer the most significant number of networks but limit the number of assignable hosts per network.
* **Class D:** Class D addresses are reserved for multicast addressing, which allows a single data transmission to be sent to a group of receivers simultaneously. The range of Class D addresses is from 224.0.0.0 to 239.255.255.255.
* **Class E:** Class E addresses are reserved for future use or experimental purposes. The range of Class E addresses is from 240.0.0.0 to 255.255.255.255.

It's important to remember that the concept of classful addressing is no longer widely used in modern internet protocol (IP) address management due to the depletion of IPv4 addresses. A more flexible approach called Classless Inter-domain Routing (CIDR) has been adopted to optimize IP address allocation. CIDR allows for the borrowing of bits from the host portion of an IP address to create subnets, enabling a more efficient distribution of IP addresses.

Unlike IPv4, IPv6 doesn't have classes defined with specific address ranges. IPv6 uses a much larger address space (128 bits compared to 32 bits in IPv4) and a different allocation strategy. Here's a breakdown of IPv6 addressing:

* **Full Address Range:** IPv6 addresses span from 0000:0000:0000:0000:0000:0000:0000:0000 to ffff:ffff:ffff:ffff:ffff:ffff:ffff:ffff.
* **Network Prefixes:** IPv6 addresses are assigned in blocks called prefixes. These prefixes define the network portion of the address, similar to the network address in classful IPv4. Prefixes are written in CIDR notation (e.g., 2001:db8::/64), where the initial part is the hexadecimal representation of the address and the ending part (/ followed by a number) indicates the number of contiguous 1's at the beginning of the address that define the network part.
* **Special Address Types:** IPv6 reserves specific address ranges for various purposes:
  * **Loopback:** ::1/128 - This is similar to 127.0.0.1 in IPv4 and represents the loopback address for the local machine.
  * **Link-Local:** fe80::/64 - Addresses in this range are automatically generated and are valid only on the local network segment. Similar to auto-configuration addresses in IPv4 (169.254.0.0/16).
  * **Unique Local:** fc00::/7 - These addresses are not routable on the public internet but can be used for private addressing within an organization.
  * **Multicast:** ff00::/8 - This range is used for sending data to a group of devices simultaneously.
* **No Classes:** There's no formal classification system for public IPv6 prefixes like Class A, B, or C in IPv4. The Internet Assigned Numbers Authority (IANA) allocates prefixes to Regional Internet Registries (RIRs) who further distribute them to Local Internet Registries (LIRs) and ultimately to end users.

In summary, IPv6 uses a flexible addressing scheme with prefixes and special address ranges instead of predefined classes. This approach allows for more efficient allocation of the vast IPv6 address space.

Subnetting is a fundamental concept in computer networking that deals with dividing a large network into smaller, more manageable segments called subnets. It leverages the flexibility within an IP address to create logical subdivisions.

Here's a breakdown of the concept:

## Why Subnet?

* **Efficiency:** Large networks with a vast number of devices can become congested and slow. Subnetting reduces the number of devices on each subnet, improving network performance and traffic flow.
* **Security:** Subnets can isolate different departments or user groups within an organization. This restricts unauthorized access to sensitive resources on other subnets.
* **Scalability:** As a network grows, it's easier to add new devices to a specific subnet rather than expanding the entire network infrastructure.

## How Does Subnetting Work?

An IP address has two parts:

* **Network Address:** This identifies the subnet to which a device belongs.
* **Host Address:** This uniquely identifies a specific device within the subnet.

Subnetting works by borrowing bits from the host portion of the IP address to create a subnet mask. The subnet mask defines the boundary between the network and host addresses. Devices within the same subnet share the same network address but have unique host addresses.

For example, consider an IP address like 192.168.1.0 with a subnet mask of 255.255.255.0 (also written in CIDR notation as /24). In this scenario, the first three octets (192.168.1) represent the network address, and the last octet (0) defines the host address. The subnet mask indicates that all 24 bits in the first three octets are used for the network address, leaving the last 8 bits (0 in this case) for host addressing. This subnet can accommodate 256 (2^8) possible devices (excluding the network address itself, which is reserved).

By changing the subnet mask (borrowing bits from the host portion), you can create subnets with varying numbers of assignable host addresses. For instance, a /27 subnet mask would provide 32 assignable addresses within that subnet.

## Benefits of Subnetting

* Improved network performance and efficiency
* Enhanced security by isolating network segments
* Increased scalability to accommodate network growth
* Better organization and management of network resources

Subnetting is a crucial concept for network administrators to understand and implement effectively to design and manage secure, scalable, and efficient network infrastructures.

In the context of computer networking, a gateway acts as a **translator and traffic director** for data flowing between different networks. It allows devices on one network to communicate with devices on another network that may use different protocols or addressing schemes.

Here's a breakdown of how gateways function:

* **Connection Point:** A gateway sits at the juncture of two or more networks. It can be a hardware device like a router or software program designed to handle data translation and routing.
* **Protocol Translation:** Networks often use different communication protocols, which are essentially the languages devices use to understand each other. Gateways can translate data from one protocol to another, ensuring compatibility and enabling communication between networks.
* **Routing:** When a device on one network sends data to a device on another network, the data packet is directed to the gateway. The gateway analyzes the destination address and routing information to determine the most efficient path to send the data packet. It then forwards the packet to the appropriate network segment.
* **Security:** Gateways can also play a role in network security. Some gateways incorporate firewall functionalities to filter incoming and outgoing traffic, helping to control access and prevent unauthorized communication.

Here are some real-world examples of gateways:

* **Home Router:** The router you use in your home network acts as a gateway, connecting your devices to the wider internet. It translates data between your local network protocol and the internet protocol (TCP/IP).
* **Enterprise Gateways:** Organizations often deploy more sophisticated gateway devices to manage traffic flow between their internal networks and the internet. These gateways may provide additional security features and manage complex routing policies.
* **Cellular Network Gateways:** When you use your phone's cellular data service, your phone communicates with a cellular network gateway that connects the cellular network to the internet.

In essence, gateways play a critical role in enabling communication and data exchange across diverse networks, forming the backbone of our interconnected digital world.

LAN and WAN are two fundamental types of computer networks that differ in their scope and purpose:

## LAN (Local Area Network)

* Covers a **limited geographical area**, typically a home, office building, or school campus.
* Connects devices in close physical proximity, like computers, printers, tablets, and smartphones.
* Offers **high data transfer rates** due to the short distances involved and the use of dedicated cabling or high-bandwidth wireless technologies.
* Relatively **simple to set up and manage**.
* Examples: Your home Wi-Fi network connecting your laptop, phone, and smart speaker, or the network in an office building allowing all the computers to share resources.

## WAN (Wide Area Network)

* Spans a **large geographical area**, potentially stretching across cities, countries, or even the entire globe.
* Connects geographically dispersed LANs or individual devices over long distances.
* Typically has **lower data transfer rates** compared to LANs due to factors like reliance on leased lines, satellite connections, or the internet itself.
* Often involves more complex **security measures** and management considerations due to the vast distances and potential for unauthorized access.
* Examples: The internet itself, a company's network connecting its offices in different cities, or a bank's network connecting its ATMs across a country.

Here's a table summarizing the key differences:

| Feature              | LAN (Local Area Network)   | WAN (Wide Area Network)                              |
| -------------------- | -------------------------- | ---------------------------------------------------- |
| Scope                | Limited geographical area  | Large geographical area                              |
| Devices connected    | Devices in close proximity | Geographically dispersed devices or LANs             |
| Data transfer rate   | High                       | Lower                                                |
| Typical uses         | Homes, offices, schools    | Large organizations, geographically spread locations |
| Setup and management | Relatively simple          | More complex                                         |

#### Ports and Services: Communication Endpoints

A network port is a virtual point where network connections start and end. Ports are software-based and allow multiple services to listen on a network interface for incoming requests. Each port is associated with a specific process or service to provide multiplexing services over the network.

For example, HTTP traffic usually uses port 80, while HTTPS uses port 443. When you type a web address into your browser, it uses these port numbers to access web services.

In summary, understanding these basic networking concepts is essential for anyone navigating the world of IT, cybersecurity, or any field that relies on networked communications. These fundamentals lay the groundwork for more advanced networking knowledge and practices.

Here's a list of some of the most common TCP and UDP ports and their associated services:

## TCP Ports

* **Port 21:** FTP (File Transfer Protocol) - Used for transferring files between computers.
* **Port 22:** SSH (Secure Shell) - Provides secure remote access to a computer system.
* **Port 23:** Telnet (deprecated) - Unencrypted remote login protocol (not recommended due to security risks).
* **Port 25:** SMTP (Simple Mail Transfer Protocol) - Used for sending emails.
* **Port 53:** DNS (Domain Name System) - Translates domain names (like \[invalid URL removed]) into IP addresses.
* **Port 80:** HTTP (Hypertext Transfer Protocol) - The foundation of web communication, used for accessing websites.
* **Port 443:** HTTPS (Secure Hypertext Transfer Protocol) - Encrypted version of HTTP, securing communication between web browser and server.
* **Port 110:** POP3 (Post Office Protocol) - Used for retrieving emails from a mail server.
* **Port 143:** IMAP (Internet Message Access Protocol) - Another protocol for accessing emails, offering more features than POP3.
* **Port 3389:** RDP (Remote Desktop Protocol) - Enables remote graphical access to a desktop environment.

## UDP Ports

* **Port 53:** DNS (Domain Name System) - Can also be used over UDP for DNS queries (less common than TCP for DNS).
* **Port 67:** DHCP (Dynamic Host Configuration Protocol) - Used by devices to obtain IP addresses from a DHCP server (UDP for server responses).
* **Port 68:** DHCP (Dynamic Host Configuration Protocol) - Used by devices to request IP addresses from a DHCP server (UDP for client requests).
* **Port 161:** SNMP (Simple Network Management Protocol) - Used for network device management and monitoring.
* **Port 1900:** Used for some streaming protocols like UPnP (Universal Plug and Play).
* **Port 5000:** Often used for various UDP-based communication protocols or custom applications.
* **Port 5060:** SIP (Session Initiation Protocol) - Used for VoIP (Voice over IP) calls.

**Note:** This is not an exhaustive list, and there are many other ports used for various services and applications. It's important to consult reliable sources for specific port number and service information.
