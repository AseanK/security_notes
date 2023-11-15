# Network

## Network traffic

The amount of data that moves across a network

*Network data* is the data that's transmitted between devices on a network

- By understanding how data should be flowing acress the network, you can develop an understanding of expected network traffic flow
  - By knowing what's normal, you can easily spot what's abnormal
- Can detect traffic abnormalities through observation to spot *indicators of compromise*
  - Indicators of compromise (IoC)
    - Observable evidence that suggests signs of a potential security incident
    - I.e. data exfiltration: the unauthorized transmission of data from a system
  
![img](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/R-C-xmdWTRe8XfbJ4V9BMg_01d033967efe41ba898db5755db1f4f1_i-QtA3HA4BNT_yYXJ-qbty4-R8tuDG73XRllvRqnBMgcopHG7JmrlZYtjv-Jeorch1-w-rQhfh9u1ObkqF6KNsslNqhqyacRusAj38ehIjgImRN2lSB6DQ49MsFJCYgPdG2iBrOt-HEU99JuvC-070uPrh1M9UxFjb-Hvmfaa4yaGyn5kno71tlvVr_xgg?expiry=1700092800000&hmac=rERXP5Q1ZxeT3nbkmN46F2m_heC8kF4OuJ5d4lFFpj4)

- A baseline is a reference point that's used for comparison
- Once determined, you can monitor a network to identify any deviations from that baseline
  - Monitoring involves examining network components to detect unusual activities
    - I.e. large and unusual data transfer

### Flow analysis

- *Flow* refers to the movement of network communications and includes information related to packets, protocols, and ports
  - Packets can travel to ports, which receive and transmit communications
  - Ports are often, but not always, associated with network protocols
- Malicious actors can use protocols and ports that are not commmonly associated to maintain communications between the compromised system and their own machine
  - Command and Control (C2)
    - The techniques used by malicious actors to maintain communications with compromised systems
    - I.e. Malicious actors can use HTTPS protocol over port 8088 opposed to its commonly associated port 443 to communicate with compromised systems

### Network operations center (NOC)

An organizational unit that monitors the performance of a network and responds to any network disruption, such as a network outage

- SOC is focused on maintaining the security of an organization through detection and response
- NOC is responsible for maintaining network performance, availability, and uptime

## Data exfiltration attack

#### Process

##### Attacker

1. Before attackers can perform data exfiltration, they need to gain initial access into a network and computer system
  - This can be done through a social engineering attack
2. After compromising, the goal for attackers is to maintain access in the environment and avoid being detected for as long as possible
  - This can be done using a tatic known as *pivoting*, or lateral movement
  - They'll spend time exploring the network with the goal of expanding and maintaining their access to other systems on the network
3. As an attacker pivots in the network, they'll scope out the environment to identify valuable assets
4. After finding the assets of value, they need to collect, package, and prepare the data for exfiltration outside of the organization's network and into the attacker's hands
  - One way they may do this is by reducing the data size. This helps attackers hide the stolen data and bypass security controls
5. Finally, the attacker will exfiltrate the data to their destination of choice
  - FTP/email

##### Defender

1. Security teams must prevent attacker access
2. Security teams must monitor network activity to identify any suspicious activity that can indicate a compromise
3. As a part of an organization's security policy, all assets should be cataloged in an asset inventory
  - The appropriate security controls should also be applied to protect these assets from unauthorized access
4. If a data exfiltration attack is successful, security teams must detect and stop the exfiltration
  - To detect the attack, indicators of unusual data collection can be identified through network monitoring
  - SIEM tools can detect an alert on these activities

## Packets and packet captures

### Components of a packet

1. Header
  - Includes information like the type of network protocol and port being used
  - Also contains the packet's source and destination IP address
2. Payload
  - Contains the actual data that's being delivered
3. Footer
  - Signifies the end of the packet

## Packet sniffer (Network protocol analyer)

A tool designed to capture and analyze data traffic within a network

**P-Cap**, or a packet capture, is a file containing data packets intercepted from an interface or network
- P-cap files can come in many formats depending on the packet capture library that's used
  - Libpcap
    - Pcap designed to be used by Unix-like system, like Linux and MacOS
    - Tools like tcpdump use Libpcap as the default pcap file format
  - WinPcap
    - Open-source packet capture library designed for devices running Windows operating systems
    - Considered an older file format and isn't predominatly used
  - Npcap
    - A library designed by the port scanning tool `Nmap`
    - Commonly used in Windows operating system
  - PCAPng
    - A modern file format that can simultaneously capture packets and store data
    - Its ability to do both explains the "ng" (Next generation)

### Examples

- tcpdump
- Wireshark
- Tshark

### How Packet sniffers work

1. First, packets must be collected from the network via the Network Interface Card (NIC), which is hardware that connects computers to a network, like a router. NICs receive and transmit network traffic, but by default they only listen to network traffic that’s addressed to them
  - To capture all network traffic that is sent over the network, a NIC must be switched to a mode that has access to all visible network data packets (monitor mode)
2. The network protocol analyzer collects the network traffic in raw binary format
  - The network protocol analyzer takes the binary and converts it so that it’s displayed in a human-readable format, so analysts can easily read and understand the information

## IPv4 Header

![img](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Mi_kryGkRiyYUOJDIwnPCw_ac942d1eec284467a5ca533cb99c4bf1_S20G003.png?expiry=1700179200000&hmac=9QFx7Lsa53wv6WXym85cWw_XQD5bSb6Dh3UEkko3Rvg)

