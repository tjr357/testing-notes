---
id: a73LmV10qQENnUM6RcRcx
title: S67202
desc: ''
updated: 1645032732947
created: 1645032732947
stub: false
isDir: false
---
# S67202

### [S67202](https://rally1.rallydev.com/#/?detail=/userstory/623323875839&fdp=true): B+S: Update the User Layout with Agent fields

### Story

| Steps     | Details                                                                                                                                        |
| --------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| **Given** | I'm logged in as an Admin                                                                                                                      |
| **When**  | I view anyone's user record                                                                                                                    |
| **Then**  | I should be able to see Connects for Cisco Contact Center section with these 3 fields in it - Agent Id, Extension, and an Auto Login checkbox  |

### Test Users & Data

- **Name:** 
- **Profile:** System Admin
- **Role:**
- **Permission Set(s):**

### Acceptance Criteria

| Steps     | Details                                                                                                                                        |
| --------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| **Given** | I'm logged in as an Admin                                                                                                                      |
| **When**  | I view anyone's user record                                                                                                                    |
| **Then**  | I should be able to see Connects for Cisco Contact Center section with these 3 fields in it - Agent Id, Extension, and an Auto Login checkbox  |

### Steps

1. Logged in as myself, a sys admin
2. Opened up a user record for [Denise Adelsberg](https://sherwin--qa.lightning.force.com/lightning/setup/ManageUsers/page?address=%2F00541000003qSQOAA2%3Fnoredirect%3D1%26isUserEntityOverride%3D1)
3. Scrolled down and confirmed the Cisco Contact Center settings are there:
   ![](/assets/images/2022-02-04-11-59-15.png)

### Issues
