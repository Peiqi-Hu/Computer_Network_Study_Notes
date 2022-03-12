# Computer Networking Course - Network Engineering (CompTIA Network+) Part 3

## Implementing a basic network

### Plan the network

- A nw plan is vital whem implementing any nw more complicated than the most basic. 

- **list of requirements**
  
  - define why the nw is needed
  
  - define what nw features are required
  
  - define the scope of the nw
  
  - eastablish a budget

- **nw design**
  
  - what equipment is needed to implement the nw
  
  - how the nw be organized
  
  - how the shared resources be placed on the nw

- **compatibility issues**
  
  - what standards are in play now and in the future
  
  - does current equipment require specific cabling or connection types

- **internal connections**
  
  - how many node connections
  
  - how will future expansion be planned

- **external connections**
  
  - how will the nw connect to the outside

- **nw equipment placement**
  
  - is there a wiring/equipment closet
  
  - what env considerations 

- **how will nw security be implemented**
  
  - firewall type and placement considerations
  
  - VLANs required or not
  
  - how the port security be implemented

### Configure the network

- Network configuration considerations
  
  - How clients receive their IP addr:
    
    - <u>static IP addr</u> configuration creates more security, but harder to manage
    
    - <u>DHCP</u> to automatically assign IP addr from a pre-configured pool
  
  - **MAC filtering**: only <u>allow specified MAC addr onto the nw</u>. It is effective but difficult to control
  
  - A **demilitarized zone (DMZ)** will be required if a server will be hosted on the nw that needs to be accessed from outside the nw. 
    
    - the <u>DMZ is an area of the nw in which outside connections are allowed, while the internal nw remains protected</u>
      
      - will require a custom configuration of the firewall; in most implementations,<u> 2 firewall</u>s are used
  
  - Firewall placement and configuration considerations
    
    - if a DMZ needs to be deployed, the best method is to <u>introduce an additional router and firewall</u> into the nw, with the DMZ residing between the WAN equipment and the new router/firewall combination
    
    - if a DMZ is deployed,<u> port forwarding should also be used at the router/firewall level</u>
  
  - router/firewall config considerations
    
    - **port forwarding** is used to direct requests for specific resources to the computer that has the resource 
  
  - wireless nw config considerations
    
    - **Service set identifier (SSID)**: the name of the wireless nw 
      
      - SSID can be set to broadcast in the clear
      
      - SSID can alternatively be set for the broadcast to be hidden
    
    - **Encryption**: needs to be tunred on (by default wireless routers and WAPs do not have encryption enabled) and, at the minimum, WPA2-Personal should be enabled
    
    - some wireless nw equipment comes with **Wi-Fi protected setup (WPS)** enabled by default. This **<u>should be turned off and not used</u>**, as it creates a weakness in the wireless nw.
      
      - WPS can be easily exploited by an attacker

- Document any changes 

## Analyzing monitoring reports

### Baselines

- Baseline documentation provides a snapshot of the nw when it is running efficiently. <u>Baselines are usually kept as a log file</u>, although they may also be graphical in nature. 

- Baselines should be established on <u>CPU utilization and nw utilization</u>. **Periodic tests** should be conducted to determine if the baseline has changed. You can use Windows Performance Monitor to help establish the baseline. 

- **Items to consider for baselines**
  
  - **nw device CPU utilization**
    
    - help to determine when a nw device is going to fail
    
    - help to determine when more nw devices should be installed in a growing nw
  
  - **nw device memory utilization**
    
    - help to determine when it is time to expand the memory of nw devices
  
  - **bandwidth utilization**
    
    - help to determine the overall health of a nw
    
    - help to determine when nw segmentation should occur
    
    - help to determine if a nw device is failing 
    
    - help to identify when a security breech has occured
  
  - **storage device utilization**
    
    - help to determine when storage utilization has become a bottleneck on the nw
    
    - help to determine when to increase the storage capacity of the nw
  
  - **wireless channel utilization**
    
    - help to determine how saturated the wireless channels have become; a new **wireless access point (WAP)** can be installed to alleviate the pressure if saturated
    
    - help to determine if there is unauthorized wireless access occurring

### Reports

- **Log management**
  
  - <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-03-03-16-20-25-image.png" title="" alt="" width="448">

- **Interface link status**
  
  - <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-03-03-16-21-36-image.png" title="" alt="" width="425">      

