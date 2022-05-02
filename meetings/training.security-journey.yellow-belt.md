---
id: u8y1cfg1uny4p06iddb11yq
title: Training Security Journey Yellow Belt
desc: ''
updated: 1651434733318
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

---

## Module 15: Buffer Overflows & Remote Code Execution
- Occurs when a program attempts to put more data into a buffer than that buffer can hold
- If the attacker can drop to a shell, they can run commands on the server
- Why Care?
  - ![](/assets/images/2022-04-30-14-27-09.png)
- Classic buffer overflow
  - ![](/assets/images/2022-04-30-14-29-16.png)
- Buffer overflow Threats
  - ![](/assets/images/2022-04-30-14-29-32.png)
- Types of buffer overflow
  - ![](/assets/images/2022-04-30-14-32-54.png)
- Mitigations
  - ![](/assets/images/2022-04-30-14-35-36.png)
  - ![](/assets/images/2022-04-30-14-36-09.png)
- Key Takeaways
  1. A buffer overflow occurs when a program attempts to put more data in a buffer than the buffer is setup to hold.
  2. Remote code execution is when an attacker executes any command on a target machine or in a target process across the Internet.
  3. A stack based overflow changes an instruction on the stack, a heap based overflow changes a buffer stored in the heap, and an integer overflow increments larger than what an integer can hold, causing unexpected results.
  4. Mitigate buffer overflows through language choice, safe C libraries, ASLR, NX, and least privilege. 

--- 
## Module 16: Denial of Service
- Denial of Service: An attempt to make a machine or network resource unavailable to its intended users
- Distrubuted DoS: coming from multiple sources, multiple compromised systems are used to target a single system
- 
- Why care?
  - ![](/assets/images/2022-04-30-14-41-24.png)
- Threats
  - ![](/assets/images/2022-04-30-14-43-48.png)
- Types
  - ![](/assets/images/2022-04-30-14-45-20.png)
  - ![](/assets/images/2022-04-30-14-45-49.png)
  - ![](/assets/images/2022-04-30-14-46-09.png)
  - ![](/assets/images/2022-04-30-14-48-08.png)
  - ![](/assets/images/2022-04-30-14-50-09.png)
  - ![](/assets/images/2022-04-30-14-50-19.png)
  - ![](/assets/images/2022-04-30-14-50-56.png)
    - ![](/assets/images/2022-04-30-14-51-52.png)

## Module 17: XXS Part 1
- What is Cross-Site Scripting (XSS)?
  - ![](/assets/images/2022-04-30-15-11-57.png)
- Why care?
  - ![](/assets/images/2022-04-30-15-12-08.png)
- Threats
  - ![](/assets/images/2022-04-30-15-12-44.png)
- Stored or persistent XSS
  - ![](/assets/images/2022-04-30-15-14-49.png)
- Example
  - ![](/assets/images/2022-04-30-15-15-55.png)
  - ![](/assets/images/2022-04-30-15-17-12.png)
- Key Takeaways
  1. Cross site scripting (XSS) is a type of injection attack in which malicious scripts are injected into otherwise benign and trusted web sites.
  2. The prevalence of XSS has been stable for many years and is still a major threat.
  3. Stored or Persistent XSS is when a malicious script is permanently stored, causing a victim to retrieve it when requesting information.

---

## Module 18: XSS Part 2
- Reflected or non-persistent XSS
  - ![](/assets/images/2022-04-30-15-22-12.png)
  - Not stored in a Database
- Reflected XSS example
  - ![](/assets/images/2022-04-30-15-22-37.png)
- DOM based XSS
  - ![](/assets/images/2022-04-30-15-26-56.png)
- Sources and Sinks
  - ![](/assets/images/2022-04-30-15-28-11.png)
- ![](/assets/images/2022-04-30-15-30-49.png)
- Mitigations
  - ![](/assets/images/2022-04-30-15-31-07.png)
- Key Takeaways
  1. Reflected or non-persistent XSS is when an injected script is delivered via an e-mail or other web site and takes the victim to the vulnerable site, which reflects the attack back to the victim’s browser.
  2. DOM Based XSS is when an injected script is inserted into the Document Object Model environment and executes in the victim’s browser.
  3. Stored XSS has a large target range and the vuln exists server side; reflected has a small target range, also existing server side; DOM based has a small target range, and can impact both server and client.
  4. Practice proper mitigations to mitigate XSS, including using frameworks to escape output, review client side for use of sources and sinks, and enact a Content Security Policy to control where JavaScript may originate.

---

## Module 19: Injection: SQL and Command
- ![](/assets/images/2022-04-30-15-39-23.png)
- Why care?
  - ![](/assets/images/2022-04-30-15-39-33.png)
- Types of Injection
  - ![](/assets/images/2022-04-30-15-39-48.png)
- Threats
  - ![](/assets/images/2022-04-30-15-42-37.png)
  - Simple command injection
    - ![](/assets/images/2022-04-30-15-45-59.png)
  - SQL Injection
    - ![](/assets/images/2022-04-30-15-46-18.png)
- Mitigations
  - ![](/assets/images/2022-04-30-15-47-12.png)
  - ![](/assets/images/2022-04-30-15-47-20.png)
