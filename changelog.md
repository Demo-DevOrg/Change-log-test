# Changelog for GTPP

This changelog covers what's changed in GTPP.

### Jan 12, 2021
1. Edu Org Manager/Edu Org Trainer will have access to create a survey and view their survey response.
2. Edu Org managers will be able to see all their trainer's survey details in the manager view.
3. Survey chart will be enabled in the dashboard for edu Org users.

### Dec 3, 2020
Achievement code dropdown - bulk data binding issue fixed

### Nov 30, 2020
Tenant validation Regular expression updated

### Nov 17, 2020
Approval mail contents updated and contents are configured in appsettings.json

### Oct 24, 2020
Release 1:
1. Organization Manager - Allow 2 users without the need for approval. After that Send an email to the Admin and wait for Approval
2. Remove Survey chart if the user doesn't have a survey company
3. Add Achievement filter in View All Events and Events lists in Manager and Admin
4. Tenant Field validation
5. Fixed Profile code issue if exceeds 1 year time
7. Dashboard chart "y-axis" values round off
8. Accessibility issues fixed


### Sep 2, 2020
New pre-package course added
In EduTrack, these should be listed under 1-hour trainings:
    ­ Hybrid Learning: a New Model for the Future of Learning
    - Hybrid Learning in the Primary Classroom
    - Hybrid Learning in the Intermediate Classroom
    - Hybrid Learning for the Adolescent Learner

### Jun 19, 2020
updated the role name from Edu Org training trainer to Edu Org Trainer

### Jun 13, 2020
Removed accidental use of NOLOCK in table lookup

### Jun 9, 2020
MEC Store Names List Bulk Upload

### Jun 4, 2020
1. Create a new event date must be greater than June 1, 2019, and less than today’s date+60 days.
2. When a user edits an old event date before June 1, 2019 event date select box should be empty.  Again they choose a new date that must be greater than June 1, 2019, and less than today’s date+60 days.

### May 18, 2020
1. Removed all warnings while deploying.
2. Capture all errors in an error page. Show description of the error in the page.

### May 13, 2020
1. Updated Export survey link to provide both Survey and Event details in separate tabs.
2. Move the updated code to Stage1 and verify.

### May 8, 2020
Removed the Top 5 Organization chart for trainer also (like in manager dashboard view) and extend the width of Top 5 Training Topics chart area.

### May 7, 2020
1. Updated column wrap in excel download in Manager view
2. Cookie expire time updated from 20 to 45

### May 6, 2020
1. Limit 3 courses should be applied separately for topics and pre-packaged course. The message should be different. Client side validation possible? 
2. Include total redeemed count in the performance report table (Manager view) 
3. Redeem count chart need to be replaced. 

### Apr 24, 2020
Additional changes release 2:
1. Pre-packaged List
    - Change Did you use pre-packaged training from http://aka.ms/mieacademy?  To Did you use pre-packaged training from http://aka.ms/mieacademy? or aka.ms/teachertrainingpacks?
    - Create new category at top titled Teacher Training Packs with the following choices.
        Building Literacy
        Data collection and assessment
        Creativity in the classroom
        Unlock Office 365 for the classroom
        21st century classrooms with Microsoft Teams
        Inclusive classrooms
    - Remove the following from the Pre-Packaged training list:     
        1 hour & 3 hour:  Physical computing and its role in education
        Lead the transformation:  An administrator’s pathway to success with the Education Transformation Framework
        Let’s get phygital:  Mixing digital and physical technology for engagement
        The pen is mightier than the keyboard:  Benefits of digital inking across Windows 10
        Tweet and tag your way to a stronger #PLN
        What’s your app-titude?  Discover the best-loved apps for teaching and learning in the Microsoft store
2. Training Topics: Limit to 3 or fewer topics selected.
3. Manager Role: 
    Add an XLS export to the Survey Results and Recent Training List
4. All Roles: 
    Enable users to delete a training event (If we spin up more work, can we reduce the original $16k cost estimate?)
    Add column to Event List table to include # of Codes Redeemed.
    Change users dashboard to remove Top 5 Organizations to capture Achievement Codes Redeemed YTD.
5. Admin Role:
    Provide feasibility for Admin to change the URL where the MIE Master and MIE Trainer code badges replicate on users sites, removing reference to field for changing existing “promocode”.
6. Reporting:  For Survey tab, add Organization, Partner Role, Date.  Tie back the Event ID included in Survey tab to Events

### Apr 17, 2020
Role name changes:
1. Partner Manager  -> GTP Manager
2. Partner Trainer -> GTP Trainer
3. Independent School Manager -> Edu Org Training Manager
4. Independent School Trainer -> Edu Org Training Trainer

