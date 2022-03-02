---
id: iw9gFlAQROflJbNgxzCbo
title: Security Journey
desc: ''
updated: 1646151974766
created: 1645541776502
---

---
---
#### All images are owned by Security Journey
- This is strictly to capture my notes
---
---
# Module 1: Intro
- Security level
    - recognition of an achievement
- Showing how to use the Dojo
- 20-30 questions per Assessment
- Experiments are available, live-code editor
- __Tip 1:__ Embrace the game elements of the platform, have fun with it
- __Tip 2:__ Create a plan that works for you
- __Tip 3:__ Remember, security is a journey, not a destination, you never learn everything

# Module 2: Intro to Security
- Connected world, simple software error could lead to loss in lots of money
- coveted assets and clients data need to be protected

- People, Process, Tools
    - All neccessary to be secure
- Attackers
    - There are many different types
- Finding, fixing and preventing security problems

- Threat - possible danger that might breach security, could become a risk
- Risk
- Attack surface
    - All the different interfaces that an attacker can approach 

- Builder
    - Developer building something
- Breaker
    - People who are trying to break into something
- Defender
    - People looking to overall secure something

- Need to have Shared Responsibility, security awareness

# Module 3: Core Security Concepts
![](/assets/images/2022-02-08-13-48-13.png)

# Module 4: Attacks

### Anatomy of an Attack
![](/assets/images/2022-02-22-10-00-23.png)

- Attackers will take measures to clean up and cover their tracks

### Types of attacks
![](/assets/images/2022-02-22-10-02-27.png)
- Buffer overflow = privileged access 
- (Distributed) Denial of Service = getting system offline
    - Typically only takes a single packet and can be repeated
    - DDoS, a more coordinated attack, floods the network
- Social Engineer
    - Human-based attack, tricking people with stories
    ![](/assets/images/2022-02-22-10-16-55.png)

### Results of Attacks
- System or App compromised
- Data breach
    - Customer and user info can be shared to people that have no right to see it
- Malware and ransomware

# Module 5: Adversaries
- Knowing about the adversaries helps us defend against them
![](/assets/images/2022-02-22-10-31-31.png)

### Motivations
- Financial gain
- Espionage
    - Could be theft of intellectual property
- Fun
- Grudge

### Cybercrime Revenues
![](/assets/images/2022-02-22-10-36-28.png)

### Depths of Internet
- Surface net
- Deep net
    - Not search engine accessbile
- Dark net
    - No search engine, usually need special applications to access
    - Typically illicit activity
### Cost of Dark Net on Data
- Data is worth a loooooot!
![](/assets/images/2022-02-22-10-39-26.png)

### Advanced Persistent Threat (APT)
![](/assets/images/2022-02-22-10-40-31.png)
- Typically funded by governments
- Target specific econ sectors
- Use public and non-public malware
- Specific attack vectors
    - Helps to figure out where they are coming from 

### Why care?
- Helps keep us protected

# Module 6: Data Breaches
### Why care?
- If a company's data has been breached it will make headlines and make this known to many people
    - People can look for this
    - Make's companies look bad too
### Business impact
![](/assets/images/2022-02-22-10-47-16.png)

### Common "story" of a data breach
- Attacker researches target
- Attacks
- Exfiltration

### Data breaches average cost
![](/assets/images/2022-02-22-10-49-09.png)
- The longer it goes undetected, the more time a malicious person has

### Verizon DBIR
![](/assets/images/2022-02-22-10-50-00.png)

### Learning - Case Studies
- On average there are 2000 data breaches a year
#### Equifax
- Lack of patching
- Lateral movement
- Exfiltration
- Lack of disclosure
    - The company waited waaaay too long to share with public
- Lessons learned
![](/assets/images/2022-02-22-10-54-30.png)
#### PDL/OxyData
- These companies scrape data from internet and put into one location
- 1.2 billion people
- Elastic search server was publicly available
- Lessons learned
![](/assets/images/2022-02-22-10-56-53.png)
- Still don't know who's behind this
#### Marriot
- Scope - 383 million people
- After acquiring a reservation system, there was a vulnerability in that system
![](/assets/images/2022-02-22-10-59-18.png)

> Patching should be done regularly, especially after a vulnerability has been announced in a third-party application or platform you use.

# Module 7: Security Business Case

