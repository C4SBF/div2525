# 25.25.40 - Digital Applications
This section is about the software applications that use data from the building and external sources to provide actionable information to the user. It identifies the applications that are part of the smarter building functionality, lays out how those applications are to co-exist within the building environment, and explains how data is retained and used by the applications. The application layer should provide software developers with the key requirements for developing interoperable, multi-system applications. This section discusses:
- What is an Application in the Smarter Stack?
- Identify Which Applications You Have and Which Applications You Need
- General Requirements for Applications
- Examples of Single-System Digital Applications
- Examples of Multi-System Digital Applications
- Digital Applications Do Not Include...

## 40.1 What is an Application in the Smarter Stack?

Applications make up the 'intelligence' layer of the Smarter Stack, manipulating data, transforming it into useful and actionable information, providing control logic, business intelligence algorithms, machine learning, administration of systems, and additional management capabilities. Digital applications typically monitor and/or manage one or more systems that help a building operate the way it is intended. Applications can run specific systems, can integrate across multiple systems, or might be required for the operation of the building (per sections 10 and 20), but not be tied to a specific system. Sometimes what people commonly call applications or "apps" (like on their smartphones) wrap together a lot of the layers of what we refer to as the Smarter Stack (from connecting to devices, to data storage, to business intelligence, to user interface) to perform a specific function. For the purpose of this DIV 25.25 Framework, we are using "application" to refer only to the layer where data is manipulated and transformed into useful and actionable information or where it is directly involved in the sequence of operations of a single system or of multiple systems. Where the data comes from (70, 80), how it is stored (60), how it is accessed (50), and how it is displayed (30) are covered in their respective sections. If devices are connected and data is exchanged well, per sections 50, 60, 70 and 80, the Application layer may be the most creative layer of the Smarter Stack.

## 40.2 Identify Which Applications You Have and Which Applications You Need

A well-prepared Owner's Project Requirement document and the BAS designer's Project Specification can use this section to identify all the digital applications that are expected to run

the building(s) and how they work with each other to deliver the desired smarter building functionality. It is recommended that the process of identifying all the needed applications follow four steps:

- **1.** Inventory all the applications, existing and planned (if new construction or adding systems)

- **2.** Identify the key things each application does to fulfill the Required Outcomes (operations model and occupant experience outcomes identified in section 10, delivered to users identified in section 20, via UIs identified in section 30).

- **3.** Define the key data each application creates and requires (in line with section 60)

- **A.** Identify the key data sources for each application, which could be from controllers in the building, other building applications, the BMS front end, or third-party external sources.
- **B.** Define the application interface requirements, protocols, rules, and methodologies.
- **C.** Identify any application network access requirements, permissions, dataflows, data usage expectations.
- **D.** Identify any custom integration requirements for each application (i.e., scripting, rules engine development, data transfer interval configuration, etc.).

- **4.** If the existing applications do not deliver what is needed, then look at integration needs and opportunities to create new applications. It is preferred that any new applications should use standardized data available from section 50.

Here are some examples of applications and their data sources:
- Energy Management - Data sources: Real time utility meter data, historical utility meter data (imported from utility feed), networked submeter, internal equipment controller with internal CTs (current transducer used for power/energy calculations), electrical panels with CTs measuring specific circuits and plug loads (often used for high energy usage equipment).
- Automated Fault Detection and Diagnostics - Data sources include field equipment and controllers across multiple subsystems.
- Centralized Alarm Management and CMMS Interface - Data sources include networked sensors, actuators, and embedded controllers, programmable controllers, and supervisory controllers across multiple domains.
- Scheduling - Data sources include external IRTC (internet real time clock web services) used for time synchronization, master schedule database, local and regional offset databases, and supervisory controller data (such as override and local scheduling rules).

- DER (Distributed Energy Resources) and Load Management - Data sources: Solar PV Inverter, standby and co-generation equipment, power monitoring equipment, load shed/automated demand response signals from utility, onsite real-time energy demand, weather data from internet sources, building weather station, equipment and controller with setback and load shed mode control, and more.

## 40.3 General Requirements for Applications

Common requirements that all digital applications in your Smarter Stack should include:

### 40.3.1       Applications will have the capability to provide all user interfaces (UIs) with
setup, configuration, operation, etc., as per 25.25.20. (Reference assumes these requirements are described in 25.25.20.)

