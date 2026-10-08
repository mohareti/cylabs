---
description: "The Purdue Model, also known as the Purdue Enterprise Reference Architecture (PERA), is a framework designed to improve the security of industrial control systems (ICS) by advocating for network segmentation."
---

# Purdue Model

The Purdue Model, also known as the Purdue Enterprise Reference Architecture (PERA), is a framework designed to improve the security of industrial control systems (ICS) by advocating for network segmentation. It defines different zones with varying levels of security and restricts communication flow between them.

## Purpose

* The primary goal of the Purdue Model is to isolate critical industrial control systems from potential threats originating from the business network or the internet. This segmentation helps prevent malware or unauthorized access from disrupting critical operations.

## Zones and Security Levels

The model divides the network into six logical zones, each with increasing levels of security and restrictions:

1. **Physical Process (Level 0):** This zone represents the actual physical equipment and sensors involved in the industrial process. It's not part of the network itself.
2. **Intelligent Devices (Level 1):** This zone encompasses sensors and actuators that directly monitor and control the physical processes. They communicate with controllers in Level 2.
3. **Control Systems (Level 2):** This zone includes Programmable Logic Controllers (PLCs), Distributed Control Systems (DCS), and other devices that manage and regulate the industrial process in real-time.
4. **Manufacturing Operations (Level 3):** This zone houses Human-Machine Interfaces (HMI) used by operators to monitor and interact with the control systems. It might also include engineering workstations for process optimization.
5. **Enterprise Resource Planning (Level 4):** This zone encompasses business IT systems like ERP, MES (Manufacturing Execution Systems), and SCADA (Supervisory Control and Data Acquisition) systems that monitor and manage the overall production process.
6. **Business Network (Level 5):** This zone represents the organization's standard corporate network, including email servers, internet access, and other business applications.

## Communication Flow

* Communication is generally allowed only between adjacent levels. For example, Level 2 control systems can communicate with Level 1 sensors and Level 3 HMIs, but not directly with Level 5 business systems.
* Firewalls and other security controls are implemented at the boundaries between zones to restrict unauthorized access and enforce data flow policies.

## Benefits of the Purdue Model

* **Improved Security:** Network segmentation creates a layered defense, making it more difficult for attackers to breach critical systems.
* **Reduced Risk of Disruption:** By isolating the control network, the Purdue Model helps prevent malware or unauthorized access from impacting core operations.
* **Enhanced Manageability:** Segmenting the network simplifies network management and facilitates the implementation of specific security controls for each zone.

## Limitations and Considerations

* **Complexity:** Implementing and maintaining a segmented network can be complex, especially for larger or more intricate industrial control systems.
* **Legacy Systems:** Integrating the Purdue Model with existing, non-compliant legacy systems might require additional effort and modifications.
* **Evolving Threats:** The model should be viewed as a foundational framework, and security measures need to be continuously updated to address evolving cyber threats.
