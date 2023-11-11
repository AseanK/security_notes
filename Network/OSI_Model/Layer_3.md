# Layer 3 - Network

Responsible for **packet** forwarding including routing through intermediate routers\
it also manages quality of service (QoS), and recognizes and forwards local host domain messages to the Transport layer (layer 4)\
*Routers* are used in layer 3

## IP Address

Logical addressing scheme which implemented at Layer 3
- Network designers use IP addressing to partition the overall network into smaller subnets to improve performace, security, and trouble shooting

### 3 Main IP Traffic Types

- **Unicast**
  - A communication where a message is sent from one sender to one receiver
  - Uses a unique destination address
  - Generates the least amount of network traffic
  - More secure because data is sent to a specific recipient
  - E.g. Email, File transfer
- **Broadcast**
  - A communication where a message is sent from one sender to all receivers
  - Uses a special broadcast address
  - Generates the most amount of network traffic
  - Less secure because data is sent to all devices in the network
  - E.g. DHCP requests, ARP requests
- **Multicast**
  - A communication where a message is sent from one sender to a group of receivers
  - Uses a special multicast address
  - Generates moderate network traffic
  - Moderately secure because data is sent to a specific group of devices
  - E.g. Video streaming, online gaming

### IPv4

IPv4 addresses still routes most of today's internet traffic
- 32-bits long
- 4 octets in dotted decimal format
- Each octet is 8-bits long

![img](https://bluecatnetworks.com/wp-content/uploads/2020/05/ipv4-1.png)

- 32-bits address space limits the number of unique hosts to 232 ~ 4,294,967,296 addresses which is not enough

#### IPv4 Classes

- **Class A**
  - For networks with large number of total hosts
  - Public IP Range: 1.0.0.0 to 127.0.0.0
  - Private IP Range: 10.0.0.0 to 10.255.255.255
  - Subnet Mask: 255.0.0.0 (/8)
  - 126 Networks / 16,777,214 Hosts per Network
- **Class B**
  - For medium to large sized networks
  - Public IP Range: 128.0.0.0 to 191.255.0.0
  - Private IP Range: 172.16.0.0 to 172.31.255.255
  - Subnet Mask: 255.255.0.0 (/16)
  - 16,382 Networks / 65,534 Hosts per Network
- **Class C**
  - For small LANs (Local Area Network)
  - Public IP Range: 192.0.0.0 to 223.255.255.0
  - Private IP Range: 192.168.0.0 to 192.168.255.255
  - Loop-back Range: 127.0.0.1 to 127.255.255.255
  - Subnet Mask: 255.255.255.0 (/24)
  - 2,097,150 Networks / 254 Hosts per Network
- **Class D**
  - Multicasting
  - Range: 224.0.0.0 to 239.255.255.255
- **Class E**
  - Reserved/Research/Experimental
  - Range: 240.0.0.0 to 255.255.255.255

#### Subnet Mask

identify the range of IP addresses that make up a subnet, or group of IP addresses on the same network
- 32-bits long that can be written in dotted decimal or slash notation
- Defines boundary of network portion and host portion of the IP address
- 1 indicates network and 0 indicates host


255 in binary:
|  128  |  64   |  32   |  16   |   8   |   4   |   2   |   1   |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   |   1   |   1   |   1   |   1   |   1   |   1   |   1   |

255.255.255.0 subnet in binary:
|   255    |   255    |   255    |    0     |
| :------: | :------: | :------: | :------: |
| 11111111 | 11111111 | 11111111 | 00000000 |
