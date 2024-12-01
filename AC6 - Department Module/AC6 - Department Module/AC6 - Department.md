# HR Module Documentation

## Table of Contents
- [User-Centered Design (UCD)](#user-centered-design-ucd)
- [SRS Application](#srs-application)
- [SRS Web Interface](#srs-web-interface)
- [API Specifications](#api-specifications)
- [UI for Application](#ui-for-application)
- [UI for Web](#ui-for-web)
- [Database Schema](#database-schema)

## User-Centered Design (UCD)
![Use Case Diagram](assets/AC6_UCD.png)

## SRS Application

**AC-6 Department Module (Mobile App)**

**Prepared By**

Anoop Kumar(21BCS026) Alok Kumar(21BCS018) Ankit Singh(21BCS024) Dharavath Vinod(21BCS076) Vishal Parihar(21BCS244)

**Student Mentor: Varun Sandeep Singh(21BCS237) Faculty Mentor: Prof. Pritee Khanna**

Table of Contents

1. Introduction………………………………………………………………………..3
1. Introduction about the Fusion – A brief Description………….….3
1. Purpose of the module …………………………………………………………………………4
1. Scope of the module………………………………………………………………………………4
2. User/Actor Characteristics…………………………………………….5
1. Student……………………………………......................................................................5
1. Faculty………………………………………….……………………………………………………………….5
1. Admin…………………............................................................................................6
3. Functional Requirements…….…….…………………………………7
1. Use case diagram…………………………………………………………………………..……….7
1. Use case description……………………………………………………………………….……..8
1. Other constraints…………………………………………………………………………………...15
1. User Interfaces………………………………………………………………………..….…15
1. Software (Tech) Stack used……………………………………………………..15
4. Non-Functional Requirements….………………………………16
1. Performance…………………………………………………………………………………………….16
1. Scalability…………………………………………………………………………………………………16
1. Availability………………………………………………………………………………………………..16
1. Security………………………………………………………………………………………………………16
5. Module dependencies with other modules.….………16
1. Integration at UI level………………………………………………………………………...16
1. Database level dependencies…………………………………………………………..17
1. Module level dependencies……………………………………………………………….17
1. **Introduction**
1. **Introduction about the Fusion – A brief Description**

Embark on a transformative journey with the FusionIIIT Mobile App, a cutting-edge solution meticulously crafted using Flutter and Dart to enhance the operational landscape of PDPM Indian Institute of Information Technology, Design and Manufacturing, Jabalpur. Developed by proactive students, this mobile app serves as a dynamic companion, seamlessly integrating and automating diverse functions across the campus.

Picture the FusionIIIT Mobile App as your digital ally, streamlining administrative tasks, elevating academic experiences, and ensuring the smooth functioning of various departments. Whether you're navigating complex paperwork on the admin side or seeking a digital touch for enhanced learning and course management, FusionIIIT Mobile App goes beyond the ordinary to foster a well-organized and enjoyable campus life.

Much like its web counterpart, the FusionIIIT Mobile App is not just a tool; it's a friendly companion that accompanies you through every facet of campus life. From simplifying administrative processes to enhancing academic efficiency, this app is designed to make your experience at PDPM IIITDM Jabalpur more organized and enjoyable. Embrace the future of campus management with FusionIIIT Mobile App – your key to a seamlessly integrated and automated campus experience.

2. **Purpose of the module**

This document outlines the specific requirements for the development of the "Department Module" within the Institute's Enterprise Resource Planning (ERP) system. The Department Module aims to establish a comprehensive platform, enabling all students at IIITDMJ to access detailed information about various departments and facilitate their registration into specific departments. Furthermore, it will ensure the timely dissemination of notifications regarding meetings, webinars, and essential announcements made by faculty members. The system will empower faculty members to efficiently access and modify student data, offering an automated and streamlined alternative to the current manual application procedures.

3. **Scope of the module**

The Department module is designed to efficiently view all details regarding students , faculty , department and alumni. Seamless interactions with faculty is facilitated through this module . It has three primary actors : Student , Faculty and Admin.

2. **User/Actor characteristics**
1. **Student**

A student of IIITDM Jabalpur who first logs into the system. He is able to browse through the details of the student, faculty, Alumni and the department

**Role:** View the details of students , faculty, department and alumni. **Specific Functionalities:**

- View Student details
- VIew Faculty details
- View Department details
- View Alumni details
- Browse announcements made by faculty/administrator
2. **Faculty**

Faculty can view details of students,faculty,department and alumni.

**Role:** Make announcement related to academics ,internships or initiatives

**Specific Functionalities:**

- View Student details
- VIew Faculty details
- View Department details
- View Alumni details
- Make announcements
- Browse announcements
3. **Admin**

Head of department

**Role:** Responsible for circulating notification / making announcement regarding meetings/webinar/conferences. Each Department has different admin and the respective admin can make the announcement for that department .

**Specific Functionalities:**

- View Student details
- VIew Faculty details
- View Department details
- View Alumni details
- Make announcements for the faculty and students
- Browse announcements
3. **Functional Requirements**
1. **Use case diagram**

   ![](Aspose.Words.03b6b10e-f281-46bd-b878-717d3c69ada8.001.png)

2. **Use case description Use case #1**



<table><tr><th colspan="1" valign="top">UC ID</th><th colspan="2" valign="top">UC#1</th></tr>
<tr><td colspan="1" valign="top">Use case name</td><td colspan="2" valign="top">View_student_detail</td></tr>
<tr><td colspan="1" valign="top">Description</td><td colspan="2" valign="top">The actor can view the student registered in respective departments in the institute according to the batches.</td></tr>
<tr><td colspan="1" valign="top">Actor</td><td colspan="2" valign="top">Student,Faculty,Admin</td></tr>
<tr><td colspan="1" valign="top">Precondition</td><td colspan="2" valign="top">Actor logged in, opens Department module and system has updated information of the students.</td></tr>
<tr><td colspan="1" rowspan="3" valign="top">Main Flow</td><td colspan="1" valign="top">1\.</td><td colspan="1" valign="top">Actor selects the respective department on the main page of the module.</td></tr>
<tr><td colspan="1" valign="top">2\.</td><td colspan="1" valign="top">Actor clicks the “Students” tab and selects the batches.</td></tr>
<tr><td colspan="1" valign="top">3\.</td><td colspan="1" valign="top">Actor clicks on the respective batch to view the details.</td></tr>
<tr><td colspan="1" valign="top">Post condition</td><td colspan="2" valign="top">List of the student for the selected option are displayed</td></tr>
<tr><td colspan="1" valign="top">Alternate Flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" valign="top">Sub flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">Global Alternate flow</td><td colspan="1" rowspan="2" valign="top">GA1</td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on the dashboard button.</td></tr>
<tr><td colspan="1" valign="top">Post condition: The system returns to the actor’s dashboard.</td></tr>
</table>

**Use case #3****
<table><tr><th colspan="1" valign="top">UC ID</th><th colspan="2" valign="top">UC#2</th></tr>
<tr><td colspan="1" valign="top">Use case name</td><td colspan="2" valign="top">View_faculty_detail</td></tr>
<tr><td colspan="1" valign="top">Description</td><td colspan="2" valign="top">The actor can view the faculty registered in respective departments in the institute according to the department.</td></tr>
<tr><td colspan="1" valign="top">Actor</td><td colspan="2" valign="top">Student,Faculty,Admin</td></tr>
<tr><td colspan="1" valign="top">Precondition</td><td colspan="2" valign="top">Actor logged in, opens Department module and system has updated information of the faculties.</td></tr>
<tr><td colspan="1" rowspan="3" valign="top">Main Flow</td><td colspan="1" valign="top">1\.</td><td colspan="1" valign="top">Actor selects the respective department on the main page of the module.</td></tr>
<tr><td colspan="1" valign="top">2\.</td><td colspan="1" valign="top">Actor selects the “Faculty tab”.</td></tr>
<tr><td colspan="1" valign="top">3\.</td><td colspan="1" valign="top">Actor clicks on the view faculty to view the details.</td></tr>
<tr><td colspan="1" valign="top">Post condition</td><td colspan="2" valign="top">List of the faculties for the selected option are displayed</td></tr>
<tr><td colspan="1" valign="top">Alternate Flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" valign="top">Sub flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">Global Alternate flow</td><td colspan="1" rowspan="2" valign="top">GA1</td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on the dashboard button.</td></tr>
<tr><td colspan="1" valign="top">Post condition: The system returns to the actor’s dashboard.</td></tr>
</table>



<table><tr><th colspan="1" valign="top">UC ID</th><th colspan="2" valign="top">UC#3</th></tr>
<tr><td colspan="1" valign="top">Use case name</td><td colspan="2" valign="top">View _department_detail</td></tr>
<tr><td colspan="1" valign="top">Description</td><td colspan="2" valign="top">The actor can view the faculty registered in respective departments in the institute according to the department.</td></tr>
<tr><td colspan="1" valign="top">Actor</td><td colspan="2" valign="top">Student,Faculty,Admin</td></tr>
<tr><td colspan="1" valign="top">Precondition</td><td colspan="2" valign="top">Actor logged in, opens Department module and system has updated information of the department.</td></tr>
<tr><td colspan="1" valign="top">Main Flow</td><td colspan="1" valign="top">1\.</td><td colspan="1" valign="top">Actor selects the respective department on the main page of the module.</td></tr>
<tr><td colspan="1" valign="top">Post condition</td><td colspan="2" valign="top">List of the department for the selected option are displayed</td></tr>
<tr><td colspan="1" valign="top">Alternate Flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" valign="top">Sub flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">Global Alternate flow</td><td colspan="1" rowspan="2" valign="top">GA1</td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on the dashboard button.</td></tr>
<tr><td colspan="1" valign="top">Post condition: The system returns to the actor’s dashboard.</td></tr>
</table>


**Use case #4**



<table><tr><th colspan="1" valign="top">UC ID</th><th colspan="2" valign="top">UC#4</th></tr>
<tr><td colspan="1" valign="top">Use case name</td><td colspan="2" valign="top">View_alumni_detail</td></tr>
<tr><td colspan="1" valign="top">Description</td><td colspan="2" valign="top">The actor can view the Alumni registered in respective departments of the institute according to the department.</td></tr>
<tr><td colspan="1" valign="top">Actor</td><td colspan="2" valign="top">Student,Faculty,Admin</td></tr>
<tr><td colspan="1" valign="top">Precondition</td><td colspan="2" valign="top">Actor logged in, opens Department module and system has updated information of the Alumni.</td></tr>
<tr><td colspan="1" rowspan="3" valign="top">Main Flow</td><td colspan="1" valign="top">1\.</td><td colspan="1" valign="top">Actor selects the respective department on the main page of the module.</td></tr>
<tr><td colspan="1" valign="top">2\.</td><td colspan="1" valign="top">Actor selects the “Alumni tab”.</td></tr>
<tr><td colspan="1" valign="top">3\.</td><td colspan="1" valign="top">Actor clicks on the view Alumni to view the details</td></tr>
<tr><td colspan="1" valign="top">Post condition</td><td colspan="2" valign="top">List of the Alumni for the selected option are displayed</td></tr>
<tr><td colspan="1" valign="top">Alternate Flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" valign="top">Sub flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">Global Alternate flow</td><td colspan="1" rowspan="2" valign="top">GA1</td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on the dashboard button.</td></tr>
<tr><td colspan="1" valign="top">Post condition: The system returns to the actor’s dashboard.</td></tr>
</table>

**Use case #5****
<table><tr><th colspan="1" valign="top">UC ID</th><th colspan="2" valign="top">UC#5</th></tr>
<tr><td colspan="1" valign="top">Use case name</td><td colspan="2" valign="top">Browse_announcement</td></tr>
<tr><td colspan="1" valign="top">Description</td><td colspan="2" valign="top">User of the system can browse the available notifications/announcement</td></tr>
<tr><td colspan="1" valign="top">Actor</td><td colspan="2" valign="top">Admin,Student,Faculty</td></tr>
<tr><td colspan="1" valign="top">Precondition</td><td colspan="2" valign="top">The user must be logged in and the system is having the updated information of all the departments and announcements made.</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">Main Flow</td><td colspan="1" valign="top">1\.</td><td colspan="1" valign="top">Actor logs into the system and opens Department Page.</td></tr>
<tr><td colspan="1" valign="top">2\.</td><td colspan="1" valign="top">Actor selects the Browse announcement option</td></tr>
<tr><td colspan="1" valign="top">Post condition</td><td colspan="2" valign="top"><p>The necessary details of the department are displayed .</p><p>The system returns to the actor’s dashboard</p></td></tr>
<tr><td colspan="1" valign="top">Alternate Flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" valign="top">Sub flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" valign="top">Global Alternate flow</td><td colspan="1" valign="top">GA1</td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on the dashboard button.</td></tr>
</table>


**Use case #6**

Use case description for Admin (extending User) as an actor.



<table><tr><th colspan="1" valign="top">UC ID</th><th colspan="2" valign="top">UC#6</th></tr>
<tr><td colspan="1" valign="top">Use case name</td><td colspan="2" valign="top">make_announcement</td></tr>
<tr><td colspan="1" valign="top">Description</td><td colspan="2" valign="top">Admin can make new announcement related to department for student and Faculty related to that specific department</td></tr>
<tr><td colspan="1" valign="top">Actor</td><td colspan="2" valign="top">Admin</td></tr>
<tr><td colspan="1" valign="top">Precondition</td><td colspan="2" valign="top">Admin logged in ,opened Department module</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">Main Flow</td><td colspan="1" valign="top">1\.</td><td colspan="1" valign="top">Admin selects the “Make Announcement “ tab</td></tr>
<tr><td colspan="1" valign="top">4\.</td><td colspan="1" valign="top">Admin types the announcement and clicks publish</td></tr>
<tr><td colspan="1" valign="top">Post condition</td><td colspan="2" valign="top">The announcement made by the admin is visible to the faculty and students under the “browse announcement “ option.</td></tr>
<tr><td colspan="1" valign="top">Alternate Flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" valign="top">Sub flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">Global Alternate flow</td><td colspan="1" rowspan="2" valign="top">GA1</td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on the dashboard button.</td></tr>
<tr><td colspan="1" valign="top">Post condition: The system returns to the actor’s dashboard.</td></tr>
</table>

**Use case #7**

Use case description for Faculty (extending User) as an actor.



<table><tr><th colspan="1" valign="top">UC ID</th><th colspan="2" valign="top">UC#7</th></tr>
<tr><td colspan="1" valign="top">Use case name</td><td colspan="2" valign="top">make_announcement</td></tr>
<tr><td colspan="1" valign="top">Description</td><td colspan="2" valign="top">Faculty can make new announcement related to department for student and admin related to that specific department</td></tr>
<tr><td colspan="1" valign="top">Actor</td><td colspan="2" valign="top">Faculty</td></tr>
<tr><td colspan="1" valign="top">Precondition</td><td colspan="2" valign="top">Faculty logged in ,opened Department module</td></tr>
<tr><td colspan="1" rowspan="4" valign="top">Main Flow</td><td colspan="1" valign="top">1\.</td><td colspan="1" valign="top">Faculty selects the “Make Announcement “ tab</td></tr>
<tr><td colspan="1" valign="top">2\.</td><td colspan="1" valign="top">Faculty selects who he/she wants to make an announcement for i.e. either B.Tech/M.Tech students or all students.</td></tr>
<tr><td colspan="1" valign="top">3\.</td><td colspan="1" valign="top">Faculty selects a year .Then faculty selects the course which the faculty wants to make an announcement for.</td></tr>
<tr><td colspan="1" valign="top">4\.</td><td colspan="1" valign="top">Faculty types the announcement and clicks publish</td></tr>
<tr><td colspan="1" valign="top">Post condition</td><td colspan="2" valign="top">The announcement made by the faculty is visible to the admin and particular students under the “browse announcement “ option.</td></tr>
<tr><td colspan="1" valign="top">Alternate Flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" valign="top">Sub flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" valign="top">Global Alternate flow</td><td colspan="1" valign="top">GA1</td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on the dashboard button.</td></tr>
</table>



|||Post condition: The system returns to the actor’s dashboard.|
| :- | :- | :- |

3. **Other constraints**
1. **User Interface**
- The application's interface will be developed using Flutter and Dart and is intended to be hosted on a mobile platform.
- The module will experience differing initial load times based on the strength of the mobile device's internet connection, influenced by the source media from which it is accessed.
- The mobile app's user interface should prioritize simplicity and ease of use in its design.
2. **Software(Tech) Stack Used**
- **Flutter SDK**: The official software development kit for building natively compiled applications for mobile, web, and desktop from a single codebase.
- **Dart Programming Language**: The language used to write Flutter applications, providing a reactive and component-based structure.
- **Flutter Framework**: The UI toolkit that facilitates the creation of natively compiled applications for mobile, web, and desktop from a single codebase.
- **Android Studio**: Popular integrated development environments (IDEs) for Flutter development, offering features like code completion, debugging, and more.
- **Visual Studio Code with Flutter Extension**: A lightweight and powerful code editor with extensions for Flutter development.
- **Firebase**: A mobile and web application development platform that provides various services such as authentication, cloud storage, and a real-time database.
- **Git**: A version control system commonly used to manage and track changes in the source code.
- **GitHub**: Platforms for hosting and collaborating on Git repositories.
4. **Non-Functional Requirements**
1. **Performance**

The system is required to exhibit prompt responsiveness to user interactions. Specifically, the response time for actions related to booking,inventory updates, and notifications is mandated to be minimized.

2. **Scalability**

The system must demonstrate the capability to accommodate a substantial volume of concurrent users. Evaluation of system performance should be conducted under conditions of increasing load.

3. **Availability**

The system is expected to maintain an availability rate of 99.9%, ensuring continuous operational functionality.

4. **Security**

Robust measures must be implemented to ensure the confidentiality and integrity of data. Role-based authorization mechanisms should be in place to restrict users to actions pertinent to their designated roles

5. **Module dependencies with other modules**
1. **Integration at the UI level**

Users log into the Fusion application and land on the main dashboard. The user (student, faculty, and other community members of IIITDMJ ) can navigate to the department module . Navigation should include direct links or buttons in Fusion's menu, ensuring a clear path for each actor (Student, Faculty,Admin) to access their specific functionalities within the Department Module.

2. **Database level dependencies**



|**S.No**|**Table Name**|**Primary Key**|**Foreign Key**|**Owner**|**Reference Table**|
| - | - | :- | :- | - | :- |
|1\.|department\_a nnouncements|id|maker\_id \_id|fusion\_ad min|globals\_extr ainfo|
|2\.|department\_s pecialrequest|id|request\_ maker\_id|fusion\_ad min|globals\_extr ainfo|

3. **Module level dependencies**

Department registration Module interact with Notification, and Dashboard.

Faculty details are gathered from HR department and Alumni details are gathered from Training & Placement cell.

Student details from course registration .


## SRS Web Interface

**Software Requirements Specification**

**Department Module (AC6-Web)**

Faculty Mentor: Dr. Pritee Khanna Mentor: Prajjwal Kapoor(21bcs158)

Team Members:

Aryan Shrivastava(21bcs040) Rushikesh Shinde(21bcs190) Manoj Panjwani(21bec068) Sudarshan Patidar(21bcs208) Jesvia Susan Varghese(21bcsd01)

1. Introduction
1. **Introduction about the Fusion – A Brief Description**

Fusion IIIT serves as a testament to the seamless integration and automation of diverse functions within the precincts of PDPM Indian Institute of Information Technology, Design, and Manufacturing, Jabalpur. Developed with precision through the utilization of Python 3.8 and bolstered by the Django Web framework, this initiative stands as a testament to a student-driven pursuit geared towards the enhancement of the operational fabric of the institute. Its purpose is to provide a comprehensive solution, addressing myriad facets ranging from adept administration management to the facilitation of academic excellence and the efficient handling of departmental tasks, thereby bringing cohesion to the intricate tapestry of campus life.

On the administrative front, Fusion IIIT adeptly manages intricate paperwork and processes. In the academic sphere, it introduces a digital paradigm, simplifying the realms of learning and course management. Its impact, however, transcends these specific domains;Fusion IIIT assumes the role of a genial companion for every facet of the campus, meticulously ensuring the optimal functioning of all processes.

In summary, Fusion IIIT transcends its status as a mere tool;it emerges as a discerning companion, contributing significantly to a more organized and enjoyable milieu for the entire community at PDPM IIITDM Jabalpur.

2. **Purpose of the module**

The purpose of the module is to showcase all available departments, faculty and resources available in this institute, along with the ability to make requests to the faculty and view various announcements made by the faculty and staff members.

The department view will display information regarding the department and facilities offered in the concerned department student details, faculty details, alumni details, and published announcements if any.

3. **Scope of the module**

The Department module will allow students to browse through relevant announcements and view details of faculty or students. This module also allows faculty or admin to make announcements related to either their course or announcements related to their department.

2. User/Actor characteristics
1. **Student :**

   Students can do the following tasks:

- Browse announcements which will show announcements which will be filtered based on courses which the student is attending.
- View department details which will show details about the department and its resources available like labs and equipment.
- View faculty details which will display a list of faculties which will contain a link to their information.
- View alumni details which will display details related to alumni filtered based on their year of passing out.
- View student details which will contain a list of students filtered based on year and program.
2. **Faculty :**

   The faculty can do the following tasks:

- Browse announcements which will show the announcements made by a faculty regarding a particular course or a particular department.
- View department details which will show details about the department and its resources available like labs and equipment.
- View faculty details which will display a list of faculties which will contain a link to their information.
- View alumni details which will display details related to alumni filtered based on the department and their year of passing out.
- View student details which will contain a list of students filtered based on year and program.

**Specific Functionalities:**

- Faculty can announce as per their needs. For Eg. If a faculty needs to make an announcement related to their courses this semester they can select the particular course or if they want to make an announcement for all students of the department they can do so.
3. **Admin :**

   The faculty can do the following tasks:

- Browse announcements which will show the announcements made by a faculty regarding a particular course or a particular department.
- Make announcements which will allow the faculty to make announcements as per their requirements.
- View department details which will show details about the department and its resources available like labs and equipment.
- View faculty details which will display a list of faculties which will contain a link to their information.
- View alumni details which will display details related to alumni filtered based on the department and their year of passing out.
- View student details which will contain a list of students filtered on the basis of year and program.

**Specific Functionalities:**

- Admin can make an announcement as per their needs .

3 Functional Requirements

1. **Use Case Diagram**

![](assets/AC6_UCD.png)

2. **Use Case Description** Use Case #1

 

<table><tr><th colspan="1" valign="top">UCID</th><th colspan="2" valign="top">UC#1</th></tr>
<tr><td colspan="1" valign="top">Use case name</td><td colspan="2" valign="top">Browse announcement</td></tr>
<tr><td colspan="1" valign="top">Description</td><td colspan="2" valign="top"><p>Users of the system can browse the available notifications/announcements as per the need of the user.</p><p>Announcements will be fetched on the basis of the course in which the student is enrolled and only those announcements will be visible to a particular student.for a user which is student.</p></td></tr>
<tr><td colspan="1" valign="top">Actor</td><td colspan="2" valign="top">Admin,Student,Faculty</td></tr>
<tr><td colspan="1" valign="top">Precondition</td><td colspan="2" valign="top">The user must be logged in and the system is having the updated information of all the departments and announcements made.</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">Main Flow</td><td colspan="1" valign="top">1\.</td><td colspan="1" valign="top">Actor logs into the system and opens the Department Page.</td></tr>
<tr><td colspan="1" valign="top">2\.</td><td colspan="1" valign="top">Actor selects the Browse announcement tab.</td></tr>
<tr><td colspan="1" valign="top">Post condition</td><td colspan="2" valign="top">The necessary details of the department are displayed.</td></tr>
<tr><td colspan="1" valign="top">Alternate Flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" valign="top">Sub flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" valign="top">Global Alternate flow</td><td colspan="1" valign="top">GA1</td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on the dashboard button.</td></tr>
</table>

Use Case #2



<table><tr><th colspan="1" valign="top">UCID</th><th colspan="2" valign="top">UC#2</th></tr>
<tr><td colspan="1" valign="top">Use case name</td><td colspan="2" valign="top">Make New announcement for the admin.</td></tr>
<tr><td colspan="1" valign="top">Description</td><td colspan="2" valign="top">Admin can make new announcement related to department for student and Faculty related to that specific department</td></tr>
<tr><td colspan="1" valign="top">Actor</td><td colspan="2" valign="top">Admin</td></tr>
<tr><td colspan="1" valign="top">Precondition</td><td colspan="2" valign="top">Admin logged in ,opened Department module</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">Main Flow</td><td colspan="1" valign="top">1\.</td><td colspan="1" valign="top">Admin selects the “Make Announcement “tab</td></tr>
<tr><td colspan="1" valign="top">2\.</td><td colspan="1" valign="top">Admin types the announcement and clicks publish.</td></tr>
<tr><td colspan="1" valign="top">Post condition</td><td colspan="2" valign="top">The announcement made by the admin is visible to the faculty and students under the “browse announcement “option.</td></tr>
<tr><td colspan="1" valign="top">Alternate Flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" valign="top">Sub flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">Global Alternate flow</td><td colspan="1" rowspan="2" valign="top">GA1</td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on the dashboard button.</td></tr>
<tr><td colspan="1" valign="top">Post condition : the system returns to the actor’s dashboard.</td></tr>
</table>

Use case#3



<table><tr><th colspan="1" valign="top">UCID</th><th colspan="2" valign="top">UC#3</th></tr>
<tr><td colspan="1" valign="top">Use case name</td><td colspan="2" valign="top">make new announcement</td></tr>
<tr><td colspan="1" valign="top">Description</td><td colspan="2" valign="top">Faculty can make new announcement related to department for student or other users related to that specific department</td></tr>
<tr><td colspan="1" valign="top">Actor</td><td colspan="2" valign="top">Faculty</td></tr>
<tr><td colspan="1" valign="top">Precondition</td><td colspan="2" valign="top">Faculty logged in ,opened Department module</td></tr>
<tr><td colspan="1" rowspan="4" valign="top">Main Flow</td><td colspan="1" valign="top">1\.</td><td colspan="1" valign="top">Faculty selects the “Make Announcement “tab</td></tr>
<tr><td colspan="1" valign="top">2\.</td><td colspan="1" valign="top">Faculty selects who he/she wants to make an announcement for i.e either M.Tech/B.Tech students or all students.</td></tr>
<tr><td colspan="1" valign="top">3\.</td><td colspan="1" valign="top">Faculty selects a year. Then the Faculty selects the course which the faculty wants to make an announcement for.</td></tr>
<tr><td colspan="1" valign="top">4\.</td><td colspan="1" valign="top">Faculty publishes the announcement.</td></tr>
<tr><td colspan="1" valign="top">Post condition</td><td colspan="2" valign="top">The announcement made by the faculty is visible to the admin and particular students under the “browse announcement “ option.</td></tr>
<tr><td colspan="1" valign="top">Alternate Flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" valign="top">Sub flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">Global Alternate flow</td><td colspan="1" rowspan="2" valign="top">GA1</td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on the dashboard button.</td></tr>
<tr><td colspan="1" valign="top">Post condition : the system returns to the actor’s dashboard.</td></tr>
</table>

Use case #7



<table><tr><th colspan="1" valign="top">UCID</th><th colspan="2" valign="top">UC#4</th></tr>
<tr><td colspan="1" valign="top">Use case name</td><td colspan="2" valign="top">view student detail</td></tr>
<tr><td colspan="1" valign="top">Description</td><td colspan="2" valign="top">The actor can view the student registered in respective departments in the institute according to the batches.</td></tr>
<tr><td colspan="1" valign="top">Actor</td><td colspan="2" valign="top">Student, Faculty,Admin</td></tr>
<tr><td colspan="1" valign="top">Precondition</td><td colspan="2" valign="top">Actor logged in, opens the Department module and the system has updated information about the students.</td></tr>
<tr><td colspan="1" rowspan="3" valign="top">Main Flow</td><td colspan="1" valign="top">1\.</td><td colspan="1" valign="top">Users select the respective department on the main page of the module.</td></tr>
<tr><td colspan="1" valign="top">2\.</td><td colspan="1" valign="top">Users clicks the students tab and selects the batches</td></tr>
<tr><td colspan="1" valign="top">3\.</td><td colspan="1" valign="top">Users clicks on the respective batch to view the details</td></tr>
<tr><td colspan="1" valign="top">Post condition</td><td colspan="2" valign="top">List of the student for the selected option are displayed</td></tr>
<tr><td colspan="1" valign="top">Alternate Flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" valign="top">Sub flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">Global Alternate flow</td><td colspan="1" rowspan="2" valign="top">GA1</td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on the dashboard button.</td></tr>
<tr><td colspan="1" valign="top">Post condition: the system returns to the actor’s dashboard.</td></tr>
</table>



<table><tr><th colspan="1" valign="top">UCID</th><th colspan="2" valign="top">UC#5</th></tr>
<tr><td colspan="1" valign="top">Use case name</td><td colspan="2" valign="top">view faculty detail</td></tr>
<tr><td colspan="1" valign="top">Description</td><td colspan="2" valign="top">The actor can view the faculty registered in respective departments in the institute according to the department.</td></tr>
<tr><td colspan="1" valign="top">Actor</td><td colspan="2" valign="top">Student, Faculty,Admin</td></tr>
<tr><td colspan="1" valign="top">Precondition</td><td colspan="2" valign="top">Actor logged in, opens the Department module and the system has updated information of the faculties.</td></tr>
<tr><td colspan="1" rowspan="3" valign="top">Main Flow</td><td colspan="1" valign="top">1\.</td><td colspan="1" valign="top">Users select the respective department on the main page of the module.</td></tr>
<tr><td colspan="1" valign="top">2\.</td><td colspan="1" valign="top">Users select the “Faculty tab”.</td></tr>
<tr><td colspan="1" valign="top">3\.</td><td colspan="1" valign="top">Users clicks on view faculty to view the details</td></tr>
<tr><td colspan="1" valign="top">Post condition</td><td colspan="2" valign="top">List of the faculties for the selected option are displayed</td></tr>
<tr><td colspan="1" valign="top">Alternate Flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" valign="top">Sub flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">Global Alternate flow</td><td colspan="1" rowspan="2" valign="top">GA1</td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on the dashboard button.</td></tr>
<tr><td colspan="1" valign="top">Post condition: the system returns to actor’s dashboard.</td></tr>
</table>



<table><tr><th colspan="1" valign="top">UCID</th><th colspan="2" valign="top">UC#6</th></tr>
<tr><td colspan="1" valign="top">Use case name</td><td colspan="2" valign="top">view department details</td></tr>
<tr><td colspan="1" valign="top">Description</td><td colspan="2" valign="top">The actor can view the faculty registered in respective departments in the institute according to the department.</td></tr>
<tr><td colspan="1" valign="top">Actor</td><td colspan="2" valign="top">Student, Faculty,Admin</td></tr>
<tr><td colspan="1" valign="top">Precondition</td><td colspan="2" valign="top">User logged in, opens the Department module and the system has updated information of the department.</td></tr>
<tr><td colspan="1" valign="top">Main Flow</td><td colspan="1" valign="top">1\.</td><td colspan="1" valign="top">User selects the respective department on the main page of the module.</td></tr>
<tr><td colspan="1" valign="top">Post condition</td><td colspan="2" valign="top">List of the department for the selected option are displayed</td></tr>
<tr><td colspan="1" valign="top">Alternate Flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" valign="top">Sub flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">Global Alternate flow</td><td colspan="1" rowspan="2" valign="top">GA1</td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on the dashboard button.</td></tr>
<tr><td colspan="1" valign="top">Post condition : the system returns to the actor’s dashboard.</td></tr>
</table>



<table><tr><th colspan="1" valign="top">UCID</th><th colspan="2" valign="top">UC#7</th></tr>
<tr><td colspan="1" valign="top">Use case name</td><td colspan="2" valign="top">View Alumni Details.</td></tr>
<tr><td colspan="1" valign="top">Description</td><td colspan="2" valign="top">The actor can view the faculty registered in respective departments in the institute according to the department.</td></tr>
<tr><td colspan="1" valign="top">Actor</td><td colspan="2" valign="top">Student, Faculty,Admin</td></tr>
<tr><td colspan="1" valign="top">Precondition</td><td colspan="2" valign="top">User logged in, opens the Department module and the system has updated information of the department.</td></tr>
<tr><td colspan="1" valign="top">Main Flow</td><td colspan="1" valign="top">1\.</td><td colspan="1" valign="top">User selects the view Alumni tab on the main page of the module.</td></tr>
<tr><td colspan="1" valign="top">Post condition</td><td colspan="2" valign="top">List of the Alumni for the selected option are displayed</td></tr>
<tr><td colspan="1" valign="top">Alternate Flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" valign="top">Sub flow</td><td colspan="2" valign="top">nil</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">Global Alternate flow</td><td colspan="1" rowspan="2" valign="top">GA1</td><td colspan="1" valign="top">The actor can return to the dashboard at any time by clicking on the dashboard button.</td></tr>
<tr><td colspan="1" valign="top">Post condition : the system returns to the actor’s dashboard.</td></tr>
</table>

3. **Otherconstraints**
1. User Interfaces

The user interface should comply with the color scheming and dashboard design of the FUSIONIIT. Users should be able to navigate from one functionality to another. Inter module navigation should be smooth. Allthe functionalities should be easy to use and no specific training should be required for the usage of the module


2. Tech Stack Used
- **Django**: Django is a high-level Python web framework that encourages rapid development and clean, pragmatic design. It follows the Model-View-Controller (MVC) architectural pattern.
- **Visual Studio Cod**e: Alightweight and versatile code editor commonly used for developing Flutter applications, which offers extensive Flutter and Dart extensions for enhanced development capabilities.
4. Non- Functional Requirements
1. **Performance:**
- The department module should provide quick response times for user interactions, such as department registration, student data modification, and notification retrieval.
- Response time for actions like department registration, student data updates, and notification retrieval should be within acceptable limits, with a maximum page load time of 3 seconds.
2. **Scalability:**
- The system should scale efficiently to accommodate a growing number of students and departments.
- Performance evaluations should be conducted under increasing load conditions to ensure the system remains responsive as the user base expands.
3. **Availability:**
- The department module should aim for a high availability rate, with a target of 99.9% uptime.
- Scheduled maintenance activities should be planned during non-peak hours to minimize impact on users.

4. **Security:**
- Data confidentiality and integrity should be maintained, with secure storage and transmission of sensitive information.
- Role-based authorization should be implemented to ensure that only authorized users, such as faculty members, can view and modify student data.
- Passwords should be securely hashed and stored to prevent unauthorized access.
- The department module should comply with data protection laws and ensure the privacy of student and faculty information.
5. **Usability:**
- The user interface of the department module should be designed to be intuitive and user-friendly,ensuring a positive user experience for both students and faculty.
6. **Reliability:**
- The system should have a high level of reliability,with minimal downtime for maintenance or unexpected issues.
5. Module dependencies with other fusion modules

**5.1. UILevel**

User logs into Fusion portion and lands on the main dashboard.The user (student,faculty,department admin) can click on the department button and go to the department page .From there students are able to view announcements regarding their department,courses and view student,faculty,and alumni details.

The faculty is able to make announcements and browse announcements from the department page.

2. **DB Level :**



|**S.No**|**Table Name**|**Primary Key**|**Foreign Key**|**owner**|**Reference Table**|
| - | - | - | - | - | - |
|1\.|department\_annou ncements|id|maker\_id\_id|fusion\_ admin|globals\_extrainf o|
|2\.|department\_specia lrequest|id|request\_maker\_id|fusion\_ admin|globals\_extrainf o|

3. **Module Level :**

The module will use the notification module for notifying information about announcements.



## API Specifications

**APIStatus**

**of**

**Department Module (AC6 Mobile)**

Faculty Mentor: Dr. Pritee Khanna Mentor: Varun Sundeep Singh(21BCS237)

Team Members:

Anoop Kumar(21BCS026) Alok Kumar(21BCS018) Ankit Singh(21BCS024) Dharavath Vinod(21BCS076) Vishal Parihar(21BCS244)

**Module Name** - Department AC6

**Student Mentor** - Varun Sundeep Singh(21BCS237)

**Please mention all the APIs used in the module below**

1\.{/} name = dep [Implemented]

- Parameters : none
- Description : make and browse announcements

2\.{facView/} name = faculty\_view [Implemented]

- Parameters : request
- Description : request contains metadata about the requested page

3\.{staffView/} name = staff\_view [Implemented]

- Parameters : request
- Description : request contains metadata about the requested page

4\.{All\_Students/bid} name = all\_students [Badly Implemented]

- Parameters : request , bid
- Description : request contains metadata about the requested page , bid stores key for batches

5\.{approved/} name = approved [Implemented] \*\*(to be removed)

- Parameters : request
- Description : request contains metadata about the requested page ; approve requests

6\.{deny/} name = deny [Implemented] \*\*(to be removed)

- Parameters : request
- Description : request contains metadata about the requested page ; deny requests

7\.{alumni/} name = alumni [Yet to be Implemented]

- Parameters : none
- Description : list of alumni filtered on the basis of their department

**Overview of the module:-**

The purpose of the module is to showcase all available departments, faculty and resources available in this institute, along with the ability to view various announcements made by the faculty and staff members. The department view will display information regarding the department and facilities offered in the concerned department student details, faculty details, alumni details, and published announcements if any.

The actors in this module are Student, Faculty and Staff.

APIs:-

**Already Implemented**

- **browse\_announcements :**
- *API Index 1* :
- The browse\_announcements function is designed to facilitate the browsing of announcements department-wise, as made by various faculties and administrators.
- Database - **department\_announcements** table is used to store all announcements and their information.
- **view\_department\_details :**
- API index 1 :
- Displays information regarding a particular department fetched from **department\_notification.**
- Database - globals\_department\_info table is used to fetch information regarding the department.
- **view\_faculty\_details** :
- API index 1
- Displays information regarding a particular department fetched from **department\_notification.**
- Database - globals\_department\_info table is used to fetch information regarding the department.
- **view\_students\_details**:
- API Index 4 :
- Fetches a list of all students according to their department and year (bid).
- Database - **globals\_extrainfo** table is used to fetch a list of students filtered on the basis of department and year and branch.
- **make\_announcemen**t:
- API index 2:
- facView opens faculty view through which a faculty is able to make announcements and view all requests made to him.
- Database- **department\_announcements and department\_specialrequest** tables are used to fetch announcements and requests made to the faculty.
- **make\_announcement** :
- API index 3 :
- staffView opens the staff view through which a staff member is able to make announcements..
- Database- **department\_announcements** is used .

**Yet to be Implemented**

- **view\_alumni\_details :**
- API index 7 :
- It should open a list of alumni filtered on the basis of their department.The implementation should be as follows :
  - Upon clicking on the tab it should display sections for department after which it should display a list of alumni which should contain a link to alumni’s profile similar to how view\_faculty\_details work.
- Database- this data should be taken from the placement module when implemented.

**Current problems with the module / use cases —**

- [view\_faculty\_details] : the list of faculties is fetched but some of the links are invalid as their ID should be integer but they are string. The data type of all faculty ID needs to be changed into the same input type as the function displaying their details.
- [All\_students/bid] : implementation of this API is very repetitive which could be further optimized. Every possible case is listed inside an if-else conditional statement which is highly optimizable.
- [view\_department\_details] : this function for faculty does not exist and needs to be implemented.
- DRF/Serialiser not implemented . The Serializer converts complex data types, supports validation, handles nested relationships, and integrates seamlessly with Django models. In production, DRF accelerates API development, provides authentication and permission features, supports versioning, and generates user-friendly documentation. The Serializer ensures efficient data conversion and validation, contributing to the rapid and reliable development of APIs in Django applications.
- Bad naming conventions

Document link:

[API Status AC6 Mobile App](https://docs.google.com/document/d/1HO_7TOPpjRAkQ-dGLJMWp3wTBxN8G0ftfmbGwGZcF1M/)


## UI for Application

**Figma Profiles for Department Module AC6(Mobile App)**

1. **Module Description:**

The module is to showcase all available departments, faculty and resources available in this institute and view various announcements made by the faculty and staff members. The department view will display information regarding the department and facilities offered in the concerned department student details, faculty details, alumni details, and published announcements if any.

[Use Case Specification](https://docs.google.com/document/d/1M6BCW4HeEJZqWDJlbQataBlFPpn6Q3ky40FKBvH8U7M/edit?usp=sharing)

2. **Actors**
1. **Student**

A student of IIITDM Jabalpur who first logs into the system. He is able to browse through the details of the student, faculty, Alumni and the department . Browse announcements made by faculty/administrator.

![](Aspose.Words.0c72de44-f047-49b5-9ec0-bc7371be3826.001.jpeg)

[Figma profile of Student](https://www.figma.com/file/gq1amAroXZPykbmlf6Ri7J/Fusion-AC6-Mobile-App?type=design&node-id=0-1&mode=design&t=aKoeZ7JhZTgnZ5ZO-0)

2. **Faculty**

Faculty can view details of students , faculty ,department and alumni. Make a new announcement and browse announcements made by faculty/administrator.

![](Aspose.Words.0c72de44-f047-49b5-9ec0-bc7371be3826.002.jpeg)

[Figma profile of Faculty](https://www.figma.com/file/gq1amAroXZPykbmlf6Ri7J/Fusion-AC6-Mobile-App?type=design&node-id=0-1&mode=design&t=aKoeZ7JhZTgnZ5ZO-0)

3. **Admin**

Admin can view details of students , faculty ,department and alumni. Make a new announcement and browse announcements made by faculty/administrator.

![](Aspose.Words.0c72de44-f047-49b5-9ec0-bc7371be3826.003.jpeg)

[FIgma profile of Admin](https://www.figma.com/file/gq1amAroXZPykbmlf6Ri7J/Fusion-AC6-Mobile-App?type=design&node-id=0-1&mode=design&t=aKoeZ7JhZTgnZ5ZO-0)

**Figma Profile Design Guidelines and Additional Considerations**

1. **Cross-Platform Compatibility:**
- Verify that Figma designs and features are compatible across both web and app versions.
2. **Dimension Standardization:**
- Ensure all Figma designs have the same dimensions: 1920 x 1080 for web and around 360px width for mobile.

  **5.3Actor-oriented Use Case-Based Design:**

- Strictly base all Figma designs on use cases of actors and maintain consistency with previous and newly added designs.

  -- Each actor should have different page in figma

- If the Figma profiles are already existing make sure all the actors have their own figma profiles and also wireframe those across all use cases for that actor
- Figma link (only) for reference (Figma profiles created by the previous batch): [https://www.figma.com/file/pzhw34xBvEK0hm5Yx4bh0P/Fusion-APP?type=design&nod e-id=0%3A1&mode=design&t=J0f6T5YoUiKbp17u-1](https://www.figma.com/file/pzhw34xBvEK0hm5Yx4bh0P/Fusion-APP?type=design&node-id=0%3A1&mode=design&t=J0f6T5YoUiKbp17u-1)


## UI for Web

**Figma Profile**
**of**
**Department Module (AC6-Web)**

Faculty Mentor: Dr. Pritee Khanna Mentor: Prajjwal Kapoor(21bcs158)

Team Members:

Aryan Shrivastava(21bcs040) Rushikesh Shinde(21bcs190) Manoj Panjwani(21bec068) Sudarshan Patidar(21bcs208) Jesvia Susan Varghese(21bcsd01)

**Figma Profiles for Department Module(Web)**

1. **Module Description:**

The purpose of the module is to showcase all available departments, faculty and resources available in this institute, along with the ability to view various announcements made by the faculty and staff members.

The department view will display information regarding the department and facilities offered in the concerned department student details, faculty details, alumni details, and published announcements if any. The actors in this module are Student, Faculty and Staff.

Use Case Specifications:

[AC6 Department Web SRS](https://docs.google.com/document/d/1O1wkP6rRSKNFe1PxgkkP9bNgLyjMKxnCjhx3KncUnvg/edit)

2. **Actors**
1. **Student**

Student uses the system to browse announcements which will show the announcements made by a faculty or staff.

View department details which will show details about the department and its resources available like labs and equipment.

View faculty details which will display a list of faculties which will contain a link to their information.

View alumni details which will display details related to alumni filtered based on the department and their year of passing out.

View student details which will contain a list of students filtered based on year and program.

![](Aspose.Words.bf731013-240b-4b13-86f3-70c1c4285409.001.jpeg)

Figma Link:

[https://www.figma.com/proto/ghc7ej07obPHwZzay48dg0/Department-Fig ma-Web?type=design&node-id=7-19&t=VmM2yna1Lq3YCD8v-0&scaling =scale-down&page-id=0%3A1&starting-point-node-id=7%3A19&show-pr oto-sidebar=1](https://www.figma.com/proto/ghc7ej07obPHwZzay48dg0/Department-Figma-Web?type=design&node-id=7-19&t=VmM2yna1Lq3YCD8v-0&scaling=scale-down&page-id=0%3A1&starting-point-node-id=7%3A19&show-proto-sidebar=1)

2. **Faculty**

Faculty uses the system to browse announcements which will show the announcements made by a faculty or staff.

View department details which will show details about the department and its resources available like labs and equipment.

View faculty details which will display a list of faculties which will contain a link to their information.

View alumni details which will display details related to alumni filtered based on the department and their year of passing out.

View student details which will contain a list of students filtered based on year and program.

Faculty can announce as per their needs. For Eg. If a faculty needs to make an announcement related to their courses this semester they can select the particular course or if they want to make an announcement for all students of the department they can do so.

![](Aspose.Words.bf731013-240b-4b13-86f3-70c1c4285409.002.jpeg)

Figma Link:

[https://www.figma.com/proto/ghc7ej07obPHwZzay48dg0/Department-Fig ma-Web?type=design&node-id=21-11&t=VmM2yna1Lq3YCD8v-0&scalin g=scale-down&page-id=0%3A1&starting-point-node-id=21%3A11&show- proto-sidebar=1](https://www.figma.com/proto/ghc7ej07obPHwZzay48dg0/Department-Figma-Web?type=design&node-id=21-11&t=VmM2yna1Lq3YCD8v-0&scaling=scale-down&page-id=0%3A1&starting-point-node-id=21%3A11&show-proto-sidebar=1)

3. **Staff**

Staff uses the system to browse announcements which will show the announcements made by a faculty or staff.

View department details which will show details about the department and its resources available like labs and equipment.

View faculty details which will display a list of faculties which will contain a link to their information.

View alumni details which will display details related to alumni filtered based on the department and their year of passing out.

View student details which will contain a list of students filtered based on year and program.

Faculty can announce as per their needs. For Eg. If a faculty needs to make an announcement related to their courses this semester they can select the particular course or if they want to make an announcement for all students of the department they can do so.

![](Aspose.Words.bf731013-240b-4b13-86f3-70c1c4285409.003.jpeg)

Figma Link:

[https://www.figma.com/proto/ghc7ej07obPHwZzay48dg0/Department-Fig ma-Web?type=design&node-id=21-11&t=VmM2yna1Lq3YCD8v-0&scalin g=scale-down&page-id=0%3A1&starting-point-node-id=21%3A11&show- proto-sidebar=1](https://www.figma.com/proto/ghc7ej07obPHwZzay48dg0/Department-Figma-Web?type=design&node-id=21-11&t=VmM2yna1Lq3YCD8v-0&scaling=scale-down&page-id=0%3A1&starting-point-node-id=21%3A11&show-proto-sidebar=1)

**Figma Profile Design Guidelines and Additional Considerations**

1. **Cross-Platform Compatibility:**
- Design is compatible with the web version.
2. **Dimension Standardization:**
- Standardization has been followed.
3. **Actor-oriented Use Case-Based Design:**
- Design is based on use cases of actors and consistency has been maintained with the theme of the previous designs.
- Each actor has a different page in figma.


## Database Schema

**Database Documentation of [ AC6 - DEPARTMENT ] 4.0**

**Overview of the Module:**

The purpose of the module is to showcase all available departments, faculty and resources available in this institute, along with the ability to view various announcements made by the faculty and staff members.

The department view will display information regarding the department and facilities offered in the concerned department student details, faculty details, alumni details, and published announcements if any. The actors in this module are Student, Faculty and Staff.

**SRS:**

1. **ER Diagram (to be created using draw.io): [ER_Department**](https://drive.google.com/file/d/1R9Eqdu1zwO9aVOcANrerL7bOq9gjoMYL/view)**
1. **Database Schema Info (in the Google sheet): [Department Database Info**](https://docs.google.com/spreadsheets/d/1F1ZwnPJga40VgInpQ13APgLfGQqmtW65-JlhT4SDmEE/edit#gid=0)**
1. **Mention all the changes required in the currently implemented Tables:-**

**(These changes will be done in this current version 4.0)**

1\.)department\_announcements

- Table name
  - Change: change to
  - Justification: bad naming convention
- Id
  - Change: name change to id
  - Justification: does not follow naming convention
- ann\_date
  - Change: name change to announcement\_date
  - Justification: readability improvement
- maker\_id\_id
1) Change: name change to announcement\_maker\_id
1) Justification: readability improvement

2\.)department\_specialrequest

- Complete table
1) Change: Remove the table
1) Justification: Functionality not required.
4. **Data Availability for API and Functional Testing D.1 Mention the tables that are already populated**
- department\_announcements

**D.2 Mention the tables required to be populated**

- None

**D.3 Mention any difficulties faced by your team regarding populating any table (if any)**

- view\_faculty\_details API which utilizes EIS module throws an error for IDs which are not integer as some IDs are string.

