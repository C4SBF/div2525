# 25.25.70 - Control Systems
This section defines the control systems directly connected to the physical elements listed in section 25.25.80, and that provide "built in" controls and automation, and/or the digital communication bridge to other components of the same system, as well as to other systems, applications, buildings, or entities outside of the portfolio. The control system may be referred to as the Building Automation System (BAS) and, based on the ASHRAE Guideline 13, include Tier 2 infrastructure equipment and their controllers, and Tier 3 packed equipment with embedded controllers, programmable controllers, and supervisory controllers. The control system includes those components that ensure the building's control sequences of operation are met. Often the BAS networked controls can run autonomously from the BMS front end and along report to the front end for alarming and event management. Some vendors lump the BAS and BMS into one solution. For the discussion in this framework, we separate the two to be more in line with ASHRAE and provide more clarity for specifiers. Topics include:
- List what control systems are included. For your project, use this section to define (list) the control and automation systems that connect to the physical devices (identified in section 25.25.80) and that provide "built in" controls and a communication bridge to other components of the same system, as well as to other systems, applications, buildings, or entities outside of the portfolio.
- Define what each needs to do to work with other systems (following requirements of sections 25.25.50 and 25.25.60 above) to deliver the intended smarter building functionality. This includes interoperability requirements common to all control systems and interoperability requirements that might be specific to an individual control system. These can include:
- Define data required for meeting multi-system sequences of operation.
- Define any control system platform requirements for interoperability.
- Define how each control system supplies data to higher level applications.
- Define any system-to-system integration requirements.
- Define what each needs to do to run the physical layer below it. For this, it's ok to reference sequences of operations defined in another CSI division specific to certain equipment.

> **Expert Tip:** You can think of the systems and equipment identified in sections 25.25.70 Control Systems and 25.25.80 Physical Elements as needing to run "on their own" in order to meet the building's basic operations. In other words, if the "smarter building" applications and communication didn't work (because Internet connections were down, or an app was offline), the building should still operate "in normal mode." Designing the control system with the "Intelligence at the Point of Control" using a distributed architecture will help remove single points of failure and over-reliance on higher level applications and networks. Remote visibility and control, and higher-level automation might not work, but basic building operations like doors opening and locking, lights can be turned on and off, there is heat and air conditioning, etc., would.

## 70.1 Which Control Systems are Init cluded?

For your project, use this section to list the control and communication systems that provide "built in" controls and that connect the physical components to the digital network. Make a list, ideally coordinated with the components list in section 80. Examples include:
- A Building Automation System (BAS) that controls HVAC equipment.
- A lighting controls system.
- A fire alarm control panel.
- A set of power/electrical panels with a supervisory controller aggregating submetering, quality, and other useful data and performing backup generation coordination.
- A refrigeration panel and supervisory controller for multiple coolers, freezers, cases
- A solar inverter(s) interface panel and supervisory controller providing power information from PV and batteries and managing co-generation and other DERs.
- An edge control panel (PLC) for a specific device

## 70.2 Requirements for Control Systems to Work with the Smarter Building

All the control systems specified for your project will need to adhere to requirements that will enable them to operate as part of the smarter building. You can organize requirements for interoperability based on which are common to all control systems, and which are specific to an individual system. The following list is an example. All of these are not necessary for ALL projects. Your list may be different.

### 70.2.1      Common Interoperability Requirements

For this project, all systems should comply with:
- **A.** Exchange of data between field device networks to use open protocol standards that maintain interoperability.
- **B.** Data shall use models that are open, standardized and allow access to web services that allow for accumulation and storage as referenced in section
### 25.25.60 Data.
- **C.** Control system applications shall support portability.
- **D.** Control system applications must be interoperable and, where practical, self-installing.
- **E.** Communication channels shall use standard media to facilitate data transfer. Such media can utilize (your spec should specify which are acceptable): - Twisted Pair Copper Wires (RS-485, Free-Topology) - Multiple Twisted Pair Copper Wires (Ethernet) - Power Line Wiring (HD-PLC) - Fiber Optic Cable

