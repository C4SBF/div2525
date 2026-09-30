# 25.25.95 - Cybersecurity
This cross-cutting section discusses risks, assessment strategies, and design of cybersecurity best practices for OT systems. This section presents basic, moderate, and advanced suggestions for managing cybersecurity risks both at the physical security and the logical security levels for OT building systems along with guidance for working within and alongside IT based infrastructures. Do I really need cybersecurity for my building systems? In today's connected world, building Operational Technology systems are subject to the same cybersecurity threats as IT systems. Whether your building or all of its systems are 'smart' and connected to the Internet or not, data accidents can happen, and bad-intending actors can try to digitally plug into major devices and software systems, and cause problems. The impact of these threats differs in the fact that OT systems are responsible for controlling the mechanical and electrical systems within a facility, in addition to the potential for data loss. For your IT systems, cybersecurity threats must be managed continuously reflecting the changing nature of the threats and the major risk coming from the users themselves. It is no different for OT systems. In addition to the typical IT related threat vectors, OT systems pose an increased risk for disruption to the physical building. Bad actors can disrupt or damage a facility if they can get access to the control system. Control systems in general should be designed to have fail-safe conditions as part of their underlying design. No controller should be allowed to have a networked message with a data value change that would put the system under control into any unsafe condition. For example, you would never allow a programmable controller to override a temperature or pressure setpoint that is above or below a hard coded value in the controller. Furthermore, any controller that received a request to change a value to an unsafe or out of range condition should immediately flag that message as an alarm, which can help quickly identify potential cybersecurity threats in real-time. More likely it was someone who entered a wrong value, but the end result should be the same, which is part of any cybersecurity check and balance systems. The IT industry has developed a comprehensive set of risk management principles to identify, protect, and respond to cybersecurity threats. Although these principles can be equally applied to OT systems, it is critical to understand that the two worlds are very different operationally and technically. Threats to the OT system must be responded to in real-time or something potentially catastrophic could happen. The OT system should have full monitoring capability for outside threats both in access and disruption. Therefore, the risk management practices outlined in this framework reflect these differences and the recommended solutions to them. To simplify the framework, we start out by asking several fundamental questions:
- What is the acceptable risk to my building(s) or business?
- What are the major risks I need to focus on?
- How do I protect OT systems from these risks?
- If my facility has a high-risk profile, what other steps will I need to consider to minimize my risk?

## 95.1 What is the acceptable risk to my building(s) or business?

Risk varies widely in the OT world based on the size, type, sophistication and usage of a building. A retail store in a strip mall has a very different risk profile than a pharmaceutical research and manufacturing facility. The table below provides a basic guideline for classifying low, medium, and higher risk facilities.

*Figure 4. What Risk Level is My Building?*

| | Low | Medium | High |
|---|---|---|---|
| **Typical Facility Types** | Small retail, office, local government | Class A office, K-12, light industrial, warehouses | Universities, pharma/biotech, hospitals, data centers, petrochemical, utilities, banking |
| **Typical OT Systems** | Smart thermostats, intrusion security, cameras, fire | BAS, access control, video surveillance, elevator control, lighting control, fire & life safety | BAS, access control, video surveillance, elevator control, lighting control, fire & life safety, power management, digital signage, occupant tracking |
| **Operational Characteristics** | 9-5, limited or no remote access, no access to PII | Remote access for service providers, extended business hours, converged IT and OT networks | 24/7, occupant health and safety, explosive materials, large public venues |

## 95.2 What are the major risks I need to focus on?

The #1 risk to be managed is around who has access to the systems and in particular if this access is possible over the Internet. The table below identifies the top 5 risk areas common to OT systems.

*Figure 5. What Risks Do I Need to Focus On?*

| Risk | Description |
|---|---|
| **Remote User Access** | Where remote access is possible over the Internet, the security of this connection is critical to preventing the system from being exploited by cybercriminals and malware. |
| **System Backup** | The ability to quickly recover from a cyber event or a system failure such as a server crash is directly related to having a current, secure backup file. |
| **User Administration** | It is essential to know the names of every individual that has access to the OT system both inside and outside of the organization. Administration of these individuals includes adherence to policies governing user credentials, employment status, job responsibilities, and auditing. |
| **Software Maintenance** | Software is subject to having security flaws which are identified over time and suppliers provide patches and upgrades to address them. |
| **Malware Protection** | Malware in the form of viruses, worms, trojans, bots and ransomware is pervasive with new types constantly emerging. Malware infects OT systems through user activity and directed attacks from cybercriminals. |

