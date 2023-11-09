# Authentication, Authorization, and Accounting

## Access Controls

Security controls that manage access, authorization and accountability of information

### Frequently used access controls

#### HTTP (Hypertext transfer protocol)

- Uses basic auth (ther technology used to establish a user's request to access a server)
  - Works by sending an identifier every time a user communicates with a web page
- Considered to be vulnerable to attacks because it communicates in plain text

#### OAuth (Open-standard authorization protocol)
- Shares designated access between applications
- Uses API tokens to verify access betweeb you and a service provider
  - API token is a small block of encrypted code that contains information about a user

## Authentication

Acceses controls that process by which a system verifies the identity of a user who wishes to access the system
- General factors
  - Knowledge - Refers to something the user knows
    - A password or the answer to a security question they provided previously
  - Ownership - Refers to something the user possesses
    - A one-time passcode (OTP)
  - Biometric - Refers to a person's physical traits
    - Fingerprint, Face, or iris recognition

### SSO and MFA

Single sign-on (SSO) is a technology that combines several different logins into one
- Convenient, but present a significant vulnerability when used alone
- Commonly rely on two different authentication protocols
  - LDAP (Lightweight Directory Access Protocol)
    - Mostly used to transmit information on-premises
  - SAML (Security Assertion Markup Language)
    - Mostly used to transmit information off-premises like in cloud
  - LDAP and SAML protocols are often used together

Multi-factor authentication (MFA) is a security measure which requires a user to verify their identity in two or more ways to access a system
- Not convenient for users, but provides more security

SSO and MFA are often used in conjunction whith one another to layer the defense capabilities of authentication system

## Authorization

Access controls that process by which a system grants or revokes the right to access some data or perform some action\
Depends on a system or user's role

### Principle of least privilege

The principle that a security architecture should be designed so that each entity is granted the minimum system resources and authorizations that the entity needs to perform its function

### Separation of duties

The principle that users should not be given levels of authorization that would allow them to misuse a system
- Reduces the risk of system failures and inappropriate behavior from users

Both Principle of least privilege and Separation of duties apply to all systems including networks, databases, processes, and any other aspect of an organization

## Accounting

Practice of monitoring the access logs of a system\
Access logs contains helpful data to identify trends, such as failed login attempts

- Access logs are essentially records of sessions that capture the moment a user enters a system until the moment they leave
- Anytime a user accesses a system, they initiate session
  - Session is a sequence of network HTTP requests and responses associated with the same user
- When session begins, the session ID gets created
  - Session Id is a unique token that identifies a user and their device while accessing the system
- After creating session ID, session cookies are exchanged between a server and a user's device
  - Session cookie is a token that websites use to validate a session and determine how long the session should last

Cookies make web sessions safer and more efficient. The exchange of tokens means no sensitive information are shared, but vulnerable to Session hijacking attacks
- Session hijacking: An event when attackers obtain a legitimate user's session ID

Accounting can detect these kind of attacks

## Identity and Access Management (IAM)

A collection of processes and technologies that helps organizations manage digital identities in their environment

- Both AAA and IAM systems are designed to authenticate users, determine their access privileges, and track their activities within a system

### 3 common frameworks used to authorization in IAM

#### Mandatory access control (MAC)
- The strictest of the three frameworks
- Based on a strict need-to-know basis
- Access to information must be granted manually by a central authority or system administrator

![img](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/AxrWM2DLTSunrTWYAtwc4Q_49abc18d6b1c48748e222045153881f1_image3.png?expiry=1699660800000&hmac=ISt0wpmT1HTnTyvEE7GieuB55jhBjojzO8VTuy1L9p4)

#### Discretionary access control (DAC)
- Typically applied when data owner decides appropriate levels of access

![img](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/LHnKRh7ISfCc379NmCXMlw_5c65648b2a77437ab6998e6b978afcf1_image2.png?expiry=1699660800000&hmac=WuYPuYXAqfDQztX97mGs1UPcrFRg4UGGUy0V8roRGZs)

#### Role-based access control (RBAC)
- Used when authorization is determined by a user's role within an organization

![img](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/1EBo9jW3TGW_7Hulb3cUpA_16c10e1f1de94b3c95d88760722733f1_image1.png?expiry=1699660800000&hmac=UMyJYasB58UPeQ-XHfKKYpVd1T0ykZHgh2eg5GNZZe8)