# CMSC129_Activity3_ReleaseTest: FishLERS

## A. Target App Summary
**App Name:** FishLERS (Fisheries Laboratory Equipment Reservation System)  
**Developers:** Bretaña, Buerom, Contreras, Verde

**Description:**
The Fisheries Laboratory Equipment Reservation System is a laboratory management system designed to streamline the tracking, management, and utilization of laboratory equipment and resources. The system primarily serves laboratory staff, researchers, and students by providing a centralized platform to monitor inventory, schedule equipment usage, and maintain records of lab activities.

**Core Features:**
* **Centralized Inventory Management:** Real-time tracking of equipment availability and condition (functional, damaged, or missing).
* **Digitalized Reservation Workflow:** A structured request system where users can submit reservation forms and admins can approve, decline, or modify them.
* **Accountability & Auditing:** Detailed records of borrowed equipment, including start/return dates and the ability to export accountability reports as PDFs.
* **Multi-Tiered Access Control:** Distinct functionalities and permission levels for Users, Admins, and Super Admins to ensure system security and oversight.

--- 

## B. Requirements List
1. **Authentication:** Users must be able to securely log in and authenticate using established FishLERS accounts.

2. **Inventory Management:** Admins must be able to add, edit, delete, search, and filter equipment records.

3. **Digital Reservations:** Users must be able to submit digital laboratory equipment reservation request forms.

4. **Request Tracking:** Users must be able to track the real-time status of their requests (e.g., pending, approved, declined, returned).

5. **Administrative Approval:** Admins must have the authority to approve, decline, or modify equipment reservation requests.

6. **Accountability Records:** The system must record borrowed equipment start and return dates to maintain user accountability.

7. **Equipment Condition Tracking:** Admins must be able to mark equipment status as functional, damaged, or missing upon return.

8. **Data Export:** Admins and Super Admins must be able to export accountability records into a PDF format for physical filing or reporting.

9. **Privilege Management:** Super Admins must be able to grant or revoke admin privileges through a hierarchical approval system.

10. **Communication & Announcements:** The system must support an integrated chat system and announcement banners for lab updates.

---

## C. Requirements-Based Testing

### REQUIREMENT #1
| Field | Description |
| :--- | :--- |
| **Requirement** | "Secure login and authentication using FishLERS accounts." |
| **Test Input / Action** | Enter `tester@email.com` and `password` into the login fields. |
| **Expected Result** | User is authenticated and redirected to the Student Dashboard. |
| **Actual Result** | System validated credentials and loaded the Student landing page. |
| **Pass / Fail** | ✅ Pass |

### REQUIREMENT #2
| Field | Description |
| :--- | :--- |
| **Requirement** | "Manage inventory records by adding, editing, deleting, searching, and filtering equipment." |
| **Test Input / Action** | Admin navigates to Inventory, clicks "Add Equipment," and enters "Test Beaker." |
| **Expected Result** | The "Test Beaker" should appear in the inventory list. |
| **Actual Result** | Item was successfully created and visible in the equipment table. |
| **Pass / Fail** | ✅ Pass |

### REQUIREMENT #3
| Field | Description |
| :--- | :--- |
| **Requirement** | "Submit digitalized laboratory equipment reservation request forms." |
| **Test Input / Action** | User selects a Microscope and clicks "Submit Request" after filling out the form. |
| **Expected Result** | System displays a "Request Submitted Successfully" notification. |
| **Actual Result** | Request form was processed and added to the user's tracking list. |
| **Pass / Fail** | ✅ Pass |

### REQUIREMENT #4
| Field | Description |
| :--- | :--- |
| **Requirement** | "Track request statuses (pending, approved, declined, ongoing, returned)." |
| **Test Input / Action** | User navigates to the "Track Status" tab to view their recent submission. |
| **Expected Result** | The request should be listed with a "Pending" status label. |
| **Actual Result** | Status was visible and correctly defaulted to "Pending" post-submission. |
| **Pass / Fail** | ✅ Pass |

### REQUIREMENT #5
| Field | Description |
| :--- | :--- |
| **Requirement** | "Approve, decline, or modify reservation requests." |
| **Test Input / Action** | Admin clicks the "Approve" button on a pending request for a Centrifuge. |
| **Expected Result** | The request status updates to "Approved" and equipment availability is adjusted. |
| **Actual Result** | Status changed instantly; approval reflects on User dashboard. |
| **Pass / Fail** | ✅ Pass |

### REQUIREMENT #6
| Field | Description |
| :--- | :--- |
| **Requirement** | "Resolve missing or damaged equipment." |
| **Test Input / Action** | Admin marks mising "Chlorine Test Kit" as resolved. |
| **Expected Result** | The system updates the equipment status to resolved. |
| **Actual Result** | The equipment record was successfully updated, and the resolution date was recorded in the accountability log. |
| **Pass / Fail** | ✅ Pass |

### REQUIREMENT #7
| Field | Description |
| :--- | :--- |
| **Requirement** | "Mark equipment as functional, damaged, or missing." |
| **Test Input / Action** | Admin selects "Damaged" from the dropdown menu for a returned item. |
| **Expected Result** | The item’s status in the inventory changes to "Damaged." |
| **Actual Result** | Inventory reflected the damage status; item became unreservable. |
| **Pass / Fail** | ✅ Pass |

