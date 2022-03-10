---
id: FXzCASebzXmCxcMh3BE2Z
title: S67193
desc: ''
updated: 1645033825168
created: 1645032732947
stub: false
isDir: false
---
# S67193

### [S67193](https://rally1.rallydev.com/#/?detail=/userstory/623258408425&fdp=true): B+S: Internal Transfer Numbers

| steps | details                                                                                                       |
| ----- | ------------------------------------------------------------------------------------------------------------- |
| Given | I'm logged in as a B+S Agent                                                                                  |
| When  | I go to transfer a call in the B+S widget                                                                     |
| Then  | I should be able to search for the descriptions below and have them transferred to the internal dialed number |

### Test Users & Data

- **Name:** [Christina Bonnaci](https://sherwin--qa.lightning.force.com/lightning/setup/ManageUsers/page?address=%2F00541000003qSQhAAM%3Fnoredirect%3D1%26isUserEntityOverride%3D1)
- **Profile:** Customer Support Supervisor
- **Role:** Customer Support Manager
- **Permission Set(s):**
  - ![](/assets/2022-02-07-14-10-15.png)

### Acceptance Criteria 

| steps | details                                                                                                                  |
| ----- | ------------------------------------------------------------------------------------------------------------------------ |
| Given | I'm logged in as a B+S Agent and I answer a call                                                                         |
| Then  | I should be able to click the transfer button and search for one of the names above to transfer it to that queue         |
| So    | that customers call my queue, but I am the incorrect person for resolution, I can transfer them to the right department  |

### Steps

1. Logged in as Christina
2. From my work phone followed these steps
   > Dial 216-912-7803  
   > Press 4 at the first menu option 
   > Enter in 800-444-2399  
   > Press 1 to confirm  
   > Wait for the prompt to finish and press 2
3. Answered the call in Salesforce from the B+S connector
4. Clicked the transfer button
   ![](/assets/2022-02-07-14-13-36.png)
5. Searched for each transfer number

| pic                                         | pic                                         |
| ------------------------------------------- | ------------------------------------------- |
| ![](/assets/2022-02-07-14-15-23.png) | ![](/assets/2022-02-07-14-15-44.png) |
| ![](/assets/2022-02-07-14-16-23.png) | ![](/assets/2022-02-07-14-16-42.png) |
| ![](/assets/2022-02-07-14-17-00.png) | ![](/assets/2022-02-07-14-17-30.png) |
| ![](/assets/2022-02-07-14-17-50.png) | ![](/assets/2022-02-07-14-18-11.png) |
| ![](/assets/2022-02-07-14-18-33.png) | ![](/assets/2022-02-07-14-18-48.png) |

6. Confirmed the transfer worked
