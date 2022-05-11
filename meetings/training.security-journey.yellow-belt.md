---
id: u8y1cfg1uny4p06iddb11yq
title: Training Security Journey Yellow Belt
desc: ''
updated: 1651709681485
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

---

## Module 24: AppSec in an Agile World, Part 2
- Security needs to be baked in but also include a "Security Focused" sprint every 3-6 sprints
- ![](/assets/images/2022-05-02-17-36-22.png)
- Planning
  - Security requirements
  - Security stories
- Develop
  - Threat modeling and mitigation
  - Security code review
  - Secure coding
  - Static analysis
- Test
  - Dynamic analysis
  - Vulnerability scanning
- Release
  - 3rd Party software
  - PSIRT
- Definition of done and security
  - ![](/assets/images/2022-05-02-17-40-01.png)
- Security focused sprint
  - ![](/assets/images/2022-05-02-17-41-09.png)
- Key Takeaways
  1. Agile is the way of the future for software development, and building security in is the only avenue for real security success.
  2. SDL for Agile focuses on security activities performed in standard and security sprints.
  3. The security activities of a standard sprint include security stories, threat modeling, static analysis, security code review, dynamic analysis, vulnerability scanning, and 3rd party software.
  4. Your Agile Definition of Done must include security activities.
  5. The security activities of a security sprint include privacy assessment, product security baseline, attack surface reduction, and penetration testing.

--- 

## Module 25: AppSec in a DevOps World
- ![](/assets/images/2022-05-02-17-48-45.png)
- Why care?
  - ![](/assets/images/2022-05-02-17-47-38.png)
- All things continuous
  - ![](/assets/images/2022-05-02-17-50-39.png)
- DevSecOps
  - ![](/assets/images/2022-05-02-17-54-07.png)
- Key Takeaways
  1. DevOps is a software development methodology focused on extreme code velocity.
  2. All things continuous include integration, delivery, and deployment.
  3. DevSecOps includes:

---

## Module 26: Security Behaviors in DevOps
- ![](/assets/images/2022-05-02-17-59-03.png)
- Embedding security habits
  - ![](/assets/images/2022-05-02-17-59-37.png)
- Security behaviors and habits
  - ![](/assets/images/2022-05-02-18-00-11.png)
  - ![](/assets/images/2022-05-02-18-00-21.png)
  - ![](/assets/images/2022-05-02-18-00-26.png)
  - ![](/assets/images/2022-05-02-18-00-33.png)
  - ![](/assets/images/2022-05-02-18-00-39.png)
  - ![](/assets/images/2022-05-02-18-00-46.png)
  - ![](/assets/images/2022-05-02-18-00-55.png)
  - ![](/assets/images/2022-05-02-18-01-01.png)
- Key Takeaways
  1. Build security in / start left
  2. Uncover security design problems
  3. React to automated security bugs
  4. Detect security flaws in other’s code
  5. Work towards eradication of 3rd party software vulns
  6. Be mean to your code
  7. Respond in a timely and organized fashion

---

## Module 27: Security Requirements and User Stories
- ![](/assets/images/2022-05-04-16-35-13.png)
- Why care?
  - ![](/assets/images/2022-05-04-16-35-23.png)
- Uses of security reqs
  - ![](/assets/images/2022-05-04-16-41-58.png)
- Positive impact
  - ![](/assets/images/2022-05-04-16-42-10.png)
- Source of security reqs
  - ![](/assets/images/2022-05-04-16-42-27.png)
- 3 phases
  - ![](/assets/images/2022-05-04-16-42-49.png)
- Reference Standard: ASVS
  - ![](/assets/images/2022-05-04-16-43-18.png)
- Key Takeaways
  1. Security requirements are a statement of needed security functionality that ensures one of the many different security properties of software is being satisfied.
  2. Security requirements positively impact development as a roadmap of product/application security improvements, a method to make security repeatable and standard, and as a clear definition of what developers and system architects /designers need to build.
  3. Trusted sources for requirements include industry standards, applicable laws, and vulnerability history.

---

## Module 28: Threat Modeling Basics
- ![](/assets/images/2022-05-04-16-57-24.png)
- Basic application security hygiene
  - ![](/assets/images/2022-05-04-16-57-46.png)
