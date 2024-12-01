# Awards and Scholarships Module Documentation

## Table of Contents
- [User-Centered Design (UCD)](#user-centered-design-ucd)
- [SRS Application](#srs-application)
- [SRS Web Interface](#srs-web-interface)
- [API Specifications](#api-specifications)
- [UI for Application](#ui-for-application)
- [UI for Web](#ui-for-web)
- [Database Schema](#database-schema)

## User-Centered Design (UCD)
![Use Case Diagram](assets/SPACS_UCD.png)

## SRS Application

Team Members: 

Abhishek Muwal(21BCS005) Ajay Sharma(21BCS014) Aryan(21BCS036) 

Deepak Meena (21BCS071) Sukram(21BCS212) 

Student Mentor: Soham Bakul Sarode 

***Faculty Mentor: Dr. Ayan Seal*** 

- 1.Introduction 
1. Introduction about the Fusion-A breif Description 

`     `FusionIIIT at PDPM Indian Institute of Information Technology, Design and Manufacturing, Jabalpur, is a comprehensive initiative developed by students to streamline and automate various functions across the campus. This digital platform, built with precision using Python 3.8 and Django Web framework, serves as a testament to seamless integration within the institute. 

The scope of FusionIIIT extends beyond administrative tasks, encompassing academic management and other departmental responsibilities. It acts as a digital wizard, addressing the intricacies of campus life and ensuring a harmonized operational landscape. 

On the administrative front, FusionIIIT takes care of complex paperwork and processes, simplifying tasks that would otherwise be time-consuming. In academics, it introduces a digital touch to enhance the learning experience and streamline course management. However, its impact is not limited to these areas, as FusionIIIT extends its support to various departments and sections, ensuring the smooth functioning of every aspect of campus life. 

In essence, FusionIIIT is described as more than just a tool; it is portrayed as a friendly companion that contributes to the organization and enjoyment of life at PDPM IIITDM Jabalpur for everyone involved. By handling diverse responsibilities and providing support across different domains, FusionIIIT aims to make the overall campus experience more organized and enjoyable. 

2. Purpose of the Module 

   The primary goal of this module is to establish a centralized platform for all students at IIITDMJ to access information about convocation medals, awards, and scholarships. Additionally, eligible students should be able to apply for these honors through the portal. The system aims to streamline the application process, providing automation and reducing the challenges associated with the current manual application procedures. 

3. Scope of the Module 

   This software will be mostly used by the students of IIITDM Jabalpur to get all the necessary details 

   about various scholarships and awards. They also get the feature to apply for the same and track 

   the application status. 

- 2.User/Actor Characteristics 
1. User: 

`           `A user is the person who have logged in the system.  

**Role:** Browse through catalogue of awards and scholarships          ***Specific Functionalities:*** 

- Browse available medals and scholarships 
- Browse previous winners of medals and scholarships 
- View the details of SPACS members 
2. Student: 

`        `A student is main user who will use this portal to apply for various scholarships and awards. 

**Role:** Browse through catalogue and fill forms for the available awards and scholarships. ***Specific Functionalities:*** 

- Submit applications through the ERP portal 
- Fill the form and upload required documents 
- Receives notifications about the application approval/rejection 
- Can track the application status and also see the application history 
3. SPACS CONVENER: 

`    `He is responsible for circulating notifications about the awards and also decides the recipients. 

**Role:** Invite applications and decides the winners of awards and scholarships ***Specific Functionalities:*** 

- Invite applications for awards and scholarships 
- Circulate information regarding new applications 
- Can introduce new awards and modify the existing ones 
- Finally decides who will be awarded for the medals and scholarships 
4. SPACS ASSISTANT: 

He is the person who will be responsible for physical verification of documents. **Role:** Physically verifies the documents and notify to students  

***Specific Functionalities:*** 

- Will verify the application documents physically 
- Update the application status of students in the portal 
- Notify the students in case of lack of required document 
- 3. Funtional Requirements 
1. Use Case Diagram: 

![](Aspose.Words.c154b3e5-6f3c-4428-91d6-bcdb87880290.001.jpeg)

2. Use Case Description 
1. **Use Case Description for a User as an actor to the system** 

**Use case # 1** 



|**UC ID** |UC#1 ||
| - | - | :- |
|**Use case Name** |**browse\_catalogue** ||
|**Description** |User of the system can browse the available medals/scholarships categorically ||
|**Actor** |Students, SPACS Convener, SPACS Assistant ||
|**Precondition** |The user must be logged-in and the system is having the updated catalogue of all the convocation medals, MCM scholarship and Other Prizes. ||
|**Main Flow** |1 |Actor logs into the system and opens Awards and Scholarship Page. |



<table><tr><th colspan="1" rowspan="2"></th><th colspan="2" valign="top">2 </th><th colspan="1" valign="top">Actor selects the ‘Browse Award Catalogue’ option. </th></tr>
<tr><td colspan="2" valign="top">3 </td><td colspan="1" valign="top">Actor selects the required award/scholarship/ medals and views the necessary details. </td></tr>
<tr><td colspan="1"><b>Post conditions</b> </td><td colspan="3" valign="top">The necessary details of the awards are displayed. </td></tr>
<tr><td colspan="1"><b>Alternate Flow</b> </td><td colspan="3" valign="top">NIL </td></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b> </td><td colspan="3" valign="top">NIL </td></tr>
<tr><td colspan="1"><b>Global Alternate Flow</b> </td><td colspan="1" valign="top">GA1 </td><td colspan="2" valign="top">The actor can return to the dashboard at any time by clicking on dashboard button. </td></tr>
<tr><td colspan="1"></td><td colspan="1"></td><td colspan="2" valign="top"><b>Post Condition:</b> The system returns to the actor’s dashboard. </td></tr>
</table>

**Use case # 2** 



<table><tr><th colspan="1" valign="top"><b>UC ID</b> </th><th colspan="2" valign="top">UC#2 </th></tr>
<tr><td colspan="1"><b>Use case Name</b> </td><td colspan="2" valign="top"><b>view_staff_details</b> </td></tr>
<tr><td colspan="1" valign="top"><b>Description</b> </td><td colspan="2">User of the system can view administration in charge of the system, and other related staff details. This is required so student may contact authority to ask query regarding any of medals/scholarship. </td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b> </td><td colspan="2" valign="top">Students, SPACS Convener, SPACS Assistant </td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b> </td><td colspan="2">System must have information about administration/staff. The user must be logged in and Awards and Scholarship page is opened. </td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Main Flow</b> </td><td colspan="1" valign="top">1 </td><td colspan="1" valign="top">In Awards and Scholarships page, Actor selects the ‘SPACS member details’ option. </td></tr>
<tr><td colspan="1" valign="top">2 </td><td colspan="1">Actor gets the list of SPACS Convener, SPACS Assistant and other members of SPACS involved in the system (if any). </td></tr>
<tr><td colspan="1"><b>Post conditions</b> </td><td colspan="2" valign="top">All the necessary details of the staff involved in the system are displayed. </td></tr>
<tr><td colspan="1"><b>Alternate Flow</b> </td><td colspan="2" valign="top">NIL </td></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b> </td><td colspan="2" valign="top">NIL </td></tr>
<tr><td colspan="1" rowspan="2"><b>Global Alternate Flow</b> </td><td colspan="1" rowspan="2" valign="top">GA1 </td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on dashboard button. </td></tr>
<tr><td colspan="1" valign="top"><b>Post Condition:</b> The system returns to the actor’s dashboard. </td></tr>
</table>

**Use case # 3** 



<table><tr><th colspan="1" valign="top"><b>UC ID</b> </th><th colspan="2" valign="top">UC#3 </th></tr>
<tr><td colspan="1"><b>Use case Name</b> </td><td colspan="2" valign="top"><b>view_previous_winners</b> </td></tr>
<tr><td colspan="1" valign="top"><b>Description</b> </td><td colspan="2" valign="top">User can view previous year’s winners for various convocation medals and MCM Scholarships. </td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b> </td><td colspan="2" valign="top">Students, SPACS Convener, SPACS Assistant </td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b> </td><td colspan="2">System must have information about winners of medals/scholarships/awards and actor must be logged into the system and Awards and Scholarship page is opened. </td></tr>
<tr><td colspan="1" rowspan="3" valign="top"><b>Main Flow</b> </td><td colspan="1">1 </td><td colspan="1">Actor selects the ‘Previous Award Winners’ option. </td></tr>
<tr><td colspan="1">2 </td><td colspan="1">Actor then selects respective batch and award from the dropdown list provided </td></tr>
<tr><td colspan="1">3 </td><td colspan="1">He clicks ‘Submit’ button. </td></tr>
<tr><td colspan="1"><b>Post conditions</b> </td><td colspan="2" valign="top">List of winners for the selected option are displayed in chronological order. </td></tr>
</table>



<table><tr><th colspan="1"><b>Alternate Flow</b> </th><th colspan="2" valign="top">NIL </th></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b> </td><td colspan="2" valign="top">NIL </td></tr>
<tr><td colspan="1" rowspan="2"><b>Global Alternate Flow</b> </td><td colspan="1" rowspan="2" valign="top">GA1 </td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on dashboard button. </td></tr>
<tr><td colspan="1" valign="top"><b>Post Condition:</b> The system returns to the actor’s dashboard. </td></tr>
</table>

2. **Use case description for Student (extending User) as an actor to the system** 

**Use case # 4** 



<table><tr><th colspan="1" valign="top"><b>UC ID</b> </th><th colspan="2" valign="top">UC#4 </th></tr>
<tr><td colspan="1"><b>Use case Name</b> </td><td colspan="2" valign="top"><b>apply_for_convocation_medals</b> </td></tr>
<tr><td colspan="1" valign="top"><b>Description</b> </td><td colspan="2" valign="top">The student can apply for Convocation Medals by filling out a form and uploading necessary documents. </td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b> </td><td colspan="2" valign="top">Student </td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b> </td><td colspan="2">Student Logged in, opens Awards and Scholarship portal and applications are invited for the same. </td></tr>
<tr><td colspan="1" rowspan="5" valign="top"><b>Main Flow</b> </td><td colspan="1">1 </td><td colspan="1">Student clicks on ‘Apply for Awards’ option and then Convocation Medals. </td></tr>
<tr><td colspan="1" valign="top">2 </td><td colspan="1">Student reads the instructions for applying for the Convocation Medals and clicks on ‘Proceed’ button. </td></tr>
<tr><td colspan="1" valign="top">2 </td><td colspan="1">Student selects the type of application from the available options and the respective form is displayed. </td></tr>
<tr><td colspan="1" valign="top">3 </td><td colspan="1" valign="top">Student fills up all the necessary details in the form.[S1] </td></tr>
<tr><td colspan="1" valign="top">4 </td><td colspan="1" valign="top">After successful upload student clicks on the ‘Submit’ button. </td></tr>
<tr><td colspan="1"><b>Post conditions</b> </td><td colspan="2" valign="top">Application and documents submitted for verification. </td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Sub Flow</b> </td><td colspan="1" valign="top">S1 </td><td colspan="1" valign="top">He can upload supporting documents. </td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-condition</b> - Documents are attached along with the form. </td></tr>
<tr><td colspan="1"><b>Alternate Flow</b> </td><td colspan="1"></td><td colspan="1" valign="top">NIL </td></tr>
<tr><td colspan="1" rowspan="2"><b>Global Alternate Flow</b> </td><td colspan="1" rowspan="2" valign="top">GA1 </td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on dashboard button. </td></tr>
<tr><td colspan="1" valign="top"><b>Post Condition:</b> The system returns to the actor’s dashboard. </td></tr>
</table>

**Use case # 5** 



|**UC ID** |UC#5 |
| - | - |
|**Use case Name** |**apply\_for\_mcm\_scholarship** |
|**Description** |The student can apply for MCM scholarship by filling out a form and uploading necessary documents. |
|**Actor** |Student |
|**Precondition** |Student Logged in, opens Scholarship and Awards portal and applications are invited for the same |



<table><tr><th colspan="1" rowspan="4" valign="top"><b>Main Flow</b> </th><th colspan="1">1 </th><th colspan="1">Student clicks on ‘Apply for Awards’ option and selects MCM Scholarship. </th></tr>
<tr><td colspan="1">2 </td><td colspan="1">MCM Scholarship form is displayed. </td></tr>
<tr><td colspan="1" valign="top">3 </td><td colspan="1" valign="top">Student fills up the necessary details in the form[S1] </td></tr>
<tr><td colspan="1" valign="top">4 </td><td colspan="1" valign="top">After successful upload student clicks on the ‘Submit Application’ button. </td></tr>
<tr><td colspan="1"><b>Post conditions</b> </td><td colspan="2" valign="top">Application and documents submitted for verification. </td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Sub Flow</b> </td><td colspan="1" valign="top">S1 </td><td colspan="1">He can upload supporting documents like income certificate and all the required documents (Refer to appendix A for MCM scholarship details). </td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-condition</b> - Documents are attached along with the form. </td></tr>
<tr><td colspan="1"><b>Alternate Flow</b> </td><td colspan="1"></td><td colspan="1" valign="top">NIL </td></tr>
<tr><td colspan="1" rowspan="2"><b>Global Alternate Flow</b> </td><td colspan="1" rowspan="2" valign="top">GA1 </td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on dashboard button. </td></tr>
<tr><td colspan="1" valign="top"><b>Post Condition:</b> The system returns to the actor’s dashboard. </td></tr>
</table>

**Use case # 6** 



<table><tr><th colspan="1" valign="top"><b>UC ID</b> </th><th colspan="2" valign="top">UC#6 </th></tr>
<tr><td colspan="1"><b>Use case Name</b> </td><td colspan="2" valign="top"><b>track_application_status</b> </td></tr>
<tr><td colspan="1" valign="top"><b>Description</b> </td><td colspan="2" valign="top">Student views application status for each of the applied medal/scholarship. </td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b> </td><td colspan="2" valign="top">Student </td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b> </td><td colspan="2">Student must have applied for an award/scholarship and have a valid application number assigned </td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Main Flow</b> </td><td colspan="1">1 </td><td colspan="1">Student clicks on ‘View Application Status’ option. </td></tr>
<tr><td colspan="1">2 </td><td colspan="1">Student selects the ‘Current’ option. </td></tr>
<tr><td colspan="1" valign="top">3 </td><td colspan="1" valign="top">All the applications status is displayed here along with the application ID. </td></tr>
<tr><td colspan="1" valign="top">4 </td><td colspan="1">Student can also selects the ‘History’ option to view the status of the past applied applications. </td></tr>
<tr><td colspan="1"><b>Post conditions</b> </td><td colspan="2" valign="top">The status of all applications submitted by the student in the past are displayed. </td></tr>
<tr><td colspan="1"><b>Alternate Flow</b> </td><td colspan="2" valign="top">NIL </td></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b> </td><td colspan="2" valign="top">NIL </td></tr>
<tr><td colspan="1" rowspan="3" valign="top"><b>Global Alternate Flow</b> </td><td colspan="1" rowspan="3" valign="top">GA1 </td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on dashboard button. </td></tr>
<tr><td colspan="1" valign="top"><b>Post Condition:</b> The system returns to the actor’s dashboard. </td></tr>
<tr><td colspan="1"></td></tr>
</table>
**Use case # 7** 



<table><tr><th colspan="1" valign="top"><b>UC ID</b> </th><th colspan="2" valign="top">UC#7 </th></tr>
<tr><td colspan="1"><b>Use case Name</b> </td><td colspan="2" valign="top"><b>Receives_Notification</b> </td></tr>
<tr><td colspan="1" valign="top"><b>Description</b> </td><td colspan="2">The "Receives_Notifications" use case enables a user to receive and interact with notifications generated by the Notification System. The primary actor for this use case is the User, and the secondary actor is the Notification System, responsible for generating and delivering notifications. </td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b> </td><td colspan="2" valign="top">Students, SPACS Convener, SPACS Assistant </td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b> </td><td colspan="2" valign="top">User has an active account. </td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Main Flow</b> </td><td colspan="1" valign="top">1 </td><td colspan="1" valign="top">The Notification System identifies events requiring notifications. </td></tr>
<tr><td colspan="1" valign="top">2 </td><td colspan="1" valign="top">The Notification System generates notifications based on identified events.    </td></tr>
</table>



<table><tr><th colspan="1" rowspan="2">![](Aspose.Words.c154b3e5-6f3c-4428-91d6-bcdb87880290.002.png)</th><th colspan="1" valign="top">3 </th><th colspan="1" valign="top">The Notification System sends notifications to the User. </th></tr>
<tr><td colspan="1" valign="top">4 </td><td colspan="1" valign="top">. The User receives and views the notifications through the User Interface. </td></tr>
<tr><td colspan="1"><b>Post conditions</b> </td><td colspan="2" valign="top">User successfully receives notifications. </td></tr>
<tr><td colspan="1"><b>Alternate Flow</b> </td><td colspan="2" valign="top">Delayed Notification Delivery. </td></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b> </td><td colspan="2" valign="top">NIL </td></tr>
<tr><td colspan="1" rowspan="2"><b>Global Alternate Flow</b> </td><td colspan="1" rowspan="2" valign="top">GA1 </td><td colspan="1" valign="top">`  `Notification System Failure </td></tr>
<tr><td colspan="1" valign="top"><b>Post Condition:</b> The system returns to the actor’s dashboard. </td></tr>
</table>

**Use case # 8** 



<table><tr><th colspan="1" valign="top"><b>UC ID</b> </th><th colspan="2" valign="top">UC#8 </th></tr>
<tr><td colspan="1"><b>Use case Name</b> </td><td colspan="2" valign="top"><b>View_History</b> </td></tr>
<tr><td colspan="1" valign="top"><b>Description</b> </td><td colspan="2" valign="top">The "View_History" use case allows an authenticated user to retrieve and view their historical data through the system. This historical data may include past interactions, transactions, or any relevant activities stored in the database. </td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b> </td><td colspan="2" valign="top">Students, SPACS Convener, SPACS Assistant </td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b> </td><td colspan="2" valign="top">User is authenticated and has a valid session.   </td></tr>
<tr><td colspan="1" rowspan="3" valign="top"><b>Main Flow ![](Aspose.Words.c154b3e5-6f3c-4428-91d6-bcdb87880290.003.png)</b></td><td colspan="1" valign="top">1 </td><td colspan="1" valign="top">User requests to view their history through the User Interface. </td></tr>
<tr><td colspan="1" valign="top">2 </td><td colspan="1" valign="top">System retrieves historical data from the Database.                                           </td></tr>
<tr><td colspan="1" valign="top">3 </td><td colspan="1" valign="top">System presents the historical data to the User through the User Interface.  . </td></tr>
<tr><td colspan="1"><b>Post conditions</b> </td><td colspan="2" valign="top">User successfully views their history.   </td></tr>
<tr><td colspan="1"><b>Alternate Flow</b> </td><td colspan="2" valign="top">Technical Issue Retrieving Data </td></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b> </td><td colspan="2" valign="top">NIL </td></tr>
<tr><td colspan="1" rowspan="2"><b>Global Alternate Flow</b> </td><td colspan="1" rowspan="2" valign="top">GA1 </td><td colspan="1" valign="top">No Historical Data </td></tr>
<tr><td colspan="1" valign="top"><b>Post Condition:</b> The system returns to the actor’s dashboard. </td></tr>
</table>

3. **Use case diagram and description for SPACS Convener (extending User) asan actor to the system** 

**Use case # 9** 



|**UC ID** |UC#9 |
| - | - |
|**Use case Name** |**process\_verified\_applications** |
|**Description** |<p>The actor is able to browse the awards/scholarships applications. While browsing he also gets a facility to sort them according to CPI, Income etc. </p><p>This feature provides an in depth statistics about the applicants. </p>|
|**Actor** |SPACS Convener |



<table><tr><th colspan="1" valign="top"><b>Precondition</b> </th><th colspan="2">Actor logs into the system, opens ‘Awards and Scholarships’ portal and the output of ‘process_submitted_applications’ </th></tr>
<tr><td colspan="1" rowspan="5" valign="top"><b>Main Flow</b> </td><td colspan="1">1 </td><td colspan="1">Click on ‘Browse Applications’ </td></tr>
<tr><td colspan="1">2 </td><td colspan="1">Select an award/scholarship </td></tr>
<tr><td colspan="1" valign="top">3 </td><td colspan="1">All the verified applications for the above selected option are displayed and can be sorted according to various factors as displayed in description. </td></tr>
<tr><td colspan="1" valign="top">4 </td><td colspan="1" valign="top">Actor selects one of the applications and checks that application. </td></tr>
<tr><td colspan="1" valign="top">5 </td><td colspan="1" valign="top">Actor checks the hardcopies of submitted files (if required), then he updates the status of the application to the APPROVED. [A1] </td></tr>
<tr><td colspan="1"><b>Post conditions</b> </td><td colspan="2" valign="top">Actor grants the application and the respective student is regarding the same. </td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Alternate Flow</b> </td><td colspan="1" valign="top">A1 </td><td colspan="1">If actor finds any false information he REJECTS the application by clicking the REJECT button corresponding to that application. </td></tr>
<tr><td colspan="1"></td><td colspan="1"><b>Post Condition</b>: The corresponding application gets rejected and the applicant (student) is informed regarding the same. </td></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b> </td><td colspan="2" valign="top">NIL </td></tr>
<tr><td colspan="1" rowspan="2"><b>Global Alternate Flow</b> </td><td colspan="1" rowspan="2" valign="top">GA1 </td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on dashboard button. </td></tr>
<tr><td colspan="1" valign="top"><b>Post Condition:</b> The system returns to the actor’s dashboard. </td></tr>
</table>

**Use case # 10** 



|**UC ID** |UC#10 |
| - | - |
|**Use case Name** |**manage\_catalogue** |
|**Description** |The actor can make changes to the application procedure and also scrap the existing awards/prizes/scholarship. |



<table><tr><th colspan="1" valign="top"><b>Actor</b> </th><th colspan="2" valign="top">SPACS Convener </th></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b> </td><td colspan="2" valign="top">Logs into the system, opens awards/scholarships portal </td></tr>
<tr><td colspan="1" rowspan="3" valign="top"><b>Main Flow</b> </td><td colspan="1" valign="top">1 </td><td colspan="1">Selects ‘Manage Catalogue’ option on the screen and list of awards and scholarships are displayed. </td></tr>
<tr><td colspan="1" valign="top">2 </td><td colspan="1">If an award/medal has to be modified/deleted then click on ‘edit button’ next to the award/medal </td></tr>
<tr><td colspan="1" valign="top">3 </td><td colspan="1" valign="top">Make the necessary changes and click on ‘Save changes’ button. </td></tr>
<tr><td colspan="1"><b>Post conditions</b> </td><td colspan="2">The award/scholarship database is updated accordingly, and the SPACS manual needs to be updated as a result. </td></tr>
<tr><td colspan="1"><b>Alternate Flow</b> </td><td colspan="2" valign="top">NIL </td></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b> </td><td colspan="2" valign="top">NIL </td></tr>
<tr><td colspan="1" rowspan="2"><b>Global Alternate Flow</b> </td><td colspan="1" rowspan="2" valign="top">GA1 </td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on dashboard button. </td></tr>
<tr><td colspan="1" valign="top"><b>Post Condition:</b> The system returns to the actor’s dashboard. </td></tr>
</table>

**Use case # 11** 



<table><tr><th colspan="1" valign="top"><b>UC ID</b> </th><th colspan="2" valign="top">UC#11 </th></tr>
<tr><td colspan="1"><b>Use case Name</b> </td><td colspan="2" valign="top"><b>invite_applications</b> </td></tr>
<tr><td colspan="1" valign="top"><b>Description</b> </td><td colspan="2">He can invite the applications for the MCM scholarship or awards (if necessary) for all the students satisfied the criteria as mentioned in SPACS manual. </td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b> </td><td colspan="2" valign="top">SPACS Convener </td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b> </td><td colspan="2" valign="top">Logs into the system </td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Main Flow</b> </td><td colspan="1" valign="top">1 </td><td colspan="1">Select ‘Invite applications’ option and the list of awards or scholarship is displayed for selection </td></tr>
<tr><td colspan="1">2 </td><td colspan="1">Selects one award or MCM scholarship and click NEXT. </td></tr>
<tr><td colspan="1" valign="top">3 </td><td colspan="1">He has to select the Year of Students to which he want to invite the MCM applications or awards and click NEXT. </td></tr>
<tr><td colspan="1" valign="top">4 </td><td colspan="1" valign="top">After successful completion, Clicks INVITE button. </td></tr>
<tr><td colspan="1"><b>Post conditions</b> </td><td colspan="2" valign="top">The notification is pushed to all the recipients on their homepage upon logging in. </td></tr>
<tr><td colspan="1"><b>Alternate Flow</b> </td><td colspan="2" valign="top">NIL </td></tr>
<tr><td colspan="1"><b>Sub Flow</b> </td><td colspan="2">NIL </td></tr>
<tr><td colspan="1" rowspan="2"><b>Global Alternate Flow</b> </td><td colspan="1" rowspan="2" valign="top">GA1 </td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on dashboard button. </td></tr>
<tr><td colspan="1" valign="top"><b>Post Condition:</b> The system returns to the actor’s dashboard. </td></tr>
</table>

4. **Use case diagram and description for SPACS Assistant (extends User) asactor to the system** 

**Use case # 12** 

**UC ID**  UC#12 ![](Aspose.Words.c154b3e5-6f3c-4428-91d6-bcdb87880290.004.png)



<table><tr><th colspan="1"><b>Use case Name</b> </th><th colspan="2" valign="top"><b>process_submitted_applications</b> </th></tr>
<tr><td colspan="1" valign="top"><b>Description</b> </td><td colspan="2"><p>The actor is able to browse the awards/scholarships applications. While browsing he also gets a facility to sort them according to CPI, Income etc. </p><p>This feature provides an indepth statistics about the applicants. </p></td></tr>
<tr><td colspan="1"><b>Actor</b> </td><td colspan="2">SPACS Assistant </td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b> </td><td colspan="2" valign="top">Actor logs into the system, opens ‘Awards and Scholarships’ portal </td></tr>
<tr><td colspan="1" rowspan="5" valign="top"><b>Main Flow</b> </td><td colspan="1">1 </td><td colspan="1">Click on ‘Browse applications’ </td></tr>
<tr><td colspan="1">2 </td><td colspan="1">Select an award/scholarship </td></tr>
<tr><td colspan="1">3 </td><td colspan="1">All the Submitted applications for the above selected option are displayed </td></tr>
<tr><td colspan="1" valign="top">4 </td><td colspan="1" valign="top">Actor selects one of the applications and checks that application. </td></tr>
<tr><td colspan="1" valign="top">5 </td><td colspan="1" valign="top">Actor checks the hardcopies of submitted files (if required), then he updates the status of the application to the VERIFIED. [A1] </td></tr>
<tr><td colspan="1"><b>Post conditions</b> </td><td colspan="2" valign="top">Actor verifies the application and the respective student is notified regarding the same. </td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Alternate Flow</b> </td><td colspan="1" valign="top">A1 </td><td colspan="1">If actor finds any false information, he REJECTS the application by clicking the REJECTbutton corresponding to that application. </td></tr>
<tr><td colspan="1"></td><td colspan="1"><b>Post Condition</b>: The corresponding application gets rejected and the applicant (student) is notified regarding the same. </td></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b> </td><td colspan="2" valign="top">NIL </td></tr>
<tr><td colspan="1" rowspan="2"><b>Global Alternate Flow</b> </td><td colspan="1" rowspan="2" valign="top">GA1 </td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on dashboard button. </td></tr>
<tr><td colspan="1" valign="top"><b>Post Condition:</b> The system returns to the actor’s dashboard. </td></tr>
</table>

**Use case # 13** 



<table><tr><th colspan="1" valign="top"><b>UC ID</b> </th><th colspan="2" valign="top">UC#13 </th></tr>
<tr><td colspan="1"><b>Use case Name</b> </td><td colspan="2" valign="top"><b>Notify_Students</b> </td></tr>
<tr><td colspan="1" valign="top"><b>Description</b> </td><td colspan="2">The "Notify_Students" use case enables an administrator to send notifications to targeted students through the Notification System. The primary actor for this use case is the Administrator, and secondary actors include the Notification System and Students. This use case facilitates communication from the administrator to students for various purposes, such as important announcements or updates. </td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b> </td><td colspan="2" valign="top">Students, SPACS Convener, SPACS Assistant </td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b> </td><td colspan="2"><p>- Administrator is logged into the system.                                                       </p><p>- Notification System is operational.                                                             </p><p>- Students are registered in the system.   </p></td></tr>
<tr><td colspan="1" rowspan="5" valign="top"><b>Main Flow ![](Aspose.Words.c154b3e5-6f3c-4428-91d6-bcdb87880290.005.png)![](Aspose.Words.c154b3e5-6f3c-4428-91d6-bcdb87880290.006.png)![](Aspose.Words.c154b3e5-6f3c-4428-91d6-bcdb87880290.007.png)</b></td><td colspan="1" valign="top">1 </td><td colspan="1" valign="top">Administrator initiates the notification process through the User Interface. </td></tr>
<tr><td colspan="1" valign="top">2 </td><td colspan="1" valign="top">` `Administrator provides details for the notification (e.g., message, recipients).             </td></tr>
<tr><td colspan="1" valign="top">3 </td><td colspan="1" valign="top">Notification System generates notifications based on the provided details. </td></tr>
<tr><td colspan="1" valign="top">4 </td><td colspan="1" valign="top">Notification System sends notifications to the targeted Students.    </td></tr>
<tr><td colspan="1" valign="top">5 </td><td colspan="1" valign="top">Students receive and view the notifications through the User Interface </td></tr>
<tr><td colspan="1"><b>Post conditions</b> </td><td colspan="2" valign="top">Students successfully receive notifications.   </td></tr>
<tr><td colspan="1"><b>Alternate Flow</b> </td><td colspan="2" valign="top">Delayed Notification Delivery </td></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b> </td><td colspan="2" valign="top">NIL </td></tr>
<tr><td colspan="1" valign="top"><b>Global</b> </td><td colspan="1" valign="top">GA1 </td><td colspan="1" valign="top">Notification System Failure. </td></tr>
</table>

![](Aspose.Words.c154b3e5-6f3c-4428-91d6-bcdb87880290.008.png)

**Alternate  Post Condition:** The system returns to the actor’s dashboard. ![](Aspose.Words.c154b3e5-6f3c-4428-91d6-bcdb87880290.009.png)![](Aspose.Words.c154b3e5-6f3c-4428-91d6-bcdb87880290.010.png)**Flow** 

3. Other Constraints 
1. User Interface 

`   `The user interface should comply with the colour scheming and dashboard design of the FUSIONIIT. Users should be able to navigate from one functionality to  other.  Inter  module  navigation  should  be  smooth.  All  the  functionalities should be easy to use and no specific training should be required for the usage of the module. 

2. Tech Stack Used 

For developing the mobile app, dart language is used with the flutter framework. For web Javascript, HTML, CSS are used with Django framework. Postresql database is used for storing all fusion data. 

- 4. Non- Functional Requirements
1. Performance: 

` `The system should respond to user interactions quickly. Response time for booking actions, inventory updates, and notifications should be less. 

2. Scalability:

The system should handle a mass of concurrent users. System performance should be evaluated under increasing load conditions. 

3. Availability:

The system should be available 99.9% of the time. 

4. Security:

Ensure data confidentiality and integrity. Role-based authorization ensures that users can only perform actions relevant to their designated roles. 

- 5. Module dependencies with other fusion modules 
- Integration at the UI Level: 

`       `Users log into the Fusion application and land on the main dashboard.         Navigation should include direct links or buttons in Fusion’s menu, ensuring a clear path for each actor (student, spacs convener, spacs assistant) to access their specific functionalities withing the awards and scholarships module. 

- Module Level: 

  Awards and Scholarships Module interact with Notification, Dashboard, and file transfering system. 


## SRS Web Interface

Team mentor - **Dr. Ayan Seal**

Prepared by -

1. Nitya Tiwari (21BCS150)
1. Siddhi Gubrele (21BCS201)
1. Swati Tiwari (21BCS218)
1. Utkarsh Chaturvedi (21BCS227)
1. Utkarsh Raj (21BCS228)

Team Lead - Sudheer Dagar

<a name="_page1_x72.00_y120.93"></a>**Table of Contents**

[**Table of Contents** ](#_page1_x72.00_y120.93)[Revision History](https://docs.google.com/document/d/1LlYkc220ir_8dbX34LshMYrsDrpdXUY0/edit#heading=h.30j0zll)

**Introduction**

1. Introduction to Fusion
1. About the module
1. Scope of the module
1. Purpose
1. Actors and functionality

**User/Actor[ Description](https://docs.google.com/document/d/1LlYkc220ir_8dbX34LshMYrsDrpdXUY0/edit#heading=h.2et92p0)**

4. User
4. Student
4. SPACS Convener (Faculty)
4. SPACS Assistant (staff)

**Functional Requirements**

8. [Use case Diagram](https://docs.google.com/document/d/1LlYkc220ir_8dbX34LshMYrsDrpdXUY0/edit#heading=h.2s8eyo1)
8. Use case description
1. Use case Description for user as an actor
1. Use case Description for Student as an actor
1. Use case Description for SPACS Convenor as an actor
1. Use case Description for SPACS Assistant as an actor

3\.3 Other Functional Requirements (Suggestions)

**Non-Functional Requirements**

1. PERFORMANCE REQUIREMENTS
1. Security Requirements
1. Accessibility
1. Business Rules

[**List of open issues with the module 10** ](https://docs.google.com/document/d/1LlYkc220ir_8dbX34LshMYrsDrpdXUY0/edit#heading=h.1ksv4uv)[Suggestions**](https://docs.google.com/document/d/1LlYkc220ir_8dbX34LshMYrsDrpdXUY0/edit#heading=h.44sinio)

1. **Introduction**
1. **Introduction to Fusion**

FusionIIIT at PDPM Indian Institute of Information Technology, Design and Manufacturing, Jabalpur, stands as a testament to the seamless integration and automation of diverse functions. Crafted with precision using Python 3.8 and powered by the Django Web framework, this student-driven initiative aims to elevate the institute's operational landscape. From efficient administration management to academic excellence and miscellaneous departmental tasks, FusionIIIT is a comprehensive solution that harmonizes the intricacies of campus life.

Picture FusionIIIT as a digital wizard that takes care of everything, from organizing administrative tasks to smoothing out academic processes. Its reach extends beyond the usual responsibilities, delving into various departments and sections to ensure the seamless functioning of every aspect of campus life.

On the administrative side, FusionIIIT efficiently handles complex paperwork and processes. In the realm of academics, it introduces a digital touch, simplifying learning and course management. However, its role doesn't end there; FusionIIIT acts as a friendly companion across different parts of the campus, ensuring the smooth operation of all aspects of campus life.

In essence, FusionIIIT transcends being a mere tool; it's a helpful friend, dedicated to making life at PDPM IIITDM Jabalpur more organized and enjoyable for everyone.

2. **About the module**

The Award and Scholarship Portal is designed to serve as a comprehensive platform for students at IIITDMJ. Through this portal, all students can access information regarding various convocation medals, awards, and scholarships. Eligible students have the opportunity to submit applications for these honors. The portal ensures that students receive timely notifications regarding application deadlines and the necessary procedures. This automated system aims to provide a streamlined and efficient alternative to the current manual application process.

3. **Scope of the module**
1) **Purpose**

This software is primarily intended for utilization by students affiliated with IIITDM Jabalpur. Its purpose is to furnish comprehensive details pertaining to a variety of scholarships and awards. Users are also provided with the functionality to submit applications and monitor the real-time status of their applications. The Awards and Scholarship Portal represents an innovative system designed to replace the existing manual and cumbersome processes associated with applying for diverse awards and scholarships.

**Flow :**

At IIITDM Jabalpur, the student body, staff, and faculty are integral components of the institution. One notable scholarship available is the Merit Cum Means (MCM) Scholarship. Additionally, various awards and prizes, such as the Chairman's Gold Medal, Director’s Gold Medals, D&M Proficiency Gold Medals, Academic Proficiency Medals, D&M Proficiency Prizes, Director’s Silver Medals, Notional Prizes, and Certificates of Merit, are offered.

Students meeting the specified criteria outlined in the SPACS manual can apply for the MCM scholarship and other available awards. The SPACS Assistant (Staff) is responsible for physically verifying the documents submitted by students and updating this information within the portal. Subsequently, the SPACS Convener (Faculty) reviews the submitted applications and bestows awards to eligible students. For detailed information regarding the list, eligibility criteria, and application procedures for various awards and scholarships, please refer to the following document: https://www.iiitdmj.ac.in/academics/download/SPACS-fellowships.pdf

2) **Actors & Functionality**



|**S. No.**|**Actor**|**Functionality**|
| - | - | - |
|**1.**|User|<p>- Browse through the catalog of available medals, scholarships, and other awards.</p><p>- View details of previous awardees</p><p>&emsp;- View details of SPACS members.</p>|
|**2.**|Student|<p>- Log into the system.</p><p>- Browse details and modalities regarding eligibility and application procedures.</p><p>- Apply for specific medals, scholarships, or awards.</p><p>- Track application status.</p><p>- Upload necessary documents.</p>|
|**3.**|SPACS Convener (Faculty)|<p>- Circulate notifications about awards.</p><p>- Introduce new awards and modify existing ones.</p><p>- Manage Medals/Awards/Scholarships catalog.</p><p>- Decide recipients of awards.</p>|
|**4.**|SPACS Assistant (Staff)|<p>- Physically verify documents.</p><p>- Update application status of students in the portal.</p><p>- Notify students about lack of required information in applications.</p>|
2. **User/Actor Description(characteristics)**
1. **User:**
- **Role:**
  - A person who has logged into the system.
- **Functionalities:**
  - Browse through the catalog of available medals, scholarships, and other awards.
  - View details of previous awardees.
- View details of SPACS members.
2. **Student:**
- **Role:**
  - A student of IIITDM Jabalpur who logs into the system.
- **Functionalities:**
  - Log into the system.
  - Browse details and modalities regarding eligibility and application procedures.
  - Apply for specific medals, scholarships, or awards.
  - Track application status.
  - Upload necessary documents while applying for scholarships/medals.
3. **SPACS Convener (Faculty):**
- **Role:**
  - Faculty member responsible for SPACS (Scholarship and Awards Committee).
- **Functionalities:**
  - Circulate notifications about awards.
  - Introduce new awards and modify existing ones.
  - Manage Medals/Awards/Scholarships catalog.
  - Act as the final authority to decide recipients of awards.
4. **SPACS Assistant (Staff):**
- **Role:**
  - Staff member assisting SPACS.
- **Functionalities:**
  - Physically verify documents submitted by students.
  - Update application status of students in the portal.
  - Notify students in case of lack of required information in their applications.
3. **Functional Requirements**
1. **Use case Diagram**

![](Aspose.Words.d4969777-0b4a-4882-82d2-543a8d3766c2.001.jpeg)

2. **Use case description**
1. **Use Case Description for a User as an actor to the system**

**Use case # 1**



|**UC ID**|UC#1||
| - | - | :- |
|**Use case Name**|**browse\_catalogue**||
|**Description**|User of the system can browse the available medals/scholarships categorically||
|**Actor**|Students, SPACS Convener, SPACS Assistant||
|**Precondition**|The user must be logged-in and the system is having the updated catalog of all the convocation medals, MCM scholarship and Other Prizes.||
|**Main Flow**|1|Actor logs into the system and opens Awards and Scholarship Page.|



<table><tr><th colspan="1" rowspan="2"></th><th colspan="2">2</th><th colspan="1">Actor selects the ‘Browse Award Catalog’ option.</th></tr>
<tr><td colspan="2">3</td><td colspan="1">Actor selects the required award/scholarship/ medals and views the necessary details.</td></tr>
<tr><td colspan="1"><b>Post conditions</b></td><td colspan="3" valign="top">The necessary details of the awards are displayed.</td></tr>
<tr><td colspan="1"><b>Alternate Flow</b></td><td colspan="3" valign="top">NIL</td></tr>
<tr><td colspan="1"><b>Sub Flow</b></td><td colspan="3">NIL</td></tr>
<tr><td colspan="1"><b>Global Alternate Flow</b></td><td colspan="1" valign="top">GA1</td><td colspan="2" valign="top">The actor can return to the dashboard at any time by clicking on the dashboard button.</td></tr>
<tr><td colspan="1"></td><td colspan="1"></td><td colspan="2"><b>Post Condition:</b> The system returns to the actor’s dashboard.</td></tr>
</table>

**Use case # 2**



<table><tr><th colspan="1"><b>UC ID</b></th><th colspan="2">UC#2</th></tr>
<tr><td colspan="1"><b>Use case Name</b></td><td colspan="2" valign="top"><b>view_staff_details</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2">Users of the system can view administration in charge of the system, and other related staff details. This is required so student may contact authority to ask query regarding any of medals/scholarship.</td></tr>
<tr><td colspan="1"><b>Actor</b></td><td colspan="2">Students, SPACS Convener, SPACS Assistant</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2">System must have information about administration/staff. The user must be logged in and The Awards and Scholarship page is opened.</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Main Flow</b></td><td colspan="1" valign="top">1</td><td colspan="1">In the Awards and Scholarships page, the Actor selects the ‘SPACS member details’ option.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1">Actor gets the list of SPACS Convener, SPACS Assistant and other members of SPACS involved in the system (if any).</td></tr>
<tr><td colspan="1"><b>Post conditions</b></td><td colspan="2" valign="top">All the necessary details of the staff involved in the system are displayed.</td></tr>
<tr><td colspan="1" valign="top"><b>Alternate Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1"><b>Sub Flow</b></td><td colspan="2">NIL</td></tr>
<tr><td colspan="1" rowspan="2"><b>Global Alternate Flow</b></td><td colspan="1" rowspan="2" valign="top">GA1</td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on the dashboard button.</td></tr>
<tr><td colspan="1" valign="top"><b>Post Condition:</b> The system returns to the actor’s dashboard.</td></tr>
</table>

**Use case # 3**



<table><tr><th colspan="1"><b>UC ID</b></th><th colspan="2">UC#3</th></tr>
<tr><td colspan="1"><b>Use case Name</b></td><td colspan="2" valign="top"><b>view_previous_winners</b></td></tr>
<tr><td colspan="1"><b>Description</b></td><td colspan="2">Users can view previous year’s winners for various convocation medals and MCM Scholarships.</td></tr>
<tr><td colspan="1"><b>Actor</b></td><td colspan="2">Students, SPACS Convener, SPACS Assistant</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2" valign="top">System must have information about winners of medals/scholarships/awards and actor must be logged into the system and the Awards and Scholarship page is opened.</td></tr>
<tr><td colspan="1" rowspan="3" valign="top"><b>Main Flow</b></td><td colspan="1">1</td><td colspan="1">Actor selects the ‘Previous Award Winners’ option.</td></tr>
<tr><td colspan="1">2</td><td colspan="1">Actor then selects respective batch and award from the dropdown list provided</td></tr>
<tr><td colspan="1">3</td><td colspan="1">He clicks the ‘Submit’ button.</td></tr>
<tr><td colspan="1"><b>Post conditions</b></td><td colspan="2" valign="top">List of winners for the selected option are displayed in chronological order.</td></tr>
</table>



<table><tr><th colspan="1"><b>Alternate Flow</b></th><th colspan="2" valign="top">NIL</th></tr>
<tr><td colspan="1"><b>Sub Flow</b></td><td colspan="2">NIL</td></tr>
<tr><td colspan="1" rowspan="2"><b>Global Alternate Flow</b></td><td colspan="1" rowspan="2" valign="top">GA1</td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on the dashboard button.</td></tr>
<tr><td colspan="1" valign="top"><b>Post Condition:</b> The system returns to the actor’s dashboard.</td></tr>
</table>

2. **Use Case Description for a Student (extending User) as an actor to the system**

**Use case # 4**



<table><tr><th colspan="1"><b>UC ID</b></th><th colspan="2">UC#4</th></tr>
<tr><td colspan="1" valign="top"><b>Use case Name</b></td><td colspan="2" valign="top"><b>apply_for_convocation_medals</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2" valign="top"><p>The student can apply for Convocation Medals by filling out a form and uploading necessary documents.</p><p><i>Guidelines:</i> https://www.iiitdmj.ac.in/academics/download/SPACS-fellowships.pdf</p></td></tr>
<tr><td colspan="1"><b>Actor</b></td><td colspan="2">Student</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2">Student Logged in, opens Awards and Scholarship portal and applications are invited for the same.</td></tr>
<tr><td colspan="1" rowspan="5" valign="top"><b>Main Flow</b></td><td colspan="1">1</td><td colspan="1">Students click on the ‘Apply for Awards’ option and then Convocation Medals.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1">Student reads the instructions for applying for the Convocation Medals and clicks on ‘Proceed’ button.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1">Student selects the type of application from the available options and the respective form is displayed.</td></tr>
<tr><td colspan="1">3</td><td colspan="1">Student fills up all the necessary details in the form.[S1]</td></tr>
<tr><td colspan="1">4</td><td colspan="1">After successful uploading, students click on the ‘Submit’ button.</td></tr>
<tr><td colspan="1"><b>Post conditions</b></td><td colspan="2" valign="top">Application and documents submitted for verification.</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Sub Flow</b></td><td colspan="1">S1</td><td colspan="1">He can upload supporting documents.</td></tr>
<tr><td colspan="1"></td><td colspan="1"><b>Post-condition</b> - Documents are attached along with the form.</td></tr>
<tr><td colspan="1" valign="top"><b>Alternate Flow</b></td><td colspan="1"></td><td colspan="1" valign="top">NIL</td></tr>
<tr><td colspan="1" rowspan="2"><b>Global Alternate Flow</b></td><td colspan="1" rowspan="2" valign="top">GA1</td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on the dashboard button.</td></tr>
<tr><td colspan="1" valign="top"><b>Post Condition:</b> The system returns to the actor’s dashboard.</td></tr>
</table>

**Use case # 5**



|**UC ID**|UC#5|
| - | - |
|**Use case Name**|**apply\_for\_mcm\_scholarship**|
|**Description**|<p>The student can apply for MCM scholarship by filling out a form and uploading necessary documents.</p><p>*Guidelines:* https://www.iiitdmj.ac.in/academics/download/SPACS-fellowships.pdf"</p>|
|**Actor**|Student|
|**Precondition**|Student Logged in, opens Scholarship and Awards portal and applications are invited for the same|



<table><tr><th colspan="1" rowspan="4" valign="top"><b>Main Flow</b></th><th colspan="1">1</th><th colspan="1">Students click on the ‘Apply for Awards’ option and select MCM Scholarship.</th></tr>
<tr><td colspan="1">2</td><td colspan="1">MCM Scholarship form is displayed.</td></tr>
<tr><td colspan="1">3</td><td colspan="1">Student fills up the necessary details in the form[S1]</td></tr>
<tr><td colspan="1">4</td><td colspan="1">After successful uploading, students click on the ‘Submit Application’ button.</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="2" valign="top">Application and documents submitted for verification.</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Sub Flow</b></td><td colspan="1" valign="top">S1</td><td colspan="1" valign="top">He can upload supporting documents like income certificate and all the required documents (Refer to appendix A for MCM scholarship details).</td></tr>
<tr><td colspan="1"></td><td colspan="1"><b>Post-condition</b> - Documents are attached along with the form.</td></tr>
<tr><td colspan="1" valign="top"><b>Alternate Flow</b></td><td colspan="1"></td><td colspan="1" valign="top">NIL</td></tr>
<tr><td colspan="1" rowspan="2"><b>Global Alternate Flow</b></td><td colspan="1" rowspan="2" valign="top">GA1</td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on the dashboard button.</td></tr>
<tr><td colspan="1" valign="top"><b>Post Condition:</b> The system returns to the actor’s dashboard.</td></tr>
</table>

**Use case # 6**



<table><tr><th colspan="1"><b>UC ID</b></th><th colspan="2">UC#6</th></tr>
<tr><td colspan="1"><b>Use case Name</b></td><td colspan="2" valign="top"><b>track_application_status</b></td></tr>
<tr><td colspan="1"><b>Description</b></td><td colspan="2">Students view application status for each of the applied medals/scholarships.</td></tr>
<tr><td colspan="1"><b>Actor</b></td><td colspan="2">Student</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2" valign="top">Student must have applied for an award/scholarship and have a valid application number assigned</td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Main Flow</b></td><td colspan="1">1</td><td colspan="1">Students click on the ‘View Application Status’ option.</td></tr>
<tr><td colspan="1">2</td><td colspan="1">Student selects the ‘Current’ option.</td></tr>
<tr><td colspan="1">3</td><td colspan="1">All the applications status is displayed here along with the application ID.</td></tr>
<tr><td colspan="1" valign="top">4</td><td colspan="1">Student can also selects the ‘History’ option to view the status of the past applied applications.</td></tr>
<tr><td colspan="1"><b>Post conditions</b></td><td colspan="2" valign="top">The status of all applications submitted by the student in the past are displayed.</td></tr>
<tr><td colspan="1" valign="top"><b>Alternate Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1"><b>Sub Flow</b></td><td colspan="2">NIL</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1" rowspan="2" valign="top">GA1</td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on the dashboard button.</td></tr>
<tr><td colspan="1" valign="top"><b>Post Condition:</b> The system returns to the actor’s dashboard.</td></tr>
</table>

3. **Use Case Description for SPACS convener(extending user) as an actor to the system**

**Use case # 7**



|**UC ID**|UC#7|
| - | - |
|**Use case Name**|**process\_verified\_applications**|
|**Description**|<p>The actor is able to browse the awards/scholarships applications. While browsing he also gets a facility to sort them according to CPI, Income etc.</p><p>This feature provides in depth statistics about the applicants.</p>|
|**Actor**|SPACS Convener|



<table><tr><th colspan="1" valign="top"><b>Precondition</b></th><th colspan="2">Actor logs into the system, opens ‘Awards and Scholarships’ portal and the output of ‘process_submitted_applications’</th></tr>
<tr><td colspan="1" rowspan="5" valign="top"><b>Main Flow</b></td><td colspan="1">1</td><td colspan="1">Click on ‘Browse Applications’</td></tr>
<tr><td colspan="1">2</td><td colspan="1">Select an award/scholarship</td></tr>
<tr><td colspan="1" valign="top">3</td><td colspan="1">All the verified applications for the above selected option are displayed and can be sorted according to various factors as displayed in description.</td></tr>
<tr><td colspan="1" valign="top">4</td><td colspan="1" valign="top">Actor selects one of the applications and checks that application.</td></tr>
<tr><td colspan="1" valign="top">5</td><td colspan="1" valign="top">Actor checks the hardcopies of submitted files (if required), then he updates the status of the application to the APPROVED. [A1]</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="2" valign="top">Actor grants the application and the respective student is regarding the same.</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Alternate Flow</b></td><td colspan="1" valign="top">A1</td><td colspan="1">If an actor finds any false information he REJECTS the application by clicking the REJECT button corresponding to that application.</td></tr>
<tr><td colspan="1"></td><td colspan="1"><b>Post Condition</b>: The corresponding application gets rejected and the applicant (student) is informed regarding the same.</td></tr>
<tr><td colspan="1"><b>Sub Flow</b></td><td colspan="2">NIL</td></tr>
<tr><td colspan="1" rowspan="2"><b>Global Alternate Flow</b></td><td colspan="1" rowspan="2" valign="top">GA1</td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on the dashboard button.</td></tr>
<tr><td colspan="1" valign="top"><b>Post Condition:</b> The system returns to the actor’s dashboard.</td></tr>
</table>

**Use case # 8**



|**UC ID**|UC#8|
| - | - |
|**Use case Name**|**manage\_catalogue**|
|**Description**|The actor can make changes to the application procedure and also scrap the existing awards/prizes/scholarship.|



<table><tr><th colspan="1"><b>Actor</b></th><th colspan="2">SPACS Convener</th></tr>
<tr><td colspan="1"><b>Precondition</b></td><td colspan="2">Logs into the system, opens awards/scholarships portal</td></tr>
<tr><td colspan="1" rowspan="3" valign="top"><b>Main Flow</b></td><td colspan="1" valign="top">1</td><td colspan="1">Select ‘Manage Catalog’ option on the screen and list of awards and scholarships are displayed.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1">If an award/medal has to be modified/deleted then click on ‘edit button’ next to the award/medal</td></tr>
<tr><td colspan="1">3</td><td colspan="1">Make the necessary changes and click on the ‘Save changes’ button.</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="2" valign="top">The award/scholarship database is updated accordingly, and the SPACS manual needs to be updated as a result.</td></tr>
<tr><td colspan="1" valign="top"><b>Alternate Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1"><b>Sub Flow</b></td><td colspan="2">NIL</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1" rowspan="2" valign="top">GA1</td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on the dashboard button.</td></tr>
<tr><td colspan="1" valign="top"><b>Post Condition:</b> The system returns to the actor’s dashboard.</td></tr>
</table>

**Use case # 9**



<table><tr><th colspan="1"><b>UC ID</b></th><th colspan="2">UC#9</th></tr>
<tr><td colspan="1"><b>Use case Name</b></td><td colspan="2" valign="top"><b>invite_applications</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2">He can invite the applications for the MCM scholarship or awards (if necessary) for all the students who satisfy the criteria as mentioned in SPACS manual.</td></tr>
<tr><td colspan="1"><b>Actor</b></td><td colspan="2">SPACS Convener</td></tr>
<tr><td colspan="1"><b>Precondition</b></td><td colspan="2">Logs into the system</td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Main Flow</b></td><td colspan="1" valign="top">1</td><td colspan="1">Select ‘Invite applications’ option and the list of awards or scholarship is displayed for selection</td></tr>
<tr><td colspan="1">2</td><td colspan="1">Selects one award or MCM scholarship and click NEXT.</td></tr>
<tr><td colspan="1" valign="top">3</td><td colspan="1">He has to select the Year of Students to which he wants to invite the MCM applications or awards and click NEXT.</td></tr>
<tr><td colspan="1" valign="top">4</td><td colspan="1" valign="top">After successful completion, Clicks INVITE button.</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="2" valign="top">The notification is pushed to all the recipients on their homepage upon logging in.</td></tr>
<tr><td colspan="1" valign="top"><b>Alternate Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1"><b>Sub Flow</b></td><td colspan="2">NIL</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1" rowspan="2" valign="top">GA1</td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on the dashboard button.</td></tr>
<tr><td colspan="1" valign="top"><b>Post Condition:</b> The system returns to the actor’s dashboard.</td></tr>
</table>

4. **Use Case Description for SPACS assistant (extends user) as an actor to the system**

**Use case # 10**



|**UC ID**|UC#10|
| - | - |



<table><tr><th colspan="1"><b>Use case Name</b></th><th colspan="2" valign="top"><b>process_submitted_applications</b></th></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2"><p>The actor is able to browse the awards/scholarships applications. While browsing he also gets a facility to sort them according to CPI, Income etc.</p><p>This feature provides in -depth statistics about the applicants.</p></td></tr>
<tr><td colspan="1"><b>Actor</b></td><td colspan="2">SPACS Assistant</td></tr>
<tr><td colspan="1"><b>Precondition</b></td><td colspan="2">Actor logs into the system, opens ‘Awards and Scholarships’ portal</td></tr>
<tr><td colspan="1" rowspan="5" valign="top"><b>Main Flow</b></td><td colspan="1">1</td><td colspan="1">Click on ‘Browse applications’</td></tr>
<tr><td colspan="1">2</td><td colspan="1">Select an award/scholarship</td></tr>
<tr><td colspan="1">3</td><td colspan="1">All the Submitted applications for the above selected option are displayed</td></tr>
<tr><td colspan="1" valign="top">4</td><td colspan="1" valign="top">Actor selects one of the applications and checks that application.</td></tr>
<tr><td colspan="1" valign="top">5</td><td colspan="1" valign="top">Actor checks the hardcopies of submitted files (if required), then he updates the status of the application to the VERIFIED. [A1]</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="2" valign="top">Actor verifies the application and the respective student is notified regarding the same.</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Alternate Flow</b></td><td colspan="1" valign="top">A1</td><td colspan="1" valign="top">If an actor finds any false information he REJECTS the application by clicking the REJECT button corresponding to that application.</td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post Condition</b>: The corresponding application gets rejected and the applicant (student) is notified regarding the same.</td></tr>
<tr><td colspan="1"><b>Sub Flow</b></td><td colspan="2">NIL</td></tr>
<tr><td colspan="1" rowspan="2"><b>Global Alternate Flow</b></td><td colspan="1" rowspan="2" valign="top">GA1</td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on the dashboard button.</td></tr>
<tr><td colspan="1" valign="top"><b>Post Condition:</b> The system returns to the actor’s dashboard.</td></tr>
</table>

3. **Other Functional Requirements (Suggestions)**



<table><tr><th colspan="1" valign="top"><b>UC ID</b></th><th colspan="1" valign="top">UC#11</th></tr>
<tr><td colspan="1" valign="top"><b>Use case Name</b></td><td colspan="1" valign="top">Withdraw Application</td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="1" valign="top">The actor is able to withdraw his/her application if any other private or government scholarship scheme is awarded to them within the stipulated duration.</td></tr>
<tr><td colspan="1"><b>Actor</b></td><td colspan="1">Student</td></tr>
<tr><td colspan="1"><b>Precondition</b></td><td colspan="1">Actor logs into the system, opens ‘Awards and Scholarships’ portal</td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Main Flow</b></td><td colspan="1">Click on ‘Withdraw applications’</td></tr>
<tr><td colspan="1">Select an award/scholarship to be withdrawn</td></tr>
<tr><td colspan="1">All the Submitted applications for the above selected option are displayed</td></tr>
<tr><td colspan="1" valign="top">Actor selects one of the applications and clicks on the withdraw button.</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="1" valign="top">The application’s withdrawn and the respective student is notified regarding the same.</td></tr>
<tr><td colspan="1" valign="top"><b>Alternate Flow</b></td><td colspan="1" valign="top">NIL</td></tr>
<tr><td colspan="1"><b>Sub Flow</b></td><td colspan="1">NIL</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on the dashboard button.</td></tr>
<tr><td colspan="1" valign="top"><b>Post Condition:</b> The system returns to the actor’s dashboard.</td></tr>
</table>

4. **Non-Functional Requirements**
1. **PERFORMANCE REQUIREMENTS:**
- The product shall be based on the web and has to be run from a web server.
- The product shall take initial load time depending on internet connection strength which also depends on the media from which the product is run.
- The performance shall very loosely depend upon hardware components of the user given a web-browser minimum-requirements are met.
- A lot of data has to be queried from the database which may lead to decrease in response time of the pages to load if too many users request the services from the system.
2. **Security Requirements:**
- The profile of a student must not be accessible to other students.
- The documents uploaded by the students should not be shared to any third party and should be kept stored on the database only till the duration validation and approval.
3. **Accessibility:**
- The system shall provide a uniform look and feel between all the system and web pages.
- The portal should be up and running 24 hours a day. Client side of the system can

  be accessed from any device capable of running a fully-functional web-browser.

- To use complete system features the user must login with the id provided.
4. **Business Rules:**
- Applications are invited only for a specific period of time .i.e as mentioned in the notification.
- No student is allowed to fill the other student’s application forms.
- For more details, please refer to the IIITDM SPACE-fellowships manual.
5. **List of open issues with the module**



|S. No|Issue details|Category|How can it be resolved?|Any other relevant information|
| :- | - | - | :- | :- |
|1|Problem regarding convocation medal invitation|Implementation of functionality|Implement respective functionality of medals for all batches|NA|
|2|Incomplete Notifications|Notification related|Add the notification feature|NA|
|3|UI/UX|UI|Good UI for filling the form|NA|
|4|Number of Form filling at a time|Unimplemente d functionality|Check whether form is filled before or not|Only one form we have to submit in a given deadline|
|5|Sorting and other features|Unimplemente d functionality|Implement sorting on basis of cpi and other filters|NA|

6. **Suggestions:**

In the present system we are filling the various fields like correspondence address, financial assistance etc. again and again in different convocation medals forms. This can be removed and those fields can be filled only once and can be retrieved from the previously entered data.

In MCM form, there is some information like 10th school fee, 10th school name, 12th school name, 12th fee etc. remains the same for the entire 4 years of our stay in IIITDM Jabalpur. It would be better if we store that information once after filling and from the next application we do not need to fill those details.

The approval process of MCM for the verified MCM applications can be automated.

**Appendix A: Merit Cum Means (MCM) Scholarship Form**

**Indian Institute of Information Technology, Design and Manufacturing, Jabalpur**

**Application form for Merit Cum Means Scholarship**

1. Name of the Applicant: Capital Letter
1. Category (SC/ST/OBC/GEN)
1. State:
1. (i) Institute Roll No.

   2) Hall and Room No.
   2) Allahabad Bank Account No.
1. E Mail ID Address and Mobile No.
1. a. Name of

Father b Name of

Mother

3. Name of present Guardian

   (His relationship with the student if parents are not alive)

4. Name of brother (s) and their occupation
4. Name of sister (s) and their occupation
7. Present Postal address of father/ guardian
1. Fathers Gross Annual Income
1. Mothers gross annual income (if applicable)
1. Annual Income from other source

   (i.e Investment in Bank/ post office/ UTI/ LIC/ Shares/ Debenture/ Landed Property/ Income in the name of the students etc, if any)

8. Total of 7 (1) + (2) + (3) above ………………………………………. Rs. …......
9. Fathers/ Guardians Occupational Status (tick as applicable)

1\. In service (Government/ Private/ Public)

(Supported by IT form 16/ Saral Form whose annual income is above Rs. 50000/-)

2) Other than Salaried/ Pensioner

(supported by Annual Income Certificate to be issued by SDO/BDO/MRO/Tahasilder/Local Municipal Corporation/ Gram Panchayat, etc)

If business/ Medical/ Legal Practitioner/ Consultant etc

1. Name and Address of Firm/ Organization/ Shop
1. Nature of Business/ Trade
1. Trade/ Professional License / Registration No. (Copy to be enclosed)
1. Sales Tax/ Commercial Tax Registration No/ Zone
3) Pensioners/ Family Pensioners

(Supported by Non Employment certificate to be issued by SDO/BDO/MRO/ Tahsilder/ Local Municipal Corporation Gram Panchayat etc

10. Mothers Occupation

    (With address of Employer, if employed)

11. Declaration

I declare the followings:

1. No disciplinary action has been taken against me by the Institute in the preceding academic year 2016-17.
1. I am not in receipt of any other scholarship/stipend/ financial assistance, etc. from any other sources.

Encl:

Signature of father/ Guardian Signature of Student

Questionnaire to be filled by students applying for MCM (Merit Cum means) scholarship

Name:- Roll No. Sign:-

1. Please write in detail about Father’s Occupation/Profession:-
   1. Government Service/Private Service/Business
   1. Describe the post and work if in service OR Describe the Business:-
1. Please write in detail about Mother’s Occupation/Profession:-
1. No. of Four wheeler (Giver description regarding make and year):-
1. No of Two wheeler (Giver description regarding make and year):-
1. House :
1. Rented/ Owned
1. Plot area and constructed

Area. 6.High School (10th Standard)

1. Name of School
1. Fees per

month:- 7.Inter (12th Standard)

1. Name of School:-
1. Fees per month:-

8\.Amount of Educational Bank Loan along with name of Bank:

**Part II**

**(Declaration by the father/ guardian of the student)**

I declare that my Annual Family Income from other sources during the financial year ……………… was as under:

1\. Landed Properties (Certificate from Tahsilder/ Gram Panchayet): 2.Agriculture: 3.Investment in Bank/ Post Office/Unit Trust:

4. Shares Certificates/ debenture:
4. Other Sources:

Total

Further I declare that the information given above is true. I understand that the Merit cum Means Scholarship/ free ship if awarded to my son/ daughter is liable to be withheld or discontinued at the discretion of the authorities of the PDPM-IIITDM Jabalpur, with out assigning any reason. If subsequently (after award of MCM scholarship to my ward) it is found that he/ she has been granted any other scholarship/ stipend/ financial assistance etc. by any Govt/ Non Government organization for the period, I shall be bound to refund the whole amount of scholarship/ free ship/ stipend and financial assistance etc to the scholarship awarding authority immediately. I shall also be personally held responsible for the refund of the scholarship/ free ship amount (paid to my son/ daughter by Institute) **and willing to be prosecuted as per law** in the event of any information in this declaration and also in the enclosed scholarship application form, being proved incorrect later on.

Date

Signature of the father/ guardian: Full Name:

Address with pin code:

Phone/ mobile number if any

**Form A**

Annual income Certificate for those Parents/ Guardians who are in service (Govt or Private)

**Income from Salary**

Name and Address of the Employer

Certified that is employed in this organization in the capacity of (Designation…………………………………) Post held by the Employee………………………….., and that the break up of his/ her gross annual income from salary received in the financial year is as follows:

**Item**

Basic Salary if consolidated/ pay Band:

Grade Pay:

DA/ADA/ Relief:

Special Pay and Honorarium, Bonus etc if any: Other Allowances if any:

Employer Signature with seal

**Total Amount for 12 months**

Designation Date

**N.B:** All the entries as stated in column 2 above must be supported by attested copy of IT **Form 16/ SARAL** form for the corresponding year.

Guardians whose annual gross income is below Rs. 50,000/- need not submit IT return. They have to submit a certificate from Employer/ Salary disbursing officer stating that their annual income is not taxable and they need not produce **IT Form 16**.

**Form – B**

**Format of Income Affidavit**

(For use of those parents/ guardians who are not in employment anywhere and derives income from sources other than salary / pension)

(To be submitted on Non Judicial stamp paper of Rs. 20/- and sworn in before a first class Magistrate/ Notary public)

I, Shri/ Smt. ……………………………………………….a resident of ………………………….. Solemnly declare that:

1. My son/ daughter, Shri/ Miss ……………………………………………. Is currently studying at the PDPM Indian Institute of Information Technology, Design and Manufacturing Jabalpur, in 4-year B Tech programme in Engineering.
1. He/ She is an applicant for the award of Merit Cum Means Scholarship for the Academic year

   ………………………………………

3. I, declare that my spouse is employed/ not employed of my family in the financial year ………………………………….. i.e during the period from 1st April……….. to March 31 was as mentioned hereunder (supported by document):

(A) From my own professional as indicated: Rs pa

i) Income from Business/Medical Practice Legal Practice Rs pa

Engineering Consultancy etc

ii)Income from Agriculture Rs pa iii) Income from Landed Properties Rs. ………….........pa iv) Income from Investment in Bank/ Post office etc Rs pa

v) Income from Share Certificates/ Debentures Rs pa vi) Income