- **Interface monitoring reports**
  
  - <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-03-03-16-24-11-image.png" title="" alt="" width="421">

## Network Monitoring

### The why of network monitoring

- to not be surprised by failures in nws

### Tools to monitor the network

- **Log files**
  
  - all OS offer a means of viewing events that occur to that specific machine, includes nwing equipment
  
  - some applications have been developed to monitor sys and nw that also generate log files
  
  - log files can be used to <u>help pinpoint when a problem occurred</u> and help to <u>narrow down the cause</u> of an issue
  
  - log giles can be used to <u>help create a baseline of nw behavior</u>
  
  - can usually be classified as being: <u>sys logs, general logs, history logs</u>
    
    - are an after-the-fact means of monitoring the nw, not very good for real time analysis

- **Logging tools**
  
  - Event viewer
    
    - <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-03-03-16-30-08-image.png" title="" alt="" width="394">
  
  - Application logs
    
    - <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-03-03-16-30-25-image.png" title="" alt="" width="390">
  
  - Security logs
    
    - <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-03-03-16-30-39-image.png" title="" alt="" width="412">
  
  - System logs 
    
    - <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-03-03-16-30-58-image.png" title="" alt="" width="440">
  
  - **Sysklog**
    
    - non-microsoft log
    
    - <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-03-03-16-33-12-image.png" title="" alt="" width="430">
    
    - <img src="file:///C:/Users/hupei/AppData/Roaming/marktext/images/2022-03-03-16-33-36-image.png" title="" alt="" width="365">
  
  - **SNMP (Simple Network Management Protocol)**
    
    - an <u>application layer protocol </u>used to monitor and manage a nw's health
    
    - nw or sys admin configures monitors (called **traps**) on devices that view the operation of a specific item
      
      - the monitors periodically communicate with a **nw management station (NMS)** through **GET msg** that NMS sends out
      
      - the response from the monitors is stored in a **Management Information Base (MIB)**, which is a type of log file.
      
      - the admin can configure the monitors with **SET msg** sent from the NMS.
    
    - when an event occurs (interface goes down), the trap is tripped and the event is logged
      
      - can be configured to just log the event or contact a nw admin
      
      - the ability provides a more <u>real time monitoring</u> method
  
  - **SIEM (Security information and event management)**
    
    - <u>combine **security information management (SIM)** and **security event management (SEM)**</u>
    
    - used to <u>monitor and provide real-time analysis of security alerts</u>
      
      - an example of SEM functionality
    
    - used as a<u> tool to analyze long-term data and log files</u>
      
      - an example of SIM functionality
    
    - <u>highly configured</u> to the needs of the individual nw needs

### Active network monitoring tools

- **Port scanners**
  
  - used to scan a nw for open ports and protocols, then info is then used to harden the nw
  
  - are a great method of finding vulnerabilities in the nw infrastructure and plugging them before a security breech can occur.
  
  - only use a port scanner on a nw or a sys that you are authorized to scan

- **Interface monitoring/packet flow monitoring**
  
  - are usually deployed as **active software tools to monitor and analyze nw traffic within a nw segment** 
    
    - commonly called ***packet sniffers*** or ***protocol analyzers***, allow for an in depth look at what traffic is on the nw and may reveal security issues that the nw admin can then mitigate 
  
  - can identify <u>top talkers</u> on a nw segment
    
    - the interfaces that are sending the <u>most nw traffic</u> or utilizing the <u>most bw</u> for sending packets
  
  - can identify <u>top listeners</u> on a nw segment
  
  - **Microsoft Message Analyzer** and **Wireshark** are examples of free packet flow monitoring tools

### Wireless monitoring tools

- **WiFi analyzer**
  
  - a similar tool to the protocol analyzer, but for wireless nws
    
    - sniffs out packets on wireless nws
  
  - can <u>check for bw usage, channel usage, top talkers etc.</u>
  
  - can <u>identify nws by passively scanning the radio frequencies (RFs)</u>
  
  - can <u>identify hidden nws</u> if given enough time
  
  - can infer non-beaconing nws based on data traffic

- **Wireless survey tools**
  
  - most commonly used as a design tool for <u>setting up high quality wireless nws</u>
    
    - the survey tools can help to establish the required amount of access points (APs), ideal antenna placement, and optimum channel overlap
    
    - can be used to identify possible causes of RF
  
  - used to<u> eliminate wireless nw performance and security issues</u> before they even occur.

### Environmental monitoring