### Why care?
- Customers trust you with their data with the expecation that you'll protect their data!

### Customer Mindset
![](/assets/images/2022-02-22-11-13-25.png)
- 81% of people would stop using a company after a breach
- 55% would be turned off of a company if their personal data was shared without their permission
    - What amount of info is actually pertinent

### Shifting left and shifting right
- Security should really be a part of the SDLC (Shift left)
- Being more reactive (Shift right) vs. proactive (Shift left)
![](/assets/images/2022-02-22-11-16-28.png)

### Security excuses
- **Excuse:** Resources are tight
    - More resources will be req. later if not fixed
- **Excuse:** Need to ship product
    - Product needs to be shipped securely!
- **Excuse:** Competitive pressure
    - Differenitated from competitors when it's secure
- **Excuse:** Methodology does not support security
    - It needs to be a part of every step of the process

### Value model for security
- Keep business available for daily operations
![](/assets/images/2022-02-22-11-20-06.png)

![](/assets/images/2022-02-22-11-20-45.png)

# Module 8: Security Myths

### Why care?
- Myths are a misdirection of facts, many will argue against security by claiming these myths are truth

**Myth** | **Real**
---|---
Security is someone else's problem | Security is *everyone's* problem
Nobody would want to attack us | Many will attack you
Security is too expensive | Your customers are worth the investment in security
No one would ever do that | Attackers will do something you did NOT expect
Only critical apps require security | All apps need security
Compliance = Security | Compliance DOES NOT EQUAL security
A single incidient does *little* damage | 1 incident can ruin a customer relationship
The firewall/WAF will protect | The app needs to **protect itself**
TLS = secure | TLS only protects confidentiality and integrity
Security through obscurity (hiding something) | There is NO security through obscurity
Tools solve security | Tools are not the end all be all
Pen testing or scanning solves all woes | Testing is necessary, but you cannot hack yourself secure

- Your customers' data is valuable!!!!!
- It is 100% worth to protect it!
- Attackers will go for the weaker link
- Public facing (on Internet) require protection
- People, process AND tools need to **work together**
- When problems are IDd they need to be fixed
- How are we approaching security as people and our culture

# Module 9: Threat Landscape
### Why Care?
- There are new threats, people and products every day and it's expanding all the time

### Internet of Things
- These don't have the best security because they're newer

### Cloud
- Who *owns* the data, the company, you???

### Mobile
- Because there are soooo many people that have them, they are not as tech savy

### Newer Internet security threats
- Crypto jacking
- Supply chain attacks
    - Modify new libraries, people can get into the system and place malware
- Hardware attacks; meltdown and spectre

### Weak or poorly crypotography
- Weak
    - Data can be copied and then decrypted
- Unencrypted

### Week authentication
- No enforcements of password length or strength
- Failure to enforce account lockouts
- Lack of cryptography in transit protecting auth data
- Weak password hash storage
    - Keeping in DB, could be in plain text

### Data breach
- Accidental disclosure
    - Accidentally sending an email 
- Improper access control
- Web app attacks

### APIs
![](/assets/images/2022-02-23-15-06-11.png)

### Threats to IoT
![](/assets/images/2022-02-23-15-08-26.png)

### Threats to Cloud
![](/assets/images/2022-02-23-15-10-21.png)

### Threats to Mobile
![](/assets/images/2022-02-23-15-11-39.png)

### Defender's Dilemma
- Attacker only needs to be right 1 time
- Defenders need to be better than the attacker


# Module 10: Software Supply Chain

### Why care?
- Open source and third-party software can contain known security vulnerabilities
![](/assets/images/2022-02-23-15-21-26.png)
![](/assets/images/2022-02-23-15-27-15.png)
![](/assets/images/2022-02-23-15-27-38.png)

![](/assets/images/2022-02-23-15-30-41.png)
![](/assets/images/2022-02-23-15-31-07.png)

# Module 11: Security Culture and Mindset
### Why care?
- There is a direct correlation between the strength of your security culture and the security of your apps and products
- It impacts everyone
    - Everyone needs to think like a Security Person and applies knowledge of security to their daily work
### Security Plan
![](/assets/images/2022-02-23-15-57-08.png)
- A good starting point

### Security Mindset
![](/assets/images/2022-02-23-15-58-38.png)
![](/assets/images/2022-02-23-16-01-46.png)
![](/assets/images/2022-02-23-16-02-45.png)