from any other sources (i.e. Retirement Rs. ………….........pa Benefits for VRS/ VSS etc if any

(B)Income of my wife (if any) pa

(if employed, salary certificate from employer to be enclosed) Rs pa © Income in the name of my son/ ward (if any) Rs pa

Total Income (A + B + C) Rs pa

Further, I declare that the information given above is true. I understand that the Merit Cum Means scholarship if awarded to my son/ daughter is liable to be withheld or discontinued at the discretion of the authorities of the PDPM Indian Institute of Information Technology, Design and Manufacturing Jabalpur, without assigning any reason. If subsequently (after award of MCM Scholarship to my ward) it is found that he/ she has been granted any other has been granted any other scholarship/ stipend/ Financial assistance etc by any Government / Non Government organization for the same period, I shall be bound to refund the whole amount of scholarship/ free ship/ stipend/ Financial Assistance etc to the scholarship awarding authority immediately. I shall also be personally held responsible for the refund of the scholarship/ free ship amount (paid to my son/ daughter by the Institute) **and willing to be prosecuted as per law** in the event of any information in this declaration and also in the enclosed scholarship application form, being proved incorrect later on.

(Signature of father/ guardian)

Sworn before me this ……………….. Day of ………………..2017 and signed

(Seal)

(Signature of first class Magistrate/ Notary public)

**Form C**

**(For pensioner/ family pensioner only)**

(Income/ salary certificate for those parents/ guardians who are in pensioners or retired from service or their wives are getting family pension**)**

Income from Pension/ Family pension: Rs. ………………………..

1. Name and Address of the Ex Employer with PPO Number:
1. Certified that ……………………………… was employed in this organization/ superannuated from , in the capacity of (post held by retired employee) and that the break up of his/ her annual income from Pension/ family pension received in the financial year is as follows:

**Item Total amount for 12 months**

1) Basic pension/ family pension Rs.
1) Dearness Relief: Rs.
1) Other allowances, if any Rs.