- A nw's health can be affected by more than just a nw interface failing or a possible security breech

- enviromental factors: electrical power, heat and humidity

- **power monitoring**
  
  - systems and tools can be used to <u>evaluate the amount of and the quality of the electrical power being delivered to the system</u>.
    
    - power monitoring is often deployed with, or alongside, an **uninterrruptable power supply (UPS)**
    
    - the monitor will issue an alert when an issue with electrical power has been identified

- **environmental monitors**
  
  - **heat monitors**
    
    - all electrical components are designed to operate within a specified heat range, they also generate heat when in use
  
  - **humidity monitoring**
    
    - too little humidity increases the risk of electrostatic discharge and too much humodity increases the risk of condensation



## Supporting configuration management

### Configuration management （CM）

- CM is a discipline that is used to evaluate, coordinate, approve, deny, or implement change in or to an IT system.
- helps to ensure that the nw runs efficiently and smoothly. 

### Documentation

- Documentation plays a key role in any CM sys that get developed.
- used to help evaluate and plan proposed changes, and also used in asset management, nw maintenance, and vendor evaluations. 
- **Policies and procedures**
  - Policies are <u>a set of guidelines that establish how the nw is to be configured and operated</u>. They also set the expected behavior of the people within the organization.
  - Procedures are a set of documents that detail <u>how the policies are to be implemented.</u> 
- **Asset management documentation**
  - broad category of documentation often used to help in the change management process.
  - detailed info on <u>what assets are present</u>, also includes the <u>maintenance history</u> for those assets.
  - used to <u>help track update and upgrade cycles</u>
- **Physical nw diagrams**
  - <u>a map of all nw devices and how they connect</u>
  - specifies the <u>cabling, connectors, and physical cabling runs</u>
  - cabling management documentation is a subcategory
    - A **wiring scheme** establishes the types of cabling and the connectors used, and also defines the allowed standards. 
- **Logical nw diagrams**
  - similar to a physical nw diagram but more detailed
  - details <u>IP addresses, ports, protocols</u>, etc.
  - details <u>connected nws (e.g., LANs, VLANs, and WLANs)</u>
  - details <u>IP address utilization</u> 
    - IP address utilization can greatly affect the efficiency and performance of the nw
  - physical and logical nw diagrams may be combined into a single document
- **Vendor documentation**
  - a broad category of documentation that can include:
    - approved vendor list
    - vendor approval process
    - purchase order documentation
- **Common vendor documents**
  - ![image-20220312101238037](C:\Users\hupei\AppData\Roaming\Typora\typora-user-images\image-20220312101238037.png)

### Backups

- Backups are an essential part of any CM system
  - play a key role in recovering from unexpected consequences or from the failure of a component. 
  - Backup schedules must be implemented and <u>periodic tests</u> should be conducted to ensure that the backup process is working. 
- **Types of backups**
  - **Full**
    - <u>all data</u> on the targeted sys is backed up
    - <u>slowest backup</u> method with the <u>highest storage</u> requirements, but leads to the <u>fastest recovery</u> method.
    - recovery requires the full backup files
  - **Incremental**
    - only the <u>new or modified files</u> are backed up
    - <u>fastest backup</u> method with the <u>lowest storage</u> requirements, but <u>slowest recovery</u> method
    - recovery requires the last full backup file and all of the incremental backup files
  - **Differential**
    - only <u>data that has changed since the last full backup is saved</u>
    - time is <u>moderate</u>, requires a moderate amount of storage, but also is the middle ground on the length of time for recovery
    - recovery requires the last full backup file and the last differential backup file
- The configuration files of a nw device should also be backed up. 
  - helps to speed up the recovery time in cases of equipment failure or when a change to the configuration has introduced unexpected consequences. 

### Bring your own device (BYOD)

- BYOD policies <u>allow employees to use their personal devices on an organization's nw</u>. 
  - IT departments are tasked with keeping a nw safe, yet they have <u>very little control over the devices that employees bring in</u>. In some cases, BYOD policies have led to the <u>introduction of malware</u> into an organization's nw environment. 
  - **Network Admission Control (NAC)** has been implemented in an effort to reduce the risks associated with BYOD policies and to <u>introduce CM to those devices</u>. 
