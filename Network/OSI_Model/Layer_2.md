# Layer 2 - Data-Link

Protocol layer that transfers data between adjacent network modes in WAN or between nodes on the same LAN\
Ensures error free transmission of information\
Responsible for encoding/decoding and organizing the incoming/outgoing data\
Data are sent in frames

## Sub-layers of the Data Link Layer

### Logical Link Control (LLC)

- Deals with multiplexing (flow of data among applications and other services)
- Responsible for providing error messages and ackowledgments

### Media Access Control (MAC)

- Responsible for addressing frames
- Controls physical media access

## Functions

### Framing

- At the sender's side, DLL receives packets from the Network Layer and divides them into small frames, then sends each frame in bits to the Physical Layer.
- Adds error control data at the head/tail on the frame
- At the reciver's side, DLL receives bits from the Physical Layer and organizes them into the frame, then sends them to the Network Layer

### Addressing

- Encapsulates the source and destination's MAC address in the header of each frame
  - MAC address: AKA hardware or physical address. Unique 12-character attribute that is used to identify individual electonic devices on a network

### Error Control

- Detect the error in the transmitted data and correct it using error detection and correction techniques
- Adds error detection bits into the frame's header, so that receiver can check received data is correct or not

### Flow Control

- Synchronize the sender's and receiver's data flow speed and establish flow control between them
- If the receiver's receiving speed is lower than the sender's sending speed, overflow can be caused
- Overflow in the receiver's buffer can lead to data loss

### Access Control

- Checks which device has control over the channel to avoid data collision
- Collision Detection (CD) and Collision Avoidance (CA) can be used to avoid collisions and data loss

| Collision Detection                                            |                                     Collision Avoidance |
| :------------------------------------------------------------- | ------------------------------------------------------: |
| Effective after a collision                                    |                            Effective before a collision |
| Used in wired networks                                         |                      Commonly used in wireless networks |
| Only reduces the recovery time                                 |                  Minimizes the possibility of collision |
| Re-sends the data frame when a conflict occurs                 | First transmit the intent to send for data transmission |
| Used in 802.3 standard                                         |                                 Used in 802.11 standard |
| More efficient than simple CSMA(Carrier Sense Multiple Access) |   Similar to simple CSMA(Carrier Sense Multiple Access) |
| Type of CSMA to detect the collision                           |                         Type of CSMA to avoid collision |

## Popular Data Link Layer Protocols

- ARP (Address Resolution Protocol)
- CDP (Cisco Discovery Protocol)
- LLDP (Link Layer Discovery Protocol)
- IEEE 802.11 (Wireless LAN)
- LAPD (Link Access Procedures, D channel)
- SDN (Software-defined Networking)
- Spanning Tree Protocol
