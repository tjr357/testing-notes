---
id: LUG5SdozeiBEpwTMjT6jv
title: S64303
desc: ''
updated: 1645032732946
created: 1645032732946
stub: false
isDir: false
---
# S64303

- [S64303](https://rally1.rallydev.com/#/?detail=/userstory/607679909791&fdp=true): All Service User: Email Drafting in Salesforce - Deletion Access 236977 (GO)

### Story

- | ----    | -                                                                                                                                                        |
  | ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
  | As      | any Service user                                                                                                                                         |
  | I want  | to be able to delete an email when it's a Draft                                                                                                          |
  | so that | unneeded draft emails no longer cause clutter on the Case email related list and unnecessary activities are eliminated from the Activity/Chatter section |

### Test Data & Users

- **Name:** Paula Williams
- **Profile:** P&M Sales
- **Role:** Global P&M
- **Permission Set(s):**  
  - ![](/assets/images/2022-02-03-15-35-15.png)

* * *

### Acceptance Criteria

| Scenario | Able to delete drafts                                          |
| -------- | -------------------------------------------------------------- |
| Given    | I'm logged in as Paula Williams                                |
| When     | I go to a Case and then create an email and save it as a draft |
| Then     | I should be able to delete the draft                           |

-

| Scenario | Unable to delete emails that are not drafts                   |
| -------- | ------------------------------------------------------------- |
| Given    | I'm logged in as Paula Williams                               |
| When     | I go to a Case and view the related emails                    |
| Then     | I should not be able to delete any emails that are not drafts |

* * *

### Steps

1. Logged in as Paula
2. Went to an existing Case
3. Tried to delete an existing email and received the correct error message, that it's not possible
   - ![](/assets/images/2022-02-03-15-40-27.png)

* * *

1. Logged in as Paula
2. Created a new Product Support Case
3. Created an email draft:
   ![](/assets/images/2022-02-03-16-10-20.png)
4. Then clicked the "Discard Draft" trash can button
   ![](/assets/images/2022-02-03-16-11-19.png)
   ![](/assets/images/2022-02-03-16-11-44.png)
   The Email draft is also removed from "Related List" Emails section

* * *

### Miscellaneous
