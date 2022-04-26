---
id: u8y1cfg1uny4p06iddb11yq
title: Training Security Journey Yellow Belt
desc: ''
updated: 1650921012220
created: 1650909577252
---

## Module 1: Intro
- ![](/assets/images/2022-04-25-14-00-43.png)
- ![](/assets/images/2022-04-25-14-00-59.png)
- ![](/assets/images/2022-04-25-14-01-13.png)
- ![](/assets/images/2022-04-25-14-01-28.png)
- ![](/assets/images/2022-04-25-14-01-44.png)
- ![](/assets/images/2022-04-25-14-02-00.png)

---

## Module 2: Secure Design, Part 1
- Why care?
  - ![](/assets/images/2022-04-25-14-08-36.png)
- Defense in depth
  - ![](/assets/images/2022-04-25-14-09-51.png)
  - Have different layers, to help prevent attackers from getting in
  - ![](/assets/images/2022-04-25-14-10-30.png)  
  - RASP : runtime application self-protection
  - PSIRT : Product Security Incident Response Team
- Less attack surface means less space for attacker to work with
- Only use interfaces that are needed, review on a schedule
- Avoid security by obscurity
  - ![](/assets/images/2022-04-25-14-29-57.png)
  - ![](/assets/images/2022-04-25-14-30-23.png)
  - Threat model your entire design
  - Keep security simple
  - ![](/assets/images/2022-04-25-14-33-20.png)
- Make security usable
  - ![](/assets/images/2022-04-25-14-34-20.png)
  - ![](/assets/images/2022-04-25-14-36-32.png)
- Key Takeaways
    1. Defense in depth provides a multi-layered application defense.​
    2. Minimization of attack surface results in less total methods an attacker can try to exploit.
    3. Security by obscurity is no security at all.
    4. Simple security is better than complex.
    5. Usable security has the best chance of user involvement.

---

## Module 3: Secure Design, Part 2
- Secure Design Principle
  - ![](/assets/images/2022-04-25-14-42-54.png)
- Why care?
  - Secure design equals less vulnerabilities
- Fail securely
  - Application: analyze design to esnure security relevant exceptions result in disallowing operation
- Run with least privilege
  - Grant users or apps only the **exact access** they need to perform their official duties
    - Adjust privileges as needed, build secure from the beginning
  - Review privilege levels
- Separation of duties
  - ![](/assets/images/2022-04-25-14-48-13.png)
  - Application: use more than 1 admin with different roles
- Don't trust services and infrastructure
  - Application: Use input validation and output encoding for interactions with all external requests
- Establish secure defaults
  - ![](/assets/images/2022-04-25-14-51-31.png)
  - Force the change of the default password at time of installation
  - Application: 
    - ![](/assets/images/2022-04-25-14-52-30.png)
    - Don't give them an insecure option  
- Key Takeaways
  1. Fail securely by limiting the access provided in a failure.​
  2. Run applications and services with the least possible privilege for them to still function.​
  3. Separate duties across multiple admin’s, and do not have a single admin with all the power.​
  4. Internal services and infrastructure should not be trusted. Trust only after verifying.
  5. When in doubt, provide a secure default to the user.

---

## Module 4: Input Validation
- What is it?
  - Checking potentially dangerous data to ensure that the inputs are safe before processing
- Why care?
  - ![](/assets/images/2022-04-25-15-01-12.png)
- Goals of input validation
  - ![](/assets/images/2022-04-25-15-01-41.png)
- Syntactic AND Semantic
  - Syntactic - enforce correct syntax of structured fields
  - Semantic - enforce correctness of values ina specific business context
- Dangerous and safe lists
  - ![](/assets/images/2022-04-25-15-03-50.png)
  - A bad list is constantly changing
  - A safe list is more controlled
- Client-side and server-side validation
  - ![](/assets/images/2022-04-25-15-05-27.png)
  - Choose server-side because we control the server, the user cannot turn it off
  - Client-side validation can increase performance
- Regular expressions and input validation
  - ![](/assets/images/2022-04-25-15-09-02.png)
  - Many frameworks have input validation
- Implementing input validation
  - ![](/assets/images/2022-04-25-15-27-02.png)
- Input validation mitigations
  - ![](/assets/images/2022-04-25-15-29-07.png)
- Key Takeaways
  1. The different input validation types are syntactic, semantic, safe list, dangerous list, client-side, and server-side.
  2. Each of the web application frameworks provide methods to validate input.
  3. Proper input validation includes framework data type validation, schema, type conversion, value range checks, arrays of allowed values, and regular expressions.
  4. Validate all input. Trust no input, regardless of its origin.

---

## Module 5: Output Encoding
- ![](/assets/images/2022-04-25-15-38-44.png)
- Why care?
  - ![](/assets/images/2022-04-25-15-39-51.png)
- Contextual output encoding
  - ![](/assets/images/2022-04-25-15-42-02.png)
- Goals
  - ![](/assets/images/2022-04-25-15-43-18.png)
- Tips
  - ![](/assets/images/2022-04-25-15-47-59.png)
  - Work smarter not harder & context matters!
- Key Takeaways
    1. Encoding is translating special characters into some equivalent form that is no longer dangerous in the target interpreter.
    2. Escaping is adding a special character before the character/string to avoid it being misinterpreted.
    3. Contextual output encoding is enforcing output encoding at every level of a user interface, and encoding at the last moment before untrusted data is dynamically added to HTML.
    4. The primary goal of output encoding and escaping is the prevention of XSS and command, XML, and LDAP injection.
    5. Remember the OWASP Java Encoder and .NET AntiXSSEncoder, and consider what encoding your existing framework provides.
    6. Input validation and output encoding work hand in hand to protect your application.

