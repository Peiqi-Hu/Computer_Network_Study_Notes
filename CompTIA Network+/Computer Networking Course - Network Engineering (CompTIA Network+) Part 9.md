# Computer Networking Course - Network Engineering (CompTIA Network+) Part 9

## Introduction to wireless standards

### CSMA/CA

- all wireless Ethernet standards employ an algo called CSMA/CA
- a CSMA/CA nw involves a method of transmission that avoids packet collisions. It differs from a CSMA/CD type of nw which is about how to transmit after a collision has occurred.

#### Frequency modulation

- is the process used to <u>encode data into a carrier wave</u> 
- 802.11 uses two main frequency modulation methods

#### Orthogonal frequency-division multiplexing (OFDM)

- is a frequency division multiplexing scheme that uses multiple sub-carrier channels to carry data
- is used to mitigate <u>against attenuation</u> (loss of signal strength over distances) and <u>multipath issues</u> that exist in nwing 

#### Direct-sequence spread spectrum (DSSS)

- is a <u>modulation technique</u> that <u>uses spread spectrum technology to affect data transfer</u> 
- is used to mitigate the problem of <u>multiple users on a channel</u> and for effective timing between the transmitter and receiver

### Wireless standards

- Wireless nwing standards are established by the 802.11 committee of the  IEEE. 
- the term Wi-Fi is actually a reference to the Wi-Fi Alliance, which is responsible for certifying that wireless nwing equipement actually meets the 802.11 standards. It has become synonymous with the WLAN in the English language. 

#### 802.11a

<img src="C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220324103314320.png" alt="image-20220324103314320" style="zoom:70%;" />

#### 802.11b

<img src="C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220324103333082.png" alt="image-20220324103333082" style="zoom:67%;" />

#### 802.11g

<img src="C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220324103356614.png" alt="image-20220324103356614" style="zoom:67%;" />

#### 802.11n

<img src="C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220324103431472.png" alt="image-20220324103431472" style="zoom:67%;" />

#### 802.11ac

<img src="C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220324103456561.png" alt="image-20220324103456561" style="zoom:67%;" />

##### Note:

- Each standard has a theoretical max throughput. 
- MIMO is used to increase throughput and to reduce weak spots or dead zones in a wireless nw. 



## Introduction to wired network standards

### TIA/EIA 568A and TIA/EIA 568B

#### Twisted pair wire standards

- there are 2 twisted pair cable pinout standards that are regulated by TIA/EIA (telecommunications industry association/electronic industries alliance). The pinout standards specify the ordering of the wires to ensure that proper nwing communications can take place
  - TIA/EIA 568A (T568A)
  - TIA/EIA 568B (T568B)
  - <img src="C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220324104139347.png" alt="image-20220324104139347" style="zoom:67%;" />
- all modern Ethernet nws that utilize unshielded twisted pair (UTP) or shielded twisted pair (STP) use the TIA/EIA standards.

#### Common tools used with twisted pair cable

##### Wire strippers

- used to remove the insulating jacket from the cable

##### Crimping tools

- used to secure wires into modular connectors

##### Punchdown tools

- used to secure wires into a punchdown block

##### Cable testers

- used to test the integrity of a nw cable

### Ethernet Standards

#### Distance limitations

- twisted pair is limited to 100 m without a repeater, unless otherwise stated
- coaxial LAN is limited to either 185 or 500 m, depending on the coaxial cable that is used
  - 10Base2: 10Mbps, using RG-58, limited to 185m
  - 10Base5: 10Mbps, using RG-8, limited to 500m
- Fiber optic LAN transmission is limited by the cable used, current max is over 40km over **single-mode optical fiber (SMF)**

#### Twisted pair cable

- ![image-20220324104611550](C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220324104611550.png)

#### Multi-cable standard

- 1000BaseX
  - 1000BaseSX: 1 Gbps over short distance **multimode fiber optic (MMF)** (less than 2 km)
  - 1000BaseLX: 1 Gbps over long distance SMF (greater than 2 km)
  - 1000CX: 1 Gbps over coaxial cable up to 25 m

#### 10 gigabit networking

<img src="C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220324104827906.png" alt="image-20220324104827906" style="zoom:67%;" />

### Other standards

#### DOCSIS (Data over cable service interface specification)