- Key Takeaways
  1. Injection is tricking an application into including unintended commands in the data sent to an interpreter.
  2. The major types of injection attacks are SQL, OS Command, LDAP, and XSS.
  3. Mitigate injection in your applications with proper input validation, safe API, and contextual output encoding.

---

## Module 20: Cross Site Request Forgery 
- What is it?
  - ![](/assets/images/2022-04-30-15-53-51.png)
- Why care?
  - ![](/assets/images/2022-04-30-15-54-00.png)
- Example
  - ![](/assets/images/2022-04-30-15-55-58.png)
  - ![](/assets/images/2022-04-30-15-57-05.png)
  - ![](/assets/images/2022-04-30-15-57-13.png)
  - ![](/assets/images/2022-04-30-15-57-19.png)
- Synchronizer Tokens
  - ![](/assets/images/2022-04-30-15-58-14.png)
- SameSite Cookies
  - ![](/assets/images/2022-04-30-16-00-01.png)
- ![](/assets/images/2022-04-30-16-01-44.png)
- Key Takeaways
  1. Cross Site Request Forgery is an attack that forces an end user to execute unwanted actions on a web application in which they're currently authenticated.
  2. The risk presented by CSRF is a successful attack can force the user to transfer funds, change their email address, and so forth. If the victim is an admin, CSRF can compromise the entire web application.
  3. Mitigate CSRF by adding an unpredictable CSRF token with each request, using framework-provided CSRF defenses, and consider an alternate CSRF Defense like requiring user interaction.

--- 

## Module 21: Insecure Communications
- ![](/assets/images/2022-05-01-15-08-56.png)
- Why care?
  - ![](/assets/images/2022-05-01-15-09-03.png)
- Networking sniffing
  - ![](/assets/images/2022-05-01-15-09-29.png)
    - Looks into the packet
- Threat
  - ![](/assets/images/2022-05-01-15-10-12.png)
- Some solutions
  - VPN
  - TRansport Layer Security
    - ![](/assets/images/2022-05-01-15-11-52.png)
- Protocol choices through cipher suites from Mozilla
  - ![](/assets/images/2022-05-01-15-14-53.png)
- Key Takeaways
  1. Insecure communications are the transmission of sensitive or private data in cleartext in a communication channel that can be sniffed by attackers.
  2. The threat presented by insecure communications is the failure to adequately encrypt network traffic using strong cryptography resulting in customer data exposure and compromise.
  3. Consider key exchange, authentication, bulk encryption, and message authentication code when determining if a communication's authentication and encryption are adequate.
  4. When securing network communications, use TLS, serve all pages over HTTPS, use HTTP Strict Transport Security Header, and mark cookies as secure.

---

## Module 22: Social Engineering
- ![](/assets/images/2022-05-01-15-19-46.png)
  - Wolf in sheep's clothing
- Why care?
  - ![](/assets/images/2022-05-01-15-19-56.png)
  - Developers are targeted, they have access to the source code and sys admin's
- Goal of human attack
  - Trick user into
    - Clicking a link
    - Telling a secret
    - Open a (physical) door
- The human factor
  - ![](/assets/images/2022-05-01-15-22-51.png)
- Social engineering vectors
  - ![](/assets/images/2022-05-01-15-23-13.png)
- Tactics
  - ![](/assets/images/2022-05-01-15-23-31.png)
- Social engineering process
  - Gather info > establish rapport > Exploitation > Execution
  - Gather info
    - ![](/assets/images/2022-05-01-15-27-27.png)
    - Salespeople like to share info
  - Establish rapport
    - ![](/assets/images/2022-05-01-15-27-56.png)
  - Exploitation
    - ![](/assets/images/2022-05-01-15-28-45.png)
  - Execution
    - ![](/assets/images/2022-05-01-15-28-58.png)
- Key Takeaways
  1. Human beings without knowledge of social engineering are potentially the weakest links in a system.
  2. Social engineers utilize baiting, spear-phishing, pretexting, shoulder surfing, quid pro quo, phishing, tailgating, dumpster diving, and whaling.
  3. The social engineering process includes gathering information, establishing rapport, exploitation, and execution.
  4. The various scenarios considered included tailgating at the office, engineers receiving phishing emails, talking about confidential information in a public place, and trickery through impersonation.

---

## Module 23: AppSec in an Agile World, Part 1
- Why care?
  - ![](/assets/images/2022-05-01-15-37-18.png)
- Agile basic terms
  - ![](/assets/images/2022-05-01-15-37-51.png)
  - ![](/assets/images/2022-05-01-15-38-23.png)
- Agile Manifesto
  - ![](/assets/images/2022-05-01-15-39-07.png)
- Agile principles impacting security
  - ![](/assets/images/2022-05-01-15-39-34.png)
  - ![](/assets/images/2022-05-01-15-41-49.png)
  - ![](/assets/images/2022-05-01-15-42-58.png)
  - ![](/assets/images/2022-05-01-15-43-07.png)
  - ![](/assets/images/2022-05-01-15-43-15.png)
  - ![](/assets/images/2022-05-01-15-43-21.png)
- Key Takeaways
  1. Agile is the way of the future for software development, and building security in is the only avenue for real security success.
  2. Each of the principles from the Agile Manifesto impact security, and must be considered to build a secure product or application.
  3. The Agile methodology does not include security by default, but the phases of the secure development life cycle map to the stages of Agile.