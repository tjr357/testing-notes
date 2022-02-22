---
id: iw9gFlAQROflJbNgxzCbo
title: Security Journey
desc: ''
updated: 1645547934817
created: 1645541776502
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