# 25.25.30 - Information Delivery
This section relates to how information is to be delivered to the users so they can perform their "smarter" tasks related to the building. Since we are dealing with digital information, the most important part of defining "delivery" is specifying what the digital user interfaces (UI's) are that user groups in section 25.25.20 will use. Digital UI's can take the form of mobile applications, desktop or laptop applications, websites and browser applications, digital twin models, machine-to-machine interfaces, and (soon, more) augmented reality interfaces. Related to the delivery of information is defining the sources of and structures of the data. This includes databases, query tools, API (application program interfaces), data semantics, naming conventions, and more. Most of these topics are covered in other sections, but it is worth noting here that these elements of a system must be well coordinated. Lack of coordination can lead to "islands of automation", interface "silos", where the user has way too many custom, vendor specific interfaces to deal with which reduces overall operational efficiency. The "Single Pane of Glass" for user interfaces may look like one application managing everything or it can simply be a browser that has many tabs for system specific interfaces. Requiring user interfaces to be interfaced using a common IP network browser can be a significant benefit to the user. A well-prepared Owner's Requirement Document followed by a good design Specification will outline which delivery mechanisms (which UI's) are expected to be used by each user group identified in DIV 25.25.20 Operations, and what the functional requirements are for each UI. This section discusses:
- What digital devices do you expect your users to use?
- Do you expect a Single Pane of Glass (SPoG) interface?
- General Requirements for Interfaces
- Defining Multi-System Views and Interface Functionality

## 30.1 What digital devices do you expect your users to use?

List the devices you expect the users listed in section 20 to use when interacting with the smarter building. There are two sections here. Interface platform:
- Web browsers on any browser enabled device (laptop, desktop, tablet, phone)
- Custom applications (PC, Linux, MAC/iOS, Android enabled) Physical interface devices:
- Mobile phones
- Mobile tablets
- Kiosks
- Digital signage displays

- Voice activated/intercom/digital assistant (Alexa, Google Play, etc.)
- Wearable digital devices, such as smart watches
- Augmented reality devices

## 30.2 Do you expect a Single Pane of Glass (SPoG) interface?

SPoG is a term floating around for the building automation world for the last few years. First, let's define SPoG - it is referred to as a "Single Pane of Glass" and is most often used when referring to the user interface of a building automation system. It is the single computer monitor (the glass) that the operator, technician, engineer, and manager use to interface with their entire building automation and control system. The concept is one in which there is a single place to access all of the tools necessary to view system operations, diagnose problems, and manage all of the building's integrated systems. These include the traditional mechanical, electrical, and plumbing systems along with many others.

The value of a SPoG is necessary information can be accessed from one computer workstation, which enhances operational efficiency and the reduces training, support, and maintenance of multiple computer systems, software, tools, and infrastructure. Typically, the building or campus Master Systems Integrator is the one responsible for the development and delivery of this system. There is hardware, the computer, monitor. and software, the application(s), interfaces, drivers, APIs, and more, that must be integrated.

There is some debate as to what a SPoG allows and restricts from a solution provider, product vendor, or integrator's perspective. Some suggest the best solutions is a single computer software application that does everything - often referred to as the Building Management System (BMS) Front End Graphical User Interface. Others suggest a more efficient mechanism is having a single workstation but allowing multiple software applications on the single computer. A third options is deploying a single application that can launch secondary applications from within it -often called a "container application" as it contains the access to any other application via program calls, hot links, embedded redirects, and more. One of the first questions to ask is: Do you expect all interactions by all users with all of the smarter building functions, to be through a single user interface (SPoG)? That does not necessarily mean one monolithic application that tries to do everything for every system. It simply refers to the user interface being one computer/device access point to gain access to the various application interfaces needed to operate the facility. Here we are typically referring to the interface used by normal day-to-day system operation and is not considering specific diagnostic or maintenance tools. Those tools typically require custom software and interfaces supplied by the system vendor. So, for this framework we will assume that the SPoG is ONE WORKSTATION, Multiple Applications. Having a single non-integrated application is not overly practical in today's smart buildings and smart campuses. However, a single BMS front end with required interfaces for general data, monitoring, alarming, and control is very beneficial and part of any DIV 25 contractor's responsibility. But there will be multiple applications - that's the nature of the industry today. What we don't want to see is a dozen or more custom laptop computers for each system with dedicated interfaces (serial ports) for each system. In typical medium to large buildings, the software applications typically reside on a networked server, with access from any workstation on the network. This is for general user interfaces and does not include advanced diagnostic tools, configuration tools, or maintenance tools. There are several architectures for the user interface worth discussing here. As software and hardware systems have evolved over time, the reliance on customized solutions has changed. Stand alone, hardware-based solutions have given way to more distributed, open, and flexible solutions. Here are a few system architectures to be aware of. Client Server - In this architecture there is a central server with a host application typically running on an IT managed computer server located in a dedicated IT room. Client applications are deployed to any workstation that requires access to the server and the server's data and user interface. There are two types of "clients":
- Thick Client - A thick client is an application that is loaded onto the computer workstation and communicates to the server in order to render information to the user. Thick clients require continual management and administration at the workstation. These clients are typically vender specific and require licensing and potentially annual service contracts. Thick clients may also store site data locally on the computer workstation as well as on the system server. Modern systems are moving away from thick clients as they are more costly to maintain, require additional administration, pose greater cyber security risks, and don't allow any workstation in the building to provide an operator user interface.
- Thin Client - Think clients are more acceptable where any operator workstation with a standard, open suite of applications can access the server and render information to the user. Think clients such as standard web browsers, sometimes with required browser "add-ons" are a more acceptable platform for client server user interfaces. Thin clients do not store much or any data locally on the workstation. However, certain graphics, images, and other information may be "cached" or stored locally to speed up the graphical