- Why care?
  - ![](/assets/images/2022-05-04-16-58-54.png)
- Benefits
  - ![](/assets/images/2022-05-04-16-59-07.png)
- We all do threat modeling, we just don't think about it
- Security feedback loop
  - ![](/assets/images/2022-05-04-17-00-36.png)
- Threat modeleing in SDL
  - ![](/assets/images/2022-05-04-17-00-54.png)
- Process
  - ![](/assets/images/2022-05-04-17-01-24.png)
- A "good" threat model
  - ![](/assets/images/2022-05-04-17-01-47.png)
  - ![](/assets/images/2022-05-04-17-02-04.png)
- Tools
  - ![](/assets/images/2022-05-04-17-02-33.png)
- Key Takeaways
  1. Threat modeling is an approach for analyzing the design of a feature, application, or product, and eliminating potential security flaws.
  2. Engineers and testers need threat modeling to improve product security, and threat modeling is a skill they already have.
  3. The benefits of threat modeling are building security in, identifying security problems early, and encouraging the security mindset.
  4. The threat modeling process includes scope, draw, analyze, mitigate, and document.

--- 

## Module 29: Threat Modeling Process
- Why care?
  - ![](/assets/images/2022-05-04-17-55-29.png)
- 4 questions to ask
  - ![](/assets/images/2022-05-04-17-55-46.png)
- The process
  - ![](/assets/images/2022-05-04-17-56-18.png)
  - Focus at the Feature/Module level to begin
- Attack Surface Analysis
  - ![](/assets/images/2022-05-04-17-57-49.png)
- Step 2: Draw a Data Flow Diagram (DFD)
  - ![](/assets/images/2022-05-04-17-58-32.png)
  - ![](/assets/images/2022-05-04-17-59-07.png)
- Step 3: Analyze the DFD
  - ![](/assets/images/2022-05-04-17-59-34.png)
  - STRIDE
  - Threat prioritization
    - ![](/assets/images/2022-05-04-18-01-09.png)
- Step 4: Mitigate
  - ![](/assets/images/2022-05-04-18-01-27.png)
- Step 5: Document
  - ![](/assets/images/2022-05-04-18-03-05.png)
- Key Takeaways
  1. The four questions of threat modeling are “what are we building”, “what can go wrong”, “what are we going to do about that”, and “did we do a good enough job”.
  2. The threat modeling process is light weight, including:
     1. ▶ Step 1: Scope
     2. ▶ Step 2: Draw
     3. ▶ Step 3: Analyze
     4. ▶ Step 4: Mitigate
     5. ▶ Step 5: Document
  3. Use STRIDE to enumerate threats in a DFD and apply compensating controls to mitigate threats.

--- 

## Module 30: Threat Modeling Examples
- Why care?
  - ![](/assets/images/2022-05-04-18-07-26.png)
- Never use telnet for anything
- Insecure example with telnet
  - ![](/assets/images/2022-05-04-18-07-57.png)
  - STRIDE
    - ![](/assets/images/2022-05-04-18-08-09.png)
  - Threats
    - ![](/assets/images/2022-05-04-18-08-21.png)
  - Mitigations
    - ![](/assets/images/2022-05-04-18-08-49.png)
  - A web app
    - ![](/assets/images/2022-05-04-18-09-27.png)
  - Client-side JS
    - ![](/assets/images/2022-05-04-18-09-38.png)
  - STRIDE
    - ![](/assets/images/2022-05-04-18-10-12.png)
    - User could disable JS on their side
    - Mitigate: perform auth on the server-side; move trust boundary
  - Library Web app: authentication
    - ![](/assets/images/2022-05-04-18-11-08.png)
    - STRIDE
      - ![](/assets/images/2022-05-04-18-11-19.png)
    - Threats
      - ![](/assets/images/2022-05-04-18-11-35.png)
    - Mitigations
      - ![](/assets/images/2022-05-04-18-12-14.png)
- Key Takeaways
  1. Threat modeling examples provide you a working demonstration of how to implement the threat modeling process.
  2. The data flow diagram for the telnet, client-side, and library threat models is the collection point for how a feature or application works.
  3. STRIDE is applied to the data flow diagram as a starting point for the threats that exist.
  4. Documented threats require mitigations; mitigations are the changes to the design that improve security.

