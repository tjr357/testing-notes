---
id: eQXLNC6lHDPkGTpb4fsgi
title: S65446
desc: ''
updated: 1645124865224
created: 1645032732946
stub: false
isDir: false
---
The card was also retested: [[testing-notes.S65446-retested]]
### [S65446](https://rally1.rallydev.com/#/117070905740d/teamboard?detail=%2Fuserstory%2F612142167589&view=3f2cc321-e7f8-4e13-aac7-7461bf66a431)

| steps   | details                                                       |
| ------- | ------------------------------------------------------------- |
| As      | Piper                                                         |
| I want  | to be able to send an updated branded acknowledgement         |
| So that | the customer has acknowledgement that we received their email |

### Test Users & Data


- Test Emails:
  - **EU B2C General Enquiry France Queue:** [taylor.j.ruiz@y-vz08x7qg2m7d9nw4nk1t0o1d9tykfxigqi66h62njkhlrx572.6t-4ej0eaa.cs166.case.sandbox.salesforce.com](mailto:taylor.j.ruiz@y-vz08x7qg2m7d9nw4nk1t0o1d9tykfxigqi66h62njkhlrx572.6t-4ej0eaa.cs166.case.sandbox.salesforce.com)
  - **EU B2C Poland Email Queue:** [tao.jianguk@v-h365zc1kfrezc61rt17s3flztgnu8pwp8xvqha4vb342dk0wj.6t-4ej0eaa.cs166.case.sandbox.salesforce.com](mailto:tao.jianguk@v-h365zc1kfrezc61rt17s3flztgnu8pwp8xvqha4vb342dk0wj.6t-4ej0eaa.cs166.case.sandbox.salesforce.com)
  - **EU B2C General Enquiry Poland Queue:** [poland_eu20220215@w-v2thsc1fnm0i1omwice0m5n13x4pxnbp6jqwx72qn0f61zmxn.6t-4ej0eaa.cs166.case.sandbox.salesforce.com](mailto:poland_eu20220215@w-v2thsc1fnm0i1omwice0m5n13x4pxnbp6jqwx72qn0f61zmxn.6t-4ej0eaa.cs166.case.sandbox.salesforce.com)
  - **EU B2C Poland Web Queue:** [tao.jiang24@b-1tb2bynu031oqliduvvst0u7l1yxo3qg5fd49yct8fufgv30b.6t-4ej0eaa.cs166.case.sandbox.salesforce.com](mailto:tao.jiang24@b-1tb2bynu031oqliduvvst0u7l1yxo3qg5fd49yct8fufgv30b.6t-4ej0eaa.cs166.case.sandbox.salesforce.com)

### Acceptance Criteria 

| steps | details                                                                                                                               |
| ----- | ------------------------------------------------------------------------------------------------------------------------------------- |
| Given | I'm logged in as Christina Bonacci                                                                                                    |
| When  | I receive a phone call                                                                                                                |
| Then  | I should be able to click on the Activity record that is created and see the following information in the Comments section from Cisco |
| -     | - Id - Customer Phone - Queue Name - Queue Number                                                                                     |

### Steps

1. Sent email to: [taylor.j.ruiz@y-vz08x7qg2m7d9nw4nk1t0o1d9tykfxigqi66h62njkhlrx572.6t-4ej0eaa.cs166.case.sandbox.salesforce.com](mailto:taylor.j.ruiz@y-vz08x7qg2m7d9nw4nk1t0o1d9tykfxigqi66h62njkhlrx572.6t-4ej0eaa.cs166.case.sandbox.salesforce.com)

2. Confirmed the Case was created in the proper queue
   ![](/assets/2022-02-15-15-48-08.png)

3. Went to Mailhog, the email appears but there may be some rendering issues
   ![](/assets/2022-02-15-15-51-18.png)

4. Sent email to: [tao.jianguk@v-h365zc1kfrezc61rt17s3flztgnu8pwp8xvqha4vb342dk0wj.6t-4ej0eaa.cs166.case.sandbox.salesforce.com](mailto:tao.jianguk@v-h365zc1kfrezc61rt17s3flztgnu8pwp8xvqha4vb342dk0wj.6t-4ej0eaa.cs166.case.sandbox.salesforce.com)

5. The Case was created, however it should appear in the **"EU B2C Poland Email Queue"** but it appears in the **"EU B2C General Enquiry Poland Queue"**
   ![](/assets/2022-02-15-15-57-51.png)

6. Went to Mailhog, the email appears but there may be some rendering issues
   ![](/assets/2022-02-15-15-55-20.png)

7. Sent email to: [poland_eu20220215@w-v2thsc1fnm0i1omwice0m5n13x4pxnbp6jqwx72qn0f61zmxn.6t-4ej0eaa.cs166.case.sandbox.salesforce.com](mailto:poland_eu20220215@w-v2thsc1fnm0i1omwice0m5n13x4pxnbp6jqwx72qn0f61zmxn.6t-4ej0eaa.cs166.case.sandbox.salesforce.com)

8. Confirmed the Case was created in the proper queue
   ![](/assets/2022-02-15-15-48-08.png)

9. Went to Mailhog, the email appears but there may be some rendering issues
   ![](/assets/2022-02-15-15-51-18.png)

10. Sent email to: [tao.jianguk@v-h365zc1kfrezc61rt17s3flztgnu8pwp8xvqha4vb342dk0wj.6t-4ej0eaa.cs166.case.sandbox.salesforce.com](mailto:tao.jianguk@v-h365zc1kfrezc61rt17s3flztgnu8pwp8xvqha4vb342dk0wj.6t-4ej0eaa.cs166.case.sandbox.salesforce.com)

11. The Case was created, however it should appear in the **"EU B2C Poland Web Queue"** but it appears in the **"EU B2C General Enquiry Poland Queue"**
    ![](/assets/2022-02-15-16-05-28.png)

12. Went to Mailhog, the email did _NOT_ appear within a couple of minutes