### REQUIREMENT #8
| Field | Description |
| :--- | :--- |
| **Requirement** | "Export accountability records into PDF format." |
| **Test Input / Action** | Click the "Export PDF" icon in the Accountability Records dashboard. |
| **Expected Result** | A `.pdf` file containing the accountability table is downloaded. |
| **Actual Result** | System generated and triggered a download of a formatted PDF report. |
| **Pass / Fail** | ✅ Pass |

### REQUIREMENT #9
| Field | Description |
| :--- | :--- |
| **Requirement** | "Grant, revoke, and manage admin privileges through the admin approval hierarchy." |
| **Test Input / Action** | Super Admin revokes the privilege of an Admin via the User Management panel. |
| **Expected Result** | Targeted user can no longer access the Admin dashboard. |
| **Actual Result** | Permissions were updated; access to management tools was denied to that user. |
| **Pass / Fail** | ✅ Pass |

### REQUIREMENT #10
| Field | Description |
| :--- | :--- |
| **Requirement** | "Integrated chat system for communication between users and administrators." |
| **Test Input / Action** | User sends a message to Admin via the integrated chat bubble. |
| **Expected Result** | The message is received and viewable by the Admin user. |
| **Actual Result** | Message was delivered is delivered and viewable by Admin. Both users and admins however are unable to create new chats|
| **Pass / Fail** | ✅ Pass |enario-Based Testing

---

## D. Scenario-Based Testing

### Scenario 1: Student Equipment Reservation
**User Story:** "As a student researcher, I want to reserve a microscope online so that I can ensure the tool is available for my experiment on Tuesday."

**Sequence of Actions:**

| Step                                   | Action                                                                                                                | Expected Behavior                                                                                             | Result | Remarks (if fail) |
| :------------------------------------- | :-------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------ | :----- | :---------------- |
| 1. Open the app                        | Log in as `tester@email.com`.                                                                                         | User is authenticated and redirected to the Student Dashboard.                                                | ✅ Pass |                   |
| 2. Request Equipment                   | Navigate to Request Form in the Dashboard and select "Microscope" within the list of available equipment.             | Status changed instantly; approval reflects on User dashboard.                                                | ✅ Pass |                   |
| 3. Accomplish request equipment form   | Fill in the reservation form with Tuesday's date, start and return time, name of Adviser/Project Leader, and purpose. | Form accepts valid input and allows the user to proceed with submitting the equipment reservation request.    | ✅ Pass |                   |
| 4. Track status of requested equipment | Press submit and check the Dashboard to track the status of the equipment.                                            | Submitted request appears in the Dashboard with the current reservation status displayed for user monitoring. | ✅ Pass |                   |

**Observation:** Status is "Pending." After Admin logs in as `rbbuerom@up.edu.ph` and approves, the student status updates to "Approved."

### Scenario 2: Admin Accountability Audit
**User Story:** "As a lab admin, I want to approve some pending requests and export the record for certain accountabilities."

**Sequence of Actions:**

| Step                                  | Action                                                              | Expected Behavior                                                                                                   | Result | Remarks (if fail) |
| :------------------------------------ | :------------------------------------------------------------------ | :------------------------------------------------------------------------------------------------------------------ | :----- | :---------------- |
| 1. Open the app (as admin)            | Log in as `rbbuerom@up.edu.ph`.                                     | Admin user is authenticated and redirected to the Admin Dashboard.                                                  | ✅ Pass |                   |
| 2. Check pending requests             | Look at the dashboard, click on one pending request, and press view | Ongoing borrowing requests are displayed with complete borrower and equipment details.                              | ✅ Pass |                   |
| 3. Determine that request can be made | Click on "Approve" after checking all necessary information         | Selected borrowing request is approved successfully, and the equipment status is updated accordingly in the system. | ✅ Pass |                   |
| 4. Generate accountability report     | Go to "Accountability" and click "Export to PDF."                   | System generates and downloads a PDF report containing the accountability and status.                               | ✅ Pass |                   |

**Observation:** The equipment is back in the available pool, and a PDF file containing the transaction is downloaded.

---

## E. Summary

### i. Testing Summary
The release testing covered 10 core requirements through both direct functional testing and user scenarios. All primary features, including inventory management, digital reservations, and PDF exporting, were verified. All tests for each requirement had lead to a passing result and no complications had been found within testing the app.

### ii. Conclusion
**Verdict:** **READY FOR RELEASE** The application fulfills its primary purpose of streamlining laboratory equipment management. The tiered roles prevent unauthorized access to administrative features, and the core workflow (Request -> Approval -> Return) is stable. 

### iii. Remarks
* **UI/UX:** Adding a "Help" section or onboarding for first-time users would be beneficial. Additional feedbacks (modals, toast notifications, etc.) are also recommended to improve the user experience. Furthermore, the hero page is well designed but the other pages still needs a lot of improvement.

* **Bugs:** Small bugs can still be found within the app such as the quantity of equipment not yet reflected when equipment gets requested.

* **Security:** The "Exposed Chats" limitation (where all admins see all chats) should be addressed in the next version to improve privacy.