rendering. For example, the large image of an air handler, which does not change, may be cached locally so that when an operator selects that graphical page, the image loads quickly from local memory. However, the data on the page such as temperatures, pressures, etc. are sourced from the real-time data from the server. A balance between local cached information and that downloaded from the server is required in order to provide a smooth and responsive graphical user interface system. Stand Alone Application - This is a solution where the supplier requires an application and its interface to the control network be installed on every workstation requiring access to the user interface. Common standalone applications are provided for system diagnostics, controller programming, system configuration, and more. These applications are well suited to run on field enabled laptop/notebook computers so that technicians have access to the interface while working directly on equipment. However, these applications are typically not the primary interface to the building operations team. They are removed from the system once their tasks are complete. Sometimes these applications require custom drivers and interfaces to comm ports, USB ports, WIFI, or Bluetooth interfaces to equipment. Data Storage/Management - All user interfaces must reliably access and display information sourced from the control network. The control sensors and actuators report their data across the control system to the BMS front end application (assuming a client/server architecture). The BMS application requires a system database be included and available for access by any client. Clients may be the BMS front end Graphical User Interface or any other API that requires data to perform its function. The storage and administration of that data is part of the BMS front end's role and a project may require drivers such as MQTT, SOAP, RESTful, web services, or other types of interfaces to that data. When selecting a BMS front end and the software and data architecture that support is, it is important to define all of the application interfaces required, not just the GUI for the BMS operator. Applications such as system analytics, fault detection and diagnostics, computer maintenance and management systems (CMMS), and others all require direct access to the system data and are often directly integrated into the BMS platform by the DIV 25 contractor. Server Location, Maintenance, and Support - There are several options for where the physical server is located. It can be on site in an environmentally controlled IT equipment room. In a remote owner-maintained data center, or in a 3rd party cloud-based data center. There are pros and cons for each option and this should be discussed with the design team. General best practices say to keep the intelligence at the point of control, meaning, keep the BMS server and its user interfaces as close to the actual equipment and building network as possible. Often the BMS front end is involved in real-time monitoring of alerts, alarms, and equipment status. Building equipment failures can have a direct impact on the health and safety of the building's occupants. Depending upon the type of facility, there can be strong justification for having a full-time building operations center with 24/7 staffing to ensure a high degree of reliability and maintenance. Less critical facilities can justify having the BMS server located in an owner managed data center or in a cloud/3rd party managed data center. A risk assessment should be developed by the owner and the design team to develop the right strategy for the project. The general maintenance and support of the server all factor into the decision process. If the owner is to maintain the server and its supporting hardware and software, then the owner must employ or engage the services of qualified personnel who can manage backups, software updates, security patches, and the like. If the server is managed by a 3rd party and these functions are part of the service contract, then the owner does not have be engaged in the process. However, the manager of the data center may take the BMS server offline at any time to provide

maintenance, which would interfere with the real-time monitoring of the facility. This can also cause loss of trend data, synchronization issues, and delays in graphical interfaces. Owners should evaluate the pros and cons for their particular situation. Database Development and Interoperability - One of the primary functions of the BMS server is the development of the site BMS database. This database contains a virtual repository for all of the physical sensor and actuator values including both current value and historical logs as well as all of the logical data values used by the control systems. Building the site database requires knowing all of the network-available data points, their object types, units, and all related semantic information. This database is sometimes referred to as the "data lake" or "digital twin". Open, interoperable systems require that this BMS database be designed and implemented such that any application or application interface (API) be able to access the database. There are many ways this can be achieved using standard protocols, drivers, or custom interfaces. The key here is knowing what the scope and desired outcomes are for the BMS server. The more flexible and adaptive the server database is the more useful it will be to the owner and the owner's representatives.