- to <u>provide the interface requirements for data transmissions over a broadband cable nw</u>
  - to achieve the best performance when using broadband cable, the cable modem should meet the highest DOCSIS standard used by the cable provider 
- the most current standard is DOCSIS 3.1, which allows for up to a theoretical maximum download speed of 10 Gbps with a theoretical upload speed of 1 Gbps

#### IEEE 1905.1-2013

- <u>defines a nw enable (or device) that is used to create a convergent home nwing env</u> that includes different types of wired and wireless nws
  - the standard also includes <u>Ethernet over power line</u>, which is using the existing electrical wiring in a structure as the media to transport data
  - also includes <u>Ethernet over HDMI</u>, which is using an HDMI interface and cable to transport nw traffic



## Security policies and other documents

### Security policies

- Policies: a set of guidelines, established by management, that are used to set the expected behavior in the workplace
- Procedures: the set of steps required to be taken in a given situation

#### Consent to monitoring

- A policy that established the <u>employer's right to monitor the employee's actions and communications</u>, which include:
  - monitoring emails
  - monitoring or recording of phone conversations
  - monitoring activities on computers, drives and phones
  - in highly secure work env, it may also include the video monitoring and recording of normal work activities

#### Clean desk policy

- a policy that is <u>concerned about the handling of sensitive data</u>
  - should not left unattended in a workplace and should be put away when not in use
  - includes the computer desktop; sensitive data should not be left easily accessible on the PC

#### Recording policy

- restricts the use of cameras, tape recorders, portable storage devices, or any other device that may be used to record or copy sensitive workplace info

#### Equipment access policy

- a security policy that establishes <u>who has access to which equipment and when</u>. could include access to:
  - server rooms
  - wiring closets
  - nw racks

#### Handling of user or customer information

- how to <u>secure sensitive employee and customer info</u>
  - user and customer info is a major target of hackers when they breach computing systems. The loss of control of this data can severely damage a company.

#### Note

- any policy that is used to help secure the workplace or company data is, by default, a security policy

### Other documents

#### AUP (Acceptable use policy)

- a set of rules and guidelines established by the creator, owner, or administrator of info sys that <u>detail what users may or may not do with that info sys.</u>
  - is considered to be a part of the security policy
  - should be fairly detailed in what is allowed or not allowed to occur
  - all users should be required to sign the policy and these records should be kept on file

#### Network policies 

- a broad range of policies that <u>establish the guidelines for the nw</u>, include policies that control the use and operation of the nw, as well as how to implement changes to it
  - many security policies may fall under the general nw policies category

#### Standard business documents

##### Memorandum of understanding (MOU)

- an agreement between two or more organizations that details how those organizations are to undertake some common course of action
  - often used before a legally binding agreement has been created
  - sometimes it is called **a letter of intent (LOI)**

##### Statement of work (SOW)

- a detailed document that specifies <u>what work is to be performed, the expected outcome or deliverables, and the timelines to perform the work</u>
  - plays an important role in project management documentation

##### Master license agreement (MLA)

- a legal agreement between 2 entities in which one agrees to pay the other for the use of a specific piece of software (or software package) fir a specified period of time

##### Service level agreement (SLA)

- an agreement that details the allowable amount of response time the vendor has to resolve an issue or problem
  - most commonly is associated with a service contract



## Introduction to safety practices

### Electrical safety

#### Electrical grounding

- is used to protect technicians in the case of electrical insulation failure
  - provides an alternate path for the electricity; is often referred to as a return to earth
- all electrical sys should be connected to properly grounded circuits

#### ESD (electrostatic discharge)

- is caused when 2 electrically charged objects that have different amounts of electrical charge come into contact, creating a flow of energy between the objects as they normalize the levels
  - can damage sensitive components, particularly the CPU and/or RAM
- using an ESD mat helps to reduce the chances of ESD
- using an ESD strap will also reduce the chances for ESD
  - the strap goes around the wrist and then is clipped to a ground source (usually to an exposed metal surface inside of the case)

#### Practice self grounding

- is a normalization tech used to equalize the amount of electrical charge between the worker and the equipment being worked on
  - after the case has been opened and the ESD strap is attached to a ground source, touch an exposed metal surface inside the case (before actually touching any of the components)

#### Additional equipment grounding

- in some cases, actually attaching a ground strap from the piece of equipment to a ground source is advised

#### Electrical fire safety