### 40.3.2       Applications in 25.25.40 are to be installed/removed with minimal impact to
the overall building operations and tenant experience (unless, of course, the application is directly integrated with a building subsystem's sequence of operation, safety systems, or other integrated operational system).

### 40.3.3       Applications will have the capability to retrieve data from other applications
and systems as per 25.25.50.

### 40.3.4       Applications will have the capability to store and share all their data as per
25.25.60.

### 40.3.5       Applications will store their data in open, standard database formats such
that other applications can read and write to the application's database. This may not be practical in all scenarios, however, the more open the application's database, the smarter the building becomes.

## 40.4 Examples of Single-System Digital Applications

Some examples of single-system digital applications include:
- A mobile app reporting on indoor air quality, fed from data collected by IAQ sensors
- An application that pushes new firmware to a set of controllers within a building or across a portfolio
- A supplier cloud-based application that captures runtime, event, and error log files for controllers to help improve product reliability and functionality.
- A building HVAC automation system that controls the chiller plant and multiple zoned HVAC systems (multiple controllers but all still HVAC)
- Individual AV systems in different conference rooms
- Lighting system processors which in turn manage the lighting sub-systems in different rooms and zones.

## 40.5 Examples of Multi-System Digital Applications

Digital applications also can exchange data with other digital applications. This multi-system exchange enables outcomes that one system cannot provide by itself. Some multi-system applications have a 'closed' data architecture making it difficult to exchange data with other sources and systems, and others have more open data exchange capabilities. To facilitate the best outcomes and be ready for future opportunities yet to be invented, best practice for smarter buildings is to have applications that can store and exchange standardized data and information as openly as possible. This may require that specifications define how data is to be exchanged and restrict the usage of proprietary protocols, proprietary databases, and undocumented interfaces. Examples of multi-system digital applications include:
- Computerized Maintenance Management Systems (CMMS) that tie together work order ticketing and inventory supply management.
- Energy Management Information Systems (EMIS) that summarize, analyze and manage utilities utilization, such as electricity, oil or gas fuel energy, and water use.
- Digital Twin applications to create a virtual digital model with the real-life building data. Digital Twins can be utilized to optimize building operations and utilization as well as greatly reduce operational cost across a portfolio.
- An analytics tool that consumes data from controllers, monitoring/status applications, and other sources to provide dashboard interfaces and insights into predictive maintenance.
- Backup generators that work in tandem with key critical load applications to manage power outage recovery.
- An organizational calendar (such as Outlook or a room scheduling application) for people and spaces can be utilized for automation, operational, and tenant experience required outcomes, such as:
- Energy efficiency and automation of access, HVAC and lights around occupied / unoccupied spaces.
- Occupant experience - having rooms "know" when spaces will be utilized and preparing the room for use beforehand.
- Operations requirements - enabling building staff and occupants to automate systems purely by scheduling a space for use in the calendar.
- Calendar integration applications in a convention center example, utilizing the event calendar entry and the estimated number of attendees to manage:
- Pre-cooling to the desired set point - The number of attendees can be shared from the calendar application. Based upon an average BTU per person, the anticipated increased heat load on the space can be easily calculated. With the additional heat load, the room can be pre-cooled to a set point below the desired occupied set point, so, when occupants come into the space, the room temperature will equalize to the desired set point.
- Indoor Air Quality - This can also be useful for managing air changes per hour based on actual occupancy levels, CO2 sensors, and predictive duration to ensure a healthy building.

- Lighting - The space can have brighter "work lights" active if the space is occupied before or after the calendar event. For a set amount of time before and after the scheduled calendar entry, the room can recall an occupied "event" lighting scene. Outside of those two considerations, only emergency lighting will be on and additional lighting can be turned on based upon occupancy for occupant safety.
- Audiovisual Systems - Similar to the lighting system, the sound reinforcement and background music systems can automatically turn on and off at a preset time before and after the scheduled event in the space.
- Refrigeration Systems - A supervisory software application coordinating the defrost cycles of multiple refrigeration/freezer equipment to ensure load balancing and product safety where the electrical power system plays a key role in ensuring no defrost schedule will overload any one electrical circuit and that load shedding/energy management applications can interact with the defrost schedule. Digital applications are part of the foundation of AI applications where real-time and historical data are combined with operational trends and occupant usage patterns to optimize control strategies. While we most often hear of AI applications to manage energy efficiency, they can also manage occupant comfort and performance, predictive maintenance, optimized scheduling, optimized work order flow, and much more.

## 40.6 Digital Applications Do Not Include...

It is important to recognize what digital applications for this section are NOT designed to do. These most often fall into supplier/vendor specific applications for managing their devices independent of outside input. The functionality these applications provide is discussed more in section 25.25.70 Control Systems. Some examples of these applications include:
- Controller programming and application configuration
- Applications that log usage data from controllers
- Supplier-specific automated firmware update applications
- Supplier-specific maintenance applications
- Diagnostic applications
- System-specific user interface applications - typically for advanced system insights, setup, configuration, etc. As with other subsections of Division 25.25, in order to describe all the requirements needed for the project, the Owner's Project Requirements doc (and potentially any project Specifications) would need to include sub-sections for each digital application/system in which requirements specific to that application/system are listed. This could involve a lot of work and many pages to be complete, and is not shown in the summary outline above. This version of the Framework document includes examples of application-specific requirements in the Appendix.