---

## Module 31: Static Application Security Testing (SAST)
- ![](/assets/images/2022-05-04-18-25-48.png)
- Why care?
  - ![](/assets/images/2022-05-04-18-25-55.png)
- Focus
  - ![](/assets/images/2022-05-04-18-26-09.png)
- Benefits
  - ![](/assets/images/2022-05-04-18-27-10.png)
- False positives and negatives
  - ![](/assets/images/2022-05-04-18-27-29.png)
  - No tools are perfect!
- Traits
  - ![](/assets/images/2022-05-04-18-27-45.png)
  - Whitebox, access to source code
- How SAST works
  - ![](/assets/images/2022-05-04-18-31-08.png)
- Classes of SAST findings
  - ![](/assets/images/2022-05-04-18-31-53.png)
- Use cases
  - ![](/assets/images/2022-05-04-18-32-06.png)
- Developer workflow
  - ![](/assets/images/2022-05-04-18-32-20.png)
- SAST offerings
  - ![](/assets/images/2022-05-04-18-32-38.png)
- Key Takeaways
  1. No single tool provides an application security silver bullet; choose a suite of tools that best meets your needs.
  2. SAST is static application security testing; a set of technologies that analyze application source code, byte code for security vulnerabilities.
  3. The use cases for SAST are One off, Nightly, CI/CD and Desktop / IDE integrated
  4. The SAST workflow for a developer includes Scan, Triage, Fix and Document.
  5. There are multiple options in the open source and commercial space for SAST tools.

---

## Module 32: Dynamic Application Security Testing
- ![](/assets/images/2022-05-04-18-37-33.png)
- Fuzzing
  - ![](/assets/images/2022-05-04-18-37-41.png)
- Why care?
  - ![](/assets/images/2022-05-04-18-37-49.png)
- Focus of DAST
  - ![](/assets/images/2022-05-04-18-38-26.png)
- Focus of fuzzing
  - ![](/assets/images/2022-05-04-18-38-48.png)
- DAST and SDL
  - ![](/assets/images/2022-05-04-18-39-05.png)
- Benefits
  - ![](/assets/images/2022-05-04-18-39-17.png)
- Traits
  - ![](/assets/images/2022-05-04-18-39-31.png)
- How DAST works
  - ![](/assets/images/2022-05-04-18-39-52.png)
- Classes of DAST findings
  - ![](/assets/images/2022-05-04-18-41-16.png)
- Classes of fuzz findings
  - ![](/assets/images/2022-05-04-18-41-32.png)
- Use cases
  - ![](/assets/images/2022-05-04-18-41-46.png)
- Developer workflow
  - ![](/assets/images/2022-05-04-18-42-02.png)
- DAST offerings
  - ![](/assets/images/2022-05-04-18-42-19.png)
- Fuzzing offerings
  - ![](/assets/images/2022-05-04-18-42-35.png)
- Key Takeaways
  1. No single tool provides an application security silver bullet; choose a suite of tools that best meets your needs.
  2. DAST is dynamic application security testing; a set of technologies that detect security vulnerabilities in an application in its running state.
  3. Fuzzing is an automated software testing technique that involves providing invalid, unexpected, or random data as inputs.
  4. The use cases for DAST/Fuzz are One off, Nightly, and CI/CD.
  5. The DAST/Fuzz workflow for a developer is Define, Execute, Triage, Remediate, and Rescan.
  6. There are multiple options in the open source and commercial space for DAST/Fuzz tools.

---

## Module 33: Next Gen AppSec Tools
- ![](/assets/images/2022-05-04-19-19-03.png)
- Why care?
  - ![](/assets/images/2022-05-04-19-18-52.png)
- IAST
  - ![](/assets/images/2022-05-04-19-19-34.png)
  - Focus
    - Web apps
  - Agent that runs in app
    - ![](/assets/images/2022-05-04-19-20-06.png)
- RASP
  - ![](/assets/images/2022-05-04-19-20-21.png)
  - Focus
    - ![](/assets/images/2022-05-04-19-20-37.png)
  - ![](/assets/images/2022-05-04-19-20-48.png)
    - Can block attacks and deny
