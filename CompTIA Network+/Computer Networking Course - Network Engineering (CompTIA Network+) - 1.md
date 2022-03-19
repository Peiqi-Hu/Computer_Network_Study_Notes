# Computer Networking Course - Network Engineering (CompTIA Network+) Part 1

## Devices

### Layer 1 Devices

- OSI reference model 

- **modem**: take a digital signal and convert to a analog signal and place it on wire. vice versa.

- Hub: not common any more. take the electrical signal arrived and replicate it out all of the other ports.

### Layer 2 Devices

- **Switch**: utilize an ASIC chip to learn when a device is on the network and which ports it is connected to via the device's MAC address.
  
  - only communicate with the local network devices

- **WAP (wireless access point)**: a specific type of network bridge that connects/bridges wireless network segments with wired network segments. 
  
  - most common type: bridge 802.11 wireless network segments with 802.3 ethernet network segments.
  
  - only local network devices

### Layer 3 Devices

- **MLS (multilayer switch)**: provide L2 nw switching services, as well as L3 or higher OSI model services 
  
  - most common is L3 switch: not only switching, but also programed to handle routing functions. (not limit to local network device)
  
  - expensive, not found in home and office, but interprise local area network

- **Router**: <u>most common nw device for connecting different nw </u>
  
  - use software programming for <u>decision making</u>, keep track of diiferent networks and<u> find best route</u>
  
  - can communicate with local and non-local nw devices

### Security Devices

- **Firewall**: <u>placed on routers or hosts (sw) or be its own device</u>
  
  - functions at multilayers: L2,3,4,7
  
  - block packets from entering or leaving the nw
    
    - via <u>stateless inspection</u>: examine every packet against a set of rules
    
    - via <u>stateful inspection</u>: only examine the state of the connection between networks
  
  - first line of defense in protecting the internal nw from outside threats

- **IDS (Intrusion detection system)**: <u>passive sys designed to identify when a nw breach or attack against the nw is occuring</u>
  
  - *cannot* prevent or stop nw breach or attach on its own
  
  - receives a copy of all traffic and evaluates it against a set of standards
    
    - signature based: evaluate nw traffic for known malware or attack signature
    
    - anomaly based: suspicious changes
    
    - policy based: specific declared security policy
  
  - may deploy at host level (HIDS)

- **IPS (Intrusion prevention system)**: <u>active sys designed to stop a breach or attack</u>
  
  - designed to perform an action or set of actions to stop malicious activity
  
  - all traffic on the nw segment flows through the IPS to either enter or leave the segment
    
    - all traffic is evaluated against a set of standards (like IDS)
  
  - best to be placed <u>between a router (with a firewall) and the destination nw segment</u>
  
  - programmed to make active response to situations like:
    
    - block offending IP address
    
    - close down the vulnerable interface
    
    - terminate the nw session
    
    - redirect the attack
    
    - etc.

- **VPN (virtual private network) concentrator**: allow many more secure VPN connections to a network
  
  - provide proper <u>tunneling and encryption</u>
  
  - can function at multiple layers, but most func at L3, providing IPsec encryption through a secure tunnel
    
    - SSL VPN at L7

### Optimization and Performance Devices

- **Load balancer**: content switch or content filter
  
  - used to load balance between multiple hosts that contain the same data to spread out the workload for greater efficiency
  
  - used to <u>distribute the requests to a server farm among the various servers</u>, to help not to overloaded

- **Proxy server**: requests resources on behalf of client machines 
  
  - used to <u>retrieve resources from outside untrusted nw </u>
  
  - hide and protect the requesting client
  
  - can be utilized to <u>filer allowed content</u>
  
  - can <u>increase nw performance by caching commonly requested web pages</u>

## Networking Services and Applications

### The basics of the VPN

- VPN is <u>used by remote hosts to access a private network through an encrypted tunnel through a public network.</u>

- VPN types
  
  - the site-to-site
  
  - remote-access (host-to-site): allows select remote users to connect to the local nw; making connection uses VPN client software
  
  - host-to-host (SSL VPN): secure connection between 2 sys without VPN client software