- in case of fire:
  - unplug the power source or turn off the circuit breaker
  - use a class C or multiclass fire extinguisher
  - never use water

#### Fire suppression systems

- building codes often call for the installation of fire suppression systems. There are several different types of common systems:

  - ##### Wet pipe

    - the pipes are pressurized and contain water

  - ##### Dry pipe

    - are not pressurized; water is contained in a holding tank

  - ##### Pre-action

    - similar to a dry pipe sys, but the sprinkler head contains a thermal-fusible link that must melt before the water is released

  - ##### Deluge

    - designed to release a large amount of water in a short amount of time into a predefined space
    - least desirable option for electrical components

  - ##### Halon(卤化烷)

    - a non-conducting volatile gaseous chemical
    - works by chemically disrupting combustion
    - not leave a residue upon evaporation; unlike water, halon will not ruin electrical components
    - safe for exposure to humans in limited amounts for a limited amount of time
    - environmentally safe, also known as a **clean agent**

### Installation safety

#### User proper lifting techniques

- <img src="C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220325105809741.png" alt="image-20220325105809741" style="zoom:67%;" />
- <img src="C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220325105821961.png" alt="image-20220325105821961" style="zoom:50%;" />

#### Rack installations

- <img src="C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220325105900888.png" alt="image-20220325105900888" style="zoom:67%;" />

#### Rack placement

- <img src="C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220325110032283.png" alt="image-20220325110032283" style="zoom:67%;" />
- <img src="C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220325110058169.png" alt="image-20220325110058169" style="zoom:67%;" />

#### Tool Safety

- <img src="C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220325110314241.png" alt="image-20220325110314241" style="zoom:67%;" />



### The MSDS (material safety data sheet)

- MSDSs contain safety info on materials and chemicals found in the workplace, contain all known health issues associated with a particular material, outlines what protective measures must be taken to reduce risks from exposure and what actions must be taken if the chemical is ingested. 
- also detail the physical properties of the material and the proper steps to take when disposing of it. 

### Emergency preparations

- these preparations should be detailed in a set of emergency procedure documents. The procedures should contain escape plans, including where employees will meet to ensure that all are accounted for, info on the types of fire suppression sys that are present, as well as what steps have been taken to increase the day-to-day safety in the workplace.

#### Building layout considerations

- <img src="C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220325110953622.png" alt="image-20220325110953622" style="zoom:67%;" />

#### Escape plans

- <img src="C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220325111048912.png" alt="image-20220325111048912" style="zoom:67%;" />

#### Safety or emergency exits 

- <img src="C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220325111111196.png" alt="image-20220325111111196" style="zoom:67%;" />

#### Fail open or fail close

- <img src="C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220327103058887.png" alt="image-20220327103058887" style="zoom:67%;" />

#### Emergency alert systems 

- <img src="C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220327103126151.png" alt="image-20220327103126151" style="zoom:67%;" />



## Rack and Power management

### Rack management

- Rack systems are specially designed racks used to hold nwing and computing equipment. Sometimes are referred to as server racks.
- The rack systems follow one of several different designs, however, they all follow the same height specification.
  - the specification is the standard unit (U) and it involves the amount of vertical space that can be used to hold equipment. 
  - A U = 1.75 inches. 

#### Types of racks

- are normally two-post or four-post racks
- server rail racks have slide mounts to make it easy to pull out servers to perform necessary maintenance

#### Device placement

- devices that generate the most amount of heat, or are not heat sensitive, should be placed toward the top of the rack
- all equipment cold air intakes should face the same direction; exhaust outlets should face the same direction (i.e., host aisle/cold aisle)

#### Airflow

- when mounting equipment in racks, vertical space should be left between the equipment to promote adequate airflow
- when multiple rows of racks are implemented, a hot aisle/cold aisle approach should be used to promote proper airflow and cooling

#### Rack monitoring

- racks should be monitored for environmental factors to help ensure the health of the servers and other equipment
  - monitors should be in place for: temperature, humidity, vibration, water leaks, smoke and intrusion

#### Rack security

- most rack systems do not come with rack security in mind, but it can be easily added after rack installation
  - rack doors can be added that have either keyed or electronic locks
  - <img src="C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220327104151921.png" alt="image-20220327104151921" style="zoom:50%;" />

### Power management

- It is important to know the power requirements and loads for all of the equipment that will be in place. This helps to ensure that the proper electrical circuits are installed, so that sufficient power is delivered where it is needed.