- Next gen and SDL
  - ![](/assets/images/2022-05-04-19-21-03.png)
- SCA
  - ![](/assets/images/2022-05-04-19-21-42.png)
  - Focus
    - ![](/assets/images/2022-05-04-19-21-53.png)
  - ![](/assets/images/2022-05-04-19-22-01.png)
- CWPP
  - ![](/assets/images/2022-05-04-19-22-46.png)
  - Focus
    - ![](/assets/images/2022-05-04-19-22-57.png)
  - ![](/assets/images/2022-05-04-19-23-06.png)
- Next Gen and SDL
  - ![](/assets/images/2022-05-04-19-23-44.png)
- IAST & RASP offerings
  - ![](/assets/images/2022-05-04-19-24-12.png)
- SCA & CWPP
  - ![](/assets/images/2022-05-04-19-24-34.png)
- Key Takeaways
  1. IAST is interactive application security testing, and is used to discover vulnerabilities from the inside of the application in test.
  2. RASP is runtime application self protection, and is used to detect and block vulnerabilities from the inside of the application in production.
  3. SCA is software composition analysis, and is used to detect known vulnerable components so they can be upgraded or replaced. CWPP is a set of technologies that secure virtual machines, containers and serverless workloads in public and private clouds. The next generation of AppSec tools provide new capabilities, and should be examined for inclusion in your program.

---

## Module 34: Vulnerability Scanning
- ![](/assets/images/2022-05-04-19-31-11.png)
- Why care?
  - ![](/assets/images/2022-05-04-19-31-25.png)
- Focus
  - ![](/assets/images/2022-05-04-19-31-37.png)
- In the SDL
  - ![](/assets/images/2022-05-04-19-31-53.png)
- Benefits
  - ![](/assets/images/2022-05-04-19-33-58.png)
- Traits
  - ![](/assets/images/2022-05-04-19-35-21.png)
  - A credentialed vulnerability scan means you tell the vulnerability scanner how you log in to the system. By giving it an actual username and password that works, when it does the scan, it not only looks at the system from the outside, it logs into the system and scans it from the inside to see if there are any problems.
- Process
  - ![](/assets/images/2022-05-04-19-36-05.png)
- How scanning works
  - ![](/assets/images/2022-05-04-19-38-10.png)
- Classes of findings
  - ![](/assets/images/2022-05-04-19-38-31.png)
- Workflow
  - ![](/assets/images/2022-05-04-19-39-38.png)
- Offerings
  - ![](/assets/images/2022-05-04-19-39-49.png)
- Key Takeaways
  1. No single tool provides an application security silver bullet; choose a suite of tools that best meets your needs.
  2. Vulnerability scanning is a comprehensive evaluation of a system for exposed vulnerabilities without their direct exploitation.
  3. A vulnerability scanner checks if the remote host is alive, and then performs firewall detection, TCP / UDP Port Scan, OS Detection, TCP / UDP Service Discovery, and finally Vulnerability assessment.
  4. Vulnerability scans are performed as one-offs, against nightly builds, and integrated into CI/CD.
  5. A developer uses a vulnerability scanner by scan definition, execution, report, triage, remediate of issues, and rescan.

---

## Module 35: Pen Testing & Bug Bounty
- Pen Testing
  - ![](/assets/images/2022-05-04-19-51-28.png)
- Bug bounty
  - ![](/assets/images/2022-05-04-19-51-38.png)
- Why care?
  - ![](/assets/images/2022-05-04-19-51-54.png)
- Focus
  - ![](/assets/images/2022-05-04-19-52-11.png)
- In the SDL
  - ![](/assets/images/2022-05-04-19-53-05.png)
- Benefits
  - ![](/assets/images/2022-05-04-19-53-20.png)
- How pen testing work
  - ![](/assets/images/2022-05-04-19-53-42.png)
  - Documentation is very important
- Process
  - ![](/assets/images/2022-05-04-19-54-53.png)
- How to choose a pen testing company
  - ![](/assets/images/2022-05-04-19-55-50.png)