### Protocols used by the VPN

- **IPSec (Internet protocol security)**
  
  - L3
  
  - to secure a VPN connection
  
  - <u>transmit unicast packets </u>(1-to-1)
  
  - can be used with AH protocol
    
    - *AH*: only autentication, no encryption
  
  - can be used with ESP 
    
    - **ESP**: both authenticate and encrypt packets
  
  - both AH and ESP operate in one of two modes:
    
    - transport mode: between 2 devices (host-to-host)
    
    - tunnel mode: between 2 endpoints (site-to-site)
  
  - IPSec implements internet security association and key management (ISAKMP) by default

- **GRE (Generic routing encapsulation)**
  
  - tunneling protocol that is able to encapsulate a wide variety of nw layer protocols
  
  - used to create a sub-tunnel with an IPSec connection
    
    - <u>multicast or broadcast</u>

- PPTP (point-to-point tunneling protocol)
  
  - older VPN tech that supports dial-up VPN

- **TLS (Transport layer security)**
  
  - cryptographic protocol used to create a secure encrypted connection between 2 end devices or application 
  
  - largely replaced SSL
  
  - works at L5 and above
  
  - common use: create a secure encrypted internet session (SSL VPN)

- ***SSL (secure socket layer)***
  
  - older cryptographic protocol tha is similar to TLS
  
  - most common use: internet transactions

### Network Access Services

- **NIC (Network interface controller)**
  
  - also called nw interface card
  
  - is <u>how a device connects to a nw</u>
  
  - works at:
    
    - L2: provide functional means of nw comm by determing which nw protocols will be used
      
      - provide local nw node address through its physical MAC addr
    
    - L1: determine how the nw data traffic will be converted into electrical signal
  
  - modern computers come with at least one built in ethernet NIC

- **RADIUS (Remote authentication dial in user service)**
  
  - <u>remote access service that is used to authenticate remote users and grant them access to authorized nw resources</u>.
  
  - it is a popular <u>AAA (authentication, authorization, accounting) protocol</u>
    
    - used to help ensure that only authenticated end users are using the nw resources they are authorized to use
  
  - <u>only the end user's password is encrypted</u>

- **TACACS+ (Terminal access controller access-control system plus)**
  
  - similar to RADIUS, but accounting features are not as robust as RADIUS, <u>and all transmissions between devices are encrypted</u>

### Other Services and Applications

- **RAS (Remote access services)**
  
  - not a protocol, but a roadmap
  
  - description of the combination of software and hardware required for a remote access connection.

- Web services 
  
  - creating a means of cross communication between sw packages or disparate platforms by translating communication into an XML format.

- Unified voice servie
  
  - create better voice communication systems 

## DHCP in the network

- **DHCP (Dynamic host configuration protocol)**: <u>give the PC an IP address, tell the PC the default gateway and how to find a DNS server</u> 

### Static vs. dynamic IP addressing

- computer receive the IP configuration in one of 2 ways:
  
  - statically: assigned manually, work for small and stable nw but not when nw grows                                                        
  
  - dynamically (through service like DHCP)
    
    - administrator configure a DHCP server to handle the assigning process --- automate the process 

### How DHCP works

- typical DHCP process
  
  - ![](C:\Users\hupei\AppData\Roaming\marktext\images\2022-02-02-22-42-51-image.png)

### Components and processes of DHCP

- ![](C:\Users\hupei\AppData\Roaming\marktext\images\2022-02-02-22-45-16-image.png)

- Processes:
  
  - ![](C:\Users\hupei\AppData\Roaming\marktext\images\2022-02-02-22-46-21-image.png)

- **Broadcast transmissions cannot pass through a router**. The <u>router can be configured to be a DHCP relay if no DHCP server on the local nw segment</u>. When the DHCP realy receives a discovery packet from a node, it will <u>forward the packet to the nw segment on which the DHCP server resides</u>. And so fewer configured DHCP servers are needed (reducing maintenance). 

## Introduction to the DNS service

