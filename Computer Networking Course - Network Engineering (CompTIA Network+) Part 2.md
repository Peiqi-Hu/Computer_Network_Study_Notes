# Computer Networking Course - Network Engineering (CompTIA Network+) Part 2

## Network Topologies

### What is a topology?

- a "map" that can describe how a network is laid out or how the nw functions 

- can be described as either **logical or physical.** 
  
  - logical: theoretical signal path 
  
  - physical: physical layout of the nw

### Peer-to-peer vs. client/server

- These are (not) topologies.
  
  - they don't describe signal path or the physical layout of the nw
  
  - they describe how the nw functions

- **peer-to-peer topo**
  
  - nodes control & grant access to resources on the nw
  
  - <u>each node is responsible for the resources it is willing to share</u>

- **client/server topo**
  
  - nw resources access is <u>controlled by a central server(s)</u>
  
  - a server determines what resources get shared, who is allowed to use the resources and even when the resources can be used

- **hybrid topo**
  
  - combination of two

### Network topology models

- the <u>original ethernet standards established a "bus" topo for the nw, both logically & physically</u>
  
      - "bus" topo: end2end, from one direction to the other direction and come back 
  
  - development of different physical topo, <u>logical topo remained the same to maintain backward compatibility</u>. 
  
  - when discussing Ethernet nw: logical topo is always a "bus" topo while the physical topo can be different

- ![](C:\Users\hupei\AppData\Roaming\marktext\images\2022-02-13-20-53-20-image.png)

- ![](C:\Users\hupei\AppData\Roaming\marktext\images\2022-02-13-20-54-25-image.png)
  
  - Mesh:
    
    - <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-02-13-20-55-50-image.png" title="" alt="" width="294">

- <img title="" src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-02-13-20-56-36-image.png" alt="" width="661">

- ![](C:\Users\hupei\AppData\Roaming\marktext\images\2022-02-13-20-57-35-image.png)

- ring=bus with the ends connected

- star=nodes radiate out

- mesh=multipath

- p2p=direct connection

- p2multipoint=central control

## Network infrastructure implementations

### Design vs. function

- if describe the nw's <u>design</u>, then the first place to start is to describe its<u> topo</u>

- if describe the nw's <u>function</u>, then the first place to start is to describe its <u>category or infrastructure implementation</u> 

### Categories of networks

- **Local Area Network (LAN)**
  
  - most LANs are encompassed by single nw addr range
    
    - the addr range may be <u>broken into subgroups</u>
    
    - <u>each of these subgroups is called a **virtual LAN (VLAN)**</u>
  
  - LANs can span from a small area to a builging or a small group of buildings
  
  - tend to be high speed 
  
  - most common type of nw found in LAN: <u>802.3 (Ethernet) and 802.11 (wireless LAN) WLAN</u>

- **Metropolitan area network (MAN)**
  
  - larger than a LAN
  
  - contain <u>multiple LANs</u>
  
  - often owned by <u>municipalities</u>
  
  - it sometimes called a **campus area nw (CAM)** when is owned by a private entity

- **Wide area network (WAN)**
  
  - spans <u>significant geographic distances</u>
  
  - a nw of nws
  
  - best example is the<u> Internet</u>
  
  - if the all of the infrastructure implementation has a <u>single owner, then it is not a WAN</u>

- **Personal area network (PAN)**
  
  - extremely distance and size limited
    
    - often a connection between only 2 devices
  
  - common examples:
    
    - **<u>Bluetooth</u>**: ~ between a keyboard and computer
    
    - **<u>IR (infrared)</u>** connection between a smartphone and a printer 
    
    - **<u>NFC (near field comm)</u>** between a smartphone and a payment terminal
  
  - tend to provide low throughput of data and have a low power output
    
    - throughput decreases when the distance between devices increases 

- **Supervisory control and data acquisition (SCADA)**
  
  - ![](C:\Users\hupei\AppData\Roaming\marktext\images\2022-03-01-09-57-43-image.png)

- **Medianet**
  
  - nws designed and implemented specifically to handle voice and video
  
  - to remove QoS issues (e.g., latency and jitter) that can occur in other infrastructures 
    
    - e.g., video teleconference (VTC) nw 
  
  - may be implemented as its own infrastructure or as a sub-infrastructure 

## Introduction to IPv4

- IP addresses are the location of the PC or server, identified as both nw location and host location within that nw

### Purpose of IP addressing