Advantages of a SPoG:
- One place to look for everything.
- One login gains access to all (permitted) systems and information.
- Administration of user access and permissions can be all in one place and defines who sees what and who can modify what, based upon the owner's criteria.
- Data from multiple systems can be viewed and mixed together easily. (Check how well your SPoG can do this.)
- A good SPoG should be flexible enough to be tailored for different operation functions.
- A good SPoG should be flexible enough to allow for the addition of future requirements that an interoperable solution would enable.
- Best Practice: "Light and Loose:" One strategy for connecting digital systems together is to be "light and loose," rather than deep and complex. So, while interconnections between systems enables new functionality that is the point of a smarter building, too many interconnections can be paralyzing to set up and to maintain. Minimizing how many data connections there are, and how many dependencies there are from one system to the next, allows things to work easier, at set up and over time, especially when one of the component systems is updated (which will be often, and usually without regard for how other systems might use that data).
- A "light and loose" SPoG can report on a limited set of data (often called key performance indicators, or KPIs), while also providing links and views into component systems for deeper looks at data and to use component system functionality. Disadvantages of SPoG:
- May require custom software development (and upkeep).
- Check how "standard" your vendor's SPoG offering is, how much you can customize views and functionality to fit your needs, and how the UI is kept current with changing devices, operating systems, APIs, etc.

- Practicality, budgets, and vendor willingness to support the SPoG may limit the capabilities.
- Single point of failure: Updates to or problems with component systems can interrupt how the rest of the UI works (depending on how light vs. deep certain connections are.) The system architect may consider keeping certain sensitive systems separate (or access limited).
- SPoG interfaces may be designed as "monitor only," but this is a design choice and not a technology limitation.
- Single-sign-on may not be available for all relevant systems.
- Can take a long time to specify all user roles and requirements.

## 30.3 General Requirements for Interfaces

Whether you decide you need a SPoG, or are better served by (or just need to have) multiple interfaces for your smarter building, there are some common interface requirements that are best practices/recommended/good to ask for:

### 30.3.1      Key objectives are to deliver information to users using easily accessible
platform(s):

- **A.** The user interface of all systems will be delivered on current versions of web browsers (without a specific plug-in, add-on, etc.).
- **B.** The user interface of all systems will be available on mobile devices, either via a mobile web browser or via a specified mobile app. If a mobile app is specified, it should be available for both iOS and Android devices, through the respective mobile platform's app store.
- **C.** The interface for select systems will be a digital twin model, available to appropriate users via a web browser, a specific desktop app, a mobile app, or embedded within the SPoG graphical user interface.
- **D.** The web-browser-based UI will be kept up to date with browser updates, and mobile app UIs will be kept current with mobile OS updates, within [xx] days of updates being published.
- **E.** The user interface shall meet the owner's requirements for the layout, style, color-coding, presentation, naming, tagging, access control, and related user interface requirements. Typically, this information is provided in an OPR - Owner Project Requirements document. Ensuring these requirements are met provides greater operational efficiency by staff interfacing with multiple UIs across a single building, a campus, or an enterprise. Also helps with training and staff transportability.

### 30.3.2      UI Network Access

- **A.** UIs delivered via web browsers, mobile apps, or machine-to-machine interfaces require secure interface and access to the site IT network and should follow guidance according to requirements in sections 25.25.90 Networking and
### 25.25.95 Cybersecurity

- **B.** There are multiple options for how UIs connect to the owner's network. A few considerations include:
  - **B.1.** Will the UI and its associated computer server and user interface be by a web browser that requires securely access pages on the public Internet?
  - **B.2.** Will the UI be stand alone and isolated from the public internet?
  - **B.3.** Will the UI have a VPN connection to a remote server? Based upon the answers to these questions, the system designer will need to account for access restrictions and requirements, IP network pathways, security, and other related factors.

### 30.3.3      Consistency in the Presentation of UI Elements (naming, color coding,
structure, etc.)

- **A.** Define a naming and tagging convention for use within the facility and for use by all suppliers.
- **B.** Include definitions for abbreviations and acronyms.
- **C.** Define a standard color coding for user interface graphics (piping, wiring, air, water, steam, gas, etc.)
- **D.** The owner should have a consistent naming framework as part of the Owner's Project Requirements or the Building Controls Framework and should be used by all contractors, suppliers, and consultants.

### 30.3.4      User interfaces should use the same naming convention that the physical
devices use. There should be consistency between the internal database(s) and control network data object naming, and all API naming and tagging. Administrator Users

- **A.** Admin users will have permissions to all administrative functions for any central interface and all of the component applications. (See also sec 95)
- **B.** Do you also need to have separate admin roles (and permissions) for different apps?
- **C.** Admin users will be able to control what is viewable/controllable by any given user.
- **D.** Admin user credentials are required to on-board and off-board general users.