### Apr 4, 2020
GTPP Additional changes release 1:
1. 5 new roles will be added - Showcase training Manager, School training Manager, School trainer, MS Store Manager and MS Store Trainer.

2. To setup a store or a school, Admin will add a new Organization and assign the roles. Profile code should be given for each role. 

3. No change in the registration screen.
1. School trainer will register as "Independent trainer". After they register, they should be able to associate with an Independent school in the edit registration screen without any profile code(But admin have to create profile code while creating organization).  They should be able to change this anytime but they cannot remove by himself/herself and only one association is allowed at a time.  - done (as we discussed)
2. All the other role users will be able to join using their profile code.

4. School trainer will be able to still add events as "Independent trainer". In this case, this data will not be visible to the School Manager.  

5. School trainer will be able to add co-trainers for an event within their Independent School.

6. Similar to Showcase schools, survey will not be available for Independent Schools and MS Stores as well.  

7. Showcase school manager, School training manager and MS Store manager have option to remove a user from their Organization. 

8. Showcase school manager will be able to see their Organization data that is already recorded by their Showcase school trainers.

9. When an Independent trainer associate themself to an Independent school, their existing event data will not move to the Independent school. It will stay as Independent trainer event and it will not be visible to the School manager.  

10. New users and existing store users (STORES789) will use the profile code to join a store.

11. For existing store users, when they enter the new store profile code, we need to migrate their old data to the new Store. 

### Jan 29, 2020
Redeem functionality changed:
1. Below are the links that we would need to point to, dynamically adjusting to whether they are an MIE Trainer or MIE Master Trainer.  Two options:
    - Ideally, you change the “Redeem Code” to say Get your badge and link to below.
    - If unable to do #1, then temporarily change the redeem code link to resolve to the following links.
 
Here is the link to the Trainer badge: https://1drv.ms/f/s!AgTGj1QY5vSRrjM4CtBsDwJxtYZ6

And the master trainer badge: https://1drv.ms/f/s!AgTGj1QY5vSRrjK3L80lypsJQ7pX

### Jan 8, 2020
Removed asterisk from Other Trainers

### Dec 23, 2019
Mec API URL Changed:
The old URL is:
https://preview.education.microsoft.com/api/v1/learningContent

New URL is:
https://education.microsoft.com/api/v1/learningContent

Just "preview" part is removed. Everything stays same.

### Dec 10, 2019
PowerBi Report Updated: Sample powerbi report added  - Rolled back

### Oct 21, 2019
1. Remove asterisk & requirement for O365 Tenant and Domain
2. Manager List Update: 
• Sort table by Action Required so those that require approval are at the top of the list.
• Replace Reg Date with Country (Event Country)
3. Event List: 
• Can you replace Training Period with # of Attendees
• Replace Training Topics with Trainer Name (moving Organization to the left one column, so it sits before Trainer Name)
4. Need to add 2 new pre-packaged courses. 
Under the 1-day group add:
Student Teacher Education Program (STEP) Academy, 1-Day
Inclusive Classrooms Academy
Under the 2-day group, add:
Student Teacher Education Program (STEP) Academy, 2-Day
5. Update the event duration text to 3+ days 
6. Event List:  Change Org Country to Event Country.  This will address the Independent Trainer as a "US" organization issue. 

### Oct 19, 2019
1. Handled Null pointer exception due to empty FirstName, Surname, Givenname and lastname.
2. Handled Empty Username due to Token expired.

### Oct 15, 2019
1. Removed Session Usage to store the Firstname.
2. Updated logic to generate Acheivement code of 5 digit random value to start with an alphabet.
3. Removed Welcome <Username> after clicking "Cancel" button in Registration page.
4. Removed the Rio Jhonson account from Production. (Issue in production - Need to fix)
5. Created a new User account bridgetestteam@outlook.com and registered as MIE Trainer.

### Sep 27, 2019
1. Manager dashboard update. Chart report will show the manager company report.
2. Survey response update for Deleted user. It will show the Deleted Trainer in Dropdown & also update the view training event page.
3. In case we show the deleted trainer survey response only the common question not show trainer based questions.
4. Organization or user delete from the tool automatically discrepancy report will be updated.
5.Promo code name change to Achievement code.

### Aug 29, 2019
1. In Manager VIew - Events List, Trainer List, trainer Performance show his own record - Working as expected
2. Dashboard - Show company based dashboard for Manager.
3. Performance Chart - Merge Performance column with bar in all areas.
4. In Manager Event List - show Trainer Name, # of Attendees (Remove Organization & Org Country)

### Aug 22, 2019
New API Updates:
1. API changes 
        1. Need to return updated JSON content                
        2. Need to load duration. MEC learningContent api should return duration for the topics?                
                