### DNS servers

- **DNS (Domain name system)**: <u>map human friendly names to IP addresses. </u>
  
  - hierarchical 
  
  - from right to left (read back-forward)

- Different levels of DNS servers
  
  - **local DNS server**: the server on the local nw that contains the HOSTS file that maps the FQDN to IP addresses in the local subdomain
  
  - **top level domain (TLD) server**: the server contains the records for a top level domain (.com, .orgn, .net, .edu, etc)
  
  - **root server**: contains the records for the TLD servers 
  
  - ![](C:\Users\hupei\AppData\Roaming\marktext\images\2022-02-07-18-44-52-image.png)
  
  - **authoritative server**: responds to a request that has been specifically configured to contain the info. An authoritative response comes from the DNS server that actually holds the original record.
  
  - **non-authoritative**: responds to a request with DNS info that it <u>received from another DNS server</u>. 

### DNS records

- A record: maps hostnames to IPv4 addr.

- AAAA record: ~ to IPv6 addr.

- CNAME record: map canonical names to hostnames

- PTR record: pointer record that points to a canoncial name

- MX record: maps to the email server that is specified for a specific domain. It determines how email travels from sender to recipient. 

### Dynamic DNS  (DDNS)

- permits lightweight and immediate updates to a local DNS databse. It is useful when the <u>FQDN remains the same, but the IP addresses is able to change on a regular basis</u>. 

- DDNS updating
  
  - method of updating traditional name servers without the intervention of an administrator (no manual editing is required)

## Introduce nw address translation (NAT)

### The purpose of nw addr. translation

- Solve the problem of how to route non-routable IP addresses. 
  
  - private IPv4 address spaces are non-routable across public IPv4 nw, a router with NAT enabled will <u>translate a private IP addr into a routable public IP addr</u>. 

### How it works?

- 2 categories of NAT
  
  - **Static NAT (SNAT)**: each private IP addr is assigned to a specific routable public IP addr, and kept by the NAT enabled router.
    
    - when a device needs access outside of the local nw, the router translates the local IP addr to the assigned public IP addr. 
    
    - not flexible and has scalability issues. 
  
  - **Dynamic NAT (DNAT):** the router dynamically assign a routable IP addr to devices from a pool of available public IP addr.
    
    - more flexible than SNAT, but as more nw traffic, more access to remote nw required, the pool of available public IP addr needs to be increased.
  
  - **Port address translation (PAT)**: a type of DNAT that was developed to increase the scalability of NAT.
    
    - addition of dynamically assigning a port bumber to the end of the public IP addr. 
    
    - still require a pool of public IP addr. but less public IP addr required and easier for administrator to maintain.

- The NAT terminology
  
  - ![](C:\Users\hupei\AppData\Roaming\marktext\images\2022-02-07-19-08-38-image.png)
  
  - ![](C:\Users\hupei\AppData\Roaming\marktext\images\2022-02-07-19-09-46-image.png)

## WAN technologies (Wide Area NW)

### Public switched telephone nw (PSTN)

- one of the most common physical infrastructures used in WAN tech due to its widespread availability. 

- **Dial-up**
  
  - <u>utilizes the PSTN to transmit nw traffic as an analog signal </u>
    
    - require an analog modem to format the nw traffic
    
    - max theoretical speed: 56 Kbps

- **ISDN (Intergrated Services Digital NW)**
  
  - digital point-to-point WAN tech using the PSTN
  
  - completely digital service
    
    - <u>require the use of a terminal adpater (TA) for the connection to the end node (digital modem)</u>
    
    - ![](C:\Users\hupei\AppData\Roaming\marktext\images\2022-02-07-19-15-25-image.png)

- **xDSL**
  
  - A digital WAN tech using PSTN
  
  - require digital modem
  
  - dedicated digital line between the end point and a class-5 central office (CO) ---- withiin 18K feed of the CO
  
  - <u>carries vocie and data</u>

- **SDSL (Symmetric DSL)**
  
  - synchronous in nature (<u>same upload and download speed</u>)
  
  - not carry voice communication 

