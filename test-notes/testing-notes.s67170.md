---
id: LqfxvaOlznCKWKUo08eEh
title: S67170
desc: ''
updated: 1645033799021
created: 1645032732947
stub: false
isDir: false
---
# S67170

### [S67170]

| steps  | details                                              |
| ------ | ---------------------------------------------------- |
| As     | a Customer Service Agent who uses B+S                |
| I want | to be able to view details about my calls from Cisco |
| So     | that I can know information about the calls I've had |

### Test Users & Data

- **Name:** [Christina Bonnaci](https://sherwin--qa.lightning.force.com/lightning/setup/ManageUsers/page?address=%2F00541000003qSQhAAM%3Fnoredirect%3D1%26isUserEntityOverride%3D1)
- **Profile:** Customer Support Supervisor
- **Role:** Customer Support Manager
- **Permission Set(s):**
  - ![](/assets/2022-02-07-14-10-15.png)

### Acceptance Criteria 

| steps | details                                                                                                                               |
| ----- | ------------------------------------------------------------------------------------------------------------------------------------- |
| Given | I'm logged in as Christina Bonacci                                                                                                    |
| When  | I receive a phone call                                                                                                                |
| Then  | I should be able to click on the Activity record that is created and see the following information in the Comments section from Cisco |
| -     | - Id - Customer Phone - Queue Name - Queue Number                                                                                     |

### Steps

1. Logged in as Christina
2. From my work phone followed these steps
   > Dial 216-912-7803  
   > Press 4 at the first menu option 
   > Enter in 800-444-2399  
   > Press 1 to confirm  
   > Wait for the prompt to finish and press 2
3. Answered the call in Salesforce from the B+S connector
4. Clicked the "Call Activity" button
   ![](/assets/2022-02-14-15-47-03.png)
5. The Task page opens
   ![](/assets/2022-02-14-15-47-57.png)
6. The Activity details appear correctly in the "Comments" box
   ![](/assets/2022-02-14-15-49-36.png)
