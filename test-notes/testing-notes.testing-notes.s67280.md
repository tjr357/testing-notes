---
id: ZdXVEs1mEvHJVq7xXH0vP
title: S67280
desc: ''
updated: 1645032732947
created: 1645032732947
stub: false
isDir: false
---
# S67280

[S67280](https://rally1.rallydev.com/#/?detail=/userstory/623951326475&fdp=true) B+S: Increase Queue View Size

### Story

- This will show to users in Production if we deploy it early. They will be able to click the b+s Realtime View, but there will not be any information in it. 

### Test Users & Data

- **Name:** Christina Bonnaci
- **Profile:** Customer Support Supervisor
- **Role:** Customer Support Manager
- **Permission Set(s):**
- ![](/assets/images/2022-02-10-10-33-35.png)

### Acceptance Criteria

| Steps | Details                                                                                                                |
| ----- | ---------------------------------------------------------------------------------------------------------------------- |
| Given | I'm logged in as a B+S Agent                                                                                           |
| When  | I am in the Customer Service Lightning Console and I click on the b+s RealTime view in my utility bar                  |
| Then  | I should be able to see Team and Queue information in a larger screen than what is available by default in the widget  |

-

| Steps | Details                                                                                                                  |
| ----- | ------------------------------------------------------------------------------------------------------------------------ |
| Given | I'm logged in as a B+S Agent                                                                                             |
| When  | I am in the Customer Service Lightning Console I should not be able to see Queue or Team information in the Phone widget |
| So    | that I am not seeing duplicate information to what is in the b+s RealTime view                                           |

### Steps

1. Logged in as Christina
2. Confirmed I was in the "Customer Service Lightning Console"
3. Opened the "b+s RealtimeView" in the bottom left
   ![](/assets/images/2022-02-10-10-36-32.png)
4. Confirmed the new view is wider and works as expected
   ![](/assets/images/2022-02-10-10-37-18.png)
5. Expanded the view into it's own window
   ![](/assets/images/2022-02-10-10-40-50.png)

### Issues