---

## Module 6: Authentication Theory
- Why care?
  - ![](/assets/images/2022-04-25-15-56-59.png)
- Identity
  - ![](/assets/images/2022-04-25-15-58-12.png)
- Authentication
  - ![](/assets/images/2022-04-25-15-58-43.png)
- Threats
  - ![](/assets/images/2022-04-25-16-00-12.png)
  - ![](/assets/images/2022-04-25-16-00-53.png)
- Weaknesses
  - ![](/assets/images/2022-04-25-16-02-15.png)
  - ![](/assets/images/2022-04-25-16-02-31.png)
- Authentication Data
  - ![](/assets/images/2022-04-25-16-03-53.png)
- Memorized Secrets
  - aka password
- One-Time Password
  - Valid for only one login session or transaction
- Recovery keys
  - Secrets stored by user and the system, an unlock key
- Biometrics
  - physical characteristics of a person as an auth source
- Cryptographic
  - A binary string used a secret parameter
  - Needs to be protected
- Factors of Authentication categories
  - Something you know
  - Something you have
  - Something you are
  - ![](/assets/images/2022-04-25-16-08-08.png)
- Key Takeaways
    1. Digital identity is a set of attributes that uniquely describe a person and authentication is verifying the identity of a user, process, or device before allowing access to resources in an information system.
    2. There are many types of authentication specific threats and weaknesses, and it is important to consider each during threat modeling.
    3. The authentication process relies upon memorized secrets, one-time passwords, biometrics, recovery keys, and cryptographic keys.
    4. Single-factor authentication is something you know; two-factor is something you know + something you have / are; multi-factor is multiple pieces of evidence across all three categories.

---

## Module 7: Authorization Theory
- ![](/assets/images/2022-04-25-16-20-20.png)
- Why care?
  - ![](/assets/images/2022-04-25-16-20-37.png)
- Access control example
  - ![](/assets/images/2022-04-25-16-22-39.png)
- Authorization threats
  - ![](/assets/images/2022-04-25-16-23-10.png)
  - ![](/assets/images/2022-04-25-16-23-38.png)
- Authorization weaknesses
  - ![](/assets/images/2022-04-25-16-25-04.png)
  - ![](/assets/images/2022-04-25-16-25-14.png)
- Subjects and objects
  - ![](/assets/images/2022-04-25-16-25-45.png)
- Types of authorization
  - DAC
    - ![](/assets/images/2022-04-25-16-26-45.png)
    - Seen a lot in file system permissions
    - Users and file are defined
  - MAC
    - ![](/assets/images/2022-04-25-16-27-40.png)
    - Users and documents each have a particular level asigned to them
      - Unclassified
      - Confidential
      - Secret
      - Top Secret
  - RBAC
    - ![](/assets/images/2022-04-25-16-30-43.png)
  - ABAC
    - ![](/assets/images/2022-04-25-16-31-32.png)
- Design principles
  - ![](/assets/images/2022-04-25-16-32-43.png)
- Key Takeaways
  1. Authorization is the access privileges granted to a user, program, or process or the act of granting those privileges.
  2. Authorization specific threats include elevation of privilege, disclosure of confidential data, data tampering, and token stealing.
  3. Authorization weaknesses include improper or incorrect authorization, authorization bypass, and improper access control.
  4. DAC is discretionary, MAC is mandatory, RBAC is role based, and ABAC is attribute and policy based.
  5. Review the authorization design principles when making any changes to an authorization policy or enforcement point.

---

## Module 8: Logging & Exception Handling
- ![](/assets/images/2022-04-25-16-45-24.png)
- Why care?
  - ![](/assets/images/2022-04-25-16-45-33.png)
- Logging threats
  - Repudiation
    - Proof that "I" did something terrible on the system
  - Information disclosure
    - PII written in logs...a big NO NO
- Logging weaknesses
  - ![](/assets/images/2022-04-25-16-52-18.png)
  - ![](/assets/images/2022-04-25-16-52-29.png)
- Which events to log
  - ![](/assets/images/2022-04-25-16-54-33.png)
- Where to record
  - ![](/assets/images/2022-04-25-16-55-34.png) 
    - Don't record on file system in Prod
    - DB's can scale better, set permissions accordingly
    - SIEM, tech-based solutiuon to consolidate logs into one place
- Common Event Format (CEF)
  - ![](/assets/images/2022-04-25-17-00-26.png)
- Event attributes
  - ![](/assets/images/2022-04-25-17-00-39.png)
- Data to exclude
  - ![](/assets/images/2022-04-25-17-00-59.png)
  - **NEVER log these!!!**
- Protection of log data at rest
  - ![](/assets/images/2022-04-25-17-02-46.png)
  - Tamper detection, like a car alarm
- Protection of log data in transit
  - ![](/assets/images/2022-04-25-17-04-28.png)
- Monitoring of events
  - ![](/assets/images/2022-04-25-17-05-16.png)
- Security concerns for exceptions
  - ![](/assets/images/2022-04-25-17-06-52.png)
- Logging design principles
  - ![](/assets/images/2022-04-25-17-07-43.png)
- Key Takeaways
  1. The threats and weaknesses that impact logging are repudiation, information exposure, omission of security relevant info, insufficient logging, excessive data, and unchecked errors.
  2. Examples of events to include are input/output validation, authentication, authorization, and session management failures.
  3. Exclude any PII or sensitive information from log files.
  4. Protect log data by limiting access, storing read-only, and using secure transmission protocols.
  5. Log the right stuff, save logs for forensics, use a standard format, log high-value transactions, and establish monitoring and alerting.

--- 