- **ADSL (Asymmetric DSL)**
  
  - asynchronous
  
  - <u>carry data and voice </u>
  
  - most common implementation of DSL in the SOHO (small office and home office) env

- **VDSL (Very-high-bit-rate DSL)**
  
  - asynchronous
  
  - used when need<u> high quality video and VoIP</u>
  
  - only possible when located within 4K feed of a CO

### Broadband cable

- coaxial cable networking
  
  - broadband connection to a location delivered by the cable company
    
    - can deliver voice, data and television --- all through the same connection
  
  - **headend**: all cable signals are received at this point; signals are processed and formatted than transmitted to the distribution nw
  
  - **distribution nw**: smaller service areas served by the cable company. can be composed of fiber optic cabling, coaxial cabling and/or hybrid fiber-coasxial cabling (HFC)
    
    - Unlike DSL, the bw is shared by the distribution nw --- increasing latency and congestion
  
  - DOCSIS (Data over cable service interface specification)

### Fiber

- Fiber-optic networking
  
  - **use light to transmit data and voice**
    
    - allows for <u>more bw over greater distances</u>
  
  - SONET (synchronous optical nw): fiber sun data transmission standard in US
  
  - SDN (syn. digital hierarchy): international standard
  
  - **OC (Optical carrier) levels**: base rates of transmission
  
  - **DWDM (dense wavelength-division multiplexing)**: method of <u>multiplexing serveral OC levels into a single optical fiber, increasing the bw of a single optical fiber</u>
  
  - **CWDM (coarse wavelength-division multiplexing)**: <u>similar to DWDM, but only up to 8 channels on a single fiber</u>
  
  - **PON (passive optical nw)**: <u>point-to-multipoint t</u>ech that uses a single optical fiber to connect multiple locations to the internet
    
    - use unpowered optical splitters

### GSM/CDMA WAN connections

- Cellular carriers use <u>one of two methods for connecting devices to their nw</u> and they are <u>not compatible</u>.

- Currently, in US, AT&T and T-Mobile use **GSM (global system for mobile)**, Sprint and Verizon use **CDMA (code division multiple access)**.

- **Celluar networking**
  
  - involves using the cellular phone system for more than just phone calls.
  
  - **1G** cellular: <u>voice transmissions</u>
  
  - **2G**: add <u>simple data transmission (text)</u>
    
    - 2G EDGE: a stopgap between 2G and 3G
  
  - **3G**: beginning of <u>cellular WAN networking</u>
  
  - **4G**: an emerging tech, currently <u>consists of LTE and WiMAX</u>
  
  - **HSPA+ (Evolved high speed packet access)**: stopgap between 3G and 4G
  
  - **LTE (Long term evolution)**: use an all-IP based core with high data rates. compatible with 3G and WiMAX 

### WiMAX WAN connections

- **World Wide Interoperability for Microwave Access (WiMAX) networking**
  
  - was originally developed as a last mile alternative for use when DSL or cable was not available
    
    - provide an alternative broadband connection to a fixed location
  
  - <u>uses microwave transmissions as an over-the-air method to transmit voice and data</u>
    
    - requires a line of site between relay stations
  
  - can be used to cover significant geographic distances
  
  - often considered to be a type of 4G tech because of its <u>compatibility with LTE nw</u>
    
    - not compatible with 3G type nw

### Satellite WAN connections

- **Microwave satellite networking**
  
  - uses <u>microwave transmissions as an over-the-air method to transmit voice and data</u>
  
  - can be used to extend nw into places that are hard to reach
  
  - **microwave radio relay**: <u>method of transmitting through the atmosphere</u>
    
    - require <u>line-of-site relay stations</u>, but can cover vast distances
    
    - may have latency problems
  
  - communication satellite (comsat) forms part of the microwave relay nw
    
    - <u>may use a variety of orbits     </u>
      
      - molniya, geostationary, low-polar, or polar orbits
      
      - <u>low-polar and polar orbits are used to boost the microwave signal before sending the signal back to Earth</u>.
      
       

