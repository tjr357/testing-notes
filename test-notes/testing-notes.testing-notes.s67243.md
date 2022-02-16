---
id: pftmknom34uGe1EsWpiMc
title: S67243
desc: ''
updated: 1645032732947
created: 1645032732947
stub: false
isDir: false
---
# S67243

### Card Description

> As an SFDC Chatter user  
> I want to be able to make announcements to Chatter Groups  
> So that I can notify the people in those groups of important messages, even if they have their Chatter notifications turned off

> As an SFDC Chatter user  
> I want to be able to edit my own Chatter Posts or Announcements    
> So that I can delete the post/announcement if I've made a mistake

### Test User

- Name: [Lorraine Abeysinghe](https://sherwin--qa.lightning.force.com/lightning/setup/ManageUsers/page?address=%2F0054p000003WkKnAAK%3Fnoredirect%3D1%26isUserEntityOverride%3D1%26retURL%3D%252Fsetup%252Fhome)
- Profile: GI Sales 
- Role: GI NA
- Permission Set(s):  
  - ![](/assets/images/2022-01-31-13-33-37.png)  
- Make sure "Receive emails" is checked in the Chatter > Email notifcation user settings

### Acceptance Criteria

> As an SFDC Chatter user  
> I want to be able to make announcements to Chatter Groups  
> So that I can notify the people in those groups of important messages, even if they have their Chatter notifications turned off

> As an SFDC Chatter user  
> I want to be able to edit my own Chatter Posts or Announcements    
> So that I can delete the post/announcement if I've made a mistake

### Notes

1. Logged in as Lorraine
2. Navigated to the Chatter tab
   - ![](/assets/images/2022-01-31-13-38-16.png)
3. Chose the _Announcements_ tab
   - ![](/assets/images/email-all-checked.png)
4. Checked the "Email all group members" box
5. Entered a message and clicked Share
6. The email came through for all the members in the Chatter Group
7. I confirmed the Post and Announcement could not be deleted, and that it could be edited. Heres' the expected error:
   - ![](/assets/images/2022-01-31-17-07-07.png)
