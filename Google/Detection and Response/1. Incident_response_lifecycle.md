# Incident response lifecycle

Incident lifecycle frameworks provide a structure to support incident response operations\
Frameworks help organizations develop a standardized approach to their incident response process, so that incidents are managed in an effective and consistent way\
There are many different types of frameworks that organizations can adopt and modify according to their needs\

*Incident*: An occurence that actually or imminently jeopardizes, without lawful authority, the confidentiality, integrity, or availablility of information or an information system; or constitutes a violation or imminent threat of violation of law, security policies, security procedures, or acceptable use policies. (NIST)

## Frameworks

### NIST CSF

5 core functions
- Identify
- Protect
- Detect
- Respond
- Recover

Last three steps are critical stages during incident response

### NIST Incident response lifecycle

Another NIST framework with additional sebsteps dedicated to incident response

- Preparation
- Detection
- Analysis
- Containment
- Eradication
- Recovery
- Post-incident activity

## Incident response operations

### CSIRT (Computer security incident response teams)

A specialized group of security professionals that are trained in incident management and response

- The goal 
  - Effectivly and efficiently manage incidents, provide services and resources for response and recovery, and prevent future indidents from occuring
- Must work across functionally with other departments to share relevant information
- Roles
  - Security analyst
    - Continuously monitor an environment for any security threats
      - Analyzing and triaging alerts
      - Performing root-cause investigations
      - Escalating or resolving alerts 
  - Technical lead
    - Manage all of the technical aspects of the incident response process, such as applying software patches or updates
  - Incident coordinator
    - Tracks and manages the activities of the CSIRT and other teams involved in the response effort
    - Job is to ensure that incident response processes are followed and that teams are regularly updated on the incident status
  - **Not all CSIRT are the same, they might be referred to different title**

### SOC (Security operations center)

An orfanizational unit dedicated to monitoring network systems, and devices for security threats or attacks

- Often exists as its own separate unit or within a CSIRT
- Involves in various types of blue team activities, such as network monitoring, analysis, and response to incidents

#### Tiers

![img](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/CMDszNSgSryqbipKuGOU2Q_222b5865df5f4a72a785cd94279d99f1_CkqInM-0iDHKapM_2jS_68ZBhx11oR2GR_fCveMT5EI39E4h_dsAwBstgiRAXmj-mLFWXeOLNnSpBeMpDrEOiP9N8P9efbhWwLqNx-nDZFmoa6ue7SuqH0iUjmnMPWmpEcZPjKUY7ONnH6qkmt7wqF1XpuxPDe1zCbwGriZcyQRpSru_CG-tzvFvMDe5cg?expiry=1700006400000&hmac=iIYk9JYad-MharDSrsb-Bgw7mwYDOSxpBzJOqoIaSOI)

- Tier 1 SOC analyst
  - Composed of the least experienced SOC analysts who are known as level 1s
  - Responsibility
    - Monitoring, reviewing, and prioritizing alerts based on criticality or severity
    - Creating and closing alerts using ticketing systems
    - Escalating alert tickets to Tier 2 or Tier 3
- Tier 2 SOC analyst
  - Comprises the more experienced SOC anlaysts AKA level 2s
  - Responsibility
    - Receiving escalated tickets from L1 and conducting deeper investigations
    - Configuring and refining security tools
    - Reporting to the SOC Lead
- Tier 3 SOC lead
  - Composed of the SOC leads, or level 3s
  - Responsibility
    - Managing the operations of their team
    - Exploring methods of detection by performing advanced detection techniques, such as malware and forensics analysis
    - Reporting to the SOC manager
- SOC manager
  - The top of the pyramid
  - Responsibility
    - Hiring, training, and evaluating the SOC team members
    - Creating performance metrics and managing the performance of the SOC team
    - Developing reports related to incidents, compliance, and auditing
    - Communicating findings to stakeholders such as executive management
- Other roles
  - Forensic investigator
    - Commonly L2s and L3s who collect, preserve, and analyze digital evidence related to security incidents to determine what happened
  - Threat hunter
    - Typically L3s who work to detect, analyze, and defend against new and advanced cybersecurity threats using threat intelligence

### Incident plan

Document that outlines the procedures to take in each step of incident response

- Not all the same
  - Organizations tailor their plans to meet their unique requirements such as their mission, size, culture, indeustry, and structure
- Elements of an incident plan
  - Incident response procedures
    - Step-by-step instructions on how to respond to incidents
  - System information
    - Things like network diagram, data flow diagram, logging, and asset inventory information
  - Other documents
    - Things like contact lists, forms, and templates

## Tools

### Types

- Detection and management tools
  - Monitor system activity to identify events that require invastigation
- Documentation tools
  - Collect and complie evidence
- Investigative tools
  - Analyze events

### IDS, IPS and EDR

IDS (Intrusion detection system)
- An application that monitors system and network activity and produces alerts on possible intrusions
- Detection categories
  - True positive
    - Alert that correctly detects the presence of an attack
  - True negative
    - No malicious activity exists and no alert is triggered
  - False positive
    - Alert that incorrectly detects the presence of threat
  - False negative
    - Malicious activity happens but IDS fails to detect it

IPS (Intrusion prevention system)
- An application that monitors system activity for intrusions and take action to stop the activity

EDR (Endpoint Detection and response)
- application that monitors an endpoint for malicious activit
- Installed on endpoints

| Capability                   | IDS | IPS | EDR |
| ---------------------------- | --- | --- | --- |
| Detects malicious activity   | Yes | Yes | Yes |
| Prevents intrusions          | No  | Yes | Yes |
| Logs activity                | Yes | Yes | Yes |
| Generates alerts             | Yes | Yes | Yes |
| Performs behavioral analysis | No  | No  | Yes |

Many tools have the ability to perform both IDS and ISP

#### Popular tools

- Snort (IDS/IPS)
- Zeek (IDS/IPS)
- Kismet (IDS/IPS)
- Sagan (IDS/IPS)
- Suricata (IDS/IPS)
- Open EDR (EDR)
- Bitdefender (EDR)
- FortiEDR (EDR)
- Endpoint Detection and Response (EDR)

### SIEM and SOAR

#### SIEM (Security Information and Event Management)

- An application that collects and analyze log data to monitor critical activitiees in an organization
- Provides security professionals with a high-level overview of what goes on in their network

#### Advantages

- Access to event data
  - Provide access to the event and activity data that happens on a network, including real-time activity
- Monitoring, Detecting, and alerting
  - Continuously monitor systems and networks in real-time
  - Analyze the collected data using detection rules to detect malicious activity
- Log storage
  - Can act as a system for data retention, which can provide access to hisitorical data

##### Process
1. Collect and aggregate data
   - The data is typically in the form of logs
   - Data comes from multiple sources such as IDS, IPS, database, firewalls, application, and more
2. Normalize data
   - converts data into a standard, structured format that is easily searchable
3. Analyze data
   - Analyzes the normalized data against a rule set to detect any possible security incidents

#### Popular tools

- AlienVault OSSIM
- Chronicle
- Elastic
- Exabeam
- IBM QRadar
- LogRhythm
- Splunk

#### SOAR (Security Orchestration, Automation, and Response)

- A collection of applications, tools, and workflows that uses automation to respond to security events
- Automates analysis and response to security events and incidents
- Can also be used to track and manage cases
  - Multiple incidents can form a case, and SOAR offers a way to view all of the incidents in one centralized place