Signature of ex employer Pension disbursing officer Designation

Date

*(Official Seal)*


## API Specifications


**API Implementation Analysis**

Team mentor - **Dr. Ayan Seal**

Prepared by - 

1. Abhishek Muwal (21BCS005) 
1. Ajay Sharma (21BCS014) 
1. Aryan Atri (21BCS036) 
1. Deepak Meena (21BCS071) 
1. Sukram (21BCS212) 

Team Lead – Soham Bakul Sarode  

INDEX

1. *student\_view* (‘student\_view/$') 
1. *convener\_view* (‘convener\_view/$’) 
1. *staff\_view* (‘staff\_view/$’) 
1. *stats* (‘stats/$’) 
1. *convenerCatalogue* (‘convenerCatalogue/$’) 
1. *getWinners* (‘getWinners/$’) 
1. *get\_MCM\_Flag* (‘get\_MCM\_Flag/$’) 
1. *getConvocationFlag* (‘getConvocationFlag/$’) 
1. *getContent* (‘getContent/$’) 
1. *updateEndDate*(‘updateEndDate/$’) 

API Analysis

Module overview:-

- The **Award and Scholarship Portal** is designed to serve as a comprehensive platform for students at IIITDMJ. Through this portal, all students can access information regarding various convocation medals, awards, and scholarships. 
- Eligible students have the opportunity to submit applications for these honors. 
- The portal ensures that students receive timely notifications regarding application deadlines and the necessary procedures. This automated system aims to provide a streamlined and efficient alternative to the current manual application process. 

Api Counts:- Already made APIs - [count], Yet to be made API - [count] (estimated).

Implemented -

A general **user** can perform the following tasks - 

- **Browse Catalog**: Allows students to explore available courses and programs. 
- **View SPACS Member Details**: Access information about members of SPACS. 
  - **View Previous Award Winners**: Review details about past award recipients. 
1. *student\_view* (‘student\_view/$') - extends **user** 
- **Apply for MCM Scholarships and Convocation Medals**: Submit 

applications for academic honors. 

- **View Application Status**: Check the status of submitted scholarship and 

medal applications. 

2. *convener\_view* (‘convener\_view/$’) - extends **user** 
- **Invite Applications**: Allows the convener to invite applications for MCM scholarships and convocation medals. 
- **View Recent Invite Application Status**: Check the status of recently invited applications. 
- **Update End Date**: Modify the end date for the application invitation period. 
- **View Submitted Applications**: Access details of MCM and convocation medal applications submitted by students. 
- **View Files**: Examine files attached to applications for further evaluation. 
- **Accept or Reject Applications**: Provide the convener with the option to accept or reject submitted applications. 
3. *staff\_view* (‘staff\_view/$’) - extends **user** 
- **View Submitted Applications**: Access details of MCM and convocation medal applications submitted by students. 
- **View Files**: Examine files attached to applications for further evaluation. 
- **Verify or Reject Applications**: Provide the spacs assistant with the option to verify or reject submitted applications. 
4. *stats* (‘stats/$’) 
- The *stats* API allows users to retrieve information about previous award winners. 
5. *convenerCatalogue* (‘convenerCatalogue/$’) 
- Handles managing and retrieving catalog information for awards and scholarships. 
- It handles both updating the catalog content when a POST request is received and retrieving the catalog content when a GET request is made. 
6. *getWinners* (‘getWinners/$’) 
- The function is designed to retrieve information about winners of a specific award for a given batch year and program. It handles the retrieval of related student information, populates the context dictionary, and returns a JSON response indicating the success or failure of the operation along with the winner details if successful. 
7. *getContent* (‘getContent/$’) 
- Retrieve content for a specified award from the Award\_and\_scholarship model. - Returns a JSON response containing the result status and, if successful, the content of the award's catalog. 
8. *updateEndDate*(‘updateEndDate/$’) 
- Update the deadline for a form opened by SPACS (Space Programming and Advisory Committee) convener or assistant 

Partially Implemented -

1. *get\_MCM\_Flag* (‘get\_MCM\_Flag/$’) 
- Retrieves MCM\_flag information. 
- Issue: Response indicates a failure with a downloaded text file and mcm\_flag set to false. 
2. *getConvocationFlag* (‘getConvocationFlag/$’) 
- Retrieves convocation\_flag information. 
- Issue: Response indicates a failure with a downloaded text file and mcm\_flag set to false. 

Use cases:

1. **Browse\_catalogue** 

Description:User of the system can browse the available medals/scholarships categorically api: *#1, #2 , #3* 

2. **View\_staff\_details** 

Description:Users of the system can view administration in charge of the system, and other related staff details. This is required so student may contact authority to ask query regarding any of medals/scholarship api:*#1, #2, #3* 

3. **view\_previous\_winners** 

Description:Users can view previous year’s winners for various convocation medals and MCM Scholarship api:*#1, #2, #3* 

4. **apply\_for\_convocation\_medals** 

Description:The student can apply for Convocation Medals by filling out a form and uploading necessary documents. api:*#1* 

5. **apply\_for\_mcm\_scholarship** 

Description:The student can apply for MCM scholarship by filling out a form and uploading necessary documents. api:*#1* 

6. **track\_application\_status** 

Description:Students view application status for each of the applied medals/scholarships. api:*#1* 

7. **process\_verified\_applications** 

Description:The actor is able to browse the awards/scholarships applications. While browsing he also gets a facility to sort them according to CPI, Income etc.This feature provides in depth statistics about the applicants. api:*#2* 

8. **manage\_catalogue** 

Description:The actor can make changes to the application procedure and also scrap the existing awards/prizes/scholarship. api:*#5* 

9. **invite\_applications** 

*Description*:He can invite the applications for the MCM scholarship or awards (if necessary) for all the students who satisfy the criteria as mentioned in SPACS manual. api:*#2* 

10. **process\_submitted\_applications** 

Description:The actor is able to browse the awards/scholarships applications. While browsing he also gets a facility to sort them according to CPI, Income etc.This feature provides in -depth statistics about the applicants. 

api:*#3* 

This is prepared in web but no endpoints for app.

## UI for Application


***Faculty Mentor: Dr. Ayan Seal***

1 . **Module Description**:

The purpose of the project entitled as AWARD AND SCHOLARSHIP SECTION (APP) is to streamline the process

of managing awards and scholarships within the college. The scope of the application covers the entire awards and scholarships offered by the college, providing users with easy access to view available awards, eligibility criteria, application procedures, and deadlines.

Award and Scholarship Management :-

- Application Submission
- Review and Selection
- Notification and Disbursement

**2 Actors**

USE CASE DIAGRAM:

![](assets/SPACS_UCD.png)

**User/Actor Characteristics:**

1. **User:**

A user is the person who have logged in the system.

**Role:** Browse through catalogue of awards and scholarships ***Specific Functionalities:***

- Browse available medals and scholarships
- Browse previous winners of medals and scholarships
- View the details of SPACS members

![](Aspose.Words.35fd1931-0286-4422-af47-59d7af6a387d.002.png)

2. **Student:**

A student is main user who will use this portal to apply for various scholarships and awards.

**Role:** Browse through catalogue and fill forms for the available awards and scholarships.

***Specific Functionalities:***

- Submit applications through the ERP portal
- Fill the form and upload required documents
- Receives notifications about the application approval/rejection
- Can track the application status and also see the application history

![](Aspose.Words.35fd1931-0286-4422-af47-59d7af6a387d.003.png)

3. **SPACS CONVENER:**

He is responsible for circulating notifications about the awards and also decides the recipients.

**Role:** Invite applications and decides the winners of awards and scholarships ***Specific Functionalities:***

- Invite applications for awards and scholarships
- Circulate information regarding new applications
- Can introduce new awards and modify the existing ones
- Finally decides who will be awarded for the medals and scholarships

![](Aspose.Words.35fd1931-0286-4422-af47-59d7af6a387d.004.png)

![](Aspose.Words.35fd1931-0286-4422-af47-59d7af6a387d.005.png)

He is the person who will be responsible for physical verification of documents.

**Role:** Physically verifies the documents and notify to students ***Specific Functionalities:***

- Will verify the application documents physically
- Update the application status of students in the portal
- Notify the students in case of lack of required document

**Here is the figma files link :**

[https://www.figma.com/file/IHNUiFQ4nV4sOjVK1M4Huk/Untitled?type=design&n ode-id=0%3A1&mode=design&t=5wic60yGwJ8giUWS-1](https://www.figma.com/file/IHNUiFQ4nV4sOjVK1M4Huk/Untitled?type=design&node-id=0%3A1&mode=design&t=5wic60yGwJ8giUWS-1)


## UI for Web

` `Student Mentor: Sudheer Dagar 

***Faculty Mentor: Dr. Ayan Seal*** 

1 . **Module Description**: 

The purpose of the project entitled as AWARD AND SCHOLARSHIP SECTION (APP) is to streamline the process of managing awards and scholarships within the college. The scope of the application covers the entire awards and scholarships offered by the college, providing users with easy access to view available awards, eligibility criteria, application procedures, and deadlines. 

Award and Scholarship Management  :- 

- Application Submission 
- Review and Selection 
- Notification and Disbursement 

**2  Actors** 

USE CASE DIAGRAM: 

![](assets/SPACS_UCD.png)

Figma link: [https://www.figma.com/file/VXD9KBQ5ofBWvW6IJpp8Js/Untitled?type=design&node-id=1- 51&mode=design&t=oRgMfl3uz0bcE5ZP-0 ](https://www.figma.com/file/VXD9KBQ5ofBWvW6IJpp8Js/Untitled?type=design&node-id=1-51&mode=design&t=oRgMfl3uz0bcE5ZP-0) 

**User/Actor Characteristics:** 

1. **User:** 

A user is the person who have logged in the system. 

**Role:** Browse through catalogue of awards and scholarships ***Specific Functionalities:*** 

- Browse available medals and scholarships 
- Browse previous winners of medals and scholarships 
- View the details of SPACS members 

UC#1 = Browse Catalogue 

`     `UC#2 = View staff details 

`     `UC#3 = View previous winners 

2. **Student:** 

A student is main user who will use this portal to apply for various scholarships and awards. 

**Role:** Browse through catalogue and fill forms for the available awards and scholarships. 

***Specific Functionalities:*** 

- Submit applications through the ERP portal 
- Fill the form and upload required documents 
- Receives notifications about the application approval/rejection 
- Can track the application status and also see the application history 

UC#4 = Apply for convocation medals UC#5 = Apply for mcm scholarship UC#6 = Track application status 

Figma profile link: [https://www.figma.com/proto/VXD9KBQ5ofBWvW6IJpp8Js/Untitled?type=design&nod e-id=1-341&t=mCAS7vjSQ1rYwnK9-0&scaling=min-zoom&page- id=1%3A274&starting-point-node-id=1%3A341 ](https://www.figma.com/proto/VXD9KBQ5ofBWvW6IJpp8Js/Untitled?type=design&node-id=1-341&t=mCAS7vjSQ1rYwnK9-0&scaling=min-zoom&page-id=1%3A274&starting-point-node-id=1%3A341) 

3. **SPACS CONVENER:** 

He is responsible for circulating notifications about the awards and also decides the recipients. 

**Role:** Invite applications and decides the winners of awards and scholarships ***Specific Functionalities:*** 

- Invite applications for awards and scholarships 
- Circulate information regarding new applications 
- Can introduce new awards and modify the existing ones 
- Finally decides who will be awarded for the medals and scholarships 

UC#7 = Process verified applications UC#8 = Manage catalogue 

UC#9 = Invite applications 

UC#10 = Process submitted applications

Figma profile link:  

[https://www.figma.com/proto/VXD9KBQ5ofBWvW6IJpp8Js/Untitled?type=design&node-id=1- 69&t=oRgMfl3uz0bcE5ZP-0&scaling=min-zoom&page-id=0%3A1&starting-point-node-id=1%3A51 ](https://www.figma.com/proto/VXD9KBQ5ofBWvW6IJpp8Js/Untitled?type=design&node-id=1-69&t=oRgMfl3uz0bcE5ZP-0&scaling=min-zoom&page-id=0%3A1&starting-point-node-id=1%3A51) 

4. **SPACS ASSISTANT:** 

He is the person who will be responsible for physical verification of documents. 

**Role:** Physically verifies the documents and notify to students ***Specific Functionalities:*** 

- Will verify the application documents physically 
- Update the application status of students in the portal 
- Notify the students in case of lack of required document 

  Figma profile link: https://www.figma.com/proto/VXD9KBQ5ofBWvW6IJpp8Js/Untitled?type=design& node-id=1-571&t=mCAS7vjSQ1rYwnK9-0&scaling=contain&page-id=1%3A546 

**Figma files link  :** 

[https://www.figma.com/file/VXD9KBQ5ofBWvW6IJpp8Js/Untitled?type=design& node-id=1-51&mode=design&t=oRgMfl3uz0bcE5ZP-0 ](https://www.figma.com/file/VXD9KBQ5ofBWvW6IJpp8Js/Untitled?type=design&node-id=1-51&mode=design&t=oRgMfl3uz0bcE5ZP-0)     



## Database Schema

**Database Documentation of [** Awards and scholarships - AC5 **] 4.0 Overview of the Module:**

**SRS:** [Link](https://docs.google.com/document/d/1OwY8ZZfKYp2f4Dj9hpvq6YepJdEAfxMhfjNUq-vcW6c/edit?usp=sharing)

1. **ER Diagram (to be created using draw.io): [Link**](https://drive.google.com/file/d/1dqpxF-4r7yCE1d70unnMQ6ESWGrbAjCL/view?usp=sharing)**
1. **Database Schema Info (in the Google sheet): [Link**](https://docs.google.com/spreadsheets/d/1JW_q1akBwhUrQiF8jlQYrOkBRJCkMN15z16lqpAKVuM/edit?usp=sharing)**
1. **Mention all the changes required in the currently implemented Tables:- (These changes will be done in this current version 4.0)**

**[No Changes required]**

4. **Data Availability for API and Functional Testing D.1 Mention the tables that are already populated**
- Awards\_and\_Scholarships
- Director\_gold
- Director\_silver
- Mcms
- Notifications
- Previous\_winners
- Proficiency\_dm
- Releases

**D.2 Mention the tables required to be populated**

- Applications
- Holds\_designation

**D.3 Mention any difficulties faced by your team regarding populating any table (if any)**

**[None]**
