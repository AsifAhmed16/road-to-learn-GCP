# Road to Learn GCP

My process to learn GCP from zero experience.

### Learning Outcomes
- Cloud Application Components and Project Deployment


## Networking
- Basic Networking
- Cloud Networking (GCP)
  - VM
  - Physical Machine
  - Container
- Docker Networking


### OSI Model layer:
- Layer 1 - Application Layer
- Layer 2 - Presentation Layer
- Layer 3 - Session Layer
- Layer 4 - Transport Layer
- Layer 5 - Networking Layer
- Layer 6 - Data Transfer Layer
- Layer 7 - Physical Layer


### VM
- User Space (Allows UDP protocol to access user ends network)
- Kernel Space
  - It has a NIC(Network Interface Controller) Card that allows to enter data packets. It passes the data to Network layer.
  

## IP Address
- Consist of 4 blocks(8 bits/block)
- It has two parts 
  - Host part
  - Network Part
- Natting allows to communicate between two network through IP Address.
  - Public and Private IP can be distinguished for subnetting using CIDR(Classless Inter Domain Routing). Example: 10.10.0.0/16 is a CIDR Notation.
  

## DHCP(Dynamic Host Control Protocol)
- Difference between an Hub and Switch is - Hub has no DHCP but Switch has DHCP.
- It maintains a Table(with Mac-Address and IP-Address)
- ARP(Address Relational protocol) request is generated to DHCP server from NIC Card.


## BGP
- Two Types
  - IBGP (Internal with same AS Number connectivity)
  - EBGP (External with same AS Number connectivity)
- AS Number - Autonomous System Number


## TCP Connection
- IP address often changes over AS(Autonomous System) connections and its called SNAT(SourceNatting)
- Natting(Network Address Translation).
- SNAT is also responsible converting a private IP to public IP (private IP are generally changed by ISP provided public IP)
- Requires several informations. Like - 
  - SIP (Source IP)
  - DIP (Destination IP)
  - SP (Source Port)
  - DP (Destination Port)
  - MAC address
- 3 way handshaking architecture is followed.
- A connection is established for 10 seconds to transfer data with HTTPS request and it is called web transactions.


## Transport layer
- Communication between two processes inside a machine needs - IPC(Inter Process Communication)
- Communication between two different network with data like - (SIP, DIP, SP, DP, , MAC Address, Payload) needs to enable transport layer.
- Port is bind with process running inside a VM.
- Transport layer helps to bind process and port.


## DNS Query
- DNS query response is cached for saving bandwidth
- from terminal $dig or $mslookup


## NAT Gateway - Cloud NAT
- It provide a public IP so that a connection between two network is established.


## DNAT - Destination Nat
- It does natting between the destination private Ip and destination public IP of the ISP/Cloud Center Environment.


## Contrack
- Keeps track of IP address if it has been provided for uniqueness and to return response.


## Web Socket
- Spontenious connection between client and server
- Sends data through an HTTP call over a single TCP/IP connection in bidirection or half-duplex communication.


## HTTP
- Sends a request over TCP using a format
- While the request is encrypted it becomes HTTPS
- 


## Physical Machine/Virtual Machine/Container
- OS (Ubuntu)
- KVM,  it helps slicing a computer(ram, core etc) into multiple part and let us use it as a VM.
- VM consist of OS
- Container is a special case with no OS install inside it.(only os file structure)
 


## Allocating a VM based on request
- Algorithms used : Bin Packing / 0-1 Knapsack
- NFV(Network Function Virtualization) allows us to create a virtual network on the host machine
- Subnet masking (like switch) is integrated


## VPC (Virtual Private Network)
- VPC may contain multiple VM.
- VM inside VPC are connected through Subnet to the ultimate gateway or router.
- VM are 2 types :
    - Infrastructure Vertualization
    - Network Vertualization
- VPC networks allows to set a gateway, which will allow us to throw our packet.
- Next thing is to launch a VM. To launch, we need to go to - Compute Engine >> VM Instance
- VM has private(VM NIC Card has private IP) and public(Gateway has public IP) IP
- Internal IP range will realy on defined Gateway IP Range.
- Ingrace/Egrace
- IAP (Identity Aware Proxy)




