### 30.3.5      Users will be able to access information securely via a single sign-in.

- **A.** Pro Tip: This sounds great, and is something to shoot for, but implementation may be complicated by: (a) whether component systems can handle single-sign-on; and (b) whether user profiles and related permissions are sync'd from one app to the next.
- **B.** Common methods for implementing single-sign-on include OAuth and LDAP. (See also sec 95)
- **C.** Will the user interface automatically log off after a timed period inactivity?

### 30.3.6      User interfaces will be accessible by users regardless of their current
location.

- **A.** This enables mobile and remote access to the smarter building.
- **B.** Alternate: for security reason, some projects may require that user access be limited to when a user is on premises via a dedicated workstation.
- **C.** Dedicated workstations may be required in certain situations as they may be directly connected to the OT building controls network rather than the owner's IT network. Cross-over network access may be restricted or not present.
- **D.** Requiring a VPN for site-to-site access can be a good mechanism to manage cybersecurity. This is beneficial for campuses that don't have direct physical network cabling to all buildings. The owner's IT group is then responsible for setting up and maintaining the VPN, however, specifications for which user interface applications and workstations require VPN access are the responsibility of the system designer and the DIV 25 contractor. Once a VPN is set up, the owner can grant access to contractors, suppliers, and other 3rd parties allowing them access only to specific network locations and applications.
- **E.** In some cases, remote or mobile user access might make sense only for select systems or functionality. However, once your interface(s) is Internet-connected, anything less than "all mobile access" can be complicated to design and implement.

### 30.3.7      New users will be provided with access to the information they need via a
documented process.

- **A.** Documentation is key to being able to onboard new users, troubleshoot issues, and fix larger problems.
- **B.** Pro Tip: You can ask for it, but full documentation of all processes is hard to get and may be expensive to provide. Providing a contractor "check-list" of OPRs relating to documentation deliverables is a good way to help ensure project close-out goes smoothly. Additionally, the development of project documentation should continue throughout the project, be reviewed periodically, and signed off during different project phases. Leaving all the documentation to the end will cause turn-over and commissioning delays.

### 30.3.8      Information required by users will be provided via a digital mechanism such
as secure API so that future user interface technologies such as AR/VR can be provided.

### 30.3.9      All Applications listed under 25.25.40 shall be able to be delivered to users
subject to their role and security credentials as established by the site admin.

### 30.3.10     All Data managed by systems listed under 25.25.60 shall be accessible by
users subject to their role and security credentials.

### 30.3.11     Data pertaining to multiple different systems shall be viewable on a single
page or in a unified view, in accordance with the needs of users. Examples

include a single user interface page with all equipment alarms across all subsystems. Energy management data is also a good example of cross-domain user interface page (See SPoG section above to check if this is what you expect).

### 30.3.12     Some user interface applications may have the ability to allow internal
communication between users to, for example, escalate an alarm from a junior tech to a senior tech to, perhaps, process or authorize a work order. Internal user-to-user messaging may be a "nice-to-have" feature, but may not be practical or required for all projects.

### 30.3.13     User interface hardware and data exchange with items in sections 40, 50, 60,
and 70, will follow open standards when possible.

## 30.4 Defining Multi-System Views and Interface Functionality

Whether you use one unified SPoG, or multiple UIs, an important advantage of a "smarter" building that has multiple systems connected together is being able to see and interact with data from those multiple systems at the same time. Some multi-system functionality will therefore need to be developed as applications separate from, or "on top of," dedicated system apps. If section 40 - Digital Applications defines such "multi-system" apps for the project, this part of section 30 is where the requirements for displaying these "multi-system" apps would be defined and explained. An example of a SPoG with multiple applications is when one BMS front end embeds another application within it. This "windowing" is a common mechanism to merge multiple applications into one SPoG. There are multiple ways this can be done. One common mechanism is for the BMS front end to have embedded "hot links" via standard HTML5 web services. So, it looks like you've never left the "container application" - the BMS front end, but the data is being served by a separate application. It is all transparent to the user and can provide a wide variety of services all within one container. A second model is where one application makes an API call to another application to fetch data, the displays it in the native visual interface. Refer to section .40 for more information on digital applications. The specification should define how and what is needed here. The Division 25 contractor may be required to install add-on software, enable specific functionality, or work with 3rd party suppliers to provide this integration. In the end, it is highly beneficial for the owner's staff to have as much integrated into the daily workflow applications as possible. A simple example of this is an email user interface and a calendar/scheduling application integrated into one UI. As an example, a facility energy manager may wish to see both the energy consumption of the HVAC system combined with the solar PV generation on the same screen, but both data sets are sourced from different applications. Data integration between vendor systems is now very practical and achievable using standard API interface such as MQTT, RESTful, OPC, OBIX and other platforms.
