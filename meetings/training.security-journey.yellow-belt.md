---
id: u8y1cfg1uny4p06iddb11yq
title: Training Security Journey Yellow Belt
desc: ''
updated: 1651151420434
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

## Module 9: Cryptography
- ![](/assets/images/2022-04-26-17-46-26.png)
- Why care?
  - To protect data in transit and at rest
- Key
  - ![](/assets/images/2022-04-26-17-48-33.png)
  - Locks or unlocks data that is encrypted or decrypted
- Cipher
  - ![](/assets/images/2022-04-26-17-49-00.png)
  - An algorithm that performs encryption or decryption
- Symmetric Encryption & Decryption
  - Same key used for encryption and decryption
  - Shared key
  - Examples: VPN
- Asymmetric Encryption
  - Public/private key
  - Keys can be different
  - Examples: PGP or GPG email encryption
- Certificate
  - ![](/assets/images/2022-04-26-17-54-34.png)
  - Prvoes that a the webserver is bound to a particular domain name because it is signed by a trusted third party the browser has a trust relationship with cryptographically
- Hashing
  - Hashed value, smaller representation of the original value
- Digital Signature
  - ![](/assets/images/2022-04-26-17-57-24.png)
  - Asymmetric
  - Proves the authenticity
- Symmetric and asymmetric ciphers
  - ![](/assets/images/2022-04-26-17-59-24.png)
- Cryptographic guidance
  > Another resource comes from the National Institute of Standards and Technology (NIST) that's part of the United States government. It is called the Approved Security Functions for FIPS 140-2, Security Requirements for Cryptographic Modules. FIPS 140-2 is the US government and some other government standards for testing cryptography. They do have a set of best possible things that you should be using today. They update it frequently.

- Key Takeaways
  1. Basic cryptographic terms include key, cipher, certificate, plaintext, ciphertext, and hashing.
  2. Encryption uses a key to transform plaintext into ciphertext, while decryption uses a key to transform ciphertext into plaintext.
  3. Symmetric uses the same key, and asymmetric uses a public and private key pair.
  4. Digital signatures prove authenticity.
  5. Rolling your own crypto is a terrible idea because you too can create an algorithm that you yourself cannot break.​

---

## Module 10: Risk Management for AppSec
- ![](/assets/images/2022-04-26-18-15-16.png)
- Why care?
  - ![](/assets/images/2022-04-26-18-15-28.png)
- Risk Management Process
  - ![](/assets/images/2022-04-26-18-20-29.png)
- Risk Management Principles
  - ![](/assets/images/2022-04-26-18-21-52.png)
  1. ![](/assets/images/2022-04-26-18-22-22.png)
  2. ![](/assets/images/2022-04-26-18-22-37.png)
  3. ![](/assets/images/2022-04-26-18-22-47.png)
  4. ![](/assets/images/2022-04-26-18-22-56.png)
  5. ![](/assets/images/2022-04-26-18-23-05.png)
  6. ![](/assets/images/2022-04-26-18-23-12.png)
  7. ![](/assets/images/2022-04-26-18-23-21.png)
  8. ![](/assets/images/2022-04-26-18-23-32.png)
  9. ![](/assets/images/2022-04-26-18-23-41.png)
  10. ![](/assets/images/2022-04-26-18-23-48.png)

- Key Takeaways
  1. Risk management is the program and supporting processes to manage information security risk to operations, assets, individuals, and other organizations
  2. The risk management process includes identify the risk, analyze the risk, evaluate or rank the risk, treat the risk, and monitor and review the risk
  3. Apply the principles of effective cybersecurity risk management to minimize the unknown risk in your application security program.

---

## Module 11: The Hacker Mindset
- ![](/assets/images/2022-04-27-16-47-24.png)
- Thacker attitude
  - ![](/assets/images/2022-04-27-16-51-35.png)
- Hacker view
  - No such thing as 100% secure
  - Least resistance
  - Outside box thinking
- Applying hacker mindset
  - ![](/assets/images/2022-04-27-16-55-12.png)
- Key Takeaways
  1. A “hacker” is any skilled computer expert that uses their technical knowledge to overcome a problem.
  2. The word “hacker” does not imply any criminal intent.
  3. The hacker mindset includes recognizing that the world is full of fascinating problems waiting to be solved, avoiding solving the same issues and boredom, embracing freedom and competence.
  4. Apply the hacker mindset to your job role by extending competence, using threat modeling/vuln scanning/pen testing, and utilize a white-hat hacking approach.

---

## Module 12: OWASP Top 10 Part 1
![](/assets/images/2022-04-27-17-00-44.png)
- A01 Broken Access Control
  - ![](/assets/images/2022-04-27-17-11-24.png)
  - Includes privileges
  - Risks
    - Unauthorized info disclosure
    - Modification/destruction of data
    - Elevation of privilege
  - Mitigations
    - ![](/assets/images/2022-04-27-17-19-22.png)
    - JWT token, the server must invalidate it after logging out to prevent replay attacks