## 95.3 How do I protect OT systems from these major risks?

There are often numerous options for how to protect your OT systems from cybersecurity threats. It is helpful to organize options into a matrix similar to the one below, and identify which approach is going to be used for your smarter building(s).

*Figure 6. Mitigation Strategies for Different Risks*

| Risk | Risk Mitigation |
|---|---|
| **Remote User Access** | To secure remote users a firewall or firewall appliance must be installed between the Internet and the OT system. Encrypt data that is transmitted between remote users and the firewall, only authorized users are granted access, and the OT system should never have a public facing IP address. |
| **System Backup** | There are many options and suppliers to backup OT systems automatically. Backups should be done daily and saved for at least one month. Backups are to be saved in a secure location and never on the same server as the OT system itself. The owner's designated System Administrator will maintain a disaster recovery plan including an annual test of the system. |
| **User Administration** | Administration of users begins with the assignment of a Systems Administrator, who is responsible for setting and enforcing user policies. Because OT systems invariably are serviced by 3rd party suppliers, these policies must be adopted throughout the supply chain. |
| **Software Maintenance** | OT applications and their operating systems should be kept current through software maintenance agreements, and security patches applied when they become available. |
| **Malware Protection** | All servers, workstations, tablets, and smartphones should be protected with anti-virus / anti-malware software to mitigate these threats. |
| **High Risk Processes or Environments** | Consider air-gapping the OT network from any outside network access. Or, at a minimum, implement a strong firewall and setup substantial restrictions for access. Also consider implementing a one-way flow of information for monitoring and alarming with no "command and control" capability outside of the OT internal network. |

## 95.4 If my facility has a high-risk profile, what other steps will I need to consider to minimize my risk?

The OT network is often connected to the IT network in a building. For this reason, particular care must be taken to control and continuously monitor network traffic, in order to identify abnormalities that can represent malicious activity. Malicious actions are not limited to cybercriminals but can also include disgruntled employees, contractors, or others. Network monitoring is also useful for knowing exactly what devices are on the OT network. Not only is this helpful for asset management, but unknown devices that are detected through monitoring are potential security threats to your facility. Actively monitoring can also include vulnerability scans of IT devices such as servers and workstations to determine if software is out-of-date, detect malware, misconfigurations, and more. To go even further with monitoring, OT systems like IT systems can undergo PEN (penetration) testing. This is the equivalent of a white hacker being employed to identify any and all ways in which the OT system can be attacked and compromised. Obviously, this is something that only high-risk systems would normally undertake where the consequences of a system breach could impact business continuity, life safety, and / or loss of critical data.

## 95.5 Cybersecurity for Facilities

Facilities managers, owners, and end users have an increasing need to secure facilities from ever-increasing cyberattack threats. The following topics should be considered as part of an assessment and planning interview with your cybersecurity legal counsel toward implementing comprehensive cybersecurity plan for facilities.

### 95.5.1      Facilities overall data security objectives

- **A.** Data availability: timely and reliable access to info
- **B.** Data confidentiality: protecting privacy
- **C.** Data integrity: preventing or detecting modification (or lockup) of data by unauthorized persons
- **D.** Grant and regulate appropriate access by outsiders

### 95.5.2      Threat potential

- **A.** Interconnected networks lead to an increased number of entry points and paths for intrusion.
- **B.** IP addresses which are public or not secured are open doors for hackers.
- **C.** Interconnected systems lead to increased data exposure when data is aggregated.
- **D.** Using the same password on a router as on a building controller device can enable intruder to gain access to control systems.
- **E.** Expansion of collected data leads to potential compromise of security.
- **F.** Systems that interact need to have compatible security.

- **G.** Handoff and interface areas, where handshakes can be weak points, are paths for intrusion.
- **H.** When non-secure new devices (especially those which are IoT connected) are integrated into a larger building management system, the danger is that they can compromise other parts of the system. For example, hackers of Las Vegas casino gained access to an internet-connected thermometer installed in an aquarium display.
- **I.** Failure to timely apply security patches to software and firmware can leave devices and systems exposed to attack. See the Cybersecurity Risks for Facilities chart below.

### 95.5.3      Potential impact of cyberattacks on facilities

- **A.** Crashes
- **B.** Shutdown
- **C.** Slowdown
- **D.** Data lockup (via ransomware)
- **E.** Interference with operations
- **F.** Loss of operational control
- **G.** Change data, conditions, sensors, alarm alerts (to hide sabotage to apparatus)