### Security Champion
![](/assets/images/2022-02-23-16-04-47.png)

# Module 12: Prioritizing Security
### Why care?
- Everyone needs to protect data!
- Customers **demand** security!!!
- Vulnerabilities continue to rise
- Competitive advantage

### Role Behaviors
![](/assets/images/2022-02-23-16-13-24.png)
- Threat modeling: figure out all potential problems that could happen. In the design phase
![](/assets/images/2022-02-23-16-16-30.png)
- All testers should have a basic understand of pen testing skills
![](/assets/images/2022-02-23-16-19-19.png)
![](/assets/images/2022-02-23-16-21-40.png)
![](/assets/images/2022-02-23-16-23-01.png)

# Module 13: Translating Security
### Why care?
- Business and security teams appear to have different priorities and don't always speak the same language 
### Languages
![](/assets/images/2022-02-23-16-29-49.png)
![](/assets/images/2022-02-23-16-31-49.png)
![](/assets/images/2022-02-23-16-34-47.png)

# Module 14: Secured Development Lifecycle
- Standardizes best secure practices
### Why care?
- Standardizes org's approach to product and application security
 ![](/assets/images/2022-02-28-10-44-29.png)
- Will be more expensive in the short term 

![](/assets/images/2022-02-28-10-45-36.png)

- SDL's across the industry are very simliar
![](/assets/images/2022-02-28-10-47-11.png)
![](/assets/images/2022-02-28-10-47-39.png)
![](/assets/images/2022-02-28-10-49-15.png)
- Threat modeling - Part of the design process
![](/assets/images/2022-02-28-10-57-44.png)
![](/assets/images/2022-02-28-10-58-59.png)
![](/assets/images/2022-02-28-11-02-43.png)
![](/assets/images/2022-02-28-11-03-45.png)

# Module 15: Privacy and Customer Data Protection
### Why care?
- Customers will go elsewhere if there's a breach

### Privacy vs. Security
- **Security**
: Safeguarding of data
- **Privacy**
: Safeguarding of user identity
    - Shutting the blinds of a house

### Personally Identifiable Information
- PII
![](/assets/images/2022-02-28-11-16-16.png)
### Personal Health Information
- PII can be in PHI
- Medical History
- Lab results
- Insurance information

### Risks of losing PII and PHI
![](/assets/images/2022-02-28-11-17-12.png)

### Three states of digital data
- In-Use
    - Actively being accessed
    - Is ready to be accessed in memory
- In transit
    - Moving from one system to another
- At rest
    - Not currently being used, maybe a backup, database

### Customer Data
- Can be stored anywhere
    - Databases
    - Cloud
    - Log files
    - Backups

### Privacy legislation: GDPR and CCPA
- These are the 2 dominant laws to protect us
- **GDPR**
: Founded by the European Union, gives you the right to correct *inaccurate* data that you save, requires *explicit* consent
- **CCPA**
: Founded in California, requires a privacy notice on a site
- Both of them give the right to:
    - Access
    - Delete
    - Opt-out
    - Be forgotten
### Privacy legislation: COPPA and HIPPA
- **COPPA**
: Protecting the youth, 13 and under, protects them and their privacy, parents consent
- **HIPPA**
: Protects PHI

### Privacy by design
![](/assets/images/2022-02-28-11-29-03.png)
- Being proactive

### Tips to protect privacy and customer data
- Minimize use, if it's not needed, then don't collect it
![](/assets/images/2022-02-28-11-30-32.png)

# Module 16: Dealing with Vulnerabilities
### Why care?
- Need to have a process in place to clean up

### Product Security Incident Response Team
- Receives report vulnerabilities
- Investigates them
- Passes them off to developers
- Shares their disposition on them

### The need for standardized response
- Needed because new vulnerabilites come out every day
- Helps quickly mitigate issues and share that with customers
![](/assets/images/2022-02-28-11-39-29.png)
![](/assets/images/2022-02-28-11-40-25.png)

### Vulnerability researchers
![](/assets/images/2022-02-28-11-41-32.png)

### Responsible disclosure
- Responsible disclosure
: when all stakeholders agree on a timebox to fix/patch a vulnerability before sharing the details to the public
- Give the vendors the time to remediate vulnerabilities

