---
id: kpo0lpqo64u1m0dtynbjwvm
title: Go Live Backup Plan
desc: ''
updated: 1658521829972
created: 1658502182700
---

Plan B

- Let the Aurora support handle this, so there will be a remedy ticket, we will be the Remedy PoC
- Jen Kiffer - Aurora
- Facility Managers
- Chirayu
- If we get a critical issue (more 1-2 hours to fix) we will revert back to the PowerApps version and we'll need help from
  - Justin, Paul and Narendhar
    - Do they have the time blocked for this
    - Revert to the 2 old Boomi services
      - Azure SQL service
      - Getting data from the Aurora service
      - New service was tested in QA by Suresh
    - There's the Migration PPM

- We cannot we create orders in Prod, so we'll need to have someone monitor this at 6:30 AM

PPM's
248330 

- GEA Change Request 248330 - APIM PCG Workbench WorkorderQuery and WorkOrderTransaction Migration is in Change management step can we progress the ppm workflow for this.

245684

- Only to revert
  - Two Boomi Services:
    - Get WO from POS - This should be new service for Azure SQL, existing data verse one should not be modified
    - Get WO Status from Aurora - This will be modification of existing one as OSB is calling the Booomi endpoint. this supposed to be migrated today after 8 PM

Narendhar
> There are other deployments happening tomorrow, could we do the deployment tomorrow?

Facilities are closed on the weekends

10am tomorrow re-schedule



- No one is on call for this weekend