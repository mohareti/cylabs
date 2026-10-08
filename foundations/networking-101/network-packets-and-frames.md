# Network Packets and Frames

## Packets: The Units of the Network Layer

* **Definition:** Packets are self-contained units of data that are routed across networks (like the internet). They carry the actual information you're sending.
* **Components:** A packet includes:
  * **Payload:** The actual data being transmitted (part of an image, a web page, an email, etc.)
  * **Header:** Contains control information like source and destination IP addresses, protocol type, and other metadata to help it reach its destination.

## Frames: The Units of the Data Link Layer

* **Definition:** Frames are used to transmit data over a physical network medium (like Ethernet or Wi-Fi). They are the "envelopes" that carry packets.
* **Components:** A frame includes:
  * **Header:** Contains source and destination MAC addresses (hardware addresses of network devices), error detection codes, and other information for transmission over the physical network.
  * **Payload:** This is the packet received from the network layer.
  * **Trailer:** May contain error checking information.

## How Packets and Frames Work Together

1. **Encapsulation:** Your computer creates a packet containing data. This packet is encapsulated within a frame at the data link layer.
2. **Transmission:** The frame with its payload (the packet) is sent over the physical network (like an Ethernet cable).
3. **Reception:** The receiving device strips off the frame headers and trailers. The remaining packet is passed up to the network layer.
4. **De-encapsulation:** The packet is further processed to eventually bring you the data you requested.

## Key Points

* Packets are about logical routing across networks.
* Frames are about physical transmission of data.