- provides a logical addressing scheme for our computers so that they can communicate on nws. 
  
  - being logical means that an IP addr <u>can be changed within minimal fuss at any time</u>, unlike a MAC addr which is physically embedded into devices

### IPv4 address properties

- <u>32-bit binary number</u>, 2^32 possible addr combinations 

- to keep everything neat and tidy and findable: implementation of <u>subnet mask</u>
  
  - used to determine nw and node/host portions of the IP addr. 

- convert binary to decimal 

- initial properties of IPv4 
  
  - ![](C:\Users\hupei\AppData\Roaming\marktext\images\2022-03-01-10-18-47-image.png)
  
  - ![](C:\Users\hupei\AppData\Roaming\marktext\images\2022-03-01-10-20-52-image.png)

### Classes of IPv4 addresses

- run out of assignable IPv4 addr

- <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-03-01-10-24-22-image.png" title="" alt="" width="359">

- <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-03-01-10-25-05-image.png" title="" alt="" width="410">(APIPA)

- <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-03-01-10-29-00-image.png" title="" alt="" width="378">

### Classless of IPv4 addressing

- classes of addr limit flexibility 
  
  - first routing protocols requires the class structure

- classless addressing
  
  - **classless inter-domain routing (CIDR)**
  
  - slow the growth of routing tables
  
  - slow the exhaustion of IPv4 addr
  
  - create more flexbility
    
    - fluid subnet mask
  
  - not affect the private addr space ranges 
  
  - subnetting is possible and desirable

- CIDR notation
  
  - <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-03-01-10-32-03-image.png" title="" alt="" width="390">

### Subnetting IPv4 addresses

- <u>subnetting cuts the addr space into smaller pieces</u>
  
  - create flexibility in nw design
  
  - create efficiency in addr space utilization

- small office nw example 
  
  - <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-03-01-10-38-01-image.png" title="" alt="" width="428">

## Introduction to IPv6

- Internet Assigned Numbers Authority (IANA)

### IPv6 address structure

- works at L3 of the OSI model 
  
  - L3: major focus is logical nw and host addressing
  
  - IPv6 provide logical nw and host addresses to devices 

- 128-bit binary addressing scheme 
  
  - ![](C:\Users\hupei\AppData\Roaming\marktext\images\2022-03-01-10-41-55-image.png)

- **IPv6 local addr structure**
  
  - the <u>first 64 bits represent the local nw</u>, the <u>last 64 bits represent the host </u>
    
    - the local addr structure follows the Extended Unique Identifier (EUI) format <u>EUI-64</u>. The 48-bit MAC addr is padded with 16 bits to make it 64 bits in length
  
  - the local addr is called the **** link local addr****, and always begins with **fe80**

- **IPv6 global addr structure**
  
  - last 64 bits is host addr
  
  - nw portion is composed of the routing prefix and subnet 
    
    - follows CIDR convention 
    
    - the subnet is composed of the bits between the prefix and the EUI-64 host addr
  
  - global IPv6 addr always begin in the range of 2000 to 3999.

- the <u>need for DHCP has been eliminated</u> in most cases
  
  - when implemented, IPv6 will auto-configure both the local and global addr. When a device first comes online, it will us **neighbor discover protocol (NDP)** to discover what the required nw addr are, both local and global. <u>This allows the device to configure its own IPv6 addr. </u>

- IPv6 notation 
  
  - ![](C:\Users\hupei\AppData\Roaming\marktext\images\2022-03-01-15-22-54-image.png)

### IPv6 nw transmissions

- **unicast**: 1-to-1 communication
  
  - can occur on the local nw (<u>fe80</u>) or the global nw (2000 to 3999)

- **multicast**: 1-to-few comm
  
  - routers register to receive multicast transimissions that involve the routing protocols they are programmed to use 
    
    - multicast addr always begin with an **ff**
    
    - ![](C:\Users\hupei\AppData\Roaming\marktext\images\2022-03-01-15-27-01-image.png)

- **anycast**: <u>1-to-the-closest </u>
  
  - the router only sends the comm to the closest one
  
  - involves implementing DHCPv6

- **DHCPv6**
  
  - **IPv6 is capable of auto-configuring its own local and global addr**
    
    - in certain situations, that is not always desirable
  
  - <u>DHCPv6 can be configured to hand out specific IPv6 addr</u> when necessary
  
  - useful for when <u>load balancing a nw, or for when nw redundancy has been created</u>

