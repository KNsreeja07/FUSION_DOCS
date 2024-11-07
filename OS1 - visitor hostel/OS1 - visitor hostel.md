# Authentication Module Documentation

## Table of Contents
1. [User-Centered Design (UCD)](#user-centered-design-ucd)
2. [SRS Application](#srs-app)
3. [SRS Web Interface](#srs-web-interface)
4. [API Specifications](#api-specifications)
5. [UI for Application](#ui-for-app)
6. [UI for Web](#ui-for-web)
7. [Database Schema](#database-schema)

## User-Centered Design (UCD)
### Overview
![Use Case Diagram](assets/visitor_hostel.png)

## SRS App
### Functional Requirements
## Fusion ERP

### Software Requirements Specification

#### For OS-1-VISITOR HOSTEL

**Prepared by:**

- Varun Raj (21bcs236)
- Azemera Vishnu Nayak (21bcs051)
- Avneesh Dayal (21bcs046)
- Sparsh Ranjan (21bcs205)
- Sahil Chauksey (21bcs181)

**Student Mentor:** Deepanshu Kumar (21bcs072)

---

### 1. Introduction

#### 1.1 Introduction about Fusion – A Brief Description

FusionIIIT stands as a testament to the seamless integration and automation of diverse functions within PDPM Indian Institute of Information Technology, Design and Manufacturing, Jabalpur. Crafted with precision using Python 3.8 and powered by the Django Web framework, this initiative is a student-driven endeavor designed to elevate the institute's operational landscape. Encompassing everything from efficient administration management to academic prowess and miscellaneous departmental tasks, FusionIIIT is a holistic solution that harmonizes the intricacies of campus life.

Imagine it as a digital wizard that takes care of everything, from organizing administrative tasks to making academics smoother. It's not just limited to the usual operations; FusionIIIT integrates various departments and sections, ensuring that every corner of campus life runs smoothly.

In the admin side, it handles the complicated paperwork and processes. For academics, it brings a digital touch, making learning and managing courses easier. But it doesn't stop there; FusionIIIT is like a friendly companion for all the different parts of the campus, making sure everything works well.

In simpler terms, FusionIIIT is not just a tool – it's a helpful friend, making life at PDPM IIITDM Jabalpur more organized and enjoyable for everyone.

#### 1.2 Purpose of the Module

The purpose of the Visitor Hostel Management module is to streamline and enhance the overall experience of visitors seeking accommodation in the IIIT Jabalpur visitor hostel. It aims to provide a user-friendly interface for Intenders while empowering VH In-Charge and VH Caretaker with efficient tools for managing bookings, rooms, meals, billing, and inventory. The module seeks to optimize resource utilization, ensure visitor satisfaction, and maintain the hostel's operational efficiency.

#### 1.3 Scope of the Module

The Visitor Hostel Management module is designed to efficiently handle the booking and inventory management aspects of the visitor hostel at IIIT Jabalpur. This module caters to three primary actors: the Intender (students/employees for potential visitors seeking accommodation), VH In-Charge, and VH Caretaker. The primary focus is on facilitating seamless booking processes, room and meal management, and maintaining an up-to-date inventory.

---

### 2. User/Actor Characteristics

#### 2.1 Intender (Employee/Student)

Represents individuals who intend to book accommodation and follow up on the booking process for potential visitors in applicable categories in the visitor hostel.

- **Role:** Initiates the booking process for accommodation in the visitor hostel.
- **Specific Functionalities:**
  - Submits booking requests through the Fusion portal.
  - Specifies stay duration, room requirements, and meal preferences.
  - Receives notifications about booking approval/rejection and other relevant updates.
  - Accesses booking history and status.

#### 2.2 VH In-Charge

Supervises the overall operations of the visitor hostel, overseeing bookings and ensuring a smooth stay for visitors. This role is typically filled by a faculty or an officer-level employee of the institute.

- **Role:** Manages the overall operations of the visitor hostel, overseeing bookings and ensuring a smooth stay for visitors and maintaining reports.
- **Specific Functionalities:**
  - Reviews and approves/rejects booking requests.
  - Monitors overall hostel occupancy and availability.
  - Accesses summarized reports on booking statistics, room utilization, and inventory levels.
  - Has access to all functionalities available to the VH Caretaker.

#### 2.3 VH Caretaker

Responsible for managing specific details of bookings, ensuring the readiness of rooms, managing the booking process (including room assignments/vacating), bill settlement, meal preferences and management, and overall inventory control.

- **Role:** Manages specific details of bookings, including room assignments, meal preferences, and overall inventory control.
- **Specific Functionalities:**
  - Assigns available rooms based on booking requests, considering room preferences and availability.
  - Manages meal preferences for each booking.
  - Updates and manages the hostel inventory, ensuring essential items are stocked.

---

### 3. Functional Requirements

#### 3.1 Use Case Diagram

![](assets/Aspose.Words.07cc9b8d-fda2-4d7f-85e6-523ac551edb1.001.jpeg)

#### 3.2 Use Case Description

This section describes each use case in the use case diagram in detail.



**Use Case #1**



|**UC ID**|UC#1|
| - | - |



<table><tr><th colspan="1"><b>Use case Name</b></th><th colspan="1" valign="top"><b>req_for_booking</b></th></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="1">The Intender will be able to book room(s) in the VH. The Intender has to fill the form in the required format and submit for further processing.</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="1" valign="top">Intender</td></tr>
<tr><td colspan="1"><b>Precondition</b></td><td colspan="1">The Intender must be logged-in</td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Main Flow</b></td><td colspan="1">The Intender selects the option to request a booking.</td></tr>
<tr><td colspan="1" valign="top">The system generates a form to be filled with fields like start date, end date, type of room, number of guests, etc</td></tr>
<tr><td colspan="1" valign="top">The Intender fills the form in the given format.</td></tr>
<tr><td colspan="1">The Intender submits the form by clicking a button. [A2]</td></tr>
<tr><td colspan="1"><b>Post conditions</b></td><td colspan="1" valign="top">The form is forwarded to VH Incharge.</td></tr>
<tr><td colspan="1" valign="top"><b>Alternate Flow</b></td><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the Intender Dashboard.</td></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b></td><td colspan="1" valign="top">The employee is notified with the VH In-charge’s action as the status update of the application</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1" valign="top">The Intender can ‘cancel’ the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the Intender Dashboard.</td></tr>
</table>

**Use Case #2**



<table><tr><th colspan="1" valign="top"><b>UC ID</b></th><th colspan="2" valign="top">UC#2</th></tr>
<tr><td colspan="1" valign="top"><b>Use case Name</b></td><td colspan="2" valign="top"><b>check_status</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2" valign="top">After submitting a booking request, the room Intender can check if the booking is confirmed/pending/canceled.</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="2" valign="top">Intender</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2"><p>Intender must be logged in.</p><p>Intender must have applied for booking a room.</p></td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Main Flow</b></td><td colspan="1">1</td><td colspan="1">Intender clicks on my bookings button form his dashboard.</td></tr>
<tr><td colspan="1">2</td><td colspan="1">The system generates a list of Intender’s booking requests categorized by their status.</td></tr>
<tr><td colspan="1">3</td><td colspan="1">The Intender searches a booking request from the list.</td></tr>
<tr><td colspan="1" valign="top">4</td><td colspan="1" valign="top">The system shows the current status of the booking request.</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1"><b>Alternate Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1"><b>Sub Flow</b></td><td colspan="1"></td><td colspan="1">NIL</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1">GA1</td><td colspan="1">The Intender can cancel the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the Intender Dashboard.</td></tr>
</table>

**Use Case #3****



<table><tr><th colspan="1" valign="top"><b>UC ID</b></th><th colspan="2" valign="top">UC#3</th></tr>
<tr><td colspan="1" valign="top"><b>Use case Name</b></td><td colspan="2" valign="top"><b>cancel_booking</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2" valign="top">Intenders will be able to cancel their booking of room(s) in the VH with remarks.</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="2" valign="top">Intender</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2" valign="top">The Intender must be logged-in</td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Main Flow</b></td><td colspan="1">1</td><td colspan="1">The Intender clicks on my bookings button from his dashboard.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1" valign="top">The system generates a list of Intender’s booking requests.</td></tr>
<tr><td colspan="1" valign="top">3</td><td colspan="1" valign="top">The Intender selects a booking request form the list and clicks on cancel button</td></tr>
<tr><td colspan="1" valign="top">4</td><td colspan="1" valign="top">The Intender confirms by clicking on a confirm button. [A1]</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="2" valign="top">Canceled booking will be reflected in the system and notification will be sent to the Intender.</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Alternate Flow</b></td><td colspan="1" valign="top">A1</td><td colspan="1" valign="top">The Intender clicks on the cancel button and cancels the cancel booking process.</td></tr>
<tr><td colspan="1"></td><td colspan="1"><b>Post-condition –</b> The system does not cancel the booking and returns to Intender’s bookings list.</td></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1" valign="top">GA1</td><td colspan="1" valign="top">The Intender can cancel the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the Intender Dashboard.</td></tr>
</table>

**Use Case #4**



<table><tr><th colspan="1" valign="top"><b>UC ID</b></th><th colspan="2" valign="top">UC#4</th></tr>
<tr><td colspan="1" valign="top"><b>Use case Name</b></td><td colspan="2" valign="top"><b>check_availability</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2" valign="top">The Vh caretaker will be able to check the current occupancy of VH.</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="2" valign="top">Vh caretaker</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2" valign="top">Vhcaretakere should be logged in.</td></tr>
<tr><td colspan="1" rowspan="5" valign="top"><b>Main Flow</b></td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">The Vh caretaker clicks on the room availability button from their dashboard.</td></tr>
<tr><td colspan="1">2</td><td colspan="1">The system generates a form showing the option start date and end date.</td></tr>
<tr><td colspan="1" valign="top">3</td><td colspan="1" valign="top">The Vh caretaker selects starting date and ending date for history occupancy viewing.</td></tr>
<tr><td colspan="1" valign="top">4</td><td colspan="1" valign="top">The Vh caretaker submits by clicking a button.</td></tr>
<tr><td colspan="1" valign="top">5</td><td colspan="1" valign="top">The required booking details are displayed.</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="2" valign="top">The system returns to its initial condition.</td></tr>
<tr><td colspan="1" valign="top"><b>Alternate Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1"><b>Sub Flow</b></td><td colspan="2">NIL</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1" valign="top">GA 1</td><td colspan="1" valign="top">The Vh caretaker can ‘cancel’ the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1"></td><td colspan="1"><b>Post-condition –</b> The system returns to the Vh caretaker Dashboard.</td></tr>
</table>

**Use Case #5****
<table><tr><th colspan="1"><b>UC ID</b></th><th colspan="2">UC#5</th></tr>
<tr><td colspan="1"><b>Use case Name</b></td><td colspan="2"><b>allot_rooms</b></td></tr>
<tr><td colspan="1"><b>Description</b></td><td colspan="2">The caretaker will allot rooms according to the availability .</td></tr>
<tr><td colspan="1"><b>Actor</b></td><td colspan="2">Caretaker</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2" valign="top"><p>The caretaker</p><p>must be logged in.</p><p>The Intender should have applied for booking. Rooms should be available.</p></td></tr>
<tr><td colspan="1" rowspan="5" valign="top"><b>Main Flow</b></td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">The caretaker selects option booking to view booking requests.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1" valign="top">The system generates a list displaying the pending booking requests.</td></tr>
<tr><td colspan="1" valign="top">3</td><td colspan="1" valign="top">The caretaker selects a booking request.</td></tr>
<tr><td colspan="1" valign="top">4</td><td colspan="1" valign="top">The caretaker allots rooms according to the request and availability from the list of available rooms. [A1]</td></tr>
<tr><td colspan="1" valign="top">5</td><td colspan="1" valign="top">The caretaker forwards the request to the incharge.</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="2" valign="top">Room is allocated to the Intender.</td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Alternate Flow</b></td><td colspan="1" valign="top">A1</td><td colspan="1" valign="top">The VH In-charge cancels the application mentioning the remark.</td></tr>
<tr><td colspan="1"></td><td colspan="1"><b>Post-Condition:</b> Intender will get notification about cancellation of application.</td></tr>
<tr><td colspan="1" valign="top">A2</td><td colspan="1" valign="top">The caretaker does not confirm by clicking on cancel button.</td></tr>
<tr><td colspan="1"></td><td colspan="1"><b>Post-condition:</b> The system does not allot rooms and returns to booking requests list.</td></tr>
<tr><td colspan="1"><b>Sub Flow</b></td><td colspan="2">NIL</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1">GA1</td><td colspan="1">The VH In-charger can cancel the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top">The Intender can cancel the procedure at any time by exercising such an option</td></tr>
</table>

**Use Case #6**



<table><tr><th colspan="1" valign="top"><b>UC ID</b></th><th colspan="2" valign="top">UC#6</th></tr>
<tr><td colspan="1" valign="top"><b>Use case Name</b></td><td colspan="2" valign="top"><b>cancel_booking</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2" valign="top">VH Caretaker will be able to cancel any booking of room(s) in VH with remarks</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="2" valign="top">VH Caretaker</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2" valign="top">There should be a pre-booked room in VH.</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Main Flow</b></td><td colspan="1">1</td><td colspan="1">The VH Caretaker selects a booking to be canceled from the list of booked rooms.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1" valign="top">Caretaker cancels the selected booking by clicking on a button.</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="2" valign="top">Canceled booking will be reflected in the system and notification will be sent to the concerned Intender.</td></tr>
<tr><td colspan="1" valign="top"><b>Alternate Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1">GA1</td><td colspan="1">The VH Caretaker can ‘cancel’ the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the VH In-charge’s Dashboard.</td></tr>
</table>


**Use Case #7**



<table><tr><th colspan="1"><b>UC ID</b></th><th colspan="2">UC#7</th></tr>
<tr><td colspan="1"><b>Use case Name</b></td><td colspan="2" valign="top"><b>manage_guest_check_in</b></td></tr>
<tr><td colspan="1"><b>Description</b></td><td colspan="2">VH Caretaker will be able to mark the check in status of a booked VH room.</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="2" valign="top">VH Caretaker</td></tr>
<tr><td colspan="1"><b>Precondition</b></td><td colspan="2">VH Caretaker must be logged in.</td></tr>
<tr><td colspan="1" rowspan="5" valign="top"><b>Main Flow</b></td><td colspan="1">1</td><td colspan="1">VH Caretaker clicks on the check in button from his dashboard.</td></tr>
<tr><td colspan="1">2</td><td colspan="1">The system will generate the list of guests having current booking and not checked in yet.</td></tr>
<tr><td colspan="1">3</td><td colspan="1">The VH Caretaker selects the name of the guest and fills the check in time and date.</td></tr>
<tr><td colspan="1">4</td><td colspan="1">The system asks for confirmation.</td></tr>
<tr><td colspan="1">5</td><td colspan="1">The VH Caretaker clicks on the confirm button. [A1]</td></tr>
<tr><td colspan="1"><b>Post conditions</b></td><td colspan="2">System reflects the modified details regarding room status.</td></tr>
<tr><td colspan="1" valign="top"><b>Alternate Flow</b></td><td colspan="1" valign="top">A1</td><td colspan="1" valign="top">The VH Caretaker clicks cancel.</td></tr>
<tr><td colspan="1"><b>Sub Flow</b></td><td colspan="1"></td><td colspan="1">The system updates the database and marks the room as occupied.</td></tr>
<tr><td colspan="1" rowspan="2"><b>Global Alternate Flow</b></td><td colspan="1">GA1</td><td colspan="1">The VH Caretaker can ‘cancel’ the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the VH Caretaker’s Dashboard.</td></tr>
</table>

**Use Case #8**



<table><tr><th colspan="1"><b>UC ID</b></th><th colspan="2">UC#8</th></tr>
<tr><td colspan="1"><b>Use case Name</b></td><td colspan="2"><b>manage_guest_check_out</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2">VH Caretaker will be able to initiate the process of checkout on the system regarding bill clearance and room status update.</td></tr>
<tr><td colspan="1"><b>Actor</b></td><td colspan="2">VH Caretaker</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2">Guests have checked-in at VH. VH Caretaker must be logged in.</td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Main Flow</b></td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">VH Caretaker clicks on the checkout button from his dashboard.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1" valign="top">The system generates the lists of guests currently present at VH.</td></tr>
<tr><td colspan="1">3</td><td colspan="1">The VH Caretaker selects the Guest name and click on the checkout button. [A1]</td></tr>
<tr><td colspan="1" valign="top">4</td><td colspan="1" valign="top">UC#10 will be exercised.</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="2" valign="top">System reflects the modified details regarding room status and account.</td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Alternate Flow</b></td><td colspan="1" valign="top">A1</td><td colspan="1" valign="top">VH Caretaker canceled the checkout request.</td></tr>
<tr><td colspan="1"></td><td colspan="1"><b>Post-condition</b> – The system returns to the employee ‘Dashboard’ – initial screen.</td></tr>
<tr><td colspan="1" valign="top">A2</td><td colspan="1" valign="top">The head chooses not to confirm.</td></tr>
<tr><td colspan="1"></td><td colspan="1"><b>Post-condition –</b> The system displays the form with the data filled in so far.</td></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b></td><td colspan="1" valign="top">S1</td><td colspan="1" valign="top">System marks the corresponding room empty.</td></tr>
</table>



<table><tr><th colspan="1" rowspan="2"><b>Global Alternate Flow</b></th><th colspan="1" valign="top">GA1</th><th colspan="1" valign="top">The VH Caretaker can ‘cancel’ the procedure at any time by exercising such an option</th></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the VH Caretaker’s Dashboard.</td></tr>
</table>

**Use Case #9**



<table><tr><th colspan="1" valign="top"><b>UC ID</b></th><th colspan="2" valign="top">UC#9</th></tr>
<tr><td colspan="1" valign="top"><b>Use case Name</b></td><td colspan="2" valign="top"><b>manage_bill_settlement</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2" valign="top">VH Caretaker sees if the bill is paid by intender/guest. He collects the money according to the bill and updates the system accordingly.</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="2" valign="top">VH Caretaker</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2" valign="top"><p>Guests have checked-in at VH.</p><p>VH Caretaker must be logged in.</p><p>The VH Caretaker must be at the Check Out interface.</p></td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Main Flow</b></td><td colspan="1">1</td><td colspan="1">VH Caretaker clicks on the Generate bill button.</td></tr>
<tr><td colspan="1">2</td><td colspan="1">System generates the bill containing meal charges, room charges.</td></tr>
<tr><td colspan="1">3</td><td colspan="1">VH Caretaker selects the mode of payment(intender/guest/institute) from the checkbox.</td></tr>
<tr><td colspan="1">4</td><td colspan="1">VH Caretaker updates the system about the payment. [S1]</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="2" valign="top">System reflects the payment details.</td></tr>
<tr><td colspan="1" valign="top"><b>Alternate Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1"><b>Sub Flow</b></td><td colspan="1" valign="top">S1</td><td colspan="1" valign="top">System updates the VH Account.</td></tr>
<tr><td colspan="1" rowspan="2"><b>Global Alternate Flow</b></td><td colspan="1" valign="top">GA1</td><td colspan="1" valign="top">The VH Caretaker can ‘cancel’ the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the VH Caretaker’s Dashboard.</td></tr>
</table>

**Use Case #10**



<table><tr><th colspan="1" valign="top"><b>UC ID</b></th><th colspan="2" valign="top">UC#10</th></tr>
<tr><td colspan="1" valign="top"><b>Use case Name</b></td><td colspan="2" valign="top"><b>manage_inventory</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2" valign="top">VH Caretaker will be able to manage the inventory of the VH.</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="2" valign="top">VH Caretaker</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2" valign="top">The VH Caretaker should be logged in.</td></tr>
<tr><td colspan="1" rowspan="3" valign="top"><b>Main Flow</b></td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">Screen will show the inventory items with different categories consumable and non consumable..</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1" valign="top">The VH Caretaker will set the threshold levels of stock items. [A1] [A2]</td></tr>
<tr><td colspan="1" valign="top">3</td><td colspan="1" valign="top">System alerts will be generated for items below threshold.</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="2" valign="top">The inventory will be in a consistent state.</td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Alternate Flow</b></td><td colspan="1" valign="top">A1</td><td colspan="1" valign="top">VH Caretaker will add items to inventory.</td></tr>
<tr><td colspan="1"></td><td colspan="1"><b>Post-condition</b> – The inventory will be now updated and in a consistent state.</td></tr>
<tr><td colspan="1" valign="top">A2</td><td colspan="1" valign="top">VH Caretaker selects for update_consumption(UC#16).</td></tr>
<tr><td colspan="1"></td><td colspan="1"><b>Post-condition –</b> The inventory will be now updated and in a consistent state.</td></tr>
</table>



<table><tr><th colspan="1"><b>Sub Flow</b></th><th colspan="1"></th><th colspan="1">The employee is notified with the head’s action as the status update of the application</th></tr>
<tr><td colspan="1" rowspan="2"><b>Global Alternate Flow</b></td><td colspan="1">GA1</td><td colspan="1">The VH Caretaker can ‘cancel’ the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the VH Caretaker’s Dashboard.</td></tr>
</table>

**Use Case #11**



|**UC ID**|UC#11||
| - | - | :- |
|**Use case Name**|**get\_low\_on\_stock\_alerts**||
|**Description**|VH Caretaker will get alerts when any inventory item quantity falls below a pre-decided threshold.||
|**Actor**|VH Caretaker||
|**Precondition**|VH Caretaker has logged in.||
|**Main Flow**|1|System generates an alert when there is a shortage of any inventory item.|
|**Post conditions**|The VH Caretaker is notified.||
|**Alternate Flow**|NIL||
|**Sub Flow**|NIL||
|**Global Alternate Flow**|NIL||

**Use Case #12**



<table><tr><th colspan="1" valign="top"><b>UC ID</b></th><th colspan="2" valign="top">UC#12</th></tr>
<tr><td colspan="1" valign="top"><b>Use case Name</b></td><td colspan="2" valign="top"><b>update_consumption</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2" valign="top">The VH Caretaker will periodically update the system with the quantity of items consumed.</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="2" valign="top">VH Caretaker</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2" valign="top">VH Caretaker must be logged in.</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Main Flow</b></td><td colspan="1">1</td><td colspan="1">The VH caretaker will select an item from the inventory list.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1" valign="top">The VH Caretaker will update the quantity consumed.</td></tr>
<tr><td colspan="1"><b>Post conditions</b></td><td colspan="2">The system is now updated and consistent.</td></tr>
<tr><td colspan="1" valign="top"><b>Alternate Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1">GA1</td><td colspan="1">The VH Caretaker can ‘cancel’ the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the VH Caretaker’s Dashboard.</td></tr>
</table>

**Use Case #13****



<table><tr><th colspan="1" valign="top"><b>UC ID</b></th><th colspan="2" valign="top">UC#13</th></tr>
<tr><td colspan="1" valign="top"><b>Use case Name</b></td><td colspan="2" valign="top"><b>manage_noTurnUp</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2" valign="top">The system will notify VH Caretaker/VH In-charge about guests who didn’t turn up. The VH Caretaker can take actions as deemed fit.</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="2" valign="top">VH Caretaker</td></tr>
<tr><td colspan="1"><b>Precondition</b></td><td colspan="2">VH Caretaker should be logged in.</td></tr>
<tr><td colspan="1" rowspan="3" valign="top"><b>Main Flow</b></td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">System will generate an alert for the VH Caretaker about no turn up of guests.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1" valign="top">VH Caretaker will confirm such situations through the Intender.</td></tr>
<tr><td colspan="1" valign="top">3</td><td colspan="1" valign="top">VH Caretaker exercises UC#6. [A2]</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="2" valign="top">System is now updated and consistent.</td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Alternate Flow</b></td><td colspan="1">A1</td><td colspan="1">VH In-charge will ask VH Caretaker to update (cancel or retain) the system accordingly.</td></tr>
<tr><td colspan="1"></td><td colspan="1"><b>Post-Condition:</b> System is now updated and consistent.</td></tr>
<tr><td colspan="1" valign="top">A2</td><td colspan="1" valign="top">The VH Caretaker does nothing.</td></tr>
<tr><td colspan="1"></td><td colspan="1"><b>Post-condition –</b> The system does not cancel the booking.</td></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1" valign="top"><b>Global Alternate Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
</table>

**Use Case #14**



<table><tr><th colspan="1" valign="top"><b>UC ID</b></th><th colspan="2" valign="top">UC#13</th></tr>
<tr><td colspan="1" valign="top"><b>Use case Name</b></td><td colspan="2" valign="top"><b>view_bookings</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2" valign="top">The VH In-charge will be able to check the booking history and current occupancy of VH.</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="2" valign="top">VH In-charge</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2" valign="top">VH In-charge should be logged in.</td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Main Flow</b></td><td colspan="1">1</td><td colspan="1">The VH in-charge click on view booking button from their dashboard.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1" valign="top">The system generates a form showing the option start date and end date.</td></tr>
<tr><td colspan="1" valign="top">3</td><td colspan="1" valign="top">The VH In-charge selects starting date and ending date for history and occupancy viewing.</td></tr>
<tr><td colspan="1">5</td><td colspan="1">The required booking details are displayed.</td></tr>
<tr><td colspan="1"><b>Post conditions</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1" valign="top"><b>Alternate Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1" valign="top">GA1</td><td colspan="1" valign="top">The VH In-charge can ‘cancel’ the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the VH In-charge’s Dashboard.</td></tr>
</table>

**Use Case #15****
<table><tr><th colspan="1" valign="top"><b>UC ID</b></th><th colspan="2" valign="top">UC#14</th></tr>
<tr><td colspan="1" valign="top"><b>Use case Name</b></td><td colspan="2" valign="top"><b>confirm_booking</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2" valign="top">VH In-Charge will grant the confirmation of the booking after verifying the information provided in the application.</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="2" valign="top">VH In-Charge</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2" valign="top"><p>VH In-Charge has logged in.</p><p>VH In-Charge has received application(s) to book rooms in VH.</p></td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Main Flow</b></td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">VH In-charge opens the application and verifies the details.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1" valign="top">VH In-charge confirms the booking. [A1]</td></tr>
<tr><td colspan="1"><b>Post conditions</b></td><td colspan="2">VH In-Charge has responded to the booking request by the stakeholder.</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Alternate Flow</b></td><td colspan="1">A1</td><td colspan="1">VH In-charge finds discrepancies in the application and rejects it with remarks.</td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-Condition:</b> Intender is notified about the cancellation of application.</td></tr>
<tr><td colspan="1"><b>Sub Flow</b></td><td colspan="2">NIL</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1" valign="top">GA1</td><td colspan="1" valign="top">The VH In-charge can ‘cancel’ the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the VH In-charges’s Dashboard.</td></tr>
</table>

**Use Case #16**



<table><tr><th colspan="1" valign="top"><b>UC ID</b></th><th colspan="2" valign="top">UC#16</th></tr>
<tr><td colspan="1" valign="top"><b>Use case Name</b></td><td colspan="2" valign="top"><b>reject_booking</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2" valign="top">VH In-charge will be able to reject any booking of room(s) in VH with remarks</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="2" valign="top">VH In-charge</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2" valign="top">There should be a pre-booked room in VH.</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Main Flow</b></td><td colspan="1">1</td><td colspan="1">The VH In-charge selects a booking to be canceled from the list of alloted rooms.</td></tr>
<tr><td colspan="1">2</td><td colspan="1">VH In-charge cancels the selected booking by clicking on a button.</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="2" valign="top">Canceled booking will be reflected in the system and notification will be sent to the concerned Intender.</td></tr>
<tr><td colspan="1" valign="top"><b>Alternate Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1" valign="top">GA1</td><td colspan="1" valign="top">The VH In-charge can ‘cancel’ the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the VH In-charge’s Dashboard.</td></tr>
</table>

**Use Case #17****
<table><tr><th colspan="1" valign="bottom"><b>UC ID</b></th><th colspan="3" valign="bottom">UC#17</th></tr>
<tr><td colspan="1" valign="bottom"><b>Use case Name</b></td><td colspan="3" valign="bottom"><b>mange_booking</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="3" valign="top">The "Manage Booking" use case allows the caretaker of the college hostel to review, approve, reject, edit, cancel, and view booking requests for the visitor hostel through the Fusion portal.</td></tr>
<tr><td colspan="1" valign="bottom"><b>Actor</b></td><td colspan="3" valign="bottom">VH Caretaker</td></tr>
<tr><td colspan="1" valign="bottom"><b>Precondition</b></td><td colspan="3" valign="bottom">The caretaker is logged in into the system.</td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Main Flow</b></td><td colspan="1" valign="bottom">1</td><td colspan="2" valign="bottom">The Caretaker navigates to the "Manage Booking" section.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="2" valign="top">The system displays the list of bookings with its respective status.</td></tr>
<tr><td colspan="1" valign="bottom">3</td><td colspan="2" valign="bottom">The Caretaker selects a booking request to review. [A1][A2]</td></tr>
<tr><td colspan="1" valign="top">4</td><td colspan="2" valign="top">The caretaker views the booking information of approved requests. [A3][A4]</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="3" valign="top">The updated booking information is reflected in the database.</td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Alternate Flow</b></td><td colspan="1" rowspan="2" valign="top">A1</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">The request is pending. The Caretaker selects the "Approve" action.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1" valign="top">The system updates the booking status to "Approved" and the same is reflected to the Intender.</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">A2</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">The Caretaker selects the "Reject" action citing the reason for rejection.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1" valign="top">The system updates the booking status to rejected and the same is reflected to the Intender.</td></tr>
</table>




<table><tr><th colspan="1" valign="bottom"><b>UC ID</b></th><th colspan="3" valign="bottom">UC#17</th></tr>
<tr><td colspan="1" valign="bottom"><b>Use case Name</b></td><td colspan="3" valign="bottom"><b>mange_booking</b></td></tr>
<tr><td colspan="1" rowspan="5"></td><td colspan="1" rowspan="2" valign="top">A3</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">The caretaker edits the booking details, like booking date, Intender details etc.</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">2</td><td colspan="1" rowspan="2" valign="top">The edited information is updated in the database and the same is reflected to the Intender as well.</td></tr>
<tr><td colspan="1" rowspan="3" valign="top">A4</td></tr>
<tr><td colspan="1" valign="top">1</td><td colspan="1" valign="bottom">The caretaker selects the cancel booking options specifying the reason for cancellation.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1" valign="top">The system updates the booking status of that booking to “cancelled” and the same is reflected to the Intender as well.</td></tr>
<tr><td colspan="1" valign="bottom"><b>Sub Flow</b></td><td colspan="3" valign="bottom">NIL</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1" valign="top">GA1</td><td colspan="2" valign="top">The VH Caretaker can ‘cancel’ the procedure at any time by exercising such an option and will be directed to the dashboard.</td></tr>
<tr><td colspan="1" valign="top">GA2</td><td colspan="2" valign="bottom">If a technical error occurs during the execution of any action (e.g., database failure, server issues), the system displays an error message and logs the incident.</td></tr>
</table>

## 3.3. Other Functional Requirements

1. This module will make use of the **communication module** for sending notifications and alerts to various actors involved in the module, suitably for booking confirmations, rejections, or modifications, etc.

2. Automated email or SMS notifications for booking confirmations, rejections, or modifications.

3. Alerts for critical inventory levels and other important updates.

4. The **Super Admin** of Fusion should be able to assign roles for VH In-Charge and VH Caretaker.

5. The system should be able to handle offline bookings.

6. The category conversion of the visitors may be possible, subject to the approval of the competent authority.

7. Changes in the tariff may occur from time to time, as decided by the institute authorities.

---

## 3.4 Other Constraints

### 1. User Interfaces

- The user interface should comply with the color scheme and dashboard design of FUSION IIIT. Users should be able to navigate seamlessly from one functionality to another. 
- Inter-module navigation should be smooth, ensuring all functionalities are easy to use without requiring specific training.

### 2. Tech Stack Used

The project's tech stack comprises various libraries, including:
- **AMQP 5.0.2** for messaging
- **Beautiful Soup 4.9.3** for web scraping
- **Django 3.1.5** as the core framework
- **Cryptography 36.0.2** for security
- **django-allauth 0.44.0** and **django-cors-headers 3.7.0** for additional Django functionalities
- **django-debug-toolbar 3.2.4** and **djangorestframework 3.12.2** for debugging and API development
- External libraries such as **numpy 1.22.3**, **psycopg2-binary 2.8.6**, and **requests 2.25.1** contribute to data manipulation, database connectivity, and web request handling, respectively.

These components collectively form a comprehensive and efficient tech stack for the project.

### 3. Business Rules (if any)

1. The room booking and billing shall be done based on the category of the visitor (see the existing rule set for the same).

---

## Non-Functional Requirements
#### 1. Performance

- The system should respond to user interactions quickly. Response time for booking actions, inventory updates, and notifications should be minimal.

#### 2. Scalability

- The system should handle a large number of concurrent users. Performance should be evaluated under increasing load conditions.

#### 3. Availability

- The system should be available 99.9% of the time.

#### 4. Security

- Ensure data confidentiality and integrity. Role-based authorization must ensure that users can only perform actions relevant to their designated roles.

---

### 5. Module Dependencies with Other Fusion Modules

#### 5.1. UI Level

- **Color scheme and dashboard design:** The UI should adhere to the established FUSION IIIT style guide for a consistent user experience. Navigation through different functionalities should be intuitive and effortless.
- The interface of the dashboard should be similar to the home page, and the connectivity between both should be well-defined.
- **Accessibility:** The UI should be accessible to users with disabilities, following WCAG guidelines.
- **Responsive design:** The UI should adapt to different screen sizes and devices for optimal viewing and interaction.

#### 5.2. DB Level Dependencies

- **Data schema:** The database schema should be designed to efficiently store and retrieve visitor hostel booking data, including room availability, inventory levels, user roles, and booking history.
- The database is based on the registration and availability of the stocks.
- **Data integrity:** Data validation and error handling mechanisms should be implemented to ensure data accuracy and consistency.
- **Database performance:** The database should be optimized for fast retrieval and update operations, particularly during peak booking periods.

#### 5.3. Module Level Dependencies

- Module level dependencies define the intra-level dependencies in the module.
- **Communication module:** Integration with the existing communication module is required for sending email and SMS notifications about booking confirmations, rejections, or modifications.
- **Workflow engine:** A workflow engine might be utilized to automate task execution and manage approval processes for complex booking scenarios.


### SRS Web Interface
same as above 
srs app is combined of both app and web

### API Specifications
#### **Visitor Hostel Module**

**Student Mentor:** Deepanshu Kumar (21BCS072)

![Visitor Hostel Module](assets/Aspose.Words.921ed09f-d4a8-4507-a3ea-959f29cdef2d.001.png)

---

#### Team Members

- **Sparsh Ranjan (21BCS205)**
- **Varun Raj (21BCS236)**
- **Avneesh Dayal (21BCS046)**
- **Azemera Vishnu Nayak (21BCS051)**
- **Sahil Chauksey (21BCS181)**

---

### API Overview

#### **1. Endpoints**

##### Booking Management
1. **Req_for_booking:** Allows the Intender to submit a room booking request in the Visitor Hostel (VH).
   - **Database:** `get_booking_requests`
   - **Status:** Working
   - **Image:** ![Req_for_booking](assets/Aspose.Words.921ed09f-d4a8-4507-a3ea-959f29cdef2d.002.jpeg)

2. **Check_status:** Checks the status of a booking (confirmed, pending, or canceled).
   - **Database:** Not available
   - **Status Code:** 500 (Internal Server Error)
   - **Image:** ![Check_status](assets/Aspose.Words.921ed09f-d4a8-4507-a3ea-959f29cdef2d.004.jpeg)

3. **Cancel_booking:** Allows Intenders to cancel room bookings in the VH.
   - **Database:** Not available
   - **Status Code:** 404 (Not Found)
   - **Image:** ![Cancel_booking](assets/Aspose.Words.921ed09f-d4a8-4507-a3ea-959f29cdef2d.005.jpeg)

#### Room Management
4. **Check_availability:** VH caretaker checks the current occupancy of the hostel.
   - **Database:** Not available
   - **Status Code:** 403 (Forbidden)
   - **Image:** ![Check_availability](assets/Aspose.Words.921ed09f-d4a8-4507-a3ea-959f29cdef2d.006.jpeg)

5. **Allot_rooms:** Assigns rooms based on availability.
   - **Database:** Not available
   - **Status Code:** 404 (Not Found)
   - **Image:** ![Allot_rooms](assets/Aspose.Words.921ed09f-d4a8-4507-a3ea-959f29cdef2d.007.jpeg)

6. **Manage_guest_check_in:** Manages check-in status of a booked room.
   - **Status Code:** 403 (Forbidden)
   - **Image:** ![Manage_guest_check_in](assets/Aspose.Words.921ed09f-d4a8-4507-a3ea-959f29cdef2d.008.jpeg)

7. **Manage_guest_check_out:** Initiates guest checkout, manages bill clearance and updates room status.
   - **Database:** Not available
   - **Status Code:** 404 (Not Found)
   - **Image:** ![Manage_guest_check_out](assets/Aspose.Words.921ed09f-d4a8-4507-a3ea-959f29cdef2d.009.jpeg)

#### Additional APIs to Implement
- **manage_noTurnUp:** Notifies VH staff if guests fail to check in.
- **Manage_bill_settlement:** Confirms bill payment, updates status in the system.
- **Manage_inventory:** VH caretaker manages VH inventory.
- **Get_low_on_stock_alerts:** Alerts VH staff for low inventory items.
- **Update_consumption:** Periodic inventory consumption updates.
- **View_bookings:** Displays booking history and occupancy for VH in-charge.
- **Confirm_booking:** Grants booking confirmation after verification.
- **Reject_booking:** Rejects bookings with remarks as required.

---

### **2. Request/Response Formats**

#### Sample Formats for Common Requests

- **Booking Request (`Req_for_booking`):**
  - **Request:** Form data with booking details (dates, room type, etc.)
  - **Response:** Success message with booking ID and status.

- **Check Status (`Check_status`):**
  - **Request:** Booking ID
  - **Response:** Booking status (confirmed/pending/canceled).

- **Room Check-In (`Manage_guest_check_in`):**
  - **Request:** Guest details and booking ID
  - **Response:** Confirmation of check-in with room details.

---

### **3. Authentication**

- **Global API Credentials:**  
  - Essential for accessing critical features across APIs.
  - Currently missing, limiting access to drilling and comprehensive data for testing.

- **Access Control and Permissions:**
  - **VH In-Charge:** Confirm/reject bookings, view bookings, manage bills.
  - **Caretaker:** Manage check-in/out, inventory, and room availability.
  - **Intender:** Submit booking requests, check booking status, cancel bookings.

---

### Current Problems in Module

#### **Existing API Issues:**
- **Missing login credentials** prevents accessing the global API.
- **Drilling API inaccessible,** restricting data retrieval.
- **Frequent errors (400, 403, 500)** indicate security and stability issues.
- **Database redundancy** with multiple databases for single tasks requires optimization.

#### **Incomplete APIs:**
- Partial functionality in critical workflows, including `Check_status`, `Cancel_booking`, and `Allot_rooms`.

#### **Missing APIs:**
- Absence of manage_noTurnUp, Manage_bill_settlement, Manage_inventory, and other key features limits the VH staff's operational capacity.

--- 

The current structure and missing components significantly impact the functionality, security, and usability of the Visitor Hostel Module.


### UI for App
#### Design Principles
**Fusion ERP**

**Software Requirements Specification**

for

**OS-1-VISITOR HOSTEL**

Prepared by:

**Varun Raj(21bcs236) Azemera Vishnu Nayak(21bcs051) Avneesh Dayal(21bcs046)**

**Sparsh Ranjan(21bcs205) Sahil Chauksey(21bcs181)**

Student Mentor**: Deepanshu Kumar(21bcs072)**

**1 Introduction**

1. **Introduction about the Fusion – A brief Description**

FusionIIIT stands as a testament to the seamless integration and automation of diverse functions within PDPM Indian Institute of Information Technology, Design and Manufacturing, Jabalpur. Crafted with precision using Python 3.8 and powered by the Django Web framework, this initiative is a student-driven endeavor designed to elevate the institute's operational landscape. Encompassing everything from efficient administration management to academic prowess and miscellaneous departmental tasks, FusionIIIT is a holistic solution that harmonizes the intricacies of campus life.

Imagine it as a digital wizard that takes care of everything, from organizing the administrative stuff to making academics smoother. It's not just limited to the usual tasks; FusionIIIT jumps into various departments and sections, making sure every corner of campus life runs smoothly.

In the admin side, it handles the complicated paperwork and processes. For academics, it brings a digital touch, making learning and managing courses easier. But it doesn't stop there; FusionIIIT is like a friendly companion for all the different parts of the campus, making sure everything works well.

In simpler terms, FusionIIIT is not just a tool – it's a helpful friend, making life at PDPM IIITDM Jabalpur more organized and enjoyable for everyone.

2. **Purpose of the module:**

The purpose of the Visitor Hostel Management module is to streamline and enhance the overall experience of visitors seeking accommodation in the IIIT Jabalpur visitor hostel. It aims to provide a user-friendly interface for Intenders while empowering VH In charge and VH Caretaker with efficient tools for managing bookings, rooms, meals, billing, and inventory. The module seeks to optimize resource utilization, ensure visitor satisfaction, and maintain the hostel's operational efficiency.

3. **Scope of the module**

The Visitor Hostel Management module is designed to efficiently handle the booking and inventory management aspects of the visitor hostel at IIIT Jabalpur. This module caters to three primary actors: the Intender (students/employees for potential visitors seeking accommodation), VH In charge, and VH Caretaker. The primary focus is on facilitating seamless booking processes, rooms, and meal management, and

maintaining an up-to-date inventory.

2. **User/Actor characteristics**
1. **Intender (Employee/Student):**

Represents individuals who intend to book accommodation and follow up the booking process for potential visitors in applicable categories in the visitor hostel.

**Role:** Initiates the booking process for accommodation in the visitor hostel. **Specific Functionalities:**

- Submits booking requests through the Fusion portal.
- Specifies stay duration, room requirement, and meal requirements.
- Receives notifications about booking approval/rejection and other relevant updates.
- Accesses booking history and status.
2. **VH In charge**:

Supervises the overall operations of the visitor hostel, overseeing bookings and ensuring a smooth stay for visitors. This role will be typically played by a faculty or an officer- level employee of the institute.

**Role:** Manages the overall operations of the visitor hostel, overseeing bookings and ensuring a smooth stay for visitors and maintaining reports.

**Specific Functionalities:**

- Reviews and approves/rejects booking requests.
- Monitors overall hostel occupancy and availability.
- Accesses summarized reports on booking statistics, room utilization, and inventory levels.
- All the functionality exercised by VH caretaker to be also available for this actor.
3. **VH Caretaker**

Responsible for managing specific details of bookings, ensuring the readiness of rooms, managing the booking process including room assignments/vacating, bill settlement and accounting part, meal preferences and management, and overall inventory control.

**Role:** Manages specific details of bookings, including room assignments, meal preferences, and overall inventory control.

**Specific Functionalities:**

- Assigns available rooms based on booking requests, considering room preferences and availability.
- Manages meal preferences for each booking.
- Updates and manages the hostel inventory, ensuring essential items are stocked.
3. **Functional Requirements**
1. **Use Case Diagram**

![](assets/Aspose.Words.07cc9b8d-fda2-4d7f-85e6-523ac551edb1.001.jpeg)

### 2. **Use case Description**

This section describes each use case in the use case diagram in all details.

**Use Case #1**



|**UC ID**|UC#1|
| - | - |



<table><tr><th colspan="1"><b>Use case Name</b></th><th colspan="1" valign="top"><b>req_for_booking</b></th></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="1">The Intender will be able to book room(s) in the VH. The Intender has to fill the form in the required format and submit for further processing.</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="1" valign="top">Intender</td></tr>
<tr><td colspan="1"><b>Precondition</b></td><td colspan="1">The Intender must be logged-in</td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Main Flow</b></td><td colspan="1">The Intender selects the option to request a booking.</td></tr>
<tr><td colspan="1" valign="top">The system generates a form to be filled with fields like start date, end date, type of room, number of guests, etc</td></tr>
<tr><td colspan="1" valign="top">The Intender fills the form in the given format.</td></tr>
<tr><td colspan="1">The Intender submits the form by clicking a button. [A2]</td></tr>
<tr><td colspan="1"><b>Post conditions</b></td><td colspan="1" valign="top">The form is forwarded to VH Incharge.</td></tr>
<tr><td colspan="1" valign="top"><b>Alternate Flow</b></td><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the Intender Dashboard.</td></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b></td><td colspan="1" valign="top">The employee is notified with the VH In-charge’s action as the status update of the application</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1" valign="top">The Intender can ‘cancel’ the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the Intender Dashboard.</td></tr>
</table>

**Use Case #2**



<table><tr><th colspan="1" valign="top"><b>UC ID</b></th><th colspan="2" valign="top">UC#2</th></tr>
<tr><td colspan="1" valign="top"><b>Use case Name</b></td><td colspan="2" valign="top"><b>check_status</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2" valign="top">After submitting a booking request, the room Intender can check if the booking is confirmed/pending/canceled.</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="2" valign="top">Intender</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2"><p>Intender must be logged in.</p><p>Intender must have applied for booking a room.</p></td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Main Flow</b></td><td colspan="1">1</td><td colspan="1">Intender clicks on my bookings button form his dashboard.</td></tr>
<tr><td colspan="1">2</td><td colspan="1">The system generates a list of Intender’s booking requests categorized by their status.</td></tr>
<tr><td colspan="1">3</td><td colspan="1">The Intender searches a booking request from the list.</td></tr>
<tr><td colspan="1" valign="top">4</td><td colspan="1" valign="top">The system shows the current status of the booking request.</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1"><b>Alternate Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1"><b>Sub Flow</b></td><td colspan="1"></td><td colspan="1">NIL</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1">GA1</td><td colspan="1">The Intender can cancel the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the Intender Dashboard.</td></tr>
</table>

**Use Case #3****



<table><tr><th colspan="1" valign="top"><b>UC ID</b></th><th colspan="2" valign="top">UC#3</th></tr>
<tr><td colspan="1" valign="top"><b>Use case Name</b></td><td colspan="2" valign="top"><b>cancel_booking</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2" valign="top">Intenders will be able to cancel their booking of room(s) in the VH with remarks.</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="2" valign="top">Intender</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2" valign="top">The Intender must be logged-in</td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Main Flow</b></td><td colspan="1">1</td><td colspan="1">The Intender clicks on my bookings button from his dashboard.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1" valign="top">The system generates a list of Intender’s booking requests.</td></tr>
<tr><td colspan="1" valign="top">3</td><td colspan="1" valign="top">The Intender selects a booking request form the list and clicks on cancel button</td></tr>
<tr><td colspan="1" valign="top">4</td><td colspan="1" valign="top">The Intender confirms by clicking on a confirm button. [A1]</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="2" valign="top">Canceled booking will be reflected in the system and notification will be sent to the Intender.</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Alternate Flow</b></td><td colspan="1" valign="top">A1</td><td colspan="1" valign="top">The Intender clicks on the cancel button and cancels the cancel booking process.</td></tr>
<tr><td colspan="1"></td><td colspan="1"><b>Post-condition –</b> The system does not cancel the booking and returns to Intender’s bookings list.</td></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1" valign="top">GA1</td><td colspan="1" valign="top">The Intender can cancel the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the Intender Dashboard.</td></tr>
</table>

**Use Case #4**



<table><tr><th colspan="1" valign="top"><b>UC ID</b></th><th colspan="2" valign="top">UC#4</th></tr>
<tr><td colspan="1" valign="top"><b>Use case Name</b></td><td colspan="2" valign="top"><b>check_availability</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2" valign="top">The Vh caretaker will be able to check the current occupancy of VH.</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="2" valign="top">Vh caretaker</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2" valign="top">Vhcaretakere should be logged in.</td></tr>
<tr><td colspan="1" rowspan="5" valign="top"><b>Main Flow</b></td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">The Vh caretaker clicks on the room availability button from their dashboard.</td></tr>
<tr><td colspan="1">2</td><td colspan="1">The system generates a form showing the option start date and end date.</td></tr>
<tr><td colspan="1" valign="top">3</td><td colspan="1" valign="top">The Vh caretaker selects starting date and ending date for history occupancy viewing.</td></tr>
<tr><td colspan="1" valign="top">4</td><td colspan="1" valign="top">The Vh caretaker submits by clicking a button.</td></tr>
<tr><td colspan="1" valign="top">5</td><td colspan="1" valign="top">The required booking details are displayed.</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="2" valign="top">The system returns to its initial condition.</td></tr>
<tr><td colspan="1" valign="top"><b>Alternate Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1"><b>Sub Flow</b></td><td colspan="2">NIL</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1" valign="top">GA 1</td><td colspan="1" valign="top">The Vh caretaker can ‘cancel’ the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1"></td><td colspan="1"><b>Post-condition –</b> The system returns to the Vh caretaker Dashboard.</td></tr>
</table>

**Use Case #5****
<table><tr><th colspan="1"><b>UC ID</b></th><th colspan="2">UC#5</th></tr>
<tr><td colspan="1"><b>Use case Name</b></td><td colspan="2"><b>allot_rooms</b></td></tr>
<tr><td colspan="1"><b>Description</b></td><td colspan="2">The caretaker will allot rooms according to the availability .</td></tr>
<tr><td colspan="1"><b>Actor</b></td><td colspan="2">Caretaker</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2" valign="top"><p>The caretaker</p><p>must be logged in.</p><p>The Intender should have applied for booking. Rooms should be available.</p></td></tr>
<tr><td colspan="1" rowspan="5" valign="top"><b>Main Flow</b></td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">The caretaker selects option booking to view booking requests.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1" valign="top">The system generates a list displaying the pending booking requests.</td></tr>
<tr><td colspan="1" valign="top">3</td><td colspan="1" valign="top">The caretaker selects a booking request.</td></tr>
<tr><td colspan="1" valign="top">4</td><td colspan="1" valign="top">The caretaker allots rooms according to the request and availability from the list of available rooms. [A1]</td></tr>
<tr><td colspan="1" valign="top">5</td><td colspan="1" valign="top">The caretaker forwards the request to the incharge.</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="2" valign="top">Room is allocated to the Intender.</td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Alternate Flow</b></td><td colspan="1" valign="top">A1</td><td colspan="1" valign="top">The VH In-charge cancels the application mentioning the remark.</td></tr>
<tr><td colspan="1"></td><td colspan="1"><b>Post-Condition:</b> Intender will get notification about cancellation of application.</td></tr>
<tr><td colspan="1" valign="top">A2</td><td colspan="1" valign="top">The caretaker does not confirm by clicking on cancel button.</td></tr>
<tr><td colspan="1"></td><td colspan="1"><b>Post-condition:</b> The system does not allot rooms and returns to booking requests list.</td></tr>
<tr><td colspan="1"><b>Sub Flow</b></td><td colspan="2">NIL</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1">GA1</td><td colspan="1">The VH In-charger can cancel the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top">The Intender can cancel the procedure at any time by exercising such an option</td></tr>
</table>

**Use Case #6**



<table><tr><th colspan="1" valign="top"><b>UC ID</b></th><th colspan="2" valign="top">UC#6</th></tr>
<tr><td colspan="1" valign="top"><b>Use case Name</b></td><td colspan="2" valign="top"><b>cancel_booking</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2" valign="top">VH Caretaker will be able to cancel any booking of room(s) in VH with remarks</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="2" valign="top">VH Caretaker</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2" valign="top">There should be a pre-booked room in VH.</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Main Flow</b></td><td colspan="1">1</td><td colspan="1">The VH Caretaker selects a booking to be canceled from the list of booked rooms.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1" valign="top">Caretaker cancels the selected booking by clicking on a button.</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="2" valign="top">Canceled booking will be reflected in the system and notification will be sent to the concerned Intender.</td></tr>
<tr><td colspan="1" valign="top"><b>Alternate Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1">GA1</td><td colspan="1">The VH Caretaker can ‘cancel’ the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the VH In-charge’s Dashboard.</td></tr>
</table>


**Use Case #7**



<table><tr><th colspan="1"><b>UC ID</b></th><th colspan="2">UC#7</th></tr>
<tr><td colspan="1"><b>Use case Name</b></td><td colspan="2" valign="top"><b>manage_guest_check_in</b></td></tr>
<tr><td colspan="1"><b>Description</b></td><td colspan="2">VH Caretaker will be able to mark the check in status of a booked VH room.</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="2" valign="top">VH Caretaker</td></tr>
<tr><td colspan="1"><b>Precondition</b></td><td colspan="2">VH Caretaker must be logged in.</td></tr>
<tr><td colspan="1" rowspan="5" valign="top"><b>Main Flow</b></td><td colspan="1">1</td><td colspan="1">VH Caretaker clicks on the check in button from his dashboard.</td></tr>
<tr><td colspan="1">2</td><td colspan="1">The system will generate the list of guests having current booking and not checked in yet.</td></tr>
<tr><td colspan="1">3</td><td colspan="1">The VH Caretaker selects the name of the guest and fills the check in time and date.</td></tr>
<tr><td colspan="1">4</td><td colspan="1">The system asks for confirmation.</td></tr>
<tr><td colspan="1">5</td><td colspan="1">The VH Caretaker clicks on the confirm button. [A1]</td></tr>
<tr><td colspan="1"><b>Post conditions</b></td><td colspan="2">System reflects the modified details regarding room status.</td></tr>
<tr><td colspan="1" valign="top"><b>Alternate Flow</b></td><td colspan="1" valign="top">A1</td><td colspan="1" valign="top">The VH Caretaker clicks cancel.</td></tr>
<tr><td colspan="1"><b>Sub Flow</b></td><td colspan="1"></td><td colspan="1">The system updates the database and marks the room as occupied.</td></tr>
<tr><td colspan="1" rowspan="2"><b>Global Alternate Flow</b></td><td colspan="1">GA1</td><td colspan="1">The VH Caretaker can ‘cancel’ the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the VH Caretaker’s Dashboard.</td></tr>
</table>

**Use Case #8**



<table><tr><th colspan="1"><b>UC ID</b></th><th colspan="2">UC#8</th></tr>
<tr><td colspan="1"><b>Use case Name</b></td><td colspan="2"><b>manage_guest_check_out</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2">VH Caretaker will be able to initiate the process of checkout on the system regarding bill clearance and room status update.</td></tr>
<tr><td colspan="1"><b>Actor</b></td><td colspan="2">VH Caretaker</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2">Guests have checked-in at VH. VH Caretaker must be logged in.</td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Main Flow</b></td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">VH Caretaker clicks on the checkout button from his dashboard.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1" valign="top">The system generates the lists of guests currently present at VH.</td></tr>
<tr><td colspan="1">3</td><td colspan="1">The VH Caretaker selects the Guest name and click on the checkout button. [A1]</td></tr>
<tr><td colspan="1" valign="top">4</td><td colspan="1" valign="top">UC#10 will be exercised.</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="2" valign="top">System reflects the modified details regarding room status and account.</td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Alternate Flow</b></td><td colspan="1" valign="top">A1</td><td colspan="1" valign="top">VH Caretaker canceled the checkout request.</td></tr>
<tr><td colspan="1"></td><td colspan="1"><b>Post-condition</b> – The system returns to the employee ‘Dashboard’ – initial screen.</td></tr>
<tr><td colspan="1" valign="top">A2</td><td colspan="1" valign="top">The head chooses not to confirm.</td></tr>
<tr><td colspan="1"></td><td colspan="1"><b>Post-condition –</b> The system displays the form with the data filled in so far.</td></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b></td><td colspan="1" valign="top">S1</td><td colspan="1" valign="top">System marks the corresponding room empty.</td></tr>
</table>



<table><tr><th colspan="1" rowspan="2"><b>Global Alternate Flow</b></th><th colspan="1" valign="top">GA1</th><th colspan="1" valign="top">The VH Caretaker can ‘cancel’ the procedure at any time by exercising such an option</th></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the VH Caretaker’s Dashboard.</td></tr>
</table>

**Use Case #9**



<table><tr><th colspan="1" valign="top"><b>UC ID</b></th><th colspan="2" valign="top">UC#9</th></tr>
<tr><td colspan="1" valign="top"><b>Use case Name</b></td><td colspan="2" valign="top"><b>manage_bill_settlement</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2" valign="top">VH Caretaker sees if the bill is paid by intender/guest. He collects the money according to the bill and updates the system accordingly.</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="2" valign="top">VH Caretaker</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2" valign="top"><p>Guests have checked-in at VH.</p><p>VH Caretaker must be logged in.</p><p>The VH Caretaker must be at the Check Out interface.</p></td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Main Flow</b></td><td colspan="1">1</td><td colspan="1">VH Caretaker clicks on the Generate bill button.</td></tr>
<tr><td colspan="1">2</td><td colspan="1">System generates the bill containing meal charges, room charges.</td></tr>
<tr><td colspan="1">3</td><td colspan="1">VH Caretaker selects the mode of payment(intender/guest/institute) from the checkbox.</td></tr>
<tr><td colspan="1">4</td><td colspan="1">VH Caretaker updates the system about the payment. [S1]</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="2" valign="top">System reflects the payment details.</td></tr>
<tr><td colspan="1" valign="top"><b>Alternate Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1"><b>Sub Flow</b></td><td colspan="1" valign="top">S1</td><td colspan="1" valign="top">System updates the VH Account.</td></tr>
<tr><td colspan="1" rowspan="2"><b>Global Alternate Flow</b></td><td colspan="1" valign="top">GA1</td><td colspan="1" valign="top">The VH Caretaker can ‘cancel’ the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the VH Caretaker’s Dashboard.</td></tr>
</table>

**Use Case #10**



<table><tr><th colspan="1" valign="top"><b>UC ID</b></th><th colspan="2" valign="top">UC#10</th></tr>
<tr><td colspan="1" valign="top"><b>Use case Name</b></td><td colspan="2" valign="top"><b>manage_inventory</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2" valign="top">VH Caretaker will be able to manage the inventory of the VH.</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="2" valign="top">VH Caretaker</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2" valign="top">The VH Caretaker should be logged in.</td></tr>
<tr><td colspan="1" rowspan="3" valign="top"><b>Main Flow</b></td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">Screen will show the inventory items with different categories consumable and non consumable..</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1" valign="top">The VH Caretaker will set the threshold levels of stock items. [A1] [A2]</td></tr>
<tr><td colspan="1" valign="top">3</td><td colspan="1" valign="top">System alerts will be generated for items below threshold.</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="2" valign="top">The inventory will be in a consistent state.</td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Alternate Flow</b></td><td colspan="1" valign="top">A1</td><td colspan="1" valign="top">VH Caretaker will add items to inventory.</td></tr>
<tr><td colspan="1"></td><td colspan="1"><b>Post-condition</b> – The inventory will be now updated and in a consistent state.</td></tr>
<tr><td colspan="1" valign="top">A2</td><td colspan="1" valign="top">VH Caretaker selects for update_consumption(UC#16).</td></tr>
<tr><td colspan="1"></td><td colspan="1"><b>Post-condition –</b> The inventory will be now updated and in a consistent state.</td></tr>
</table>



<table><tr><th colspan="1"><b>Sub Flow</b></th><th colspan="1"></th><th colspan="1">The employee is notified with the head’s action as the status update of the application</th></tr>
<tr><td colspan="1" rowspan="2"><b>Global Alternate Flow</b></td><td colspan="1">GA1</td><td colspan="1">The VH Caretaker can ‘cancel’ the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the VH Caretaker’s Dashboard.</td></tr>
</table>

**Use Case #11**



|**UC ID**|UC#11||
| - | - | :- |
|**Use case Name**|**get\_low\_on\_stock\_alerts**||
|**Description**|VH Caretaker will get alerts when any inventory item quantity falls below a pre-decided threshold.||
|**Actor**|VH Caretaker||
|**Precondition**|VH Caretaker has logged in.||
|**Main Flow**|1|System generates an alert when there is a shortage of any inventory item.|
|**Post conditions**|The VH Caretaker is notified.||
|**Alternate Flow**|NIL||
|**Sub Flow**|NIL||
|**Global Alternate Flow**|NIL||

**Use Case #12**



<table><tr><th colspan="1" valign="top"><b>UC ID</b></th><th colspan="2" valign="top">UC#12</th></tr>
<tr><td colspan="1" valign="top"><b>Use case Name</b></td><td colspan="2" valign="top"><b>update_consumption</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2" valign="top">The VH Caretaker will periodically update the system with the quantity of items consumed.</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="2" valign="top">VH Caretaker</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2" valign="top">VH Caretaker must be logged in.</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Main Flow</b></td><td colspan="1">1</td><td colspan="1">The VH caretaker will select an item from the inventory list.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1" valign="top">The VH Caretaker will update the quantity consumed.</td></tr>
<tr><td colspan="1"><b>Post conditions</b></td><td colspan="2">The system is now updated and consistent.</td></tr>
<tr><td colspan="1" valign="top"><b>Alternate Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1">GA1</td><td colspan="1">The VH Caretaker can ‘cancel’ the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the VH Caretaker’s Dashboard.</td></tr>
</table>

**Use Case #13****



<table><tr><th colspan="1" valign="top"><b>UC ID</b></th><th colspan="2" valign="top">UC#13</th></tr>
<tr><td colspan="1" valign="top"><b>Use case Name</b></td><td colspan="2" valign="top"><b>manage_noTurnUp</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2" valign="top">The system will notify VH Caretaker/VH In-charge about guests who didn’t turn up. The VH Caretaker can take actions as deemed fit.</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="2" valign="top">VH Caretaker</td></tr>
<tr><td colspan="1"><b>Precondition</b></td><td colspan="2">VH Caretaker should be logged in.</td></tr>
<tr><td colspan="1" rowspan="3" valign="top"><b>Main Flow</b></td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">System will generate an alert for the VH Caretaker about no turn up of guests.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1" valign="top">VH Caretaker will confirm such situations through the Intender.</td></tr>
<tr><td colspan="1" valign="top">3</td><td colspan="1" valign="top">VH Caretaker exercises UC#6. [A2]</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="2" valign="top">System is now updated and consistent.</td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Alternate Flow</b></td><td colspan="1">A1</td><td colspan="1">VH In-charge will ask VH Caretaker to update (cancel or retain) the system accordingly.</td></tr>
<tr><td colspan="1"></td><td colspan="1"><b>Post-Condition:</b> System is now updated and consistent.</td></tr>
<tr><td colspan="1" valign="top">A2</td><td colspan="1" valign="top">The VH Caretaker does nothing.</td></tr>
<tr><td colspan="1"></td><td colspan="1"><b>Post-condition –</b> The system does not cancel the booking.</td></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1" valign="top"><b>Global Alternate Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
</table>

**Use Case #14**



<table><tr><th colspan="1" valign="top"><b>UC ID</b></th><th colspan="2" valign="top">UC#13</th></tr>
<tr><td colspan="1" valign="top"><b>Use case Name</b></td><td colspan="2" valign="top"><b>view_bookings</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2" valign="top">The VH In-charge will be able to check the booking history and current occupancy of VH.</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="2" valign="top">VH In-charge</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2" valign="top">VH In-charge should be logged in.</td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Main Flow</b></td><td colspan="1">1</td><td colspan="1">The VH in-charge click on view booking button from their dashboard.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1" valign="top">The system generates a form showing the option start date and end date.</td></tr>
<tr><td colspan="1" valign="top">3</td><td colspan="1" valign="top">The VH In-charge selects starting date and ending date for history and occupancy viewing.</td></tr>
<tr><td colspan="1">5</td><td colspan="1">The required booking details are displayed.</td></tr>
<tr><td colspan="1"><b>Post conditions</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1" valign="top"><b>Alternate Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1" valign="top">GA1</td><td colspan="1" valign="top">The VH In-charge can ‘cancel’ the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the VH In-charge’s Dashboard.</td></tr>
</table>

**Use Case #15****
<table><tr><th colspan="1" valign="top"><b>UC ID</b></th><th colspan="2" valign="top">UC#14</th></tr>
<tr><td colspan="1" valign="top"><b>Use case Name</b></td><td colspan="2" valign="top"><b>confirm_booking</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2" valign="top">VH In-Charge will grant the confirmation of the booking after verifying the information provided in the application.</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="2" valign="top">VH In-Charge</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2" valign="top"><p>VH In-Charge has logged in.</p><p>VH In-Charge has received application(s) to book rooms in VH.</p></td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Main Flow</b></td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">VH In-charge opens the application and verifies the details.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1" valign="top">VH In-charge confirms the booking. [A1]</td></tr>
<tr><td colspan="1"><b>Post conditions</b></td><td colspan="2">VH In-Charge has responded to the booking request by the stakeholder.</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Alternate Flow</b></td><td colspan="1">A1</td><td colspan="1">VH In-charge finds discrepancies in the application and rejects it with remarks.</td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-Condition:</b> Intender is notified about the cancellation of application.</td></tr>
<tr><td colspan="1"><b>Sub Flow</b></td><td colspan="2">NIL</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1" valign="top">GA1</td><td colspan="1" valign="top">The VH In-charge can ‘cancel’ the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the VH In-charges’s Dashboard.</td></tr>
</table>

**Use Case #16**



<table><tr><th colspan="1" valign="top"><b>UC ID</b></th><th colspan="2" valign="top">UC#16</th></tr>
<tr><td colspan="1" valign="top"><b>Use case Name</b></td><td colspan="2" valign="top"><b>reject_booking</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="2" valign="top">VH In-charge will be able to reject any booking of room(s) in VH with remarks</td></tr>
<tr><td colspan="1" valign="top"><b>Actor</b></td><td colspan="2" valign="top">VH In-charge</td></tr>
<tr><td colspan="1" valign="top"><b>Precondition</b></td><td colspan="2" valign="top">There should be a pre-booked room in VH.</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Main Flow</b></td><td colspan="1">1</td><td colspan="1">The VH In-charge selects a booking to be canceled from the list of alloted rooms.</td></tr>
<tr><td colspan="1">2</td><td colspan="1">VH In-charge cancels the selected booking by clicking on a button.</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="2" valign="top">Canceled booking will be reflected in the system and notification will be sent to the concerned Intender.</td></tr>
<tr><td colspan="1" valign="top"><b>Alternate Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1" valign="top"><b>Sub Flow</b></td><td colspan="2" valign="top">NIL</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1" valign="top">GA1</td><td colspan="1" valign="top">The VH In-charge can ‘cancel’ the procedure at any time by exercising such an option</td></tr>
<tr><td colspan="1"></td><td colspan="1" valign="top"><b>Post-condition –</b> The system returns to the VH In-charge’s Dashboard.</td></tr>
</table>

**Use Case #17****
<table><tr><th colspan="1" valign="bottom"><b>UC ID</b></th><th colspan="3" valign="bottom">UC#17</th></tr>
<tr><td colspan="1" valign="bottom"><b>Use case Name</b></td><td colspan="3" valign="bottom"><b>mange_booking</b></td></tr>
<tr><td colspan="1" valign="top"><b>Description</b></td><td colspan="3" valign="top">The "Manage Booking" use case allows the caretaker of the college hostel to review, approve, reject, edit, cancel, and view booking requests for the visitor hostel through the Fusion portal.</td></tr>
<tr><td colspan="1" valign="bottom"><b>Actor</b></td><td colspan="3" valign="bottom">VH Caretaker</td></tr>
<tr><td colspan="1" valign="bottom"><b>Precondition</b></td><td colspan="3" valign="bottom">The caretaker is logged in into the system.</td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Main Flow</b></td><td colspan="1" valign="bottom">1</td><td colspan="2" valign="bottom">The Caretaker navigates to the "Manage Booking" section.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="2" valign="top">The system displays the list of bookings with its respective status.</td></tr>
<tr><td colspan="1" valign="bottom">3</td><td colspan="2" valign="bottom">The Caretaker selects a booking request to review. [A1][A2]</td></tr>
<tr><td colspan="1" valign="top">4</td><td colspan="2" valign="top">The caretaker views the booking information of approved requests. [A3][A4]</td></tr>
<tr><td colspan="1" valign="top"><b>Post conditions</b></td><td colspan="3" valign="top">The updated booking information is reflected in the database.</td></tr>
<tr><td colspan="1" rowspan="4" valign="top"><b>Alternate Flow</b></td><td colspan="1" rowspan="2" valign="top">A1</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">The request is pending. The Caretaker selects the "Approve" action.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1" valign="top">The system updates the booking status to "Approved" and the same is reflected to the Intender.</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">A2</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">The Caretaker selects the "Reject" action citing the reason for rejection.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1" valign="top">The system updates the booking status to rejected and the same is reflected to the Intender.</td></tr>
</table>




<table><tr><th colspan="1" valign="bottom"><b>UC ID</b></th><th colspan="3" valign="bottom">UC#17</th></tr>
<tr><td colspan="1" valign="bottom"><b>Use case Name</b></td><td colspan="3" valign="bottom"><b>mange_booking</b></td></tr>
<tr><td colspan="1" rowspan="5"></td><td colspan="1" rowspan="2" valign="top">A3</td><td colspan="1" valign="top">1</td><td colspan="1" valign="top">The caretaker edits the booking details, like booking date, Intender details etc.</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">2</td><td colspan="1" rowspan="2" valign="top">The edited information is updated in the database and the same is reflected to the Intender as well.</td></tr>
<tr><td colspan="1" rowspan="3" valign="top">A4</td></tr>
<tr><td colspan="1" valign="top">1</td><td colspan="1" valign="bottom">The caretaker selects the cancel booking options specifying the reason for cancellation.</td></tr>
<tr><td colspan="1" valign="top">2</td><td colspan="1" valign="top">The system updates the booking status of that booking to “cancelled” and the same is reflected to the Intender as well.</td></tr>
<tr><td colspan="1" valign="bottom"><b>Sub Flow</b></td><td colspan="3" valign="bottom">NIL</td></tr>
<tr><td colspan="1" rowspan="2" valign="top"><b>Global Alternate Flow</b></td><td colspan="1" valign="top">GA1</td><td colspan="2" valign="top">The VH Caretaker can ‘cancel’ the procedure at any time by exercising such an option and will be directed to the dashboard.</td></tr>
<tr><td colspan="1" valign="top">GA2</td><td colspan="2" valign="bottom">If a technical error occurs during the execution of any action (e.g., database failure, server issues), the system displays an error message and logs the incident.</td></tr>
</table>

## User Flow


### 3.3 Other Functional Requirements

1. This module will make use of the **communication module** for sending notifications and alerts to various actors involved in the module, suitably for booking confirmations, rejections, or modifications.

2. Automated email or SMS notifications will be provided for booking confirmations, rejections, or modifications.

3. Alerts for critical inventory levels and other important updates will be generated.

4. The **Super Admin** of Fusion should be able to assign roles for VH In-Charge and VH Caretaker.

5. The system should be able to deal with offline bookings.

6. Category conversion of visitors may be possible, subject to the approval of the competent authority.

7. Changes in the tariff may occur from time to time based on the decisions of the institute authorities.

---

### 3.4 Other Constraints

#### 3.4.1 User Interfaces

- The user interface should comply with the color scheme and dashboard design of FUSIONIIIT.
- Users should be able to navigate seamlessly from one functionality to another.
- Inter-module navigation should be smooth, with all functionalities easy to use, requiring no specific training for module usage.

#### 3.4.2 Tech Stack Used

The project's tech stack comprises various libraries, including:

- **AMQP 5.0.2** for messaging
- **BeautifulSoup4 4.9.3** for web scraping
- **Django 3.1.5** as the core framework
- **Cryptography 36.0.2** for security
- **Django Allauth 0.44.0** and **Django CORS Headers 3.7.0** for additional Django functionalities
- Development tools like **Django Debug Toolbar 3.2.4** and **Django REST Framework 3.12.2** for debugging and API development
- External libraries such as **NumPy 1.22.3**, **Psycopg2-binary 2.8.6**, and **Requests 2.25.1** for data manipulation, database connectivity, and web request handling.

These components collectively form a comprehensive and efficient tech stack for the project, with each library contributing to the overall functionality and efficiency across different domains.

#### 3.4.3 Business Rules (if any)

1. The room booking and billing shall be done based on the category of the visitor (see the existing rule set for the same).

---

### 4. Non-Functional Requirements

#### 4.1 Performance

- The system should respond quickly to user interactions, with minimal response time for booking actions, inventory updates, and notifications.

#### 4.2 Scalability

- The system should handle a mass of concurrent users, with performance evaluated under increasing load conditions.

#### 4.3 Availability

- The system should be available **99.9%** of the time.

#### 4.4 Security

- Ensure data confidentiality and integrity. Role-based authorization should ensure that users can only perform actions relevant to their designated roles.

---

### 5. Module Dependencies with Other Fusion Modules

#### 5.1 UI Level

- **Color Scheme and Dashboard Design:** The UI should adhere to the established FUSION IIIT style guide for a consistent user experience. Navigation through different functionalities should be intuitive and effortless. Inter-module transitions should be seamless and user-friendly.
- **Dashboard Interface:** The dashboard interface should be similar to the interface of the home page, with well-defined connectivity.
- **Accessibility:** The UI should be accessible to users with disabilities, following WCAG guidelines.
- **Responsive Design:** The UI should adapt to different screen sizes and devices for optimal viewing and interaction.

#### 5.2 DB Level Dependencies

- **Data Schema:** The database schema should efficiently store and retrieve visitor hostel booking data, including room availability, inventory levels, user roles, and booking history.
- **Database Registration:** The database should be based on the registration and availability of the stocks.
- **Data Integrity:** Data validation and error handling mechanisms should be implemented to ensure data accuracy and consistency.
- **Database Performance:** The database should be optimized for fast retrieval and update operations, particularly during peak booking periods.

#### 5.3 Module Level Dependencies

- **Module Level Dependencies:** Defines the intra-level dependencies in the module.
- **Communication Module:** Integration with the existing communication module is required for sending email and SMS notifications about booking confirmations, rejections, or modifications.
- **Workflow Engine:** A workflow engine may be utilized to automate task execution and manage approval processes for complex booking scenarios.


## UI for Web
same ui as app 
above given is combined of app and web

## Database Schema
### Module Name: Visitor Hostel Module

**Faculty Mentor:** Prof. Sraban Kumar Mohanty  
**Student Mentor:** Deepanshu Kumar (21BCS072)

### Team Members
- Avneesh Dayal (21BCS046)
- Azemera Vishnu Nayak (21BCS051)
- Sahil Chauksey (21BCS181)
- Sparsh Ranjan (21BCS205)
- Varun Raj (21BCS236)

---

### Database Documentation of [OS1 - Visitor Hostel Module] 4.0

### Overview of the Module

#### SRS
[Software Requirements Specification (SRS)](https://docs.google.com/document/d/14WZh8l8T8z2mtlWU4mQ7FvhPILYn098C/edit?usp=drive_link&ouid=118421111030779763003&rtpof=true&sd=true)

---

### A. ER Diagram

![ER Diagram](assets/Aspose.Words.0d1409c4-816a-4585-864d-3187d8754c72.001.jpeg)

[View ER Diagram](https://drive.google.com/file/d/1n7_3c8hHPh4B1F-oyvBF3PrmJWkIxj7p/view)

---

### B. Database Schema

[View Database Schema](https://docs.google.com/spreadsheets/d/1Su3ap2mt32KQqCzuvUQheOCXWebTRaZd/edit#gid=1327478253)

---



#### Tables and Relationships

|**Table Name**|**Attribute Name**|**Attribute Data Type**|**Purpose**|<p>**Table Current Status (Local / Global)**</p><p>**(Local if the table is used only in current**</p><p>**module and Global if used in more than one**</p><p>**modules)**</p>|<p>**Referenced\_Table (Referenced\_Attribute)**</p><p>**(If the attribute is Foreign key then write**</p><p>**Referenced\_tablename(Referenced\_attribute)**</p><p>**otherwise write N/A )**</p>|<p>**Is Redundant (Yes / No)**</p><p>**(An attribute is considered redundant**</p><p>**if it can be derived from any other**</p><p>**attribute or set of attributes)**</p>|**Comments**|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |

<table><tr><th rowspan="6"><b>visitor_hostel_bill</b></th><th valign="bottom"><b>id</b></th><th valign="bottom"><b>INT</b></th><th valign="bottom"><b>Primary key</b></th><th rowspan="6"><b>Local</b></th><th valign="bottom"><b>N/A</b></th><th valign="bottom"><b>No</b></th><th valign="bottom"></th></tr>
<tr><td valign="bottom"><b>meal_bill</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>bill of meal</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>room_bill</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>bill of room</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>payment_status</b></td><td valign="bottom"><b>BOOLEAN</b></td><td valign="bottom"><b>yes or no</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>booking_id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>id of booking</b></td><td valign="bottom"><b>visitor_hostel_bookingdetail (id)</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>caretaker_id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>id of caretaker</b></td><td valign="bottom"><b>auth_user (id)</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td></tr>
<tr><td rowspan="3"><b>visitor_hostel_bill_room</b></td><td valign="bottom"><b>id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>Primary key</b></td><td rowspan="3"><b>Local</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>bill_id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>id of bill</b></td><td valign="bottom"><b>visitor_hostel_bill (id)</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>roomdetail_id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>id of room booked</b></td><td valign="bottom"><b>visitor_hostel_roomdetail (id)</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td></tr>
<tr><td rowspan="24"><b>visitor_hostel_bookingdetail</b></td><td valign="bottom"><b>id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>Primary key</b></td><td rowspan="24"><b>Local</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>visitor_category</b></td><td valign="bottom"><b>VARCHAR (1)</b></td><td valign="bottom"><b>category of visitor</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>modified_visitor_category</b></td><td valign="bottom"><b>VARCHAR (1)</b></td><td valign="bottom"><b>modified category of visitor</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>person_count</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>number of persons</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>purpose</b></td><td valign="bottom"><b>TEXT</b></td><td valign="bottom"><b>purpose of visit</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>booking_from</b></td><td valign="bottom"><b>DATE</b></td><td valign="bottom"><b>date of booking from</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>booking_to</b></td><td valign="bottom"><b>DATE</b></td><td valign="bottom"><b>date of booking to</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>arruval_time</b></td><td valign="bottom"><b>TEXT</b></td><td valign="bottom"><b>time of arrival of visit</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>departure_time</b></td><td valign="bottom"><b>TEXT</b></td><td valign="bottom"><b>time of departure of visit</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>forwarded_date</b></td><td valign="bottom"><b>DATE</b></td><td valign="bottom"><b>date of forwarded visit</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>confirmed_date</b></td><td valign="bottom"><b>DATE</b></td><td valign="bottom"><b>date of confirmed visit</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>check_in</b></td><td valign="bottom"><b>DATE</b></td><td valign="bottom"><b>check in date</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>check_out</b></td><td valign="bottom"><b>DATE</b></td><td valign="bottom"><b>check out date</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>check_in_time</b></td><td valign="bottom"><b>TIME</b></td><td valign="bottom"><b>check in time</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>check_out_time</b></td><td valign="bottom"><b>TIME</b></td><td valign="bottom"><b>check out time</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>status</b></td><td valign="bottom"><b>VARCHAR (15)</b></td><td valign="bottom"><b>status of room booked</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>remark</b></td><td valign="bottom"><b>VARCHAR (40)</b></td><td valign="bottom"><b>remark</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>image</b></td><td valign="bottom"><b>VARCHAR (100)</b></td><td valign="bottom"><b>image</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>number_of_rooms</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>no. of rooms booked</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>number_of_rooms_alloted</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>no. of rooms alloted</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>booking_date</b></td><td valign="bottom"><b>DATE</b></td><td valign="bottom"><b>date of booking</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>bill_to_be_settled_by</b></td><td valign="bottom"><b>VARCHAR (1)</b></td><td valign="bottom"><b>bill to be settled by</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>caretaker_id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>id of caretaker</b></td><td valign="bottom"><b>auth_user (id)</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>intender_id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>id of intender</b></td><td valign="bottom"><b>auth_user (id)</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td></tr>
<tr><td rowspan="3"><b>visitor_hostel_bookingdetail_rooms</b></td><td valign="bottom"><b>id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>Primary key</b></td><td rowspan="3"><b>Local</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>bookingdetail_id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>id of booking</b></td><td valign="bottom"><b>visitor_hostel_bookingdetail (id)</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>roomdetail_id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>id of room booked</b></td><td valign="bottom"><b>visitor_hostel_roomdetail (id)</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td></tr>
<tr><td rowspan="3"><b>visitor_hostel_bookingdetail_visitor</b></td><td valign="bottom"><b>id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>Primary key</b></td><td rowspan="3"><b>Local</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>bookingdetail_id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>id of booking</b></td><td valign="bottom"><b>visitor_hostel_bookingdetail (id)</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>roomdetail_id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>id of room booked</b></td><td valign="bottom"><b>visitor_hostel_visitordetail (id)</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td></tr>
<tr><td rowspan="12"><b>visitor_hostel_inventory</b></td><td valign="bottom"><b>id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>Primary key</b></td><td rowspan="12"><b>Local</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>item_name</b></td><td valign="bottom"><b>VARCHAR (20)</b></td><td valign="bottom"><b>name of item</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>quantity</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>quantity of items</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>consumable</b></td><td valign="bottom"><b>BOOLEAN</b></td><td valign="bottom"><b>yes or no</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>opening_stock</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>no. of opening stock</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>addition_stock</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>no. of addition stock</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>total_stock</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>total no. of stock</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>servicable</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>no. of servicable items</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>non_servicable</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>no. of non servicable items</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>inuse</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>no. of inuse items</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>total_usable</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>total no. of usable items</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>remark</b></td><td valign="bottom"><b>TEXT</b></td><td valign="bottom"><b>remark</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td></tr>
<tr><td rowspan="4"><b>visitor_hostel_inventorybill</b></td><td valign="bottom"><b>id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>Primary key</b></td><td rowspan="4"><b>Local</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>bill_number</b></td><td valign="bottom"><b>VARCHAR (40)</b></td><td valign="bottom"><b>bill number</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>cost</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>cost of bill</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>item_name_id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>id of items</b></td><td valign="bottom"><b>visitor_hostel_inventory (id)</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td></tr>
<tr><td rowspan="11"><b>visitor_hostel_mealrecord</b></td><td valign="bottom"><b>id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>Primary key</b></td><td rowspan="11"><b>Local</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>meal_date</b></td><td valign="bottom"><b>DATE</b></td><td valign="bottom"><b>date of meal booking</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>morning_tea</b></td><td valign="bottom"><b>BOOLEAN</b></td><td valign="bottom"><b>yes or no</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>eve_tea</b></td><td valign="bottom"><b>BOOLEAN</b></td><td valign="bottom"><b>yes or no</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>breakfast</b></td><td valign="bottom"><b>BOOLEAN</b></td><td valign="bottom"><b>yes or no</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>lunch</b></td><td valign="bottom"><b>BOOLEAN</b></td><td valign="bottom"><b>yes or no</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>dinner</b></td><td valign="bottom"><b>BOOLEAN</b></td><td valign="bottom"><b>yes or no</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>persons</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>no. of persons</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>booking_id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>id of booking</b></td><td valign="bottom"><b>visitor_hostel_bookingdetail (id)</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>room_id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>id of room booked</b></td><td valign="bottom"><b>visitor_hostel_roomdetail (id)</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>visitor_id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>id of visitor</b></td><td valign="bottom"><b>visitor_hostel_visitordetail (id)</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td></tr>
<tr><td rowspan="5"><b>visitor_hostel_roomdetail</b></td><td valign="bottom"><b>id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>Primary key</b></td><td rowspan="5"><b>Local</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>room_number</b></td><td valign="bottom"><b>VARCHAR (4)</b></td><td valign="bottom"><b>no. of rooms booked</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>room_type</b></td><td valign="bottom"><b>VARCHAR (12)</b></td><td valign="bottom"><b>type of room booked</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>room_floor</b></td><td valign="bottom"><b>VARCHAR (12)</b></td><td valign="bottom"><b>floor of room booked</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>room_status</b></td><td valign="bottom"><b>VARCHAR (20)</b></td><td valign="bottom"><b>status of room booked</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td rowspan="3"><b>visitor_hostel_roomdetail_visitor</b></td><td valign="bottom"><b>id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>Primary key</b></td><td rowspan="3"><b>Local</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>roomdetail_id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>id of room booked</b></td><td valign="bottom"><b>visitor_hostel_roomdetail (id)</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>visitordetail_id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>id of visitor</b></td><td valign="bottom"><b>visitor_hostel_visitordetail (id)</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td><td valign="bottom"></td></tr>
<tr><td rowspan="7"><b>visitor_hostel_visitordetail</b></td><td valign="bottom"><b>id</b></td><td valign="bottom"><b>INT</b></td><td valign="bottom"><b>Primary key</b></td><td rowspan="7"><b>Local</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>visitor_phone</b></td><td valign="bottom"><b>VARCHAR (15)</b></td><td valign="bottom"><b>phone number of visitor</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>visitor_name</b></td><td valign="bottom"><b>VARCHAR (40)</b></td><td valign="bottom"><b>name of visitor</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>visitor_email</b></td><td valign="bottom"><b>VARCHAR (40)</b></td><td valign="bottom"><b>email of visitor</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>visitor_organizataion</b></td><td valign="bottom"><b>VARCHAR (100)</b></td><td valign="bottom"><b>organization of visitor</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>visitor_address</b></td><td valign="bottom"><b>TEXT</b></td><td valign="bottom"><b>address of visitor</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="bottom"></td></tr>
<tr><td valign="bottom"><b>nationality</b></td><td valign="bottom"><b>VARCHAR (20)</b></td><td valign="bottom"><b>nationality of visitor</b></td><td valign="bottom"><b>N/A</b></td><td valign="bottom"><b>No</b></td><td valign="top"></td></tr>
</table>








### C. Changes Required in the Currently Implemented Tables

#### 1. visitor_hostel_bill
- **meal_content**
  - **Action:** Insert the meal_content attribute in the database.
  - **Reason:** Meal content will be required in the future to improve the quality of food and to make meal records tangible. This change is essential.

---

#### 2. visitor_hostel_bill_room
- **name**
  - **Action:** Insert the name attribute in the database of visitor_hostel_bill_room.
  - **Reason:** To make the record more secure and complete, the insertion of the name attribute of the person is required.

- **phone_num**
  - **Action:** Insert the phone_num attribute in the database of visitor_hostel_bill_room.
  - **Reason:** To enhance record security and completeness, the insertion of the phone_num attribute of the person is required.

---

#### 3. visitor_hostel_bookingdetail
- **modified_visitor_category**
  - **Action:** Remove the modified_visitor_category attribute from the database of visitor_hostel_bookingdetail.
  - **Reason:** This is an extra attribute consuming database space; we already have the visitor category for that purpose.

---

#### 4. visitor_hostel_bookingdetail_rooms
- **No changes required.**

---

#### 5. visitor_hostel_bookingdetail_visitor
- **phone_num**
  - **Action:** Insert the phone_num attribute in the database of visitor_hostel_bookingdetail_visitor.
  - **Reason:** To enhance record security and completeness, the insertion of the phone_num attribute of the person is required.

---

#### 6. visitor_hostel_inventory
- **No changes required.**

---

#### 7. visitor_hostel_inventorybill
- **No changes required.**

---

#### 8. visitor_hostel_mealrecord
- **No changes required.**

---

#### 9. visitor_hostel_roomdetail
- **No changes required.**

---

#### 10. visitor_hostel_roomdetail_visitor
- **No changes required.**

---

#### 11. visitor_hostel_visitordetail
- **No changes required.**

---

## D. Data Availability for API and Functional Testing

Currently, we have no database to perform testing as all the tables are empty.

### D.1 Tables That Are Already Populated

1. **visitor_hostel_inventory**
2. **visitor_hostel_inventorybill**
3. **visitor_hostel_roomdetail**
4. **visitor_hostel_visitordetail**
5. **visitor_hostel_roomdetail_visitor**

---

### D.2 Tables Required to Be Populated

1. **visitor_hostel_bill**
2. **visitor_hostel_bill_room**
3. **visitor_hostel_bookingdetail**
4. **visitor_hostel_bookingdetail_rooms**
5. **visitor_hostel_bookingdetail_visitor**
6. **visitor_hostel_mealrecord**

---

### D.3 Difficulties Faced by Your Team Regarding Populating Any Table

1. **Connection to the Backend:** The system you're using is connected to a backend, which restricts your ability to directly add data. This suggests that data addition might be controlled or require specific permissions.
  
2. **Missing Primary Database:** You don't have a primary database available for testing purposes. This makes it difficult to experiment or add data in a safe environment without potentially affecting the actual system.

---

### Additional Note

The following six tables don’t have any data at all:

1. **visitor_hostel_bill**
2. **visitor_hostel_bill_room**
3. **visitor_hostel_bookingdetail**
4. **visitor_hostel_bookingdetail_rooms**
5. **visitor_hostel_bookingdetail_visitor**
6. **visitor_hostel_mealrecord**

### Data Flow
Explanation of how data moves through the system.