- **NAC**
  - NAC is a Cisco process. Microsoft uses Network Access Protection (NAP)
  - includes more than just authenticating users and devices on the nw
  - <u>all devices requesting access to nw resources are screened for:</u>
    - type of device
    - OS used, including updates
    - security software, including updates
    - presence of malware
    - other security vulnerabilities
  - in some cases, if the connection request has been rejected, the device is redirected to a *<u>remediation（补救） server</u>*, which attempts to resolve the known issue.



## The importance of network segmentation

### The OSI model and segmentation

- Segmentation: taking a single nw or a sys and breaking it into smaller discrete units. 
  - can be achieved <u>physically or logically</u>
  - reasons to segment a nw 
    - to ease administrative tasks
    - to achieve performance gains
    - to increase security
    - to comply with regulations
- Segmenting the nw at different OSI model levels
  - **OSI (open system interconnection)** model
    - Physical layer (L1)
    - Data link (L2)
    - Network (L3)
    - Transport (L4)
    - Session (L5)
    - Presentation (L6)
    - Application (L7)

### Reasons for segmentation

- **Compliance**
  - some rules and regulations require that <u>certain data be kept separate and secure</u>
    - segmentation allows for the regulated data to flow across its own nw keeping it more secure
- **Network performance optimization** 
  - the <u>size of nws increases</u>, the amount of data flows also increases which slow down the performance of the nw.
    - segmentation breaks the larger nw into smaller units, which can lead to an increase in performance on those new segments
- **Creating high performance nws**
  - some applications <u>require more bw</u> in order to perform at a desired higher level
    - VoIP, video teleconferencing (VTC), media nets (streaming services) perform better on their own segments

- **Separate private from public networks**
- **Legacy systems**
  - some organizations use systems that are considered critical, but are not capable of residing on the modern nw. 
    - segmentation allows the legacy(遗留) sys to reside(居住) on its own subnet.
- **Testing labs**
  - the labs can be used to test new applications, os, update patches, etc. 
    - segmentation allows for testing to occur in a secure, easily controllable env.
- **Security**
  - one of the main reasons
    - segmentation allows nw and sys administrators to <u>more easily control the flow of data between sys and access to nw resources</u>.
- **Honeynets**
  - nw segments that are created with the sole <u>purpose of attracting any nw attacks through the use of multiple honeypots</u>
    - the nw segment of honeypots allows the main nw to remain secure, and gives nw administrators an opportunity to study an attack so that countermeasures can be developed to prevent future breeches.
- **SCADA (Supervisory Control and Data Acquisition) systems**
  - the most widespread of **ICS (industrial control sys)** 
    - the <u>use of coded signals over communications channels to provide control of remote equipment</u>.
    - commonly used in industrial applications to monitor and control sys.
  - <u>utilities often use SCADA sys to control their operations, through the use of a **DCS (distributed control sys)** nw</u>. 
    - The DCS allows for the <u>control of multiple SCADA sys</u> from a single location
  - The *Stuxnet virus* attacks SCADA sys and can spread through the DCS, leading to more damage from the virus
    - segmentation of the DCS can limit the amount of damage caused by such a virus attack on industrial processes.



## Applying patches and updates

### Patches and updates

The complexity of the modern OS has led to the necessity for updates, patches, and hotfixes. These are used to add features, fix bugs, and repair security holes that become know. 

The goal is to keep sys as up to date as possible through the use of updates, patches, and hotfixes ---- reduce the sys's vulnerability and increase its functionality, while reducing costs.

- **Patches, updates, hotfixes, and service packs**
  - A **patch**: is <u>small section</u> of code that is used to either increase functionality or fix a problem within a software package.
  - An **update**: is a <u>large section</u> of code that is used to either increase functionality or fix problems within a software package. 
  - A **hotfix**: (also called a **vulnerability patch**) is similar to a patch, but is smaller than a patch. They are designed to be deployed to <u>fix very specific issues</u> within an OS or other software package.
  - A **service pack**: is a <u>cumulative Windows update package</u> that contains all patches, updates, and hotfixes between two points in time. 
    - Microsoft releases service packs as a method of easing the installation of an OS, helping to keep it current. 
- It is possible to <u>*automate* the patch and update process through registering the product with the vendor</u> who created it. 
  - In a production setting, all patches and updates should be installed and tested in isolation (e.g., testing lab) before they are installed on production equipment. 

### Upgrading vs. downgrading

- Sometimes issues arise with the installation of a patch or update, leading to problems that were not caught during the testing phase. 	
  - <u>backup copies of all sys and configuration files</u> should be maintained in order to downgrade (roll back) when this occurs. 





