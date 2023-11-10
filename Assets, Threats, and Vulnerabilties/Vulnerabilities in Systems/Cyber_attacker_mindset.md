# Cyber attacker mindset

There's a wide range of vulnerabilities and systems that need to be found\
Assessing those weaknesses is a time-consuming process
To position themselves ahead of threats and
make the most of their limited resources, companies start by understanding the environment surrounding their operations\
An important part of this is getting a sense of their **attack surface**
- Attack surface is all the potential vulnerabilities that a threat actor could exploit
- Modern organizations need to concern themselves with both a physical and digital attack surface
- *Physical attack surface* is made up of peopler and their devices
  - Can be attacked from both inside and outside the organization
- *Digital attack surface* includes everything that's beyond the organization's firewall (anything that connects to an organization online)
  - Cloud computing has expanded the digital attack surface

## Types of threat actors

Threat actor is any person or group who presents a security risk

Threat actors are normally divided into five categories:
- Competitors
  - Refers to rival companies who pose a threat because they might benefit from leaked information
- State actor
  - Government intelligence agencies
- Criminal syndicates
  - Refer to organized groups of people who make money from criminal activity
- Insider threats
  - Any individual who has or had authorized access to an organization’s resources
- Shadow IT
  - Refers to individuals who use technologies that lack IT governance. A common example is when an employee uses their personal email to send work-related communications
- Hacktivists
  - Exposing secrets and disrupting organizations that are perceived as evil

## Types of hackers

Hacker is any person who uses computers to gain access to computer systems, networks, or data

Hackers are divided into three types:
- Unathorized, or unethical hacker
  - Individual who uses their programming skills to commit crimes AKA malicious hacker
- Authorized, or ethical hackers
  - Individuals who use their programming skills to improve an organization's overall security
  - Include internal members of a security team, external security vendors, and freelance hackers
- Semi-authorized hackers
  - Typically refers to individuals who might violate ethical standards, but are not considered malicious

## Advanced persistent threats (APT)

Refers to instances when a threat actor maintains unauthorized access to a system for an extended period of time
- Mostly associated with nation states and state-sponsored actors
- Typically concerned with surveilling a target to gether information

## Attack vectors
- refers to pathways attackers use to penetrate security defenses
For the most part, threat actors gain access through one of following attack vectors:
- Direct access
  - Physical access to a system
- Removable media
  - Portable hardware like USB flash drive
- Social media platforms
  - Application used for communication and content sharing
- Email
  - Both personal and business accounts
- Wireless network on premises
- Cloud services
  - Usually provided by third-party organizations
- Supply chains
  - Third-party vendors that can present a backdoor into system

### Attacker midset

Steps to process:
1. Identify a target
2. Determine how the target can be accessed
3. Evaluate attack vectors that can be exploited
4. Find the tools and methods of attack

## Brute force attack

A trial-and-error process of discovering private information

Variety of brute force attacks
- Simple brute force attack
  - Approach in which attackers guess user's login credential or use algorithm to to try all possible values
- Dictionary attacks
  - Attacker use a list of commonly used credential to access a system
- Reverse brute force attack
  - Similar to dictionary attacks, except they start with a single credential and try it in various systems
- Credential stuffing
  - A tactic in which attackers use stolen login credentials from previous data breaches to access user accounts at another organization

### Tools used
- Aircrack-ng
- Hashcat
- John the Ripper
- Ophcrack
- THC Hydra

### Prevention measures
- Hashing and salting
- MFA (Multi-factor authentication)
- CAPTCHA
- Password policies