### Metro Ethernet WAN connections

- it is when the service provider connects to the customer's site through an **RJ45 connector**

- the <u>type of connection is actually dependent on the level of service that has been purchased</u> by the customer, while customers view the WAN connection as an Ethernet connection. 

- Metro ethernet is commonly <u>deployed as a WAN tech by municipalities at the **metropolitan area nw (MAN)** level</u>.

### Leased line WAN connections

- **Leased line**
  
  - is a <u>dedicated circuit (connection) between 2 end points used for communication</u>. usually a digital point-to-point connection
  
  - can utilize either a plain old telephone service (POTS) line on the public switched telephone nw (PSTN), or can be a fiber optic cct provided by a telecomm company
  
  - tend to be more expensive for the customer, the speed is often limited by what customer willing to pay 
  
  - <u>multiplexing tech can be used to increase the amount of channels </u>that are provided on the connection.

- **Point-to-point protocol (PPP)**: <u>common data link layer protocol used with leased line nw.</u>
  
  - <u>simultaneously transmits multiple L3 protocols through the use of control protocols</u>
  
  - include a feature called **multilink PPP**, allows for multiple physical interfaces to be bonded together and act as a single logical interface --- to **increase the available bw**.

- **types of leased line connections**
  
  - **T-carrier (US, Japan, South Korea)**
    
    - each T line cct level is composed of 24 digital dignal channels (called digital signal 0 DS0)
    
    - <u>24 DS0 make a DS1 channel</u>
  
  - **E-carrier (Europe)**
    
    - composed of<u> 30 DS0 channels</u>
  
  - **Optical carrier (OC) lines**
    
    - OC data rates per channel 

### Common Standards

- Speed
  
  - <img title="" src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-02-08-17-47-45-image.png" alt="" width="372">

### Circuit switched vs. packet switched nws

- cct switched nw <u>have a dedicated cct between 2 end points used for communication.</u>
  
  - e.g., a phone call using a land line
  
  - most common in nws with leased line communication
  
  - only one path

- pkt switched nw: <u>data is broken up into smaller chunks and moved through the nw, only to be reassembled at the other end</u>.
  
  - data traffic is routed using the dest addr
  
  - data may take different paths through the nw
  
  - less expensive to maintain

### Frame relay vs. asynchronous transfer mode

- **frame relay**
  
  - <u>a WAN tech in which **variable length** pkts are switched across a nw </u>
  
  - less expensive than leased line
  
  - can be made to look like a leased line through the use of a **virtual cct (VC)**
  
  - tracks a VS using a **data link connection identifier (DLCI)**
  
  - **access rate**: the max speed of the frame relay interface
  
  - **committed information rate (CIR)**: guaranteed bw (min speed)

- **ATM**
  
  - <u>a WAN tech in which **fixed length cells** (each cell is 53 bytes) are switched across a nw</u>
  
  - can handle real time voice and video
  
  - fast tech, poor bw utilization (the small cell size reduces the efficiency of the tech)

### Multiprotocol label switching

- **MPLS**
  
  - A <u>topology</u> that is growing in popularity
    
    - scalable
    
    - protocol independent
  
  - can be used to <u>replace both frame relay switching and ATM switching</u>
    
    - can also be used to pckt switch both frame relay and ATM nw traffic. 
  
  - used to improve the QoS and flow of nw traffic
  
  - **label edge router (LER)**: <u>add MPLS labels</u> to incoming pckts if they don't have them
  
  - **label switching router (LSR)**: <u>forwards packets</u> based on MPLS labels.
    
    - ![](C:\Users\hupei\AppData\Roaming\marktext\images\2022-02-10-20-29-03-image.png)

## Network Cabling

### Twisted pair network cabling

- twisted pair cables: standard in the modern LAN
  
  - composed of <u>4 pairs of wires</u> contained within an insulating sheath. Each pair of wires is twisted together to <u>reduce electromagnetic interference (EMI)</u>. The<u> twist rates differ</u> between the pairs of wires to <u>reduce crosstalk between the pairs</u>. The color are: w o/orange, w b/blue, w g/green, w b/brown. 

