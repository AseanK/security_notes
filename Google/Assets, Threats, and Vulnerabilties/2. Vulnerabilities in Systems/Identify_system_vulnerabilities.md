# Identify system vulnerabilities

Weaknesses and flaws are generally found during a vulnerability assessment

## Vulnerability assessment

The internal review process of an organization's security systems that works similar to the process of identifying and categorizing vulnerabilities on the CVE list\
- The goal is to identify weak points and prevent attacks
- Once organizaion's security team decide whtat to focus on, vulnerability assessments typically follow a 4-step process
  1. Identification
    -  Scanning tools and manual testing are used to find vulnerabilities
    -  The goal is to understand the current state of a security system
  2. Analysis
    - Each of the vulnerabilities that were identified are tested
    - The goal is to find the source of the problem
  3. Risk assessment
    - A score is assigned to each vulnerability
    - Score is assigned based on two factors
      - Severity, and likelihood of explit
  4. Remediation
    - Vulnerabilities are addressed depending on the severity score
    - Normaly a joint effort between the security stadd and IT teams to come up with the best approach to fixing the vulnerabilities

### Vulnerability scanning tools

Commonly used to simulate threats by finding vulnerabilities in an attack surface\
They also help security teams take proactive steps towards implementing their remediation strategy\

**Vulnerability scanner** is a software that automatically compares known vulnerabilities and exposures against the technologies on the network
- Generally used to scan systems to find misconfigurations or programming flaws
- Used to analyze each of the five attack surfaces
  1. **Perimeter layer**, like authentication systems that validate user access
  2. **Network layer**, which is made up of technologies like network firewalls and others
  3. **Endpoint layer**, which describes devices on a network, like laptops, desktops, or servers
  4. **Application layer**, which involves the software that users interact with
  5. **Data layer**, which includes any information that’s stored, in transit, or in use
- Scanning tool compares the findings against databases of security threats and flags any vulnerabilities that it finds then adds them to its reference database

#### External scan vs. Internal scan

External and internal scans simulate an attacker's approach

- **External scans** test the perimeter layer outside of the internal network
  - Analyze outward facing systems e.g. websites and firewalls
  - Can uncover vulnerable network ports or servers
- **Internal scan** start from the opposite end by examining an organization's internal systems
  - E.g. Analyze application software for weaknesses in how it hangles user input

#### Authenticated vs. unauthenticated

Authenticated and unauthenticated scans simulate whether or not a user has access to a system

- **Authenticated scans** test a system by logging in with a real user account or even with an admin account\
- **Unauthenticated scans** simulate external threat actor that do not have access

#### Limited vs. comprehensive

Limited and comprehensive scans focus on particular devices that are accessed by internal and external users

- **Limited scans** analyze particular devices on a network, like searching for misconfigurations on a firewall
- **Comprehensive scans** analyze all devices connected to a network. This includes operating systems, user databases, and more

## Penetration testing

AKA pen test is a simulated attack that helps identify vulnerabilities in systems, networks, websites, applications, and processes
- Involves using the same tools and techniques as malicious actors in order to mimic a real life attack
- Considered to be a form of ethical hacking

#### Approaches to pen test

- Red team
  - Simulate *attacks* to identify vulnerabilities in systems, networks, or applications
- blue team
  - focus on *defense* and incident response to validate an organization's existing security systems
- Purple team
  - *collaborative*, focusing on improving the security posture of the organization by combining elements of red and blue team exercises

#### Strategies

- **Open-box testing**
  - The tester has the same privileged access that an internal developer would have—information like system architecture, data flow, and network diagrams. This strategy goes by several different names, including internal, full knowledge, white-box, and clear-box penetration testing
- **Closed-box testing**
  - The tester has little to no access to internal systems—similar to a malicious hacker. This strategy is sometimes referred to as external, black-box, or zero knowledge penetration testing
- **Partial knowledge testinh**
  - The tester has limited access and knowledge of an internal system—for example, a customer service representative. This strategy is also known as gray-box testing

#### Becoming a pen-tester

- Network and application security
- Experience with operating systems
- Vulnerability analysis and threat modeling
- Detection and response tools
- Programming languages
- Communication skills