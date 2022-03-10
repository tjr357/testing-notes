---
id: mb95q87xshjq4nx03cahrzc
title: S67494
desc: ''
updated: 1646668557231
created: 1646430138276
---

### Rally Card
[S67494](https://rally1.rallydev.com/#/?detail=/userstory/626968447191&fdp=true) CBG EMEA Neil is able to launch a Support Request and see a list of information he will need to submit one successfully

### Story

Story | 
------- | -------
As | CBG EMEA Neil
I want  | to be able to click on the Support Request button from a Sales Call
so that | I can start the process to submit a Support Request
-

Story | 
------- | -------
As | CBG EMEA Neil
I want  | to be able to see what information I need in order to successfully submit a Support Request before I begin it
so that | I have all the information I need to submit a Support Request since I will not be able to exit the Support Request while it is in progress

### Test Data & Users
- **Name:** [Jules Stamp](https://sherwin--qa.lightning.force.com/lightning/setup/ManageUsers/page?address=%2F0051L000008ishi%3Fnoredirect%3D1%26isUserEntityOverride%3D1)
- **Profile:** CBG Sales
- **Role:** CBG TRADE/DIY UK Trade Regional TSM
- **Permission Set(s):**
    - ![](/assets/images/2022-03-04-16-45-56.png)
    - Sales Call to Case

### Acceptance Criteria

Scenario | Can see Support Request Button
------- | -------
Given | I'm logged in as CBG EMEA Neil
When | I go to a Sales Call off of an Account
Then |I should be able to see the Support Request button
- 

Scenario | Can see list of info needed to submit Support Request
-----|-------
Given | I'm logged in as CBG EMEA Neil
When | I click on the Support Request button
Then | I should see this screen below, except for 1. which should read "Provide Product/Order Information"
![](/assets/images/Service-Planned-Sales-Call-Exisitng-user-options-appear-correctly.png)
![](/assets/images/Service-S67494-Planned-Sales-Call-Appears-correctly.png)