- **unshielded vs. shielded twisted pair (UTP vs. STP)**
  
  - STP: has <u>an additional shield</u> that is either wrapped around each pair of wires or around all four pairs
    
    - reduce EMI and crosstalk, but more expensive

- **Plenum vs. non-plenum twisted pair**
  
  - <u>most twisted pair is non-plenum grade</u>
  
  - builing codes often call for plenum grade cable to be <u>run in plenum spaces</u> (areas designed to assist in the <u>airflow of a building</u> for HVAC purposes)
    
    - jacketed in either a fire-retardant cover or in a low-smoke PVC jacket
    
    - polymer or nylon strand woven into the cable to help take the weight of hanging cables and reduce the chance for cable to stretch --> cause the pair inside to break 

- twisted pair is either a  **straight-through cable **or a **crossover cable**, it can also be used to **create a rollover (console) cable**
  
  - **straight-through cable**: used to<u> connect different types of devices</u> together (cmp to sw, or sw to router) 
  
  - **crossover cable**: <u>connect similar devices</u> together (PC to PC, or sw to sw)
  
  - rollover or console cable: required to connect to the console port on a sw or router. It is common for one end of the rollover cable to use an RJ45 connector, the other end use RS232 connector.

### Twisted pair network connectors

- <img title="" src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-02-10-20-47-53-image.png" alt="" width="437">

- <img title="" src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-02-10-20-49-19-image.png" alt="" width="435">

- ![](C:\Users\hupei\AppData\Roaming\marktext\images\2022-02-10-20-50-41-image.png)

### Categories of twisted pair

- <img title="" src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-02-10-20-51-45-image.png" alt="" width="385">

### Coaxial cabling

- one of the oldest ethernet cabling standards

- has been used for baseband (carries single digital signal)

- used for broadband (carries multiple digital signals)

- the inner metal mesh or foil layer helps to protect against EMI
  
  - <img title="" src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-02-10-20-55-00-image.png" alt="" width="316">

- coaxial cable types 
  
  - <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-02-10-20-56-25-image.png" title="" alt="" width="408">

- coaxial cable connectors
  
  - ![](C:\Users\hupei\AppData\Roaming\marktext\images\2022-02-10-20-58-06-image.png)

### Fiber optic cabling

- relatively expensive and harder to work with

- not common in LAN env

- <u>resist all form of EMI and cannot be easily tapped</u>
  
  - harder to eavedrop 

- can cover long distances at hight speed

- designated by <u>fiber type, cladding size and jacket size </u>

- the type of connector used on fiber optic cabling can impact the performance of the transmissions
  
  - UPC (Ultra physical contanct) connector
  
  - APC (Angled physical contanct) connector: better performing connector

- Fiber Types
  
  - **multimode fiber (MMF)**
    
    - use an<u> infrared LED system</u> to transmit the light
    
    - use <u>multiple rays of light</u> going down the cable
    
    - used for shorter fiber runs, <u>under 2km</u>
    
    - less expensive to implement than SMF
    
    - most common application in networking is MMF 62.5/125u
  
  - **single-mode fiber (SMF)**
    
    - use a<u> laser-diode arrangement</u> to transmit the light
    
    - use a<u> single ray of light</u> transmitted down the cable
    
    - used for longer runs that require high speed
      
      - traverse 40+ km

- Fiber optic cabling connectors
  
  - ![](C:\Users\hupei\AppData\Roaming\marktext\images\2022-02-13-20-34-27-image.png)

### Media converters

- common to see a nw contains more than one type of cabling
  
  - need to connect different types of media together 

- media converter
  
  - common to connect: <u>SMF to ethernet, MMF to ethernet, SMF to MMF, fiber to coaxial cabling</u>

### Cabling tools

- ![](C:\Users\hupei\AppData\Roaming\marktext\images\2022-02-13-20-40-45-image.png)

- ![](C:\Users\hupei\AppData\Roaming\marktext\images\2022-02-13-20-41-11-image.png)