- Version
  - Sepcifies which version of IP is being used
    - IPv4 or IPv6
- IHL (Internet Header Length)
  - Specifies the length of the IP header plus any options
- ToS (Type of Service)
  - Specifies if certain packets should be treated with different service
- Total Length
  - Identifies the length of the entire packet
    - Including the headers and the data
- Identification, Flags, and Fragment offset
  - Deals with information related to fragmentation
    - *Fragmentation* is when an IP packet gets broken up into chuncks
      - Transmitted over the wire and reassmbled when they arrive at their destination
    - These three fields specify if fragmentation has been used and how to reassemble the broken packets in the correct order
- TTL (Time To Live)
  - Determines how long a packet can live before it gets dropped
- Protocol
  - Specifies the protocol used by providing a value which corresponds to a protocol
- Header Checksum
  - Stores a value called a checksum, which is used to determine if any errors have occured in the header
- Source Address
  - Specifies the source IP address
- Destination Address
  - Specifies the destination IP address
- Options
  - Not required and commonly used for network troubleshooting rather than common traffic

## IPv6 Header

![img](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/i8ZlXBWcQnKMc9AvaOlTrg_9ae604f634bc4ea3b0bced51911d32f1_XjvmdLkZuzfhKQ0zQ_4RnCZGNxP0FDCtB0i8iwWtu30GL05Ziixkcd3YNSK8ng5tiu3X3XVOypCPywtGP01diUAvVWEkjwGWk7E_4fpFZdntBgohToxkS5cNsyZtqKsRCmssQUmWlH8Xhn2oJKG55Kv0-CUjA8Kj3yhZXTWbjjV4pYcCH9EUwPWpyFnhCQ?expiry=1700179200000&hmac=hUtmMGRBKacqjd9hKHrhMkd9kpJrf1eVibedFd3gt7w)

- Version
  - This field indicates the IP version. For an IPv6 header, IPv6 is used
- Traffic Class
  - This field is similar to the IPv4 Type of Service field. The Traffic Class field provides information about the packet's priority or class to help with packet delivery
- Flow Label
  - This field identifies the packets of a flow. A flow is the sequence of packets sent from a specific source
- Paylead Length
  - This field specifies the length of the data portion of the packet
- Next Header
  - This field indicates the type of header that follows the IPv6 header such as TCP
- Hop Limit
  - This field is similar to the IPv4 Time to Live field. The Hop Limit limits how long a packet can travel in a network before being discarded
- Source Address
  - This field specifies the source address of the sender
- Destination Address
  - This field specifies the destination address of the receiver

## Overvie of tcpdump

`tcpdump` is a command-line network protocol analyzer that is used to capture network traffic

### Commands

`sudo tcpdump -i [interface] [option(s)] [expression(s)]`
- `-i` parameter specifies the network interface to capture network traffic
- `option` are optional and provide you with the ability to alter the excution of the command
- `expression` are a way to further filter network traffic packets so that you can isolate network traffic

#### Options

- `-w`
  - Write or save the sniffed network packets to a pcap file instead of just printing it out
  - `sudo tcpdump -i any -w filename.pcap`
- `-r`
  - Read a pcap file by specifying the file name as a parameter
  - `sudo tcpdump -r filename.pcap`
- `-v`
  - Verbose, print out more of a packet's information
  - There are three levels `-v`, `-vv`, `-vvv`
  - `sudo tcpdump -r filename.pcap -vv`
- `-c`
  - Count, lets you control how many packets tcpdump will capture
  - `sudo tcpdump -i any -c 10`
- `-n`
  - Disables automatic mapping of numbers to names
  - Considered to be best practice when sniffing/analyzing traffic
  - tcpdump perfom name resolution by default
    - tcpdump automatically converts IP addresses to names, resolve ports to commonly associated services that use these port
  - `sudo tcpdump -r filename.pcap -vv -n`

#### Expressions

Using filter expressions in tcpdump is also optional
- You can use filter expressions to isolate network packets
- You can also use boolean operators like and, or, or not to further filter network traffic for specific IP addresses, ports, and more
  - `sudo tcpdump -r packetcapture.pcap -n 'ip and port 80'`
- You can use single or double quotes to ensure that tcpdump executes all of the expressions
- You can also use parentheses to group and prioritize different expressions. Grouping expressions is helpful for complex or lengthy commands
  - `sudo tcpdump -r packetcapture.pcap -n 'ip and (port 80 or port 443)'`

![img](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/3LnHDkkeQ2-a-KjHKXkBCQ_940eb009d1674c7595f8361adf48c1f1_89by7cw_y0GWsyGI4iK19PqNyVHpVO4reyeIO0v-xYeZDBID0JG0PzpqRSA7fWjmD88HKjaZ8PhlONjdsKMLrUlx0lM9lPGBVSNqO87rZPPHt00BahLIQmfBNpRTyBAgjUklW2nn3hCB5Z-x_0HC56AKW7g2hk4tXgWyjInXVJYMosY9D4pyuX2VzerrhA?expiry=1700179200000&hmac=yHb28_deesx9yHAExnVcDwWE-MS59Bpfsa-nbKWyTPg)

1. Timestamp
   1. Starts with hours, minutes, seconds, and fractions of a seconds
2. Source IP
   1. The packet's origin
3. Source port
   1. Port number where the packet originated
4. Destination IP
   1. The IP address where the packet is being transmitted to
5. Destination port
   1. Port number where the packet is being transmitted to