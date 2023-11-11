# Threat Modeling

The process of identifying assets, their vulnerabilities, and how each is exposed to threats

A typical threat modeling process is performed in a cycle:
1. **Define the scope of the model**
   - The team determines what they're building by creating an inventory of assets and classifying them
2. **Identify threats**
   - The team defines all potential threat actors and create an *attack tree*
      - *Attack tree* is a diagram that maps threats to assets
3. **Chatacterize the environment**
   - The team applies an attacker mindset to the business
   - They consider how the customers and employees interact with the environment
4. **Analyze threats**
   - The team works together to examine existing protections and identify gaps
   - They then rank threats according to their risk score that they assign
5. **Mitigate risk**
   - The team creates their plan for defending against threats
   - The choices are:
      - Avoid risk
      - Transfer risk
      - Reduce risk
      - Accept risk
6. **Evaluate findings**
   - Document everything that was done
      - Fixes that are applied
      - Any success
      - Any fail
      - Any lesson learned

## Common frameworks

- STRIDE
  - Developed by Microsoft
  - Commonly used to identify vulnerabilities in six specific attack vectors
    - Spoofing
    - Tampering
    - Repudiation
    - Information disclosure
    - Denial of Service
    - Elevation of privilege
- [PASTA](#pasta-process-for-acctack-simulation-and-threat-analysis)
  - Risk-centric threat modeling process developed by two OWASP leaders
  - Main focus is to discover evidence of viable threats and represent this information as a model
  - Evidence-based design can be applied when threat modeling an application or the environmnet that supports that application
- Trike
  - Open source methodology and tool that takes a security-centric approach
  - Commonly used to focus on security permissions, application use cases, privilege models, and other elements that support a secure environment
- VAST (Visual, Agile, and Simple Threat)
  - Part of an automated threat modeling platform called *ThreatModeler*
  - Commonly used as a way of automating and streamlining threat modeling assessments

## PASTA (Process for Acctack Simulation and Threat Analysis)

A popular threat modeling framework that's used across many industries\

### Seven Stages

1. **Define business and security objectives**
   - Decide what their goals are
2. **Define the technical scope**
   1. Identify the application components that must be evaluated
3. **Decompose the application**
   1. Identify the existing controls that will protect user data from threats
   - Normally means to work with the application developers to produce data flow diagram
4. **Perform a threat analysis**
   - The team gets into their attacker mindset
   - Reseach is done to collect the most up-to-date information on the type of attacks being used
5. **Perform a vulnerability analysis**
   - Deeply investigate potential vulnerabilities by considering the root of the problem
6. **Conduct attack modeling**
   - Test the vulnerabilities that were analyzed by simulating attacks
   - Done by creating an attack tree
7. **Analyze risk and impact**
   - Assemble all the collected information