#### Power converters

- convert electrical energy from one form to another
- **power inverters:** specifically **converts voltages DC to AC**

#### UPS (uninterruptable power supply)

- uses power converters to receive electrical current from an AC electrical source and pass it to a battery for storage
- uses power inverters to receive DC current and pass it to another devices as conditioned (well regulated) AC flow
- used to provide a steady stream of conditioned electrical power to components
  - helps to protect sensitive electrical components from power anomalies (e.g., power spikes or power sags)

#### Power redundancy

- critical components should include redundant power supplies
  - if one of the power supplies fails, the other one takes over immediately



## Cable management

### Cable distribution

#### Main distribution frame (MDF)

- the location where the demarc, demarc extension, main switch/router, and patch panel are placed
- the MDF is <u>where outside traffic enters a location and then is distributed to the internal nw</u>

#### Intermediate distribution frame (IDF)

- a location's solution <u>when a single MDF is not sufficient</u>
- usually in a multistory building 
- <u>the IDFs are connected to the MDF by vertical cross-connect (VCC) cables</u>
- it is common for an MDF to contain separate IDF panels for each floor of a building

#### VCC (vertical cross-connect)

- the main patch panel for a location.
- usually resides in the same location as (or very close to) the demarc and main switch/router

#### Patch panel

- used to <u>terminate nw cable runs</u>, usually within a building (from the wall jacks to a central location)
- used to <u>organize and administer the physical aspects of the nw cables</u>
- nw runs are punched down to the back of the patch panel (normally a 66 or 110 block) with an associated port on the front of the patch panel
- patch cables are used to connect the patch panel ports to nwing gear
- <u>workstations connect to a patch panel using horizontal cabling; this location is called the **horizontal cross-connect (HCC)** and is usually located in the IDF</u>. Switches may or may not be present
  - if a workstation needs to be relocated to a different switch, all that needs to be done is to make a change in the location of the patch cable

### Cable management components

- Labeling is an important part of cable management. It can cause stress when working with nws, but it doesn't have to.
- the key to **proper labeling** is to <u>create a naming convention</u> that makes sense for the situation. Proper labeling will ease the management of the physical aspects of the nw, especially when dealing with cables.

#### Naming convention example

- <img src="C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220327110146218.png" alt="image-20220327110146218" style="zoom:67%;" />

#### Cable trays

- masses of cables can block airflow and act as an insulator that allows for excessive heat to build up
- cable trays are used to organize cabling and to keep it away from areas where cabling may cause heat buildup 



## Basic of change management

### The reason for change management

- It is quite possible that a single change will have a ripple effect on the whole system. Change management processes are used to introduce changes to a system in a controlled manner to minimize possible disruptions and potential pandemonium(骚动). 

### Different change management processes

#### Document the reason for a change

- proposed changes should have a solid reason for occurring 
  - a best practice is to include why the change is needed for IT reasons and also for business reasons
- as the change proceeds through the process, more documentation may be added to the reasons for a change

#### Change request

- a formal change request procedure is used during the approval process and should include several other subdocuments that can be used to gain approval

- ##### Configuration procedures

  - document the exact steps required to implement the change, including affected devices, applications, and processes

- ##### Rollback process

  - as all change carries risk, a plan to reverse change is required

- ##### Potential impact

  - a good-faith effort to identify all possible impacts to the overall sys, both the positive and the negative

- ##### Notification procedures

  - after the potential impacts have been identified, the people responsible for the affected sys must receive notification of the proposed change

#### Approval process

- <img src="C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220327111135194.png" alt="image-20220327111135194" style="zoom:67%;" />

#### Maintenance window procedure

- <img src="C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220327111242548.png" alt="image-20220327111242548" style="zoom:67%;" />

#### Authorized downtime

- <img src="C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220327111325994.png" alt="image-20220327111325994" style="zoom:67%;" />

#### Notification of change

- <img src="C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220327111408095.png" alt="image-20220327111408095" style="zoom:67%;" />

#### Final documentation

- <img src="C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220327111452556.png" alt="image-20220327111452556" style="zoom:67%;" />



## Common Network Protocol

### TCP and UDP	

- both are L4 protocols, responsible for the delivery of nw data between nodes

#### TCP (transmission control protocol)

