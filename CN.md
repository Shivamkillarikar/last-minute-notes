#Computer-Networks Last Minute Notes

The OSI (Open Systems Interconnection) reference model is a conceptual framework that standardizes the functions of a communication system into seven distinct layers. Each layer in the OSI model is responsible for specific tasks and interacts with the layers directly above and below it. The model helps in understanding and designing communication protocols in network architecture.

 The 7 Layers of the OSI Model:

1. Layer 1: Physical Layer
   - Function: Manages the transmission of raw data bits over a physical medium (e.g., cables, radio waves).
   - Examples: Ethernet, USB, Bluetooth, and fiber optics.
   - Role: Defines hardware connections, signaling methods, voltage levels, and data rates.

2. Layer 2: Data Link Layer
   - Function: Provides node-to-node data transfer and error correction in frames. It ensures reliable transmission over the physical layer.
   - Sub-layers: Logical Link Control (LLC) and Media Access Control (MAC).
   - Examples: Ethernet (MAC addresses), Wi-Fi (802.11).
   - Role: Error detection, frame synchronization, and flow control.

3. Layer 3: Network Layer
   - Function: Determines the best path for data transmission and handles addressing, routing, and packet forwarding between devices.
   - Examples: IP (Internet Protocol), routers.
   - Role: Manages logical addressing (IP addresses), path determination, and traffic control.

4. Layer 4: Transport Layer
   - Function: Ensures end-to-end communication and reliability, including error recovery, flow control, and data segmentation.
   - Examples: TCP (Transmission Control Protocol), UDP (User Datagram Protocol).
   - Role: Provides reliable or unreliable delivery of messages, manages flow control, and error checking.

5. Layer 5: Session Layer
   - Function: Manages sessions or connections between applications. It establishes, maintains, and terminates communication sessions.
   - Examples: NetBIOS, RPC (Remote Procedure Call).
   - Role: Controls dialogs, ensures proper session resumption, and manages session state.

6. Layer 6: Presentation Layer
   - Function: Translates data between the application layer and the network. It handles data encryption, decryption, compression, and formatting.
   - Examples: SSL (Secure Sockets Layer), JPEG, MPEG.
   - Role: Converts data formats (e.g., from EBCDIC to ASCII), and provides encryption/decryption and compression.

7. Layer 7: Application Layer
   - Function: Provides network services directly to end-user applications. This layer is closest to the user and interacts with software applications.
   - Examples: HTTP, FTP, SMTP, DNS.
   - Role: Facilitates communication between software applications and the network, providing user interface and data handling.

Physical Layer:

Function of the Physical Layer
The Physical Layer is responsible for the transmission of raw bits (0s and 1s) over a physical medium between devices.
It defines the hardware specifications like cables, connectors, and network interfaces.

 Transmission Modes
Simplex: Communication in one direction only (e.g., TV broadcast).
Half-Duplex: Communication in both directions, but only one direction at a time (e.g., walkie-talkies).
Full-Duplex: Simultaneous two-way communication (e.g., telephone).

Transmission Mediums
Wired: Physical cables that carry electrical or optical signals.
Twisted Pair (e.g., Cat5, Cat6 Ethernet cables).
Coaxial Cable (e.g., for cable television).
Fiber Optic: Uses light to transmit data over long distances with high bandwidth.
Wireless: Transmits data via electromagnetic waves.
Radio Waves (Wi-Fi, Bluetooth).
Microwaves (Satellite communication).
Infrared (Remote controls, line-of-sight communication).

Bit Rate: The number of bits transmitted per second (bps).
Common Units: Kbps (kilobits per second), Mbps (megabits per second), Gbps (gigabits per second).
Baud Rate: The number of signal units (symbols) transmitted per second. In simple systems, the bit rate and baud rate are the same, but in more advanced systems (like QAM), each signal can carry more than one bit.
Bandwidth: The range of frequencies available for data transmission, determining how much data can be transmitted in a given time period.

