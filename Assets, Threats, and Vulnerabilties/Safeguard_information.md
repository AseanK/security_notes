# Safeguard Information

## Security controls

Safeguards designed to reduce specific security risks\
Typically, orgaization's security policy outlines the controls needed to achieve their goals\
Should be designed with the [Principle of least privilege](#principle-of-least-privilege)

### Types

- Technical
  - Technologies used to protect assets
  - Encryption, Authentication system
- Operational
  - Relate to maintaining the day-to-day security environment
  - Generally, **people** perform these controls like awareness training and incident response
- Managerial
  - Centered around how the other two reduce risk
  - Policies, standards, and procedures

### Information privacy

The protection of unauthorized access and distribution of data
- Information privacy is about the right to choose. People and organizations alike deserve the right to decide when, how, and to what extent private information about them is shared
- Plays a key role in organization's security policy decisions
- Security controls are the technologies used to regulate information privacy

### Information security (InfoSec)

Refers to the practive of keeping data in all states away from unauthorized users
- Information privacy vs. Information security
  - Information privacy is about providing people with control over their personal information and how it's shared
  - Information security is about protecting prople's choices and keeping information safe from potential threats

### Principle of least privilege

The concept of granting only the minimal access and authorization required to complete a task or function

- Fundamental security control that supports the CIA triad of information
- Rely on differentiating between data owner and data custodians
  - Data owner: The person that decides who can access, edit, use, or destroy their information
  - Data custodian: Anyone or anything (organizations and their system) that's responsible for the safe handling, transport, and storage of information
  - Data steward: The person or group that maintains and implements data governance policies set by an organization

#### Auditing account privileges

Periodically auditing accounts is a key part of keeping the sysyem secure\
Common types are:
- Usage audit
  - Review which resources each account is accessing and what the user is doing with the resource.
  - Can help determine whether users are acting in accordance with an organization's security policies
  - Can help identify whether a user has permissions that can be revoked because they are no longer being used
- Privilege audit
  - Users tend to accumulate more access privileges than they need over time, an issue known as *privilege creep*
  - *privilege creep* might occur if an employee receives a promotion or switches teams and their job duties change
- Account change audit
  - Changes to an account are usually saved and can be used to audit the directory for suspicious activity e.g. multiple attempts to change an account password

### Data Lifecycle

Important model when protecting information by influenceing how security teams set policies that align with business objectives\
Common stages are
- Collect
- Store
- Use
- Archive
- Destroy

### Examples of protected informations

- PII
  - Personally Identifiable Information
  - Information used to infer an individual's identity that can be used to contact or locate someone
- PHI
  - Protected Health Information
  - Information that relates to the past, present, or future physical or mental health or condition of an individual
  - Regulated by the HIPPA in the U.S.
  - Regulated by the GDPR in the EU
- SPII
  - Sensitive Personally Identifiable Information
  - Specific type of PII that falls under stricter handling guidelines
  - E.g. Bank account number or login credentials

### Notable privacy regulations

- GDPR (General Data Protection Regulation)
  - Set of rules and regulations developed by the European Union that puts data owners in total control of their personal information
  - Data type include person's name, address, phone number, financial information, and medical information
  - Applies to any business that handles the data of EU citizens or resident, regardless of where that business operates
- PCI DSS (Payment Card Industry Data Security Standard)
  - Set of security standards formed by major organizations in the financial industry
  - Aims to secure credit and debit card transactions against data theft and fraud
- HIPAA (Health Insurance Portability and Accountability Act)
  - U.S. law that requires the protection of sensitive patient health information
  - Prohibits the disclosure of a person's medical information without their knowlefge and consent