### 95.5.4      Planning: Policies and response

- **A.** Evaluate OT vs IT threats and risk.
- **B.** Assess current security and vulnerabilities.
- **C.** Develop a plan for remediation.
- **D.** Evaluate impact (cost vs effort vs timeframe vs benefit) of various measures.
- **E.** Determine desired security level: Platinum (best in class), gold (all areas reasonably secured), or aluminum (meets minimum legal/regulatory requirements).
- **F.** Implement plan.
- **G.** Mitigating risk involves policies, people, and processes. All three must work in harmony to be successful.

### 95.5.5      Action items

- **A.** Review vendors agreements with attorney to ensure cybersecurity obligations and liability minimize risk to the facility; amend now or at renewal time to improve. Assess new vendors as potential security risks.
- **B.** Develop or update a cybersecurity incident response plan (including a ransomware attack response plan), and practice it
- **C.** Develop or update a disaster recovery/business continuity plan
- **D.** Review and update security-related policies

- **E.** Review staff access levels to systems and deauthorize access, where inappropriate. Improve controls on who has access to software and passwords.
- **F.** Implement security incident and event management (SIEM) systems to monitor network activity and flag suspicious activity
- **G.** Review employee on/offboarding procedures
- **H.** Review building systems for compliance with cyber standards (e.g., new UL and ISA tests for IOT devices)
- **I.** Maintain adequate cybersecurity insurance; review current policy limits and exclusions (e.g., "business email compromise")

### 95.5.6      Additional tips for improving facility cybersecurity:

- **A.** Require strong passwords which must be changed at least every three months.
- **B.** Make sure employees know not to share or post passwords.
- **C.** Train employees regularly on good cyber hygiene practices.
- **D.** Review data backup frequency. Make sure critical data is backed up more frequently and all data is backed up offsite. Evaluate frequency based on ransomware lockup's effect, i.e., how many hours/days of data could you lose and still function?
- **E.** Follow your policy for retention and disposal of all sensitive information.
- **F.** Install software/firmware security patches as soon as possible.
- **G.** Encrypt highly sensitive data in storage whenever possible.
- **H.** Segregate sensitive data to reduce cross-over access by an intruder.
- **I.** Implement IP address restrictions.
- **J.** Disable/close unused ports on wireless routers.
- **K.** Employ two-factor authentication (password and additional private information).
- **L.** Verify vendor's email or faxed instructions to change their bank account information by calling the vendor using the phone number in your file, not by email or by using the phone number provided in the instructions.
- **M.** Have an outside firm conduct regular risk analysis/risk assessment tests. Source: Jason Bernstein © 2023 Barnes & Thornburg LLP. All Rights Reserved. Used with permission.

## 95.6 Sample Cybersecurity Risk Assessment Matrix

The following matrix is an example of a multi-tier assessment for cybersecurity risks. Note there are an extended set of "tiers" where threats, and therefore, controls are needed to reduce cyber threats. Each tier has a High, Medium and Low assessment based on Outside, Internal, an Physical threats where the Outside and Internal threats are logical/cyber/network threats and the Physical threats are more in line with intrusion, panel access, unauthorized computers, use of USB sticks, etc. This example can be extrapolated for both simple and very complex scenarios.

Tier Function Security Level Cyber Security Risk

Outside Network Threat - High Enterprise Tier Internal Network Threat - Medium Physical Intrusion Threat - Low

Building Management System - System Front End

Backup Servers System

Firewall/VPN Access System

Outside Network Threat - Medium Campus Tier Internal Network Threat - Low Physical Intrusion Threat - High

Building Automation System System

Outdoor Lighting System

Irrigation Control System

Outside Network Threat - Low Building Tier Internal Network Threat - High Physical Intrusion Threat - Medium

HVAC System

Lighting System

Security System

Outside Network Threat - Low Equipment Tier Internal Network Threat - High Physical Intrusion Threat - Low

Air Handler Equipment

Lighting Panel Equipment

Fire Panel Equipment

Outside Network Threat - Low Devices Tier Internal Network Threat - Medium Physical Intrusion Threat - Low

Thermostat Embedded Device

Lighting Controller Embedded Device

Energy Sub Meter Embedded Device

Source: © 2023 Ron Bernstein, RBCG Consulting - www.rb-cg.com - Used with permission.

Appendix

This Appendix includes more detailed examples of select sections of the Framework.