- A02 Cryptographic failures
  - ![](/assets/images/2022-04-27-17-22-23.png)
  - Risks
    - ![](/assets/images/2022-04-27-17-22-44.png)
  - Mitigations
    - ![](/assets/images/2022-04-27-17-23-02.png)
    - If we don't need the data, we should get rid of it
    - MAC - message authentication code
- A03 Injection
  - ![](/assets/images/2022-04-27-17-24-43.png)
  - The attacker is trying to get their data to execute as a command on your system and then return some result
  - Risks
    - ![](/assets/images/2022-04-27-17-26-04.png)
    - Exfiltration leads to a breach
  - Mitigations
    - ![](/assets/images/2022-04-27-17-26-52.png)
    - ORM's are not necessarily 100% safe
- Key Takeaways
  1. The OWASP Top 10 list is best used as an awareness tool for securing web applications.
  2. Implement access control using a deny by default approach.
  3. Classify data by sensitivity and implement appropriate cryptographic controls.
  4. Use an ORM (Object Relational Mapper), input validation, and escape characters to mitigate injection attacks.

## Module 13: OWASP Top 10 Part 2
- A04 Insecure Design
  - ![](/assets/images/2022-04-27-17-47-01.png)
  - Need to start planning for security upfront!!!
  - Risks
    - Leads to exploitation of all other OWASP Top 10 issues
  - Mitigations
    - ![](/assets/images/2022-04-27-17-50-30.png)
    - Secure Development Lifecycle
    - Embrace Threat Modeling
- A05 Security Misconfigurations
  - ![](/assets/images/2022-04-27-17-53-12.png)
  - Someone makes a mistake
  - Risks
    - Data exposure
  - Mitigations
    - Harden builds
    - Consistent
    - Minimal
      - Only install what's absolutely needed, minimize attack surface area
    - Automated
      - Implement an automated process to verify the configuration and settings
- A06 Vulnerable and Outdated Components
  - ![](/assets/images/2022-04-27-17-56-59.png)
  - Risks
    - ![](/assets/images/2022-04-27-17-57-47.png)
  - Mitigations
    - ![](/assets/images/2022-04-27-17-58-46.png)
- A07 Identification and Authentication Failures
  - ![](/assets/images/2022-04-27-17-59-53.png)
  - Identification = telling information
  - Authentication = proving the info is correct
  - Risks
    - System access
    - Admin access
  - Mitigations
    - ![](/assets/images/2022-04-27-18-03-26.png)
- Key Takeaways
  1. Establish and use a secure development lifecycle and embrace Threat Modeling.
  2. Implement an automated process to verify the configuration and settings.
  3. Use Software Composition Analysis, continuously inventory, and monitor libraries and components.
  4. Utilize Multi-Factor Authentication, replace default credentials, and implement weak password checks.

---

## Module 14: OWASP Top 10 Part 3
- A08 Software and Data Integrity Failures
  - ![](/assets/images/2022-04-28-08-39-31.png)
  - Not protecting our infrastructure or code from integrity violations
  - Risks
    - Unauthorized accessed
    - Malicious code inclusion
    - RCE (remote code execution) from insecure deserialization
  - Mitigations
    - Digital signatures
      - Ensures updates into our packages haven't been modified and are coming from a trusted, verified source
    - SCA (Software composition analysis)
      - A tool to scan our dependencies and package to make sure vulnerabilities were not introduced
    - Peer code review
    - Data integrity checks
      - Make sure serialized objects when deserialized come in just like the way it was sent and hasn't been manipulated
- A09 Security Logging and Monitoring Failures
  - ![](/assets/images/2022-04-28-08-48-17.png)
  - Could be insufficient logging
  - Risks
    - Successful attacks start with vulnerability probing. Remaining undetected raises chances of success
  - Mitigations
    - ![](/assets/images/2022-04-28-08-58-47.png)
- A10 Server-side Request Forgery
  - ![](/assets/images/2022-04-28-09-00-35.png)
  - Newer
  - Has caused several big breaches 
  - Attacker can manipulate some URLs the app is taking in as input, to fetch some resource
  - ![](/assets/images/2022-04-28-09-03-18.png)
  - ![](/assets/images/2022-04-28-09-05-05.png)
    - Attack web server itself
    - Attack internal system
      - Points towards another server within our trusted network
    - Attack to point towards a third-party system
  - Risks
    - ![](/assets/images/2022-04-28-09-07-53.png)
      - Attacker can view a map of the network
  - Mitigations
    - ![](/assets/images/2022-04-28-09-09-07.png)
- Key Takeaways
  1. Use digital signatures, Software Composition Analysis, code reviews, and data integrity checks to prevent software and data integrity failures.
  2. Ensure to log all login, access control, and server-side input validation failures and generate an audit trail for high-value transactions.
  3. Prevent Server-Side Request Forgery (SSRF) with a zero-trust architecture and do not accept untrusted input to fetch resources.