- IPv6 and IPv4
  
  - **dual stack configuration**
    
    - the nw and devices on the nw receive both an IPv6 and IPv4 configuration
  
  - **tunneling**
    
    - **6-to-4**: used to encapsulate v6 data packets in and v4 datagram, allowing v6 packets to travel across or through all v4 nws
      
      - also called **Teredo tunneling**

## Special IP networking concepts

### The media access control address (MAC)

- ****MAC addr: all nwing interfaces come with a special addr already configured ****
  
  - often referred to as the ** **physical addr**** or the burned in addr of the interface. It is set by the manufacturer and never changes.
  
  - switches and other open systems interconnection (OSI) **L2** devices rely upon the MAC addr in order to get nw packets to the correct destinations. 

- MAC addr format
  
  - ![](C:\Users\hupei\AppData\Roaming\marktext\images\2022-03-01-15-36-29-image.png)
  
  - ![](https://upload.wikimedia.org/wikipedia/commons/thumb/9/94/MAC-48_Address.svg/330px-MAC-48_Address.svg.png)(from wiki)
  
  - ![](C:\Users\hupei\AppData\Roaming\marktext\images\2022-03-01-15-39-27-image.png)

### Collision domains vs. broadcast doamins

- **Ethernet nws** use a tech called **Carrier Sense Multiple Access with Collision Detection (CSMA/CD)** when transmitting data. 
  
  - with this, a device listens to the carrier signal on the nw media. If no other device is transmitting, the device is free to send data. If another device sends data, a collision is posiible. <u>The devices listen for collisions, and will stop transmitting and wait a random period of time before attempting to transmit again.</u> 

- **Collision domains**
  
  - an area of the nw where nw packets can collide.
    
    - a collision can occur when 2 devices send packets at the same time
    
    - <u>collision domains are broken up by switches, bridges, and routers</u>
    
    - are <u>not broken up by hubs</u>

- **broadcast domains**
  
  - defined as <u>all the nodes that can be reached by a broadcast transmission </u>
    
    - all nodes that can be reached reside in the same nw
  
  - the domain <u>cannot pass routers</u>, so the domain is <u>also defined by the subnet mask </u>

- special notes
  
  - technically, v6 does not use broadcast transmissions 
    
    - *<u>v6 utilizeds multicast instead of broadcast transmissions </u>*

### Types of nw transmissions

- types of IPv4 nw transmissions
  
  - unicast: 1-to-1
  
  - muticast: 1-to-few (a specific src addr transmissions going to a set of registered dest addr)
  
  - **broadcast**: 1-to-all (to all addr on the local nws)

- types of IPv6 nw transmissions
  
  - unicast
  
  - multicast
  
  - **anycast**: 1-to-closest
    
    - going to a specific v6 addr that has been assigned to multiple devices. The router uses an algo to determine which MAC addr is the closest and only that device receives the anycast trans. 
    
    - <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-03-01-15-53-02-image.png" title="" alt="" width="363">
      
      

## Introduction to routing concepts

### Purpose of routing

- purpose: to connect different nws together to allow them to communicate and pass data traffic. 

- routing protocols are how nws determine where to send nw traffic. They build routing tables to direct nw traffic. 

### Basic routing concepts

- **Static routing**
  
  - uses <u>administrator defined routes </u>
  
  - each router must contain the route
  
  - easy to set up (in a small nw)
    
    - not easy to maintain

- **Dynamic routing**
  
  - <u>routers use protocols in order to determine the best route between 2 nws</u>
  
  - admin determines which protocols will be in use
  
  - the routers must all use the same protocols
    
    - exception: route redistribution 
  
  - <u>routing protocols can be stacked within a router</u>

- **the default route**
  
  - the direction that a router will send nw traffic <u>when there is no known route in the routing table</u>
    
    - <u>assigned by an admin</u>
    
    - usually a designated interface on the router or designated next hop interface

- **the routing table**
  
  - <u>list of known routes to all known nw from the router's perspective </u>
    
    - is established by an admin when static routing is used
    
    - dynamically built by routing protocols when dynamic routing is used
  
  - <u>each routing protocol maintains a routing table </u> 

- **Loopback interface**
  
  - an administratively configured logical number assigned to a router to ease administrative functions or routing processes
    
    - often, the loopback interface is assigned in an IPv4 addr format
  
  - the interface may be completely logical, or a physical interface may be assigned to be the loopback interface. 

- **Routing loops** 
  
  - a possible problem that can be created if interconnected routers have a breakdown in their routing algo
    
    - when a routing loop occurs, the nw<u> keeps looping through the routers </u>until some system or mechanism breaks the cycle.
    
    - they can create<u> nw congestion </u>or even bring down a nw
  
  - routing protocols use multiple methods to prevent loops from occuring
    
    - the time to live (**TTL**) field is also utilized to stop routing loops after they have occured.



### Routing metrics

- There may be more than one route available to a remote nw. **Routing protocols use metrics to determine which route is the best to use**. 

- the same basic metric may be used by different routing protocols. When this occurs, the metric is usually implemented in a different manner through the use of different algo. 

- metrics
  
  - **Hop count**
    
    - the<u> number of routers</u> between two end points
  
  - **Maximum transmission unit (MTU)**
    
    - the <u>max allowed size of a packet</u>, measured in <u>bytes</u>
    
    - packets excced the MTU must be fragmented into small pieces, leading to more packets, and slower connection
  
  - **Bandwidth**
    
    - the <u>speed of the nw connection</u> (in Kbps, Mbps, or Gbps)
  
  - **Latency**
    
    - <u>measure of time </u>that a packet takes to traverse a link
  
  - **Administrative distance (AD)**
    
    - the <u>believability of a routing protocol's advertised routes</u>
      
      - different routing protocols are considered to be more trustworthy than others
    
    - <u>routers use the AD to help determine which routing protocol to use</u> when more than one protocol is installed on the router
    
    - the **lowest AD** of an advertised route will determine the protocol use
      
      - <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-03-02-08-58-57-image.png" title="" alt="" width="362">

### Route aggregation

- It is a process used by nw admin to **condense the size of routing tables**. They do so through the <u>use of **CIDR** to summarize routes to different nws</u>. 

- <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-03-02-09-03-00-image.png" title="" alt="" width="447">

- <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-03-02-09-03-21-image.png" title="" alt="" width="442">

- route aggregation takes careful planning during the nw design phases
  
  - the above example would not work if interface S/1/1 on the same router was connected to nw 10.1.2.0 (non-contiguous nws)
  
  - <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-03-02-09-05-45-image.png" title="" alt="" width="438">

### High availability

- Part of a nw admin's job is to ensure that nws reamin up and active for the max amount of time.

- to ensure nw don't go down, admins oftern **remove single points of failure**

- **single point of a failure** in a nw is the point where<u> a single failure will casue the nw to cease functioning</u>. nw admin oftern use <u>high availability tench</u> to remove them. An example of a high availability tech is the <u>use of redundant links to outside nws</u>. 

- **Hot Standby Router Protocol (HSRP)**
  
  - a proprietary cisco method of<u> creating a **fault tolerant link** using 2 or more routers with connections **outside of the local subnet**</u>. 
    
    - the 2 routers are connected together as well as having connections outside of the local nw
    
    - a **virtual IP addr** is created and shared between the routers
    
    - devices on the nw are configured to use the virtual IP addr as the <u>default gateway</u> for pakcets leaving the nw.
    
    - if a router goes down, the link outside the nw is still available

- **Virtual Router Redundancy Protocol (VRRP)**
  
  - is an **IETF (Internet Engineering Task Force) standard** that is similar in operation to HSRP.



## Introduction to routing protocols

## Interior vs. exterior gateway routing protocols

- **Interior gateway protocol (IGP)**
  
  - a category of protocols used within **autonomous nws**.
    
    - used between nws that you can control 
  
  - the most popular IGP protocols are **OSPF** (Open Shortest Path First) and **RIPv2** (Routing Information Protocol version 2)
  
  - Note: **IS-IS** is popular with<u> extrememly large autonomous nws</u> like an **ISP**'s (internet service provider) nw. 

- **Exterior gateway protocol (EGP)**
  
  - used between **non-autonomous nws**
    
    - used between nws under separate control
  
  - **BGP** (Border Gateway Protocol) is the most popular 

- Autonomous nws: organizations have more than one nw that are routing traffic between 
  
  - some IGP routing protocols use an admin defined **autonomous system (AS) number** as one means of identifying which nws can directly communicate with each other. 
  
  - <u>AS is not a metric</u>, but a means of <u>identifying a nw that might possible accept another nw's traffic</u>. 
  
  - AS is<u> only significant within autonomous nws</u> and has no relevance outside of them. 
  
  - <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-03-02-09-38-54-image.png" title="" alt="" width="295">

### More routing concepts

- Classification of routing protocols 
  
  - <u>IGP and EGP routing protocols can be broken out into 3 other catergories of protocols</u>, which is designated by their main method of determing routes between nws.
  
  - **Distance-vector** routing protocols
    
    - routes are determined by <u>how many routers</u> exist between the src and dst. 
    
    - Periodically, the <u>whole routing table is broadcasted</u>
  
  - **Link State** routing protocols
    
    - <u>metrics are used</u> to determine the best possible route between dsts. The protocol then <u>only monitors the state of directly connected links</u> and only makes changes when changes to links occurs. 
    
    - only<u> changes in link status are broadcasted</u>.
  
  - **Hybrid** routing protocols
    
    - use aspects of both the distance vector and link state routing protocols. 

- **Next hop**
  
  - next router in the path between 2 points 

- **Routing table** 
  
  - the database table that is used by a router to determine the best possible route between 2 points

- **Convergence (steady state)**
  
  - the amount of <u>time that is takes all the routers in an AS to learn all the possible routes within that sys</u>.
    
    - faster convergence times are desirable. 

### Routing protocols

- **Routing Information Protocol v2 (RIPv2)**
  
  - <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-03-02-09-48-13-image.png" title="" alt="" width="452">

- **Open Shortest Path First (OSPF)**
  
  - <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-03-02-09-49-09-image.png" title="" alt="" width="456">

- **Intermediate System-to-Intermediate System (IS-IS)**
  
  - <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-03-02-09-51-29-image.png" title="" alt="" width="440">

- **Border Gateway Protocol (BGP)**
  
  - <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-03-02-09-52-17-image.png" title="" alt="" width="441">

- **Enhanced Interior Gateway Routing Protocol (EIGRP)**
  
  - an advanced **distance-vector (hybrid) IGP** routing protocol developed by Cisco.
  
  - <u>fast convergence</u> time
  
  - uses a **Neighbor Table (directly connected routers)** and a **Topology Table** to <u>build its routing table</u>. The protocol <u>only announced changes to the routing table</u> (on multicast addr 224.0.0.10) in order to reduce bw consumption. 



## Basic elements of unified communications

### Unified communications (UC)

- UC is not encompassed by a single product or device. It is a growing category in enterprise nws. 
  
  - is the <u>set of products and services that attempts to provide a consistent single user interface and experience across different media types and devices</u>. 
  
  - allows a user to <u>send a msg from one type of media and have that media received as a different type of media</u>. 

- **Unified communications devices**
  
  - **UC server**
    
    - specialized servers that are designed to <u>implement UC solns</u> in the workplace
  
  - **UC gateways**
    
    - a nw device that is designed to <u>translate between different signaling methods</u>(e.g., **VoIP**). Gateway will translate an analog PSTN voice signal into a signal that can be understood on the VoIP nw.
  
  - **other UC devices**
    
    - any devices that can be used in the implementation of a UC soln, may include VoIP phones, email sys, video conferencing, and instant messaging nws.

### Unified communications concepts

- **Presence**
  
  - an <u>indicator used to communicate the willingness or ability of a user to accept communication</u>
    
    - common presence statuses include available, online, offline, busy and do not disturb
  
  - presence services are important in UC solns, as they will<u> track individual users across multiple devices and nws in real time through the use of multicast transmissions</u>.
    
    - once a comm session has been established, <u>unicast nw transmissions</u> are used.

- **Quality of service (QoS)**
  
  - are implemented to<u> improve the UC by managing nw traffic</u>
  
  - **class of service (CoS)**: a QoS tech used to manage nw traffic by <u>grouping similar types of traffic and assigning a nw priority to that traffic</u>. A 6-bit **differentiated services code point (DSCP)** is used in the <u>IP header</u> to establish the CoS.

### Voice over IP

- one of the most common implementations in a UC soln. Through the use of a <u>presence service</u>, calls can be routed to the correct location. 

- 2 important protocols used in VoIP are **Session Initiation Protocol (SIP)** and **Real-time Transport Protocol (RTP)**
  
  - **SIP**: has 2 purposes
    
    - is used to <u>established a communication session</u> between two end points. 
    
    - once session is completed, <u>SIP tears down the connection</u>.
  
  - **RTP**: is used during the communication session <u>as the transport protocol, helping to provide QoS to the end points</u>. 





## Virtualization technologies

### Hypervisors and Virtual Machine Managers

- hypervisor can refer to any of the software that is used to <u>manage virtual machines</u>. 
  
  - does <u>not need a host OS</u>

- **VM managers (VMM)** <u>requires a host OS</u> such as Windows or Linux

### Components of virtualization

- **Virtual desktops**
  
  - a VM that functions as a desktop
    
    - any modern OS can be run inside of the VM desktop
    
    - multiple virtual desktops may be hosted on, or from, a single host systems

- **Virtual servers**
  
  - a VM that functions as a server
    
    - any modern server OS can be used

- **Virtual switches, firewalls, and routers**
  
  - a VM that fulfills the functions of a switch, firewall or router
  
  - <u>VF and VR are particularly effective when combined with virtual nw interface controllers (**NICs**) and VS to create virtual nws</u>.

- It is important to consider <u>how the virtual nw is going to pass traffic to remote nws</u>. 
  
  - A connection must be created <u>between the host sys's physical NIC and the virtual nwing equipment</u> to allow nw traffic to pass through (if there is a desire for nw traffic to pass beyond the host sys)

### Software defined networking (SDN)

- **SDN** is the <u>process of allowing the administration and configuration of a nw to be done dynamically</u>
  
  - the administrator can use a front end program to make adjustments to the nw with SDN.
  
  - it allow nw administrators to dynamically adjust nw performance without the need to log into each individual device that needs to be adjusted to achieve the desired performance



## Storage area networks

### Justifications for storage area networks

- dramatic decrease in the actual cost of data storage is one of factors leading to icnreased demand for data storage

- another factor is: the demand for the data to be available from anywhere and accessible from any device increased

- A **storage area nw (SAN)** can be a soln to the need for both <u>storage capacity and high availability</u>. 
  
  - advantages of SAN
    
    - **scalability**: the amount of data generated is huge and need to be stored.
      
      - as storage needs increase, the capa of the SAN can be easily increased to meet them.
    
    - **data availability**: demand increased for data to be available at anytime from anywhere.
      
      - <u>SAN are deployed as part of a cloud computing soln</u>, thus increasing availability
    
    - **optimization**: the serviers can be optimized to run applications more efficiently as the requirements to store data are removed from application servers.
      
      - data storage is also optimized

### SAN technology

- **Storage area nw (SAN**): an **acutal nw of devices** that have the sole purpose of storing data efficiently. 
  
  - a SAN may contain multiple NAS devices.

- **nw attached storage (NAS)**: is a specifically designed nw appliance that has been configured to store data more efficiently than standard storage methods. 
  
  - is a **data storage appliance that is placed on a nw**. 

- **Fibre channel (FC)**
  
  - a high speed nw tech originally developed to operate over fiber optic cables only.
    
    - now have been modified to <u>allow the use of copper cabling in conjuction with the fiber</u>
  
  - **commonly used to connect SANs**
    
    - use **fibre channel protocol (FCP)** as its <u>transport protocol to transmit **SCSI (small computer sys interface**) commands to storage devices.</u>

- **Internet SCSI (iSCSI)**
  
  - an <u>IP based nwing standard used to connect data storage facilities and SANs</u>.
    
    - allows SCSI commands and processes to take place <u>over long distances</u>.

- **Jumbo frames**
  
  - allows for <u>greater throughput of data</u> by allowing up to 9k bytes of data in a single frame
    
    - can<u> increase the efficiency of the SAN</u>



## Basic cloud concepts

### Cloud classifications

- cloud computing: virtual resources, provided by a service provider. It is highly configurable and changeable. 

- classifications
  
  - **public cloud**
    
    - sys interace with services and devices within the publich cloud and on public nw (e.g., the Internet)
  
  - **private cloud**
    
    - sys only communicate with services and devices within the specified private cloud
  
  - **hybrid cloud**
    
    - public + private
  
  - **community cloud**
    
    - cloud services used by private individuals, organizations or groups that have a common interest

### Types of cloud computing

- **Software as a service (SaaS)**
  
  - the end user purchases the rights to<u> use an application</u> without the need to configure the virtual servers that will deliver the application
    
    - usually delivered as a web application (within a web browser)

- **Platform as a service (PaaS)**
  
  - the user is provided with a <u>development platform for the creation of software packages</u>, without the need to configure the virtual servers and infrastructure that delivers it

- **Infrastructure as a service (IaaS)**
  
  - the end user is provided with <u>access to virtual servers (**configurable** by the customer) and other virtual nw resources</u>
    
    - highly configurable env
    
    - the end user supplies the software that is going to be used on the IaaS nw 



## Implementing a basic network

### Plan the network

### Configure the network
