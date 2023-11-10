# Flaws in the System

Finding vulnerabilities and fixing them before they come a problem is the key to keep an asset safe\
**vulnerability** is a weakness that can be exploited by a threat

## Vulnerability management

The process of finding and patching vulnerabilities\
4 step process
- Identify vulnerabilities
- Consider potential exploits of the vulnerabilities
- Prepare defense against threats
- Evaluate the defense

#### Zero-day exploits
- An exploit that was previously unknown

## Defense in depth strategy

A layered approach to vulnerability management that reduces risk\
Each level of defense minimizes the risk of attacks\
Mainly used to protect information using a five layer design
- Perimeter layer
  - Function is to only allow access to trusted partners to reach the next layer of defense
  - Mainly, User authentication layer that filters external access
- Network layer
  - Made up of technologies like network firewalls
  - More closely aligned with authorization
- Endpoint layer
  - Refers to the devices that have access on a network
  - Anti-virus software
- Application layer
  - Includes all the interfaces that are used to interact with technology
  - Security measures are programmed as part of an application
  - Multi-factor authentication
- Data layer
  - Layer that refers to critical data that must be protected
  - Asset classification

## Common vulnerabilities and exposures

**Exposure** is a mistake that can be exploited by a threat\
**Vulnerability** is a weakness of a system

### CVE list (Common Vulnerabilities and Exposures list)

An openly accessible dictionary of known vulnerabilities and exposures\
Originally created by MITRE in 1999
- MITRE is a collection of non-profit research and development centers

Before CVE can make in onto the CVE list, it first goes through a strict review process by a CVE Numbering Authority (CNA)
- **CNA** is an organization that volunteers to analyze and distribute information on eligible CVEs

CVE list tests four criteria that a vulnerability must have before it's assigned an ID
1. Must be independent of other issues
2. Must be recognized as a potential security risk by whoever reports it
3. Must be submitted with supporting evidence
4. Can only affect one codebase/only one program's source code

Vulnerabilities added to the CVE list are often reviwed by other online vulnerability databases\
One of the most popular is the **NIST National Vulnerabilities Database**

### NIST National Vulnerabilities Database

Uses what's known as the common vulerability scoring system (CVSS)
- Measurement system that scores the severity of a vulnerability
- Score of 0 - 10
- Base scores reflect the moment a vulerability is evaluated
- Below 4 is considered to be low risk
- Above 9 is considered to be critical risk
Security team use CVSS as a way of calculating the impact a vulnerability could have on a system and determine how quickly a vulnerability should be patched

## OWASP (Open Worldwide Application Security Project)

- Nonprofit foundation that workd to improve the secutiry of software
- An open platform that security professionals from around the world use to share information, toos, and events that are focused on securing the web

### OWASP Top 10

- Broken access control
  - Access controls limit what users can do in na web application
  - Failures in access control can lead to unauthorized information disclosure, modification, destruction or give someone unauthorized access to other business applications
- Cryptographic failures
  - Privacy laws such as GDPR require sensitive data to be protected by effective encryption methods
  - Vulnerabilities can occur when business fail to encrypt things like PII or use weak algorithm
- Injection
  - Occurs when mallicious code is inserted into a vulnerable application
  - Common target is a website's login form
  - Injection attacks can create backdoor into an organization
- Insecure design
  - Refers to a wide range of missing or poorly implemented security controls that should have been programmed into an application when it was being developed
- Security misconfiguration
  - Occurs when security settings aren't properly set or maintained
  - Mistakes often happen when systems aren't properly set up or audited
- Vulnerable and outdated components
  - Category that mainly relates to application development
  - Applications that use vulnerable components/libraries that have not been maintained are at greater risk of being exploited by threat actors
- Identification and authentication failures
  - Occurs when applications fails to recognize who should have access and what they're authorized to do
- Software and data integrity failures
  - Instances when updates or patches are inadequately reviewed before implementation
  - Attackers might exploit these weaknesses to deliver malicious software
  - Third parties are likely to become infected if a single system is compromised AKA supply chain attack
- Security logging and monitoring failures
  - Logging and tracing back events are critical to find and fixing problem
- Server-side request forgery (SSRF)
  - Occurs when attackers manipulate the normal operations of a server to read or update other resources on that server

## OSINT (Open source intelligence)

The collection and analysis of information from publicly available sources to generate usable intelligence\
Commonly used to support cybersecurity activities
- Identifying potential threats and vulnerabilities
OSNIT plays a significant role in **information security (InfoSec)**, which is the practice of keeping data in all states away from unauthorized users

### Information vs intelligence

*Information* refers to the collection of raw data or facts about a specific subject\
*Intelligence* refers to the analysis of information to produce knowledge or insights that can be used to support decision-making\
In other words, intelligence is derived from information through the process of analysis, interpretation, and integration. Gathering information and intelligence are both important aspects of cybersecurity
- OSNIT can be used to generate intelligence
  - Provide insights into cyber attacks
  - Detect potential data exposures
  - Evaluate existing defenses
  - Identify unknown vulnerabilities
  - and more..
  
Examples of tools in OSNIT
- VirusTotal
  - A service that allows anyone to analyze suspicious files, domains, URLs, and IP addresses for malicious content
- MITRE ATT&CK
  - A knowledge base of adversary tactics and techniques based on real-world observations
- OSNIT Framework
  - A web-based interface where people can find OSNIT tools for almost any kind of source or platform
- Have I been Pwned
  - Tool that can be used to search for breached email accounts