- *reliable* delivery method
- ensures that all packets are received
- uses ACK as a means of error correction
- <u>establishes flow control to reduce error rate and ensure proper delivery</u> 

#### UDP (user datagram protocol)

- *best effort* delivery method
- sends data, but not care if the packets are all received
- no error correction
- speed and low nw overhead is what concerns UDP

### Common ports and protocols

#### HTTP (Hypertext transfer protocol)

- the primary protocol used to transfer data over the Internet
- assigned to **port 80**

#### HTTPS (Hypertext transfer protocol secure)

- the primary protocol to securely transfer data over the Internet using SSL or TLS technology. (SSL is no longer be used)
- assigned to **port 443**

#### NetBIOS (Network basic Input/Output system)

- originally developed to allow hosts to be able to communicate with servers
- assigned to **ports 137-139**

#### SMTP (Simple mail transfer protocol)

- used to transfer email from a client to an email server
- used to transfer email between servers
- assigned to **port 25**

#### POPS (Post office protocol v3)

- used by <u>clients to retrieve email from servers</u>. once engaged, POP3 downloads all messages from the servers. The user cannot access email messages until they have been downloaded
- assigned to **port 110**

#### IMAP (Internet message access protocol)

- used by <u>clients to access email on email servers</u>. allows the client to administer and organize email on the server into folders
- assigned to **port 143**

#### SIP (Session initiation protocol)

- most commonly used to <u>set up and tear down multimedia communication sessions</u> (e.g., a VoIP session uses SIP to establish and terminate the session)
- assigned to **ports 5060 and 5061**

#### RTP (Real-time transport protocol)

- commonly used to <u>format and deliver multimedia or streaming content</u> (e.g., RTP handles the flow of packets in a VoIP session after SIP has established the connection)
- assigned to **ports 5004 and 5005**

#### MGCP (Media Gateway Control Protocol)

- defines the means of <u>communication between a packet switched nw and circuit switched nw</u> (e.g., the PSTN). It can be used to <u>set up, maintain, and terminate calls between multiple endpoints</u> (e.g., teleconferencing)
- assigned to **ports 2427 and 2727**

#### H.323

- provides <u>a standard for delivering video over IP nws.</u> 
- defines how real-time audio, video, and data are to be transmitted
- provides signaling and bandwidth control
- assigned to **port 1720**

### The difference between ports and protocols

#### Ports

- a method of specifying what protocol or service to access
  - protocols and services use default ports so they are easy to locate
- there are 65,536 ports available to be used for communication, but port 0 is reserved. 
  - the first 1024 ports are specifically assigned and are called **well known ports**

#### Protocols

- can be thought of as the language that the two applications on either side of the connection agree to speak
- translate requests into services
- most protocols use pre-defined ports, but some protocols must be user configured

#### Note

- Ports are used to request services or applications.
- Protocols are the services or applications that are being requested.
- When a requestor seeks to connect to a specific port, the requestor is dynamically assigned a port number to listen to for the response. This also allows computers to have many concurrent connections.

### Common ports and protocols

#### FTP (File transfer protocol)

- transfer files <u>between computing systems</u>; requires user authentication
- assigned to **port 20 and 21** (mostly uses port 20)

#### TFTP (Trivial file transfer protocol)

- transfer files <u>between servers and clients</u>; no user authentication required
- assigned to **port 69**

#### SNMP (Simple network management protocol)

- used to monitor and manage local area nws
- assigned to **port 161**

#### Telnet

- used for remote access to systems; is unsecure
- is a bidirectional terminal service
- assigned to **port 23**

#### SSH (Secure Shell)

- used to <u>encrypt data traffic on a nw</u>
- can be used in place of Telnet to provide a secure bidirectional terminal connection
- assigned to **port 22**

#### DNS (Domain name system)

- used to map computer names to their IP addresses 
- assigned to **port 53**

#### DHCP (Dynamic host configuration protocol)

- used within nws to automatically configure computers with the correct IP configurations (e.g., IP address, subnet mask, default gateway, and DNS server location)
- **Requests** are assigned to **port 67**
- **Responses** are assigned **port 68**

#### RDP (Remote desktop protocol)

- used in Microsoft nws by remote desktop connection and remote assistance to make remote connections
- assigned to **port 3389**

#### SMB (Server message block)

- used to transfer files over a nw; the process is transparent to the user
- can be configured to run over NetBIOS on ports 137-139
- assigned to **port 445**