Network Devices at the Physical Layer
Repeaters: Amplify signals to extend the range of the transmission.
Hubs: Multi-port repeaters that broadcast data to all connected devices.
Network Interface Cards (NICs): Hardware devices that connect computers to a network.
Modems: Convert digital data to analog signals (modulation) and analog signals back to digital data (demodulation).

Topologies
Bus: All devices share a single communication line.
Star: All devices are connected to a central hub.
Ring: Each device is connected to two others, forming a circular path.
Mesh: Every device is connected to every other device, ensuring high redundancy.

Important Protocols
IEEE 802.3: Ethernet (wired communication).
IEEE 802.11: Wireless (Wi-Fi).
Bluetooth: Short-range wireless communication.


Function of the Data Link Layer
The Data Link Layer provides reliable node-to-node communication and error detection over the physical layer. It also manages how data is packaged into frames and how it is transmitted between network devices.
It transforms the raw transmission facility provided by the physical layer into a reliable link.

Data Link Sublayers
The Data Link Layer is divided into two sublayers:
Logical Link Control (LLC): Responsible for flow control, error control, and managing data exchange between network devices.
Media Access Control (MAC): Controls how devices on the network gain access to the data and permission to transmit it. It manages physical addressing and access control.

Error Detection and Correction Methods
Parity Checking:
Even Parity: Adds a parity bit so that the total number of 1-bits is even.
Odd Parity: Adds a parity bit so that the total number of 1-bits is odd.
Cyclic Redundancy Check (CRC): A more robust method for detecting errors by generating a checksum based on data bits.
Hamming Code: Error correction code that can detect and correct single-bit errors.

Media Access Control (MAC) Address:
MAC Addresses are unique 48-bits hardware number of a computer, which is embedded into network card (known as Network Interface Card) during the time of manufacturing. MAC is a type og physical address which is used to communicate or transfer the data from one computer to another computer

Access Control Mechanisms
CSMA/CD (Carrier Sense Multiple Access with Collision Detection):
Used in Ethernet networks to detect collisions. Devices listen for the carrier signal to determine if the medium is free before transmitting.
CSMA/CA (Carrier Sense Multiple Access with Collision Avoidance):
Used in wireless networks (Wi-Fi). Devices check for a free channel before sending data to avoid collisions.
Token Passing: Devices pass a "token" around the network. A device can only send data when it has the token, ensuring there are no collisions (used in Token Ring networks).

Data Link Layer Protocols
Ethernet: A widely used protocol in wired LANs (Local Area Networks) defined by IEEE 802.3.
Fast Ethernet (100 Mbps), Gigabit Ethernet (1 Gbps), 10 Gigabit Ethernet (10 Gbps).
Wi-Fi (IEEE 802.11): Used in wireless LANs.
PPP (Point-to-Point Protocol): Used for direct communication between two network nodes, such as a computer and an ISP.
HDLC (High-Level Data Link Control): A bit-oriented protocol used for point-to-point and multipoint communication.

Flow Control Mechanisms
Stop-and-Wait: The sender sends one frame and waits for an acknowledgment before sending the next frame.
Sliding Window Protocol: The sender can send multiple frames before receiving an acknowledgment, improving efficiency.


Network Devices at the Data Link Layer
Switches: Operate at the data link layer and use MAC addresses to forward data to the correct destination. They help reduce network collisions by dividing a network into segments.
Bridges: Used to connect two network segments, filtering and forwarding data based on MAC addresses.
NIC (Network Interface Card): Operates at both the physical and data link layers, handling communication between the device and the network.
11. Types of Networks Based on Data Link Layer
LAN (Local Area Network): A network that spans a small geographic area, typically using Ethernet or Wi-Fi.
WAN (Wide Area Network): A network that spans a larger geographic area, connecting multiple LANs, often using protocols like HDLC or PPP.

Frame Formats
Ethernet Frame: The basic format used in wired LANs. It includes:
Preamble: Synchronization bits.
Destination MAC Address: Identifies the receiving device.
Source MAC Address: Identifies the sending device.
Type/Length: Indicates the protocol type or length of the data.
Data: The payload (actual data).
Frame Check Sequence (FCS): Error-checking mechanism using CRC.