- How bug bounty works
  - ![](/assets/images/2022-05-04-19-56-11.png)
- Basics of bug bounty
  - ![](/assets/images/2022-05-04-19-56-56.png)
- Process
  - ![](/assets/images/2022-05-04-19-57-30.png)
- Offerings
  - ![](/assets/images/2022-05-04-19-57-47.png)
- Key Takeaways
  1. Penetration testing is an authorized simulated attack on a computer system, performed to evaluate the security of the system.
  2. Bug bounty is a crowdsourcing initiative that rewards individuals for discovering and reporting software bugs.
  3. The benefits of pen testing and bug bounty are they find missed vulnerabilities, test internal response, and augment internal efforts with outside experts.
  4. The pen testing process includes evaluate and choose a partner, scope and goal setting, discovery, exploitation, and documentation.
  5. The bug bounty process includes establish goals, set scope, engage participants, review and prioritize submissions, pay for results, and fix.

--- 

## Module 36: Secure Code Review, Part 1
- ![](/assets/images/2022-05-04-20-02-03.png)
- Why care?
  - ![](/assets/images/2022-05-04-20-02-22.png)
- Purpose
  - ![](/assets/images/2022-05-04-20-03-00.png)
- Process
  - ![](/assets/images/2022-05-04-20-03-16.png)
- Checklist
  - ![](/assets/images/2022-05-04-20-03-52.png)
  - It's important to remember the question we're asking here is what you, as a developer, need to ask of the code you're reviewing at the moment. Take the question, and then look at the code and say, "How do I answer that question?" If you find enough evidence that the question is true, and there are ways to achieve it, you're good; it's not a finding.
- ![](/assets/images/2022-05-04-20-05-51.png)
- ![](/assets/images/2022-05-04-20-05-57.png)
- ![](/assets/images/2022-05-04-20-06-04.png)
- ![](/assets/images/2022-05-04-20-06-10.png)
- Key Takeaways
  1. Secure code review is an examination of source code intended to find mistakes overlooked in development, improving the overall quality of software.
  2. The purpose of a secure code review is to refactor, detect and fix errors, and expose vulnerabilities.
  3. The process for performing secure code review includes analyze, review, triage, remediate, review again, and close.
  4. Ask security questions each time you review code; consider input validation, server side validation, output encoding, and default/hard coded credentials.

---

## Module 37: Secure Code Review Part 2
- Why care?
  - ![](/assets/images/2022-05-04-20-14-06.png)
  - Secure code review is all about discovering potential vulnerabilities in the code we write. There will be problems with security in the code we write, the code we review. We go through this process to try to eliminate those as early as possible.

We're setting up the process for outlining a blueprint of the types of questions you need to be asking about the code that you're reviewing for security purposes. As a developer, ask these questions about your code. Does my code do this? If it doesn't, then there's a problem.


Are all SQL queries parameterized?

I'm looking at a particular snippet of code; it's making a database call, and I need to examine that code to conclude if they are using parameters in that SQL query. Are they using string concatenation? If I see string concatenation, that means there's potential for SQL injection, and then that's a high priority finding.


We have a series of questions related to user management and authentication. Question number one, is authentication implemented in a central way that applies to all pages?

I'm looking at a snippet of code, and I'm looking to determine if authentication is being performed. Is it being done in a centralized way? The reason I'm looking for that is if authentication is being implemented differently for different parts of an application, then that tells me I need to take a closer look at how they're doing each of those individual ways. There could very easily be problems in the first one and no problems in the second one. We're calling for a standard approach because then you have one implementation, then I can spend a lot of time reviewing the code for that one implementation, and know that it's used across the entire application.

A second question related to user management and authentication is, what functionality can be accessed without authentication?

As I'm looking at this piece of code, I'm looking to see if it requires authentication. If it requires authentication and doesn't, that's a big deal; we want to get that fixed. I'm trying to determine if authentication is needed for the piece of code I'm looking at.

The third question, are security checks placed before processing inputs?

We want to ensure we're doing input validation even on authentication data because an attack can be disguised as a legitimate input. We're looking at this code to determine if input validation is done first, and then authentication checks are being processed, or is it reversed? If they're making authentication decisions first, we want to ensure that input validation is applied earlier.