2. UI Changes:
        1. Separate MEC Courses from default Topics.        

#### Update Prepackaged courses and GTPP topics

UI Updates:
1. Update MEC topics in Prepackaged dropdown.
2. Fetching MEC topics from API should only update the Prepackaged topics based on Name match. If matched, then update the ID column. No Insertion of MEC topics into Prepackaged table.
3. Duration flow is as it is. 
4. Generate Promocode for all events irrespective of any conditions.

API Updates:
1. Show Duration in API Response as single value. [Not for each topic] Duration should be the midrange value. [If duration is 1-2 hours, then show it as 1.5 hrs]
2. Send each MEC courses as separate object  and general or prepackaged topics as single object

### Aug 14, 2019
Updated the API changes

### Jul 27, 2019
1. Create Promocode on selected training topics during Create/Edit event
2. Redeem API to send Training topics for the promocode
3. Client view to access thos APIs

### Jul 22, 2019

1. On Event Create - If this training topic is available in MEC system, then we need to genrate Promocode.
        (From MEC system, get all promocodes and verify that the selected training topics is available - through api)
        
2. Generate 2 APIs, one for sending the MEC training topics selected for that promocode (and reduce the count to 1 from total attendees)
        second api for adding the attendees count for that promocode.
1. Learning Topics API with client view to access the Api
2. Keep link at Admin View page to refresh the list.

While calling the API, insert the topics into DB and show the inserted topics to the user

Avoid keeping button in Admin View. Instead, populate the Topics from API on clicking Create event


### Jul 12, 2019, Jul 27, 2019

1. Update the latest Topics and Pre-Packaged courses in DB. The GTPP Topics and the Pre-packaged courses list remains the same all the time. If any change is needed it will be handled manually at the backend.

2. Using the MEC API response, check whether any of the MEC courses exist in the pre-packaged courses list by matching the course name. If found, need to save all the MEC details (MEC ID, type, name, description) so we can return this information when redeem code API gets called. [DOn't insert new topics from API]
Note: These 3 pre-packaged courses are MEC courses so we will do the mapping manually if needed (Microsoft Innovative Educator (MIE) Trainer Academy, MIE OneNote Teacher Academy, MIE Office 365 Teacher Academy)

3. Promo code should be generated for all the Events irrespective of the delivery type.

4. Promo Codes should start with the letter of first name and last time (ie Ginelle Cousins = GC) and end with fiscal year (ie FY20 = 20).  In between 5 alpha and numeric characters, avoiding using a zero and O unless it’s in trainer name.  Example for Ginelle Cousins = GC9YTL20

5. Instead of the range, need to calculate the middle of the event duration and include that in the redeem API response. [Refer the email with Subject; Updated API format]

6. In Manager VIew - Events List, trainer Performance show his own record - Working as expected
7. Dashboard - Show company based dashboard for Manager. - on hold.
8. Performance Chart - Merge Performance column with bar in all areas.
9. In Manager Event List - Trainer Name, # of Attendees (Remove Organization & Org Country)
10. Remove MLC
11. Microsoft Field - Don't have option to generate Survey as of ShowcaseSchool Trainer.

### June 22, 2019

1. Manager view, Trainer Performance list, with N/A in performance column, if there are no responses for that trainer.
2. Manager View, trainer Performance list, click on Trainer name, will show popup with all Events and its Survey responses. If no survey Response, then show N/A in performance column.
3. Trainer Dashboard, show Smiley based on 1st Survey question response. (Average to max. 5)
4. View Event page, Show Survey Response with number of response counts. If there are no response, then show (0 Response)
5. If event has been created with Independent Organisation Or Showcase School Trainer, hide Survey Language.
6. In Edit Event page hide Survey Language for Independent Organisation Or Showcase School Trainer
7. In View Event page hide Survey Information part
8. Updated latest Training topics in dropdown.
9. Updated Prepackaged courses as Grouped list in dropdown.
10. Updated the ccompany fake data
11. Updated the Region column in discrepancy report.

### June 10, 2019

1. Remove Company from table view
2. Add Trainers name
3. Count of training trained based on filter (Near filter or dropdown)
4. Datewise or monthwise report.

1. Inactive Users, not able to login or register into the tool. (Need to clarify)
2. User can able to unregister and delete their data from the tool
3. As admin can manage Users/Managers
4. As admin can able to add/delete admins

1. Check for Adding dynamic text in Survey (Event Date and Training Tools)
Use Descriptive TExt Question type at the top of the question. Dynamically retrieve the question on Copy survey and append the Event Date and Tools Trainedceful termination logic.
