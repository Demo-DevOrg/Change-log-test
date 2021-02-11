# Changelog for GTPP

This changelog covers what's changed in GTPP.

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

####Update Prepackaged courses and GTPP topics

UI Updates;
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