Our final question related to this topic, if passwords are operated upon in this section of code, is a password complexity check enforced on the password?

If this application or product requires password complexity, it must be checked in the authentication routine. We want to look at that code to see if it is enforcing the complexity the way we expect it to according to our organizational policy.


Now we come to session management. The first question we want to ask is, are sessions handled correctly and securely?

We're looking to see, first of all, does the application have sessions? Often, we get session management from whatever framework, whatever language we're relying upon, but not necessarily all the time. We have to ask that; it seems like a simple question. But we do have to say, is there an approach for sessions? Is it being done securely? Some of the flags that can be set for cookies we want to ensure are done. Those are the types of things we're doing when we do that overarching view of session management. If we find that some of those things are not being done, those will be findings.

The obvious next question, is session data validated?

We've seen lots of times where applications use sessions, but they never check them. They're going through all the trouble of creating a session ID value, and then that session ID gets sent back to the server, then they determine if it's valid or not. That's something I'm looking for when I'm looking at session management code.

Finally, are sessions stored in a secure manner?

That's another piece we need to look at from a session management perspective. The session ID is very valuable, because if an attacker gets access to that session ID, they may get into the application. We want to see how those things are being stored on the server-side. If they're being stored on the client-side, we want to take a closer look to determine if they're being stored, should they be stored, or where they are being stored? And if they are, is it truly secure?

With session management, we're looking at how session sharing is done. How is the system going to relate to multiple users logging in at the same time? Or the same user logging in multiple times across different devices? We're looking to see if the application is passing session parameters and URLs, which is bad because they can get recorded at other places we don't intend. Are they using unencrypted session keys? Weak session IDs are a problem. We want to look at how they're generating their session IDs to say, if you have a session ID at one, then that tells me the next one's probably going to be two, which would be bad because I can guess the session ID you're using along the way.


Let's move on to authorization. The first question is, are authorization checks granular (page and directory level)? And for all resources?

This gets back to the same issue we talked about with authentication. Is there a centralized approach to authorization? Is it being done granularly at the page, at the directory level? Is it being applied to all resources? We're coming back around to, is it central? If not, we need to look at all the schemes used for authorization throughout the code.

The next question is, is authorization based on clearly defined roles?

I'm looking at the code; I'm looking to see if they're doing role checks and if it's being done predictably and consistently. Are there 17 different roles defined in this small block of 100 lines of code? If there are, that's probably an issue, and we probably need to reevaluate. Things might be working correctly, but there's probably a bigger challenge in how they've approached the architecture.

Next, is there execution stopped/terminated after invalid requests, i.e., when the authentication/authorization check fails?

We're going through, and we're saying, "what happens in this code block if authorization does fail?" The determination is, "Hey, you don't have access." We're tracing to ensure that there isn't some potential back door where somebody could drop through an authorization check and have access when they shouldn't have it.

The next question, are the checks correctly implemented?

In our block of code, when there's an authorization check, we're going to look at that piece of code to say, "Hey, are they doing what we expected them to do?" Are they checking against the policy? This is how we do authorization for our application and our product.

Our final question related to authorization is, is the check applied on all the required files and folders?

This is an authorization from a file-level access perspective, something your application is controlling, whether one user can store files that only they have access to. We have to check the code to ensure there isn't some scenario where someone could access a file they're not supposed to.


Next up is cryptography. Our first question is, is the password stored in an encrypted format? With authentication and cryptography working together, when we have passwords, we have to store them securely. We're looking to see how the application or product is storing the representation of the password. We're looking to confirm they're using a password hash, the proper salt, randomness, and the right algorithm to hash the stored passwords.

We want to ask the same question of database credentials, so are database credentials stored in an encrypted format? With this, it may mean we're looking at configuration files that are part of the application or product that we're doing the code review on. Because we're saying secure code review, that also means we can go into the configuration files. They're part of the code review process. We want to confirm that there are no database credentials stored in plain text anymore.

Now we get to the movement of data. Is the data sent on encrypted channels? That's going to come out in the code. There's going to be code to send data, whether it's the result of a request coming into a web application or whether it's a product communicating with a client or another version of the product somewhere. Data will be sent; we're looking to see in the code if we're doing encryption on the information sent from point A to point B.

