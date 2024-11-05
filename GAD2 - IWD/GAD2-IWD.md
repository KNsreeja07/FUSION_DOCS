# Authentication Module Documentation

## Table of Contents
- [User-Centered Design (UCD)](#user-centered-design-ucd)
- [SRS Application](#srs-application)
- [SRS Web Interface](#srs-web-interface)
- [API Specifications](#api-specifications)
- [UI for Application](#ui-for-application)
- [UI for Web](#ui-for-web)
- [Database Schema](#database-schema)

## User-Centered Design (UCD)
- **Overview:** Brief description of UCD in this module.
- **User Personas:** Details about the target users.
- **User Journeys:** Diagrams or descriptions of user interactions.

## SRS Application
- **Functional Requirements:** List and descriptions.
- **Non-Functional Requirements:** Performance, security, etc.

## SRS Web Interface
- **Features:** Detailed features of the web interface.
- **Technical Specifications:** Technologies used, frameworks, etc.

## API Specifications
# GAD-2 IWD Module (Web)

### **Student Mentor**: Kushagra Yadav (21BCS121)

---

## **Overview**

The **IWD Module** in the Fusion ERP system plays a vital role in maintaining and managing campus infrastructure. It handles both the routine upkeep of assets and the construction of new properties, ensuring efficient management and smooth operations across the campus.

The module ensures:
- Swift resolution of any on-site asset malfunctions.
- Coordination of construction and development of new campus properties.

---

## **API Documentation**

### **Implemented APIs**

1. **`/page1_1`**
   - **Parameters**: `aes_file`, `dASAName`, `nitNiqno`, `proth`, `emdDetails`, `preBidDate`, `technicalBidDate`, `financialBidDate`.
   - **Description**: Stores important details related to the work being done and approved requests.

2. **`/page2_1`**
   - **Parameters**: `corrigendum`, `addendum`, `preBid`, `technicalBid`, `qualifiedAgencies`, `financialBid`, `lowAgency`, `letterOfIntent`, `workOrder`, `agreementLetter`, `milestones`.
   - **Description**: Stores the necessary documents and information required for the issued work.

3. **`/corrigendumInput`** (Partially Implemented)
   - **Parameters**: `id`, `issueDate`, `nitNo`, `name`, `lastDate`, `lastTime`, `env1BidOpeningDate`, `env1BidOpeningTime`, `env2BidOpeningDate`, `env2BidOpeningTime`.
   - **Description**: Users can correct errors during the submission of their documents.

4. **`/addendumInput`**
   - **Parameters**: `id`, `issueDate`, `nitNiqNo`, `name`, `openDate`, `openTime`.
   - **Description**: Allows users to submit updated documents.

5. **`/milestoneForm`**
   - **Parameters**: `id`, `description`, `timeAllowed`, `amountWithheld`.
   - **Description**: Timeframe for agencies to resolve payment issues.

6. **`/TechnicalBidForm`**
   - **Parameters**: `id`, `requirements`.
   - **Description**: Lists details and requirements in the bidding process.

7. **`/extensionForm`**
   - **Parameters**: `id`, `hindrance`, `periodOfHindrance`, `periodOfExtension`.
   - **Description**: Agencies can request deadline extensions.

8. **`/letterOfIntent`**
   - **Parameters**: `id`, `nitNiqNo`, `dateOfOpening`, `agency`, `name`, `tenderValue`.
   - **Description**: Communicates agency intent regarding the assigned work.

9. **`/workOrderForm`**
   - **Parameters**: `id`, `issueDate`, `nitNiqNo`, `agency`, `name`, `amount`, `time`, `startDate`, `completionDate`, `deposit`, `contractDay`.
   - **Description**: Submits work order details for assigned tasks.

10. **`/agreement`**
    - **Parameters**: `id`, `date`, `dateOfOpening`, `agencyName`, `workName`, `fdrSum`.
    - **Description**: Formal agreement submission for assigned work.

11. **`/page3_1`**
    - **Parameters**: `id`, `extensionOfTime`, `actualCostOfBidding`.
    - **Description**: Submit details for extension requests.

### **API Views**

1. **`/page1View`** (Partially Implemented)
   - **Description**: Administrator can view details from `page1_1` submissions.

2. **`/page2View`**
   - **Description**: Administrator can view details from `page2_1` submissions.

3. **`/page3View`**
   - **Description**: Administrator can view details from `page3_1` submissions.

4. **`/extensionFormView`**
   - **Description**: Administrator can view details from `extensionForm`.

5. **`/workOrderFormView`**
   - **Description**: Administrator can view details from `workOrderForm`.

6. **`/letterOfIntentFormView`**
   - **Description**: Administrator can view details from `letterOfIntent`.

7. **`/preBidDetailsFormView`**
   - **Description**: Administrator can view details from the pre-bid form.

---

## **APIs Under Development**

1. **`/create_new_request`** (UC#1)  
   - **Description**: Users can create new requests for maintenance or construction.  
   - **Database**: Not yet created.

2. **`/forward_complaints`** (UC#10)  
   - **Description**: Forward complaints to higher authorities.  
   - **Database**: Not yet created.

3. **`/process_request`** (UC#5)  
   - **Description**: Dean processes the user request.  
   - **Database**: Not yet created.

4. **`/audit_final_bill`** (UC#4)  
   - **Description**: Dean audits the final bill submitted by the agency.  
   - **Database**: Not yet created.

5. **`/approve_reject_request`** (UC#6)  
   - **Description**: Director approves or rejects the processed request.  
   - **Database**: Not yet created.

6. **`/audit_document`** (UC#7)  
   - **Description**: Auditor reviews and requests corrections on user-submitted documents.  
   - **Database**: Not yet created.

7. **`/settle_bill`** (UC#8)  
   - **Description**: Account admin processes bill settlement.  
   - **Database**: Not yet created.

8. **`/manage_inventory`** (UC#9)  
   - **Description**: IWD admin manages and ensures availability of resources.  
   - **Database**: Not yet created.

---

## **Use Case Diagram**


![GAD-2 IWD Use Case Diagram](assets/GAD-2_UCD.jpg)



---

## **Current Issues**

- The use case diagram was recently updated, and many specified use cases are yet to be implemented.

---

**Google Doc Link**: [Modules Testing Assignment](https://docs.google.com/document/d/1YHGPKiRUQ0TMEIk8w4HZ7sWOhSeqEkCdI3leq7ubZ_k/edit?usp=sharing)

## UI for Application
- **Design Principles:** Guidelines followed.
- **Screenshots:** Embedded images with descriptions.
- **User Flow:** How users navigate the application.

## UI for Web
- **Design Elements:** Colors, typography, etc.
- **Responsive Design:** How UI adapts to different devices.
- **Accessibility:** Compliance with accessibility standards.

## Database Schema
- **ER Diagrams:** Visual representation of the database.
- **Tables and Relationships:** Detailed descriptions.
- **Data Flow:** How data moves through the system.