### PSIRT Process
![](/assets/images/2022-02-28-11-46-19.png)
![](/assets/images/2022-02-28-11-46-36.png)
![](/assets/images/2022-02-28-11-47-52.png)
- CVSS - Common Vulnerability Scoring System

![](/assets/images/2022-02-28-11-49-31.png)
![](/assets/images/2022-02-28-11-50-46.png)
![](/assets/images/2022-02-28-11-51-30.png)

### How to have success with a response
![](/assets/images/2022-02-28-11-52-51.png)

# Module 17: Knowledge Sources
### Why care?
-  The basic building blocks of security knowledge are accessilbe and seamlessly integrate into the life of the security person

### Common Weakness Enumeration
![](/assets/images/2022-02-28-15-35-15.png)
### CAPEC
![](/assets/images/2022-02-28-15-37-40.png)
- Explains to folks how an attack can happen
### ATT&CK
![](/assets/images/2022-02-28-15-40-45.png)
### National Vulnerability Database
![](/assets/images/2022-02-28-15-42-24.png)
### Interconnection of Security Resources
![](/assets/images/2022-02-28-15-43-22.png)
### OWASP
![](/assets/images/2022-02-28-15-45-20.png)
![](/assets/images/2022-02-28-15-45-59.png)

### National Institute of Standards and Technology
- Provides a catalog of standards and controls to use within security
- It's beneficial to programs that need to kick off their guidance, standards and policies


# Module 18: OWASP Universe
### Why care?
- it's THE open source resources for awareness docs, process, measurement, tools, conferences, and local meet ups

### Top Resources:
- OWASP Top 10 - awareness document
![](/assets/images/2022-02-28-16-01-26.png)
- OWASP ProActive Controls - follow up to the Top 10
![](/assets/images/2022-02-28-16-01-18.png)
- OWASP Cheat Sheet Project
![](/assets/images/2022-02-28-16-01-07.png)
- Juice Shop - vulnerable web app to practice
![](/assets/images/2022-02-28-16-00-54.png)
- Software Assurance Maturity Model
![](/assets/images/2022-02-28-16-00-46.png)
- Application Security Verification Standard
![](/assets/images/2022-02-28-16-01-54.png)
    - Use as a guideline
- Code Review Guide
![](/assets/images/2022-02-28-16-03-04.png)
- Web Security Testing Guide
![](/assets/images/2022-02-28-16-03-28.png)
    - Aimed at testers
- ModSecurity Core Rule Set
![](/assets/images/2022-02-28-16-04-27.png)
- Dependency Check
![](/assets/images/2022-02-28-16-04-48.png)
- ZAP
![](/assets/images/2022-02-28-16-05-02.png)
- Threat Dragon
![](/assets/images/2022-02-28-16-05-38.png)
- Helps diagram threat modeling

# Module 19: Security at Home
![](/assets/images/2022-02-28-16-53-15.png)
![](/assets/images/2022-02-28-16-54-27.png)
![](/assets/images/2022-02-28-16-54-44.png)
![](/assets/images/2022-02-28-16-58-59.png)
![](/assets/images/2022-02-28-16-59-05.png)
![](/assets/images/2022-02-28-16-59-14.png)
![](/assets/images/2022-02-28-16-59-23.png)

# Module 20: Threat Landscape Cloud
### Why care?
- Cloud is being used everywhere, there are unique security threats that come with it

### Unique Security Issues
![](/assets/images/2022-03-01-10-36-25.png)
- Multi-tenancy - multiple customers sharing a piece of infrastructure, there may be an overlap in company data!!
- Storages have been open to public access and they typically have customer lists on there
- Less visibility because we cannot see the physical machines where they are hooked up

### Threats to Cloud
![](/assets/images/2022-03-01-10-39-34.png)
![](/assets/images/2022-03-01-10-41-15.png)
![](/assets/images/2022-03-01-10-42-25.png)
![](/assets/images/2022-03-01-10-44-35.png)
![](/assets/images/2022-03-01-10-46-50.png)
![](/assets/images/2022-03-01-10-48-12.png)

# Module 21: Trends and Application Security
### Why care?
- We need to stay ahead of the attackers and need to be aware of the trends
![](/assets/images/2022-03-01-11-24-37.png)
![](/assets/images/2022-03-01-11-25-53.png)

### Trends