When we get to PII and sensitive information, is that sent over the network in encrypted form? Whenever I look at a block of code, I'm always looking for personally identifiable information that could be in play, because if I see that, that means we have to be careful. We have to dial in and focus on this block of code because PII ultimately leads to data breaches if there are vulnerabilities in that code. It means we have to be more on guard when we see that type of data processed. The other thing is to verify the data is sent in an encrypted form.

Next, we want to ask, are the application's cryptographic functions the most recent versions of the protocols? If you see DES encryption, which is ancient, if you see MD5 as a hash, that is a gigantic finding. That's the type of thing we want to answer with this question, are there old versions of protocols that need to get ripped out that are relied upon in this block of code?

Finally, are plain text secrets stored in memory for extended periods of time? We're using passwords or keys in our systems. The question is, is this block of code using and storing that value and leaving it in memory? Or does it use it and then dispose of it, so that it doesn't even exist in memory? We can do a lot of really secure things, but if we leave the keys on the counter, and the house is unlocked---someone's going to drive off with your car.


We now come to logging and error handling. Are logs logging personal information, passwords, or other sensitive information? When I do a code review, I always look for how logging is performed. Then I start to scan all the created logs because a lot of times, as developers, we'll leave debug logs in for our benefit, and we don't always remember to delete them. When I'm looking at someone else's code, I'm always on guard to look for places where personal information is logged. Are there log statements that don't even need to be there anymore? I'm a firm believer in, keep it as simple as possible. If we don't need all these extra debug things there, let's take them out when we're done doing our debugging.

Next, do audit logs log connection attempts, both successful and failures? I'm looking for the way the system application product relates to individual connections. Suppose the code is processing a connection request coming inbound. Is it properly auditing what's happening, both from a positive perspective when somebody was supposed to get in, and from a negative perspective, when someone wasn't supposed to get access?

Our third and final question, is the password disclosed to the user or written to a file, logs, or console? With this one, we're paying attention to when we see a password. We want to check whether the password is never written out to the user directly in a plain text, unscrambled format. That could be an authentication page, where we want to make sure that there are stars, for example, in place of the password. We want to make sure there's never a case where we can give the user their password because it's stored in our system. If we ever see that in code, that is a gigantic finding. We never want to print out a password for somebody into their view. From a log file, console perspective, people will accidentally write a password as part of a log record. That's a big no-no, and if we see that, we need to get that fixed fast.


We've talked a little bit about configuration files, but the key question we want to ask about security configuration is, is there any sensitive data in configuration files? We mentioned earlier that configuration files are part of our code. In this step, you should be searching the configuration files for any sensitive information like passwords, database strings, or keys; things that you can see printed out that would be stored in the source code control system. When they're in the source code control system with sensitive information included, anybody who has access to that code will see the actual values, such as a password.


Race conditions are where you have two threads trying to access the same variable or the same piece of data. They can get into some security challenges when it isn't predictable as far as which thread gets to update the piece of information, and if things aren't being done correctly. This can impact C and C++; it can also impact Java and C# if you get into the nitty-gritty details of dealing with threads. Most of the other languages will obstruct you away from that, which is a nice thing.

The second one I want to consider here is buffer overruns specific to the world of C and C++. Buffer overflows and buffer overruns result from not doing proper input validation when you take a piece of data from the user or the network. The guidance here is you want, in your C and C++ context, to be looking at where data is coming from and ensuring it's properly validated. Use routines in your program, which will not allow you to put too much data into a buffer, causing the buffer overrun.

One of the interesting takeaways from the secure code review modules is just how much there is to remember, which could feel intimidating. That's why we created the checklist. If any of these questions are not asked and answered securely, it introduces vulnerabilities. The checklist is the solution to this problem because, as a developer, you don't want to remember all of these things, but you should understand what they are. I want the checklist to go through and ensure that I connect with each of them, check it off, and make sure there isn't an actual problem in the code I'm reviewing.

Key Takeaways
Ask security questions each time you review code.
Consider: parameterized SQL queries, user management and authentication, session management, authorization, cryptography, logging/error handling, and security configuration.