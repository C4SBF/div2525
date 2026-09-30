# 25.25.20 - Operating Roles & Responsibilities
This section is about Who will be expected to interact with the applications, data, and systems in the smarter building, to achieve the Purposes (goals) laid out in section 25.25.10. This section can also be used to outline the operational processes, in a list or task flow chart(s), that each group is expected to follow to achieve those goals. And finally, this section can connect the people to the processes by specifying roles, responsibilities, job descriptions and career paths (usually for staff) and training requirements (for any user group). To provide a clear picture of who will be expected to interact with the smarter building, this section outlines the following steps:
- Define the Users of Your Smarter Buildings
- Define Responsibilities, Job Titles, and Training Needs (if applicable)
- Define the Process Each User Group is Expected to Perform

## 20.1 Define the Users of Your Smarter Building(s)

"Who" can be generally broken down into three groups:
- Owners. The people who own the property or are designated to act on the owners' behalf. Can include C-suite executives, governing boards or committees, portfolio managers, and project managers.
- Operators. The people who run the building(s) and portfolio, including property managers, facilities personnel, production staff, and (don't forget) the system administrators. Often there are both internal (staff) roles (by department or function) and external (vendor provided) roles.

A subset of the Operators includes the contractors, consultants, and specialty service providers who support the facility and play a vital role in the continuous operational maintenance, and management of the building. They may have special access credentials, job-specific tools, and requirements for accessing the systems they maintain. There will likely be external, internet-based tools and access required for off-site tools and applications requiring well-defined roles and responsibilities for access the data and systems.
- Occupants. The people who use the building, either in a role internal to the organization (non-facilities staff, employees, or students) or external (visitors, customers, general public.)

## 20.2 Define Responsibilities, Job Titles, and Training Needs (if applicable)

A well-prepared Owner's Requirement Document or Specification will outline the specific roles, job titles (as applicable to staff or vendors), areas of responsibility (and possibly specific tasks) each user group would be expected to perform, training needs and methods to be delivered for each group, and an org chart to depict the relationships among the different users.

The owner will typically have many user groups that will provide input on the owner's requirements including the IT group, facility maintenance and operations, and many types of process, office, clinical, educational, and human resource staff. It is crucial to get input for all of these groups into the owner's general project requirements. This may include requirements for certain data sets being made available to non-OT teams or the BAS needing to interface to certain process or clinical equipment.

> **Expert Tip:** Managers of some projects find it useful to create an Operational Responsibilities Matrix, similar to the Contractors' Project Responsibilities Matrix, but focusing on who is expected to do what in terms of interacting with the smarter building, when the building is operating.

*Figure 3. Sample Operational Responsibilities Matrix*

**10 MAIN STREET OFFICE BUILDING - SMARTER BUILDING OPERATIONAL RESPONSIBILITIES**

| Task | Owner - Portfolio Manager | Operator - Facilities Manager | Occupant - Tenant |
|---|---|---|---|
| **ESG Reporting** | Approve and submit annual local disclosure report. | Monitor monthly utility bills and EnergyStar scores. | Read/consume latest ESG scores via building website or app. |
| **HVAC Control** | | See, control, and troubleshoot HVAC, in-person (at equipment) and via mobile device. | No direct settings available. |
| **HVAC Comfort** | | Manage comfort issues submitted by tenants. | Building will automatically know when I am in, what spaces I use, to set HVAC. Report comfort issues via building app. |
| **Etc.** | *(add as many rows as necessary)* | | |

In addition to an operational responsibility's matrix, developing a Project Delivery Responsibility Matrix will similarly help all stakeholders define and understand their scope, roles, and responsibilities. This significantly reduces the eventual finger-pointing during construction on a project. This matrix should include:
- Basis of Design - Owner Project Requirements, Frameworks, Playbooks, Standards
- Design Phase - Including Engineering, Equipment Selection, Data Set Requirements, Points Lists, Network Infrastructure, Connectivity, and Interoperability

- Implementation Phase - Including Installation and Integration and the BMS Integration and Programming
- Commissioning and Handover - Including documentation, drawings, points list, tagging sheets, and database files
- Warranty and Maintenance
- The typical stakeholders include:
- Consulting Engineer
- Owner's BAS representative
- General Contractor
- Architect
- Master Systems Integrator
- Mechanical
- Electrical
- Communication
- Structured Cabling
- Other specialty subcontractors
- IT/Cybersecurity
- Facilities Management and Engineering
- Security
- The project responsibility matrix typically includes all of the physical and logical components and interconnections required for the project. It includes:
- DIV 22 - Plumbing
- DIV 23 - Mechanical/HVAC
- DIV 25 - Integrated Automation
- DIV 26 - Electrical
- DIV 27 - IT Structured Cabling
- DIV 27 - Communication/Teledata
- DIV 27 - Audio/Visual
- DIV 28 - Electronic Security and Physical Security
- DIV 34 - Transportation
- Other specialty systems (Solar PV, EV Charging, Backup Generators, etc.)
- Furniture, Fixture, and Equipment (FF&E)
- Construction Administration Note: Some elements of a project have multiple stakeholders involved and must clearly define who is in charge of what. An example is designing and installing the OT IP backbone

infrastructure of a building. This typically includes a DIV 27 low voltage wiring contractor to design and install the wiring (Ethernet, Fiber), the owner's IT group or consultant/contractor that configures the OT IP network and provides and installs the equipment such as switches, routers, patch panels, etc. It may also require the DIV 25 contractor install software on the BMS server, assign IP addresses, set up all of the required integrations, and test all of the data pathways. The DIV 25 contractor may also be engaged in defining the "spots and dots", the location and quantity of all of the OT equipment requiring Ethernet connectivity. Regarding staff training requirements, specifications should define all the training required and the mechanisms that this training should use. This includes hands on and classroom training. Consider requiring that all training be recorded and delivered as MP4 videos for archiving. More complex facilities may want to ensure these training videos are accessible from the BMS server for use by any authorized person. Very long training videos should consider requiring the use of indexes and tables of contents to help personnel find the information they need rapidly. Of special interest in the context of networked data systems is the training on how and where information is stored, the backup and restore routines, any required scheduled maintenance, server software monitoring and maintenance (patch files, security updates, user credentialing, and more).

## 20.3 Define the Process Each User Group Is Expected to Perform

A well-prepared Owner's Requirement Document or Specification may also include flowcharts to illustrate the processes that the smarter building system will support for each user group, putting the responsibilities listed above into context in relation to how the data flows and what other users do. Process flow charts are especially useful to illustrate how and when users need to interact with digital information from the building, which is the basis for defining the requirements for Delivery (sec 30) and Applications (sec 40). This also may include details about the data source, structure, context, semantics, rate of update, and who and how the data is to be used. Applications that may use the data may come from an operational/maintenance application interface, from 3rd party analytics application, or from energy management and optimization application. The users of each of these applications vary substantially but all are sourcing the same network and the same data, just using it in substantially different ways.
