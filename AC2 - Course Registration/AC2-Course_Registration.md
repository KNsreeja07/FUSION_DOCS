## AC-2 COURSE REGISTRATION

## Table of Contents
- [User-Centered Design (UCD)](#user-centered-design-ucd)
- [SRS Application](#srs-application)
- [SRS Web Interface](#srs-web-interface)
- [API Specifications](#api-specifications)
- [UI for Application](#ui-for-application)
- [UI for Web](#ui-for-web)
- [Database Schema](#database-schema)

## User-Centered Design (UCD)
![](./Assests/Course%20reg%20v2.jpg)

## SRS Application

### Faculty Mentor: 
Dr. Vinod Kumar Jain

### Prepared by:
Aryan Sharma - 21BCS038  
Bhavik Agarwal - 21BCS056  
Deepanshu Singh - 21BCS073  
Samyak Bhargava - 21BEC097  
Vinayak Mittal - 21BEC124  

### Mentor :
Raman Chaudhary - 21BCS170

---

## 1. Introduction

#### Introduction about the Fusion – A brief Description
FusionIIIT stands as a remarkable example of seamlessly integrating and automating diverse functions within PDPM Indian Institute of Information Technology, Design, and Manufacturing, Jabalpur. Developed meticulously using Python3 and driven by the Django Web framework, this student-led initiative aims to enhance the operational landscape of the institute. Covering a spectrum from efficient administration management to academic excellence and various departmental tasks, FusionIIIT stands out as a comprehensive solution that deals with all the complexities of campus life, from optimizing administrative processes to ensuring smoother academic journeys. FusionIIIT actively engages with various departments and sections, ensuring a seamless flow in every nook of campus life.

On the administrative side, FusionIIIT adeptly manages intricate paperwork and processes. In the academic sphere, it introduces a digital touch, simplifying learning and course management. Yet, FusionIIIT transcends its roles; it's more like a congenial companion, consistently contributing to the efficiency of life at PDPM IIITDM Jabalpur.

To put it simply, FusionIIIT goes beyond being just a tool, it embodies a supportive companion, significantly contributing to a more organized and enjoyable campus life experience for everyone at PDPM IIITDM Jabalpur.

#### 1.2 Purpose of the module
The purpose of the Course Registration module is to streamline and enhance the overall user experience of the students, allowing them to register courses seamlessly. The module seeks to automate all the course registration activities for the Academic Section, students, and faculties.

#### 1.3 Scope of the module 
The scope of this module includes the complete course registration flow for students, allowing them to add, drop, replace, and view courses. The module also allows the Acad admin to manage courses, collect fee payments, and generate a course list. The Course Registration module is designed for scalability, optimization, and seamless integration with other modules of the application.

---

## 2. User/Actor Characteristics

### 2.1 Student 
Represents individuals who intend to use this module for course registration, pre-registration, add/drop/replace courses, view registration, backlog form, etc. Students are divided on the basis of programme, discipline, year of joining, etc.

**Role:** Initiates the course registration process, including replace/drop courses.  
**Specific Functionalities:**
- Submits personal information for pre-registration required for college administration.
- Ability to view the offered course list for each semester along with course details, including credits, number of lectures, labs, etc.
- Generate course list for each semester based on the curriculum.
- Select the courses/electives for the current semester, assigning priority to each course available in the course list.
- Can see the details of the registration and the information entered by them.
- Can apply to register for backlog courses.

### 2.2 Academic Administration
Supervises the overall operations of the pre-registration and course registration for each semester.

**Role:** Manages the overall operations of the course registration process, scheduling registration timings, generating course lists, updating academic curriculum, etc.  
**Specific Functionalities:**
- Can add or remove courses from the list of available courses for the next semester.
- Update the faculty details who will be taking the course.
- Schedule pre-registration and course registration for each semester.
- Generate roll list after the successful course registration process.
- Configure pre-registration and main registration processes.

### 2.3 Faculty
Can view the courses assigned and check the students enrolled in his/her course.

**Specific Functionalities:**
- Generate the roll list of the students enrolled in his/her course.
- View the courses assigned to him/her.

---

## 3. Functional Requirements

### 3.1 Use Case Diagram

![Use Case Diagram](../AC2%20-%20Course%20Registration//Assests/Course%20reg%20v2.jpg)

---

### 3.2 Use case Description  

### UC#1 - Add/Drop Course

| **UC ID**    | UC#1                       |
|--------------|----------------------------|
| **Use case Name**   | Add/Drop Course            |
| **Description**     | The "Add/Drop " focuses on the addition/removal of courses in/from the course list of a UG/PG for the upcoming/ongoing semester. Students select the option of adding/dropping courses from a list of options and can add/drop the courses in/from his/her course list. |
| **Actor**           | Student                    |
| **Precondition**    | The student must be logged in into the system. |
| **Main Flow**       | 1. User selects the option of add/drop courses from a list of options.<br>2. User is displayed with the list of courses he/she is enrolled in and the list of courses the user can add.<br>3. User selects the course from the list he/she wants to add or remove.<br>4. The user clicks on the submit button to submit the form. |
| **Post Conditions** | The course list of the user is updated and the user is removed/added from the attendance sheet of the added/removed course. |
| **Alternate Flow**  | A1. Users can not have less than 12 credits in a semester.<br>A2. No vacant seats available for the selected course.<br>A3. User can not have more than 26 credits in a semester. |
| **Sub Flow**        | NIL                        |

---

### UC#2 - View Offered Courses

| **UC ID**    | UC#2                       |
|--------------|----------------------------|
| **Use case Name**   | View Offered Courses        |
| **Description**     | The “View Offered Courses” use case allows the student whether UG or PG to view the offered courses from the course list offered in the respective semester. |
| **Actor**           | Student                    |
| **Precondition**    | The student is logged in into the system. |
| **Main Flow**       | 1. The Student navigates to the "View Courses" section.<br>2. The system displays the list of courses available for the respective semester.<br>3. The Student views the available courses in the list. |
| **Post Conditions** | The student navigates to pre-registration to select the viewed courses. |
| **Alternate Flow**  | NIL                        |
| **Sub Flow**        | NIL                        |
| **Global Alternate Flow** | If a technical error occurs during the execution of any action (e.g., database failure, server issues), the system displays an error message and logs the incident. |

---

### UC#3 - Replace A Course

| **UC ID**    | UC#3                       |
|--------------|----------------------------|
| **Use case Name**   | Replace A Course           |
| **Description**     | The “Replace a course” use case allows the student to view the offered courses and replace the course in the respective semester with extra credits. |
| **Actor**           | Student                    |
| **Precondition**    | P1. The student is logged in into the system.<br>P2. The acad admin has started the registration process. |
| **Main Flow**       | 1. The Student navigates to the "Replace Courses" section.<br>2. The system displays the list of courses.<br>3. The Student selects the courses from the list.<br>4. The student submits the list and exits. |
| **Post Conditions** | The updated booking information is reflected in the database. |
| **Alternate Flow**  | A1. The course selected by the user does not have vacant seats. |
| **Sub Flow**        | NIL                        |
| **Global Alternate Flow** | GA1. The acad admin can ‘cancel’ the replace course procedure at any time by exercising such an option and will be directed to the dashboard.<br>GA2. If a technical error occurs during the execution of any action (e.g., database failure, server issues), the system displays an error message and logs the incident. |

---

### UC#4 - Pre-Registration

| **UC ID**    | UC#4                       |
|--------------|----------------------------|
| **Use case Name**   | Pre-Registration           |
| **Description**     | The "Pre-Registration” use case allows students to select courses to enroll from the course list and submit the form to register for the next semester. |
| **Actor**           | Student                    |
| **Precondition**    | The student is logged in into the system and the acad admin has started the pre-registration process. |
| **Main Flow**       | 1. The Student navigates to the "Pre-registration" section.<br>2. The system displays the form to select courses.<br>3. The Student selects the courses as per his/her interest and submits the form. |
| **Post Conditions** | The acquired courses are reflected in the database and are reflected on the screen. |
| **Alternate Flow**  | A1. The total credits required are not fulfilled and the system rejects the submission, requesting to select more courses. |
| **Sub Flow**        | NIL                        |
| **Global Alternate Flow** | GA1. The Student can ‘cancel’ the procedure at any time by exercising such an option and will be directed to the dashboard.<br>GA2. If a technical error occurs during the execution of any action (e.g., database failure, server issues), the system displays an error message and logs the incident. |

---

### UC#5 - View-Registration

| **UC ID**    | UC#5                       |
|--------------|----------------------------|
| **Use case Name**   | View-Registration           |
| **Description**     | The "View Registration" use case allows the student to review his/her selected courses through the Fusion portal. |
| **Actor**           | Student                    |
| **Precondition**    | The student is logged in into the system and registered courses. |
| **Main Flow**       | 1. The Caretaker navigates to the "Profile" section.<br>2. The system displays the options to view courses of a semester.<br>3. The Student selects a semester and clicks submit.<br>4. The Student’s registered courses will display on the page. |
| **Post Conditions** | The Student is able to view his registered courses. |
| **Alternate Flow**  | A1. The Student has not selected any courses for the selected semester.<br>A2. The Course Registration window is still not open. |
| **Sub Flow**        | NIL                        |
| **Global Alternate Flow** | GA1. Courses List is not fetched from the database due to API error. |

---

### UC#6 - Fill Backlog/Improvement Form

| **UC ID**    | UC#6                       |
|--------------|----------------------------|
| **Use case Name**   | Fill Backlog/Improvement Form |
| **Description**     | The use case allows some specific users to fill the backlog/improvement form for the courses they want to repeat. |
| **Actor**           | Student                    |
| **Precondition**    | The user must be logged in to the system. |
| **Main Flow**       | 1. User navigates to the "Backlog/Improvement" section.<br>2. The system displays the list of eligible courses that student can repeat.<br>3. Student fill in the form for the course that he/she wants to repeat.<br>4. Student click on the submit button to submit the form. |
| **Post Conditions** | Student is enrolled in the course he/she wants to repeat. |
| **Alternate Flow**  | NIL                        |
| **Sub Flow**        | NIL                        |
| **Global Alternate Flow** | GA1. If a technical error occurs during the execution of any action (e.g., database failure, server issues), the system displays an error message and logs the incident. |

---

### UC#7 - Final Registration

| **UC ID**    | UC#7                       |
|--------------|----------------------------|
| **Use case Name**   | Final Registration         |
| **Description**     | The "Final Registration" use case allows the students to make final registrations and make payment. |
| **Actor**           | Student                    |
| **Precondition**    | The student is logged in into the system and the acad admin has configured main registration. |
| **Main Flow**       | 1. The student navigates to the registration section and then navigates to the payment section.<br>2. The system displays payment amount and available payment methods for further process.<br>3. The Student selects a payment method to make payment.<br>4. The student makes the transaction from the selected payment gateway/method. |
| **Post Conditions** | The updated registration and payment information is reflected in the database. |
| **Alternate Flow**  | A1. The payment is successful.<br>2. The system displays the success status and the fees receipt of the payment giving option to print it or save it.<br>A2. The payment is unsuccessful and the system redirects the student to the dashboard displaying registration pending and payment not successful. |
| **Sub Flow**        | NIL                        |
| **Global Alternate Flow** | GA1. The Student can ‘cancel’ the procedure at any time by exercising such an option and will be directed to the dashboard.<br>GA2. If a technical error occurs during the execution of any action (e.g., database failure, server issues), the system displays an error message and logs the incident. |

---

### UC#8 - Generate Roll List

| **UC ID**    | UC#8                       |
|--------------|----------------------------|
| **Use Case Name**   | Generate Roll List         |
| **Description**     | This use case “Generate Roll List” details the procedure for the academic admin to generate the list of students eligible for the course registration process. |
| **Actor**           | Acad Admin                    |
| **Precondition**    | The user must be logged into the system. |
| **Main Flow**       | 1. User checks the payment status of students and removes the names of the users from the roll list who left the Institute.<br>2. User then generates the course list for the particular semester. |
| **Post Conditions** | The generated course list is made available to the students where they can view the generated course list. |
| **Alternate Flow**  | NIL                        |
| **Sub Flow**        | NIL                        |
| **Global Alternate Flow** | GA1. If a technical error occurs during the execution of any action (e.g., database failure, server issues), the system displays an error message and logs the incident. |

---

### UC#9 - Configure Pre-registration

| **UC ID**    | UC#9                       |
|--------------|----------------------------|
| **Use Case Name**   | Configure Pre-registration         |
| **Description**     | The "Configure pre-registration" use case highlights the process by which the Acad admin can configure the pre-registration process, i.e., set the registration window, configure settings, etc. |
| **Actor**           | Acad Admin                    |
| **Precondition**    | The Acad Admin must be logged into the system. |
| **Main Flow**       | 1. The User navigates to the "Pre Registration" section.<br>2. Admin chooses the time he/she wants to open the registration window.<br>3. Admin divides the pre-registration window into slots for every specific batch.<br>4. Admin finalizes the pre-registration schedule and provides the details to students. |
| **Post Conditions** | The details of pre-registration windows can now be viewed by students. |
| **Alternate Flow**  | A1. The selected time slot for the pre-registration window collides with any other allotted schedule. |
| **Sub Flow**        | NIL                        |
| **Global Alternate Flow** | GA1. If a technical error occurs during the execution of any action (e.g., database failure, server issues), the system displays an error message and logs the incident. |

---

### UC#10 - Generate Course List

| **UC ID**    | UC#10                      |
|--------------|----------------------------|
| **Use Case Name**   | Generate Course List         |
| **Description**     | The Generate Course List use case allows the user to generate the course list for each course for each batch after the course registration process. |
| **Actor**           | Acad Admin                    |
| **Precondition**    | The acad admin should be logged into the system.<br>The new academic year has started. |
| **Main Flow**       | 1. The admin selects the option to generate the course list.<br>2. The admin selects the batch and course.<br>3. The academic admin generates the list of enrolled students in the courses. |
| **Post Conditions** | The list of enrolled students should be generated in the Excel format. |
| **Alternate Flow**  | NIL                        |
| **Sub Flow**        | NIL                        |
| **Global Alternate Flow** | GA1. If a technical error occurs during the execution of any action (e.g., database failure, server issues), the system displays an error message and logs the incident. |

---

### UC#11 - Add Courses

| **UC ID**    | UC#11                      |
|--------------|----------------------------|
| **Use Case Name**   | Add Courses         |
| **Description**     | The "Add Courses” use case allows acad admin to add courses to the offered course list for the upcoming semester. |
| **Actor**           | Acad Admin                    |
| **Precondition**    | The Acad admin is logged into the system (as admin). |
| **Main Flow**       | 1. The Acad Admin navigates to the add courses section.<br>2. The system displays the list of courses available to add in the course list.<br>3. The Acad Admin selects course(s) to add to the list. |
| **Post Conditions** | The updated course list is reflected in the database and displayed on the student’s screen. |
| **Alternate Flow**  | A1. 1. The acad admin proceeds with the selected courses(s) and finally adds them to the list by submitting the form.<br>2. The system updates the offered course list for the upcoming semester.<br>A2. 1. The Acad admin decides to not proceed with the selected course to add and deselects it. |
| **Sub Flow**        | NIL                        |
| **Global Alternate Flow** | GA1. The Acad Admin can ‘cancel’ the procedure at any time by exercising such an option and will be directed to the add courses section.<br>GA2. If a technical error occurs during the execution of any action (e.g., database failure, server issues), the system displays an error message and logs the incident. |

---

### UC#12 - Remove Courses

| **UC ID**    | UC#12                      |
|--------------|----------------------------|
| **Use Case Name**   | Remove Courses         |
| **Description**     | The "Remove Courses" use case allows the acad admin to remove any course from the courses list. |
| **Actor**           | Acad Admin                    |
| **Precondition**    | The acad admin is logged into the system. |
| **Main Flow**       | 1. The Acad admin navigates to the "Remove Courses" section.<br>2. The system displays the list of all available courses.<br>3. The Acad admin selects the course to be deleted.<br>4. The system shows confirmation to delete the course.<br>5. The acad admin confirms that they want to delete the selected course. |
| **Post Conditions** | The selected course has been deleted from the list of available courses. |
| **Alternate Flow**  | A1. 1. The acad admin presses the back button.<br>A2. 1. The acad admin doesn’t confirm to delete the course. |
| **Sub Flow**        | NIL                        |
| **Global Alternate Flow** | GA1. The Acad Admin can ‘cancel’ the procedure at any time by exercising such an option and will be directed to the dashboard.<br>GA2. If a technical error occurs during the execution of any action (e.g., database failure, server issues), the system displays an error message and logs the incident. |

---

### UC#13 - Generate Roll List

| **UC ID**    | UC#13                      |
|--------------|----------------------------|
| **Use Case Name**   | Generate Roll List         |
| **Description**     | This use case “Generate Roll List” details the procedure for Faculty to generate the list of students eligible for the course registration process. |
| **Actor**           | Faculty                    |
| **Precondition**    | The user must be logged into the system. |
| **Main Flow**       | 1. User checks the students enrolled in his/her course. |
| **Post Conditions** | The generated course list is made available to the students where they can view the generated course list. |
| **Alternate Flow**  | NIL                        |
| **Sub Flow**        | NIL                        |
| **Global Alternate Flow** | GA1. If a technical error occurs during the execution of any action (e.g., database failure, server issues), the system displays an error message and logs the incident. |

---

### UC#14 - View Assigned Courses

| **UC ID**    | UC#14                      |
|--------------|----------------------------|
| **Use Case Name**   | View Assigned Courses         |
| **Description**     | This use case allows the faculty to view the courses assigned to them. |
| **Actor**           | Faculty                    |
| **Precondition**    | The user must be logged into the system. |
| **Main Flow**       | 1. User checks the course assigned to him/her. |
| **Post Conditions** | NIL                        |
| **Alternate Flow**  | NIL                        |
| **Sub Flow**        | NIL                        |
| **Global Alternate Flow** | GA1. If a technical error occurs during the execution of any action (e.g., database failure, server issues), the system displays an error message and logs the incident. |

---

## 3.4 Other Constraints

### 3.4.1 User Interfaces
The user interface should comply with the colour scheming and dashboard design of the FUSION IIIT. Users should be able to navigate from one functionality to another. Inter module navigation should be smooth. All the functionalities should be easy to use and no specific training should be required for the usage of the module.

### 3.4.2 Technology Stack Used
Django will be used for backend development using Python, and Flutter for the frontend, using Dart.

### 3.4.3 Data Migration
Existing data from the college database including the data of the students, courses etc needs to be migrated to Fusion database.

### 3.4.4 Business Rules
1. Only registered students who have paid their fees should be eligible to register for the courses.
2. Each course has a capacity limit and thus students should not be allowed to register for a course once its capacity is free.
3. Course registration is allowed only during a pre-specified registration period and students should be allowed to register only during that window.
4. If there are any compulsory prerequisites for a course, then only those students who have completed those prerequisites should be allowed to register in that course.

## 4. Non-Functional Requirements

### 4.1 Performance Requirements
The system should respond to user requests very fast and be able to handle 500 concurrent users during the registration. The system should also be scalable in order to handle an increase in the number of students and courses over time.

### 4.2 Reliability and Availability
The system should be available during the critical registration periods. The system should be reliable and not fail during the registration process thus affecting the procedure.

### 4.3 Security Requirements
Before using the app, the users must authenticate using a secure login mechanism. Role based access control should be implemented to ensure users can perform only those actions which they are authorized to.

### 4.4 Compatibility
The system should be compatible with most of the popular operating systems (eg. Android, IOS).

### 4.5 Maintainability
The source code should follow coding standards, be well documented in order to facilitate future enhancements and maintenance.

## 5. Module Dependencies with Other Fusion Modules

### 5.1 UI Level
The Course Registration module in Fusion relies on the integration with other modules at the UI level.

**UI Integration with:**
- **Program and Curriculum (AC1):** Students and academic advisors will use this integration to ensure that registered courses align with the chosen program and curriculum.
- **Course Management (AC3):** Students will use this integration to make informed decisions during course selection.
- **Dashboards (GAD5):** Dashboard will be used for visual representation of the registered student data.

### 5.2 DB Level Dependencies
Course Registration module in Fusion at the DB Level Dependencies with other modules:
- **Program and Curriculum (AC1):** The Course Registration module likely maintains a foreign key relationship with the Program and Curriculum database tables. This ensures that the selected courses align with the programs and curricula offered by the institution.
- **Course Management (AC3):** Regular synchronization processes between the Course Registration and Course Management databases to update and fetch course details, availability, and prerequisites.
- **Dashboards (GAD5):** The Dashboard module's database-level interactions involve managing and processing data from various sources to provide meaningful visual representations.
- **Department Module (AC6):** The Department module will interact with Course Registration for managing the roll list of all the students enrolled in the particular department.

### 5.3 Module Level Dependencies
- **Program and Curriculum (AC1):** The Course Registration module depends on the Program and Curriculum module to retrieve accurate information about available programs, associated courses, and curriculum details.
- **Course Management (AC3):** The Course Registration module relies on the Course Management module to integrate course data, ensuring that students have up-to-date information about course availability, prerequisites, and descriptions.
- **Other Academic Procedures (AC4):** The Course Registration module needs to align with academic procedures defined in the Other Academic Procedures module.

## SRS Web Interface

- Divyanshu Srivastava 21BCS080  
- Divyanshu Sharma 21BCS079  
- Devesh Kumar 21BCS075  
- Deepranjan Kumar 21BCS74  
- Aman Sharma 21BCS19
  
#### Faculty Mentor: 
Dr. Vinod Kumar Jain

#### Mentor :
Pranav Bharadwaj 21BCS160  

---

### 1 Introduction

#### 1.1 Introduction about the Fusion – A brief Description
FusionIIIT stands as a transformative initiative within PDPM Indian Institute of Information Technology, Design and Manufacturing, Jabalpur. Developed with precision using Python 3.8 and leveraging the Django Web framework, this student-driven endeavor is reshaping the operational landscape of our institute. Going beyond mere functionality, FusionIIIT assumes the role of a strategic partner, seamlessly integrating and automating diverse functions to enhance the efficiency and coherence of campus life. In essence, FusionIIIT serves as a sophisticated digital solution, addressing administrative complexities, optimizing academic processes, and extending its influence across various departments. On the administrative front, it adeptly manages intricate paperwork and procedural challenges. Within the academic sphere, it introduces a digital framework, thereby facilitating a more streamlined approach to learning and course management. Its impact transcends these realms, ensuring a holistic and well-coordinated environment throughout the campus. To encapsulate, FusionIIIT transcends its utility as a mere tool; it embodies a sophisticated ally committed to augmenting the organizational structure and overall experience at PDPM IIITDM Jabalpur. In the realm of campus life, FusionIIIT stands as a testament to efficiency, cohesion, and innovation.

#### 1.2 Purpose of the module:
Academic Course Registration (AC-2) is a software designed to manage different activities related to the Course Registrations of PDPM IIITDM Jabalpur. The module seeks to optimize resource utilization, to provide automated features and a smooth interface to the Academic staff, students and faculties to handle different Course registration and corresponding related activities.

#### 1.3 Scope of the module
This software will take care of the following activities: Admission, Courses Registration, add-drop, replace, apply for backlog, fee deposit, manage schedule, course-list generation, roll list generation and more.

---

### 2. User/Actor characteristics

#### 2.1 Student:
Students are the registered students of PDPM IIITDM Jabalpur who wish to register themselves with the offered courses for the upcoming semester.  
**Role:** Initiates the registration related process  
**Specific Functionalities:**
- They can view offered courses
- They can add, drop and replace the course
- They can do pre-registration
- They can do final registration and can do the payment
- They can view the registration
- They can fill backlog form

#### 2.2 Acad Admin
Acad Admin of the Institute is responsible for managing and displaying the course.  
**Role:** Manage the registration process.  
**Specific Functionalities:**
- Manage schedule and view registration process.
- Generate list of course and roll list.
- Configure Pre-Registration and Main-Registration.

#### 2.3 Faculty
Faculty are the teaching staff of the institute which are responsible for teaching the courses.  
**Role:** Viewing the courses under him/her and generating roll list  
**Specific Functionalities:**
- View the courses that he will be teaching in the upcoming/current semester
- Generate the roll list of any course being taught by him/her

### 3. Functional Requirements

#### 3.1 Use Case Diagram

![Use Case Diagram](../AC2%20-%20Course%20Registration/Assests/Course%20reg%20v2.jpg)

---

#### 3.2 Use Case Description
##### 3.2.1 For Student:

### UC#1 - Add a Course

| **UC ID**           | UC#1                       |
|---------------------|----------------------------|
| **Use Case Name**   | Add a Course               |
| **Description**     | The use case describes how to add courses to the course list of a UG student. |
| **Actor**           | UG Student                 |
| **Precondition**    | UG Students must be logged in the system. |
| **Main Flow**       | 1. UG Student selects the option of adding courses from a list of options.<br>2. UG Student is displayed a list of courses he/she can add in his course list.<br>3. UG Student chooses a course from a list of courses which he/she wants to add.<br>4. UG student submits the form. |
| **Post Conditions** | 1. Successful completion.<br>2. Course is added to the course list of UG students.<br>3. UG Student is added to the attendance sheet of added courses. |
| **Alternate Flow**  | 1. Constraints not met.<br>2. UG Student is prompted a message about constraints not met due to either of the following conditions:<br>&nbsp;&nbsp;3. UG Students with CPI less than 8.0 are not eligible.<br>&nbsp;&nbsp;4. UG Students cannot add more than two courses in a semester.<br>&nbsp;&nbsp;5. UG Students cannot have more than 26 credits in a semester.<br>6. UG Student is redirected to the form. |
| **Sub Flow**        | NIL                        |
| **Global Alternate Flow** | If a technical error occurs during the execution of any action (e.g., database failure, server issues), the system displays an error message and logs the incident. |

---

### UC#2 - Drop a Course

| **UC ID**           | UC#2                       |
|---------------------|----------------------------|
| **Use Case Name**   | Drop a Course              |
| **Description**     | The use case describes how to drop courses from the course list of a UG student. |
| **Actor**           | UG Student                 |
| **Precondition**    | UG Students must be logged in the system. |
| **Main Flow**       | 1. UG Student selects the option of dropping course from a list of options.<br>2. UG Student is displayed on his/her course list.<br>3. UG Student chooses the course from the list which he/she wants to drop.<br>4. UG student submits the form. |
| **Post Conditions** | 1. Successful completion.<br>2. Course/s is/are removed from the course list of UG students.<br>3. UG Student is removed from the attendance sheet of removed courses. |
| **Alternate Flow**  | 1. Constraints not met.<br>2. UG Students cannot drop more than two courses in a semester.<br>3. UG Students cannot have less than 12 credits in a semester. |
| **Sub Flow**        | NIL                        |
| **Global Alternate Flow** | If a technical error occurs during the execution of any action (e.g., database failure, server issues), the system displays an error message and logs the incident. |

---

### UC#3 - Replace with Swayam Course

| **UC ID**           | UC#3                       |
|---------------------|----------------------------|
| **Use Case Name**   | Replace with Swayam Course |
| **Description**     | The use case describes how to replace a course from the course list with a Swayam course of same credit. |
| **Actor**           | Student                    |
| **Precondition**    | Students must be logged in the system. |
| **Main Flow**       | 1. Student selects the option of replacing course from a list of options.<br>2. Student is displayed on his/her course list.<br>3. Student chooses the course from the list which he/she wants to replace.<br>4. List of Swayam courses that students have completed will be shown.<br>5. Among completed Swayam courses student shall choose the corresponding Swayam course which he will replace with.<br>6. Student submits the choices. |
| **Post Conditions** | 1. Successful completion.<br>2. Old Course/s is/are removed from the course list of UG students.<br>3. UG Student is removed from the attendance sheet of removed courses. |
| **Alternate Flow**  | 1. Constraints not met.<br>2. Students cannot replace the course or student haven’t completed enough Swayam course to replace. |
| **Sub Flow**        | NIL                        |
| **Global Alternate Flow** | If a technical error occurs during the execution of any action (e.g., database failure, server issues), the system displays an error message and logs the incident. |

---

### UC#4 - Final Registration

| **UC ID**           | UC#4                       |
|---------------------|----------------------------|
| **Use Case Name**   | Final Registration          |
| **Description**     | The use case handles the student registration system. |
| **Actor**           | Student                    |
| **Precondition**    | 1. Student must be logged in the system.<br>2. Final Registration form which includes courses of the next semester is provided to the students. |
| **Main Flow**       | 1. Students confirm the courses to enroll for next semester.<br>2. Student selects the fee payment mode and enters the transaction number.<br>3. Students click the Register button to register. |
| **Post Conditions** | Registration is completed successfully. |
| **Alternate Flow**  | Students can change the opted course. |
| **Sub Flow**        | NIL                        |
| **Global Alternate Flow** | If a technical error occurs during the execution of any action (e.g., database failure, server issues), the system displays an error message and logs the incident. |

---

### UC#5 - Pre Registration

| **UC ID**           | UC#5                       |
|---------------------|----------------------------|
| **Use Case Name**   | Pre Registration            |
| **Description**     | The use case handles the student registration system. |
| **Actor**           | Student                    |
| **Precondition**    | 1. Student must be logged in the system.<br>2. Pre-Registration form which includes courses of the next semester is provided to the students. |
| **Main Flow**       | 1. Students select the courses to enroll for next semester.<br>2. Students click the Register button to register. |
| **Post Conditions** | Pre-registration done successfully. |
| **Alternate Flow**  | Return back to the same page with blank form. |
| **Sub Flow**        | NIL                        |
| **Global Alternate Flow** | If a technical error occurs during the execution of any action (e.g., database failure, server issues), the system displays an error message and logs the incident. |

---

### UC#6 - Fill Backlog Form

| **UC ID**           | UC#6                       |
|---------------------|----------------------------|
| **Use Case Name**   | Fill Backlog Form          |
| **Description**     | This use case helps the student to fill the form for covering their backlog courses. |
| **Actor**           | Student                    |
| **Precondition**    | 1. Students must be logged in the system. |
| **Main Flow**       | 1. Student will select this option.<br>2. Form will be opened on the screen, in which student have to fill all the details regarding the course and other required details.<br>3. Student finally submits the form. |
| **Post Conditions** | 1. Submission successful. |
| **Alternate Flow**  | 1. Form submission fails, and student is redirected back to same page. |
| **Sub Flow**        | NIL                        |
| **Global Alternate Flow** | If a technical error occurs during the execution of any action (e.g., database failure, server issues), the system displays an error message and logs the incident. |

---

### UC#7 - View Registration

| **UC ID**           | UC#7                       |
|---------------------|----------------------------|
| **Use Case Name**   | View Registration           |
| **Description**     | This use case describes how the Students can check their profile and courses after registration. |
| **Actor**           | Student                    |
| **Precondition**    | 1. Student must be logged in the system. |
| **Main Flow**       | 1. Student can select the option of view registration to see their profile and courses they have registered for. |
| **Post Conditions** | 1. All the related details will be displayed on the screen. |
| **Alternate Flow**  | 1. Student haven’t completed the registration yet, so nothing to display yet. |
| **Sub Flow**        | NIL                        |
| **Global Alternate Flow** | If a technical error occurs during the execution of any action (e.g., database failure, server issues), the system displays an error message and logs the incident. |

---

### UC#8 - View Offered Courses

| **UC ID**           | UC#8                       |
|---------------------|----------------------------|
| **Use Case Name**   | View Offered Courses        |
| **Description**     | The “View Offered Courses” use case allows the student whether UG or PG to view the offered courses from the course list offered in the respective semester. |
| **Actor**           | Student                    |
| **Precondition**    | The student is logged in into the system. |
| **Main Flow**       | 1. The Student navigates to the "View Courses" section.<br>2. The system displays the list of courses available for the respective semester.<br>3. The Student views the available courses in the list. |
| **Post Conditions** | The student navigates to pre-registration to select the viewed courses. |
| **Alternate Flow**  | NIL                        |
| **Sub Flow**        | NIL                        |
| **Global Alternate Flow** | If a technical error occurs during the execution of any action (e.g., database failure, server issues), the system displays an error message and logs the incident. |

---

### 3.2.2 For Acad Admin:

#### Use Case #9
| **Use Case ID**  | UC#9                                   |
|-------------------|----------------------------------------|
| **Use Case Name** | Manage_schedule                        |
| **Description**   | This use case describes how the Academic Person updates and adds the schedule of courses and time table. |
| **Actor(s)**      | Acad Admin                             |
| **Precondition**  | 1. Academic Person must be logged in the system. |
| **Main Flow**     | 1. Academic person selects this option from the list of options.<br>2. All the schedules are displayed.<br>3. Options for adding/deleting/updating the schedules are displayed.<br>4. Academic person can manage the schedule with these options. |
| **Post-condition**| Changes in schedule will be displayed to everyone. |
| **Alternate Flow**| NIL                                    |
| **Sub Flow**      | NIL                                    |

---

#### Use Case #10
| **Use Case ID**  | UC#10                                  |
|-------------------|----------------------------------------|
| **Use Case Name** | View_registration                      |
| **Description**   | This use case describes how the Academic Person checks the final registration of students for the semester. |
| **Actor(s)**      | Academic Person                        |
| **Precondition**  | 1. Academic Person must be logged in the system. |
| **Main Flow**     | 1. Academic Person selects the option of Checking Registrations of all students. |
| **Post-condition**| Student can check the updated registered courses through his link. |
| **Alternate Flow**| NIL                                    |
| **Sub Flow**      | NIL                                    |

---

#### Use Case #11
| **Use Case ID**  | UC#11                                  |
|-------------------|----------------------------------------|
| **Use Case Name** | Generate_roll_list                    |
| **Description**   | This use case allows an Academic Admin to generate a roll list for a specific course, containing student information such as names, ID numbers, and contact details. |
| **Actor(s)**      | Acad Admin                             |
| **Precondition**  | 1. The Academic Admin is logged into the Fusion system.<br>2. The Course Registration module is accessible.<br>3. The registration for the desired course has been finalized. |
| **Main Flow**     | 1. The Academic Admin initiates the use case by accessing the "Generate Roll List" option within the Course Registration module.<br>2. The system prompts the Academic Admin to select the course for which they want to generate the roll list.<br>3. The system retrieves the list of registered students for the selected course from the database.<br>4. The system generates a roll list in a specified format (e.g., PDF, Excel, printable webpage).<br>5. The system displays the generated roll list to the Academic Admin.<br>6. The Academic Admin can download, print, or save the roll list as needed. |
| **Post-condition**| The roll list is generated and available for the Academic Admin's use. |
| **Alternate Flow**| NIL                                    |
| **Sub Flow**      | NIL                                    |

---

#### Use Case #12
| **Use Case ID**  | UC#12                                  |
|-------------------|----------------------------------------|
| **Use Case Name** | Configure_pre_reg                      |
| **Description**   | This use case allows an Academic Admin to configure the settings for the pre-registration period, including dates, eligibility criteria, and student permissions. |
| **Actor(s)**      | Acad Admin                             |
| **Precondition**  | 1. The Academic Admin is logged into the Fusion system.<br>2. The Course Registration module is accessible. |
| **Main Flow**     | 1. The Academic Admin initiates the "Configure Pre-Registration" section.<br>2. The system displays the current pre-registration settings.<br>3. The Academic Admin modifies the following settings as needed like start and end dates, eligible students groups, etc.<br>4. The Academic Admin confirms the changes.<br>5. The system validates the inputs and saves the updated settings.<br>6. The system displays a confirmation message indicating that the pre-registration settings have been successfully configured. |
| **Post-condition**| The pre-registration settings are updated and ready for the upcoming pre-registration period. |
| **Alternate Flow**| 1. If the Academic Admin enters invalid data (e.g., end date before start date), the system displays an error message and prompts for correction. |
| **Sub Flow**      | NIL                                    |

---

#### Use Case #13
| **Use Case ID**  | UC#13                                  |
|-------------------|----------------------------------------|
| **Use Case Name** | Configure_main_reg                     |
| **Description**   | This use case allows an Academic Admin to configure the settings for the main-registration period, including dates, eligibility criteria, and student permissions. |
| **Actor(s)**      | Acad Admin                             |
| **Precondition**  | 1. The Academic Admin is logged into the Fusion system.<br>2. The Course Registration module is accessible. |
| **Main Flow**     | 1. The Academic Admin initiates the "Configure Main-Registration" section.<br>2. The system displays the current main-registration settings.<br>3. The Academic Admin modifies the following settings as needed like start and end dates, eligible students groups, etc.<br>4. The Academic Admin confirms the changes.<br>5. The system validates the inputs and saves the updated settings.<br>6. The system displays a confirmation message indicating that the main-registration settings have been successfully configured. |
| **Post-condition**| The main-registration settings are updated and ready for the upcoming main-registration period. |
| **Alternate Flow**| 1. If the Academic Admin enters invalid data (e.g., end date before start date), the system displays an error message and prompts for correction. |
| **Sub Flow**      | NIL                                    |

---

#### Use Case #14
| **Use Case ID**  | UC#14                                  |
|-------------------|----------------------------------------|
| **Use Case Name** | Generate course list                   |
| **Description**   | This use case allows an Academic Admin to generate a list of courses offered in a specific semester or academic year, including relevant course details. |
| **Actor(s)**      | Academic Person                        |
| **Precondition**  | 1. The Academic Admin is logged into the Fusion system.<br>2. Course information for the desired semester or year is available in the system.<br>3. The Course Registration module is accessible. |
| **Main Flow**     | 1. The Academic Admin initiates the use case by accessing the "Generate Course List" option within the Course Registration module.<br>2. The system prompts the Academic Admin to specify the semester or academic year for which they want to generate the list and the desired format for the list.<br>3. The system retrieves course information from the database based on the specified parameters.<br>4. Fetched list of courses is displayed to the user. |
| **Post-condition**| List generated successfully.          |
| **Alternate Flow**| NIL                                    |
| **Sub Flow**      | NIL                                    |

---

### 3.2.3 For Faculty:

#### Use Case #15
| **Use Case ID**  | UC#15                                  |
|-------------------|----------------------------------------|
| **Use Case Name** | View Assigned courses                  |
| **Description**   | This use case allows a Faculty to view a list of courses that they are going to teach in the upcoming semester. |
| **Actor(s)**      | Faculty                                 |
| **Precondition**  | 1. The Faculty is logged into the Fusion system.<br>2. Courses information for the desired semester or year is available in the system. |
| **Main Flow**     | 1. The Faculty initiates the use case by accessing the "Get courses under him" option within the Course Registration module.<br>2. The system retrieves course information from the database based on the specified parameters.<br>3. Fetched list of courses is displayed to the user. |
| **Post-condition**| List generated successfully.          |
| **Alternate Flow**| 1. Faculty is not teaching any courses.<br>2. List of courses is not yet updated in the database. |
| **Sub Flow**      | NIL                                    |

---

#### Use Case #16
| **Use Case ID**  | UC#16                                  |
|-------------------|----------------------------------------|
| **Use Case Name** | Generate Roll list                     |
| **Description**   | This use case allows a Faculty to generate a roll list for a specific course, containing student information such as names, ID numbers, and contact details. |
| **Actor(s)**      | Faculty                                 |
| **Precondition**  | 1. The Faculty is logged into the Fusion system.<br>2. Course information for the desired semester or year is available in the system.<br>3. The Course Registration module is accessible. |
| **Main Flow**     | 1. The Faculty initiates the use case by accessing the "Generate Roll List" option within the Course module.<br>2. The system prompts the Faculty to select the course for which they want to generate the roll list.<br>3. The system retrieves the list of registered students for the selected course from the database.<br>4. The system generates a roll list in a specified format (e.g., Excel). |
| **Post-condition**| Roll List generated successfully.     |
| **Alternate Flow**| NIL                                    |
| **Sub Flow**      | NIL                                    |



### 3.3 Other Functional Requirements
1. This module will use notification and alert to notify the students about the added courses, scheduled time for pre and final registration etc.
2. This software should be compatible with different browsers like Google Chrome, Firefox, Edge and Safari. Users should be able to use and navigate on any browser available.
3. The system should raise errors and invalid flags when users go opposite to the exceptions.

### 3.4 Other Constraints
#### 3.4.1 User Interfaces
The color palette should match the design and pattern of the FusionIIIT dashboard. All the buttons should be clickable and there should be smooth navigation from one functionality to another. Inter module navigation should be reachable from within the module. The UI should be easy to use and intuitive.

#### 3.4.2 Tech stack
Web application uses Django framework for frontend and backend functionality. PostgreSQL is used as the RDBMS. Mobile application uses Flutter SDK for its frontend and Django API for its backend. MySQL is used for the database.  
Sub Flow NIL

#### 3.4.3 Business rules
1. There should be eligibility criteria for admission of prospective students after the system has processed their application.
2. The system should display a list of available courses for registration.
3. Students should meet the course prerequisites before allowing registration.
4. Add/drop time period should be specified to students.
5. Automated processing of backlog applications with notification outcomes.
6. Dynamic course and roll list generation.

---

### 4. Non-Functional Requirements
#### 4.1. Performance:
- **Response Time:** The system should respond to user actions within reasonable time frames, even during peak registration periods.
- **Scalability:** The system should be able to handle a growing number of students and courses without significant performance degradation.
- **Load Testing:** Conduct thorough load testing to identify and address potential bottlenecks.

#### 4.2. Availability:
- **Uptime:** The system should be highly available during registration periods, with minimal downtime for maintenance or outages.

#### 4.3. Security:
- **Authentication and Authorization:** Enforce strong authentication mechanisms for users and implement role-based access controls to sensitive data and functionalities.
- **Data Protection:** Protect sensitive student and course information from unauthorized access, modification, or disclosure.

#### 4.4. Maintainability:
- **Modular Design:** Structure the code in a modular and well-organized manner to facilitate updates and bug fixes.
- **Documentation:** Maintain comprehensive and up-to-date documentation for developers and administrators.
- **Version Control:** Use version control systems to track code changes and manage updates effectively.

#### 4.5. Scalability:
- **Capacity:** The system should be able to accommodate expected growth in student enrollment and course offerings without significant performance degradation.
- **Architecture:** Design the system with scalability in mind, using technologies and architectures that can handle increased load.

---

### 5. Module Dependencies with other Fusion Modules
#### 5.1 UI Level:
1. **Integration within Fusion's UI:**
   - **Placement within Navigation Menu:** The module should be integrated into Fusion's main navigation menu, likely under a section dedicated to academic activities.
   - **Distinct Sections for Actors:** Within the module, there should be clear sections or tabs for students and academic admins, ensuring a tailored experience for each actor.
   - **Consistent Styling and Navigation:** The module's UI elements should align with Fusion's overall visual design and navigation patterns to maintain a cohesive user experience.

2. **Actor-Specific Functionalities:**
   - **Students:**
     - **View Offered Courses:**
       - Access via a dedicated "Course Catalog" or "Course Search" tab within the module.
     - **Add Courses:**
       - Provide a mechanism to add selected courses to a "Cart" or "Registration List."
       - Display clear feedback on course availability and potential conflicts.
     - **Drop Courses:**
       - Provide a mechanism to drop selected courses.
       - Display clear message whether the course was successfully dropped and if yes which is the new course allotted if applicable.
     - **Replace Courses:**
       - Provide a mechanism to replace selected courses with courses of Swayam.
       - Proper list of Swayam courses offered by the department of the particular student should be displayed.
     - **Finalize Registration:**
       - Present a summary of selected courses for confirmation.
       - Handle payment processing (if applicable).
       - Generate and display a registration confirmation.
     - **View Registration Status:**
       - Display a comprehensive list of registered courses with details (e.g., meeting times, instructors, credits).
       - Allow for printing or exporting registration information.
     - **Fill Backlog Form:**
       - Provide a dedicated form within the module for students to apply for backlog clearance.
       - Integrate with relevant approval workflows and notifications.
     - **Pre-Registration:**
       - Offer a separate section for students to indicate their course preferences for upcoming semesters.
       - Indicate any pre-requisites or course availability constraints.
     - **Final-Registration:**
       - Offer a separate section for students to finalize their course preferences for upcoming semesters.

   - **Academic Admins:**
     - **Manage Course Schedule:**
       - Provide a calendar-based interface for creating and managing course schedules.
       - Integrate with faculty assignment and classroom allocation systems (if applicable).
     - **View Registration Details:**
       - Display lists of registered students for each course, with options to filter and sort data.
       - Allow for exporting student lists for further analysis or reporting.
     - **List Courses:**
       - Provide a comprehensive view of all courses offered, with options to edit course information.
     - **Generate Roll Lists:**
       - Allow admins to generate class rosters for each course, with options for downloading or printing.
     - **Configure Pre-Registration and Main Registration Settings:**
       - Offer dedicated settings sections within the module for admins to adjust registration deadlines, rules, and permissions.

   - **Faculty:**
     - **Generate Roll Lists:**
       - Allow Faculty to generate class roll lists for each course, with options for downloading or printing.
     - **View assigned courses:**
       - Provide a comprehensive view of all courses offered by the faculty that he is going to teach in the upcoming semester.

#### 5.2 DB Level Dependencies:
1. **Students:**
   - **Owner:** Course Management Module
   - **User:** Course Registration Module (for admin data)
   - **Potential Fields:** student_id, username, password, role (student/admin), other personal details

2. **Courses:**
   - **Owner:** Course Management Module (if separate) or Course Registration Module
   - **User:** Course Registration Module, Academic Admin Module, Timetable Module, Fee Management Module
   - **Potential Fields:** course_id, course_name, department, credits, prerequisites, instructor_id, semester

3. **Registration:**
   - **Owner:** Course Registration Module
   - **User:** Course Registration Module, Academic Admin Module, Transcript Module, Fee Management Module
   - **Potential Fields:** registration_id, student_id, course_id, semester, grade (optional), payment_status

4. **Schedule:**
   - **Owner:** Timetable Module (if separate) or Course Registration Module
   - **User:** Course Registration Module, Academic Admin Module, Faculty Module
   - **Potential Fields:** course_id, section_id, timeslot_id, classroom_id, instructor_id

5. **Payments:** (if applicable)
   - **Owner:** Fee Management Module
   - **User:** Course Registration Module
   - **Potential Fields:** payment_id, student_id, amount, payment_date, registration_id

6. **Fee:**
   - **Owner:** Mess Module, Accounts Module
   - **User:** Course Registration Module
   - **Potential Fields:** student_id, amount, payment_date, registration_id, deadline

#### 5.3 Module Level Dependencies:
1. **Academic Information Module:**
   - **Dependency Direction:** Course Registration Module depends on Academic Information Module.
   - **Purpose:**
     - To retrieve student academic data (e.g., program, year of study, GPA, completed courses) for eligibility checks and prerequisite enforcement.
     - To update student academic records with registered courses and grades.

2. **Notifications Extension:**
   - **Dependency Direction:** Course Registration Module depends on Notifications Extension.
   - **Purpose:**
     - To trigger notifications for various events:
       - Registration confirmations and reminders
       - Backlog clearance approvals
       - Course schedule changes
       - Registration deadlines

**Additional Module-Level Dependencies (Potential):**
- Authentication/User Management Module: For user authentication and authorization.
- Fee Module: For handling course fees and payment processing.
- Exam Module: For recording student grades and generating transcripts.

## API Specifications
			
##### Student Mentor - Pranav Bharadwaj (21BCS160)

## Overview of the module:
Academic Course Registration (AC-2) is a software designed to manage different activities related to the Course Registrations of PDPM IIITDM Jabalpur. The module seeks to provide automated features and a smooth interface to the Academic staff, students and faculties to handle different Course registration and corresponding related activities such as:
- Admission
- Courses Registration
- add-drop
- replace
- apply for backlog
- manage schedule
- course-list generation
- roll list generation
- and more.

### Please mention all the API used in the module below 
1. **POST academic-procedures/auto_pre_registration/** - Implemented  
   **Description** - used by student to do the pre registration by new method (without priority system) by directly assigning the courses is available, for the next semester 
<br>

2. **POST academic-procedures/final_registration/** - Implemented  
   **Description** - used by student to do the final registration for the next semester by providing fee payment details
<br>

3. **POST academic-procedures/api/stu/view_offered_courses** - Implemented  
   **Description** - used by student to see the courses offered in the upcoming semester
<br>

4. **POST academic-procedures/addCourse/** - Implemented  
   **Description** - used by student to add the courses that are not registered till now
<br>

5. **POST academic-procedures/drop_course/** - Implemented  
   **Description** - used by student to drop the registered courses
<br>

6. **POST academic-procedures/replace_one_course/** - Implemented  
   **Description** - used by student to replace the registered optional course in a slot with another optional course in same slot
<br>

7. **POST academic-procedures/replaceCourse/** - Implemented  
   **Description** - used by student to replace the multiple optional courses from the currently registered optional to other choices in the same optional slot
<br>

8. **POST academic-procedures/register_backlog_course/** - Implemented  
   **Description** - student can apply for backlog in any course with this request
<br>

9. **POST academic-procedures/api/stu/pre_registration/** - Implemented  
   **Description** - used by student to do pre registration using priority based logic (not used now instead auto_pre_registration used)
<br>

10. **GET academic-procedures/api/fac** - Implemented  
    **Description** - returns details of the faculty that is currently logged in the system
<br>

11. **GET academic-procedures/api/stu** - Implemented  
    **Description** - returns all details of the student currently logged in the system such as profile details, curr sem details, courses registered, next sem courses, backlog course list and more. 
<br>

12. **POST academic-procedures/acad_person/student_list/** - Implemented  
    **Description** - returns the list of students who have done the final registration and completed the fee payment, but their verification is pending
<br>

13. **POST academic-procedures/auto_process_verification_request/** - Implemented  
    **Description** - with this api request acad admin can approve or decline the final registration of any student 
<br>

14. **POST academic-procedures/acad_person/allot_courses/** - Implemented  
    **Description** - acad person can give an excel sheet with specified columns, and the record from that sheet will be used to allot courses to student
<br>

15. **POST academic-procedures/acad_person/remove_course_from_slot/** - Implemented  
    **Description** - acad person can remove some course in a course slot by giving course code of the course and slot code
<br>

16. **POST academic-procedures/acad_person/add_course_to_slot/** - Implemented  
    **Description** - acad person can add some course in a course slot by giving course code of the course and slot code
<br>

17. **POST academic-procedures/acad_person/get_next_sem_courses/** - Implemented  
    **Description** - acad person can get the list of courses for any batch semester that will be show to students during their next sem pre registration
<br>

18. **POST academic-procedures/acad_person/replaceSwayam/** - Implemented  
    **Description** - acad person can get the all swayam courses and optional courses that will be needed for allotting swayam to any specific student
<br>

19. **POST academic-procedures/acad_person/swayam_replace/** - Implemented  
    **Description** - acad person can replace swayam courses with optional courses for any student
<br>

20. **POST academic-procedures/api/acad/configure_pre_registration/** - Implemented  
    **Description** - with this request acad person can schedule the pre registration date for any upcoming semester
<br>

21. **POST academic-procedures/api/acad/configure_final_registration/** - Implemented  
    **Description** - with this request acad person can schedule the final registration/fee payment date for upcoming semester
<br>

22. **POST /aims/generate_preregistration_report/** - Implemented  
    **Description** - with this api request acad admin can generate the pre registration report of any batch and semester in excel sheet
<br>

23. **POST /aims/generatexlsheet/** - Implemented  
    **Description** - with this api request excel sheet of the registered student in any course can be downloaded for any batch
<br>

24. **GET academic-procedures/api/fac/view_assigned_courses** - Implemented  
    **Description** - Faculty will be able to see the courses assigned to him that are currently running and active with this api request.
<br>

25. **GET academic-procedures/api/get_user_info/** - Implemented  
    **Description** - Extra api for knowing the details of the currently logged user into the system.

<br>

### APIs:-	

#### Actor: Student

###### Implemented by us:

- #### view_offered_courses: UC#8
  - **Index of api’s used** -  3, 11  
  - This use case helps students to see all the courses offered to them in the upcoming semester.  
  - Databases - [programme_curriculum_course, extra_info , student , auth_user, semester]

- #### add course: UC#1
  - **Index of api’s used** -  4  
  - The use case describes how to add courses to the course list of a UG student.  
  - Databases -[programme_curriculum_course , auth_user, course_registration , ,academic_procedures_minimumcredits]

- #### Drop course: UC#2
  - **Index of api’s used** -  5  
  - The use case describes how to drop courses to the course list of a UG student.  
  -  Databases -[programme_curriculum_course , auth_user, course_registration ,academic_procedures_minimumcredits]

- #### Replace course: UC#3
  - **Index of api’s used** -  6 , 7  
  - The use case describes how to replace a course from the course list with a swayam course of the same credit.  
  - Databases -[programme_curriculum_course , course_registration ,auth_user,academic_procedures_minimumcredits]

- #### fill_backlog _form: UC#6
  - **Index of api’s used** -  8  
  - This use case helps the student to fill the form for covering their backlog courses.  
  - Databases - [course_registration , programme_curriculum_course, auth_user, semester ,batch]

- #### Pre_registration: UC#5
  - **Index of api’s used** -  1, 9  
  - The use case handles the student registration system.  
  - Databases - [InitialRegistration , auth_user , programme_curriculum_course, StudentRegistrationChecks , semester , course_registration]

- #### Final_register: UC#4
  - **Index of api’s used** -  2  
  - The use case handles the students final registration system.  
  - Databases - [FinalRegistration , auth_user , StudentRegistrationChecks, semester]

- #### view_registration: UC#7
  - **Index of api’s used** -  11  
  - This use case describes how the Students can check their profile and courses after registration.  
  - Databases - [course_registration , auth_user , StudentRegistrationChecks]


---

#### Actor: Acad Admin

##### APIs:-
###### Already Implemented 

- #### manage_schedule: UC#9
  - **Index of api’s used** -  20 , 21  
  - This use case describes how the Academic Person updates and adds the schedule of courses and time table.  
  - Databases - [programme_curriculum_course, programme_curriculum_curriculum, Timetable]

- #### view_registration: UC#10
  - **Index of api’s used** -  13 , 22  
  - This use case describes how the Academic Person checks the final registration of students for the semester.  
  - Databases - [programme_curriculum_course, auth_user, FinalRegistration]

- #### list_courses: UC#14
  - **Index of api’s used** -  14  
  - This use case allows an Academic Admin to generate a roll list for a specific course, containing student information such as names, ID numbers, and contact details.  
  - Databases - [Courses, auth_user, programme_curriculum_curriculum, FinalRegistration, academic_information_student]

- #### generate_roll_list: UC#11
  - **Index of api’s used** -  23  
  - This use case allows an Academic Admin to generate a roll list for a specific course, containing student information such as names, ID numbers, and contact details.  
  - Databases - [Courses, auth_user, programme_curriculum_curriculum, FinalRegistration, faculty, batch]

- #### configure_pre_reg: UC#12
  - **Index of api’s used** -  15 , 16 , 17  
  - This use case allows an Academic Admin to configure the settings for the pre-registration period, including dates, eligibility criteria, and student permissions.  
  - Databases - [InitialRegistration, auth_user, courses, faculty, timetable, programme_curriculum_curriculum]

- #### configure_main_reg: UC#13
  - **Index of api’s used** -  14  
  - This use case allows an Academic Admin to configure the settings for the main-registration period, including dates, eligibility criteria, and student permissions.  
  - Databases - [InitialRegistration, auth_user, courses, timetable, programme_curriculum_curriculum]

- #### allot_swayam: UC#17
  - **Index of api’s used** -  18 , 19  
  - This use case allows an Academic Admin to replace optional courses of any student with swayam courses.  
  - Databases - [programme_curriculum_course, course_registration, student, extra_info]

---


#### Actor: Faculty

##### APIs:-
###### Already Implemented 

- #### generate_roll_list: UC#16
  - **Index of api’s used** -  23  
  - This use case allows a Faculty to generate a roll list for a specific course, containing student information such as names, ID numbers, and contact details.  
  - Databases - [Courses, auth_user, faculty, batch, course_registration, programme_curriculum_course]

- #### View_assigned_course: UC#15
  - **Index of api’s used** -  24  
  - This use case allows a Faculty to view a list of courses that he is going to teach in the upcoming semester.  
  - Databases - [curriculum_instructor, programme_curriculum_course, auth_user, programme_curriculum_curriculum]


## UI for Application

### Figma Profiles for AC-2 Course Registration

### 1. Module Description
The purpose of the Course Registration module is to streamline and enhance the overall user experience of the students, allowing them to register courses seamlessly. The module seeks to automate all the course registration activities for the Academic Section, students, and faculties.

### 2. Actors 

#### 2.1 Actor #1: Student
Represents individuals who intend to use this module for course registration, pre-registration, adding/dropping/replacing courses, viewing registration, backlog forms, etc. Students are divided based on the programme, discipline, year of joining, etc.

**Role:** Initiates the course registration process including replace/drop courses.

**Specific Functionalities:**
- Login into the app to gain access and perform the available operations.
- **UC#2:** View the offered core and elective course list for each semester along with the course details including credits, number of lectures, labs, etc.
- **UC#4:** Select from the list of available courses and submit them, thus completing pre-registration.
- Select the courses/electives for the current semester assigning priority to each course available in the course list.
- **UC#5:** View the list of selected courses entered during the registration process for a particular semester.
- **UC#1:** Perform Add/Drop of courses.
- **UC#3:** Perform Replace of courses.
- **UC#6:** Can apply/register for backlog courses.
- **UC#7:** Perform final registration.

![Diagram Image](../AC2%20-%20Course%20Registration/Assests/Student_usecase.png)

**FIGMA Profile Link:** [Figma Profile for Student](https://www.figma.com/file/bceLd1tpX7tpYUHuGTzEM5/Fusion-APP-(Copy)?type=design&node-id=0%3A1&mode=design&t=H3fWEfPYCuwLdklf-1)

---

#### 2.2 Actor #2: Faculty
Can view the courses assigned and check the students enrolled in his/her course.

**Specific Functionalities:**
- **UC#13:** View the generated roll list of the students enrolled in his/her course.
- **UC#14:** View the courses assigned to him/her.

![Diagram Image](../AC2%20-%20Course%20Registration/Assests/Faculty_usecase.png)

**FIGMA Profile Link:** [Figma Profile for Faculty](https://www.figma.com/file/bceLd1tpX7tpYUHuGTzEM5/Fusion-APP-(Copy)?type=design&node-id=0%3A1&mode=design&t=H3fWEfPYCuwLdklf-1)

---

#### 2.3 Actor #3: Academic Administration
Supervises the overall operations of the pre-registration and course registration for each semester.

**Role:** Manages the overall operations of the course registration process, scheduling registration timings, generating course lists, updating academic curriculum, etc.

**Specific Functionalities:**
- **UC#11,12:** Can add or remove courses from the list of available courses for the next semester.
- **UC#10:** Update the faculty details who will be taking the course.
- **UC#8:** Generate a roll list after the successful course registration process.
- **UC#9:** Enable pre-registration and course registration according to the Academic Calendar.

![Diagram Image](../AC2%20-%20Course%20Registration/Assests/AcadAdmin_usecase.png)

**Figma Profile Link:** [Figma Profile for Academic Administration](https://www.figma.com/file/bceLd1tpX7tpYUHuGTzEM5/Fusion-APP-(Copy)?type=design&node-id=0%3A1&mode=design&t=H3fWEfPYCuwLdklf-1)

## Database Schema

#### Faculty Mentor
Dr. Vinod Kumar Jain

#### Student Mentor
Raman Chaudhary

#### Our Team
- Aryan Sharma (21BCS038)
- Bhavik Agarwal (21BCS056)
- Deepanshu Singh (21BCS073)
- Samyak Bhargava (21BEC097)
- Vinayak Mittal (21BEC124)

## Overview of the Module
Academic Course Registration (AC-2) is software designed to manage different activities related to the Course Registrations of PDPM IIITDM Jabalpur. The module seeks to provide automated features and a smooth interface for the academic staff, students, and faculties to handle different course registration and corresponding related activities such as:
- Admission
- Course Registration
- Add-Drop
- Replace
- Apply for Backlog
- Manage Schedule
- Course-list Generation
- Roll List Generation
- And more

#### A. ER Diagram
[ER Diagram.drawio](https://drive.google.com/file/d/1GzOi2ZHEv4nxwm0_hxn843wypIjxIrgH/view)

#### B. Database Schema Info
[Database Schema || AC2 - Course Registration](https://docs.google.com/spreadsheets/d/1BrEmNJYlWcaOWRnA8d8_c_W8e1Jekoj9isDnGde1gxk/edit?gid=0#gid=0)

#### C. Changes Required in the Currently Implemented Tables
None	

#### D. Data Availability for API and Functional Testing

##### D.1 Mention the Tables That Are Already Populated
- Initial Registration
- Final Registration
- Course Registration
- Timetable
- Calendar
- Curriculum
- Student Registration Checks

##### D.2 Mention the Tables Required to Be Populated
- Curriculum_Instructor
- CourseRequested (only 1 entry)
- FeePayments

##### D.3 Mention Any Difficulties Faced by Your Team Regarding Populating Any Table
None