- Radio Frequency (450 kHz to 300 GHz fixed, multi-band, and frequency hopping) - WIFI - LoRa - Zigbee - zWave
- **F.** Hardwired connections to equipment and devices will utilize established industry standard plugs and terminals that provide mechanically secure and long-term reliable contacts. Wired connections shall not emit electro-magnetic radiation that exceeds authorized frequencies and transmission power levels specified for the project's geographic region.
- **G.** Wireless connections will communicate over authorized frequency ranges and transmission power levels specified for that geographic region.
- **H.** Control signal connections will not be placed in close proximity to power cables such that interference, noise, and transients are introduced onto the control signal communication that may disrupt or prevent reliable data transmission.

### 70.2.2      System-Specific Interoperability Requirements

The following control systems have interoperability requirements specific to each, as noted. Your document will be longer here because you will fill in the details for each system. This section lists requirements for each system to interoperate with other systems, in addition to the common requirements in the preceding section. Each system has other requirements to perform the control and operations of its component equipment, and those are described in the specification division for each system (such as Division 21 Fire, Division 23 HVAC, Division 26 Electrical, Division 27 Communications, etc.)
- **A.** HVAC BAS System
- **B.** Lighting Control System
- **C.** Water/Steam/Boiler Control System
- **D.** Access Control System
- **E.** Elevator Control System
- **F.** Electrical Control System
- **G.** Solar/Generator/DER Control System
- **H.** EV Charging System
- **I.** Refrigeration Control System

### 70.2.3      Requirements for Control Systems to Independently Run the Physical Building

At a higher level, more sophisticated projects may require articulating what needs to happen WITHOUT the smarter building technology. Sometimes Internet connections go down, unified dashboards have issues, and mobile apps don't work. So, it is useful to define which building operations must work independent of whether the smarter building higher level functions are working.

Use this section to identify the basic building operations that are required to work in the event that higher level smarter building functionality isn't available. To think this all the way through, follow the following steps for your project:
- **A.** Define desired conditions and systems that require no intervention needed from within the internal and external spaces. Samples include:
- Fire alarm system must be fully operational.
- Fire suppression system (e.g., sprinklers) must be fully operational.
- HVAC smoke evacuation system, triggered by the fire system, to work independently and be fully operational.
- Emergency exits must always operate.
- Exterior and interior doors must be accessible for egress and ingress.
- Lab pressurization must be maintained.
- Gas sensor alarming system (refrigerant leak detection, H2S, SO2, VOC and other toxic sensors) must be fully functioning independent of any other system.
- **B.** Define desired conditions and systems that will work based on manual intervention from within the internal and external spaces. Samples include:
- Emergency power (generator or battery system) must be able to be turned on and off manually.
- Exterior doors must be lockable and unlockable.
- Elevators must function manually and in fire-support mode.
- Hot water heaters must function, at least manually.
- The building must have heat, equivalent to fully occupied and fully unoccupied (off-hours) modes.
- Lights (perhaps only in specified areas?) must be able to be turned on and off via manual switches or circuit breakers.
- **C.** Define desired conditions that allow for automated processes to provide intervention within the internal and external spaces. (This is when your building operates as a smarter building.)

### 70.2.4      Network Infrastructure

The control systems will require specific network infrastructures for their installation and operation. While most of the details regarding the network for communications is typically covered in Division 27 Communications, it is good to address any specific requirements for the smarter building in Division 25 (using section 25.25.90 Networking). For example, BACnet IP requires that all devices that will communicate with each other exist on the same subnet. If not, them more complex "routers/bridges" are required to bridge two subnets - something to avoid if possible. A good network diagram capturing all of the wiring, pathways, connections, ports, and equipment will help all project team members efficiently and effectively provide the network backbone.

Network infrastructure drawings typically provide very sensitive detailed data about the facility such as MAC addresses, IP address, locations, and functionality. These drawings and documents should be labeled sensitive and be tightly controlled. Bad actors may use this detailed information to access the control network. See the Cybersecurity section for details. The control networks will typically require a lot of wire. Understanding the wiring, cabling, cable tray, panels, ports, and rack requirements is, again typically a Division 27 and sometimes Division 26 section, but the Division 25 spec must include the overview architecture, responsibilities, and connectivity of all control network elements. Coordination between the parties is very important. Specifiers may opt to include the same information in multiple divisions and identify the primary and secondary responsible parties. Duplicating information in specifications is acceptable as long as the divisions of responsibility are clearly identified. Using the phrase, "installed by others" and then identifying the contractor or division is very appropriate.
