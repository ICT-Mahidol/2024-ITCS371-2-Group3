# Revision Log

## Use Case Diagrams
  
1.  **Added MOI (Ministry of Interior) as an Actor**
The MOI is included as an external actor responsible for providing access to the National ID Card database. This allows the system to cross-check the information provided by the user against official government records for accurate identity verification.
  ---

2.  **Added View Event Use Case**
This use case has been added to provide users with easy access to event information, helping them make informed decisions about participation.

  ---

3.  **Added TrueMoney as a Payment Option by Using Extend**
This extension allows users to select TrueMoney for payments, providing a secure and convenient payment method. It enhances the platform’s flexibility by offering an alternative payment option for users who prefer using TrueMoney.

  ---

4.  **Added Credit Card as a Payment Option by Using Extend**
This extension allows users to make payments via credit card, offering a secure and widely-accepted payment method. It enhances the platform’s flexibility by providing an additional convenient payment option for users who prefer to use credit cards.

  ---

5.  **Removed Oversee Booth Booking as an Include Use Case**
This use case has been removed because its functionality is already incorporated into other processes, eliminating redundancy and streamlining the overall workflow.

## Functional Decomposition Diagram

### 1. Registration
- **Expanded into:**
  - User registration
  - Email and ID verification
  - Profile setup
  - Account confirmation
- **Purpose of Expansion:**  
  To guide users through a complete registration process and ensure secure access to the system.

---

### 2. View Booth
- **Expanded into:**
  - Logging in
  - Viewing available booths
  - Selecting a booth
  - Viewing booth details
- **Purpose of Expansion:**  
  To provide users with a clear process for exploring and selecting booths, ensuring they can access all relevant booth information before booking.

---

### 3. Booth Management
- **Expanded into:**
  - Logging in
  - Communicating with booth managers
  - Setting booth prices, sizes, and facilities
- **Purpose of Expansion:**  
  To introduce collaborative tools for booth managers and provide a comprehensive system to manage booth details.

---

### 4. Booking Request
- **Expanded into:**
  - Logging in
  - Selecting a booth
  - Booking it
  - Confirming booking details
- **Purpose of Expansion:**  
  To ensure that users follow a clear sequence of steps for booking, reducing errors and improving the experience.

---

### 5. Make Payment
- **Expanded into:**
  - Selecting payment methods
  - Entering payment information
  - Confirming payment
  - Uploading proof
  - Recording payment
- **Purpose of Expansion:**  
  To ensure a structured payment process that includes validation and record-keeping for secure transactions.

---

### 6. Approve/Reject Booking
- **Expanded into:**
  - Logging in
  - Reviewing booking information
  - Approving or rejecting the booking
  - Notifying users of the decision
- **Purpose of Expansion:**  
  To streamline decision-making for admins and ensure users are promptly informed about the status of their booking.

---

### 7. Oversee Booking
- **Expanded into:**
  - Logging in
  - Viewing the status of bookings
- **Purpose of Expansion:**  
  To create a clear tracking mechanism for users to monitor their bookings.

---

### 8. Generate Report
- **Expanded into:**
  - Monitoring booth bookings and event activity
  - Creating custom reports by date, event, or booth type
- **Purpose of Expansion:**  
  To give admins the ability to analyze data effectively and make informed decisions.

---

### 9. Announcement/Update
- **Expanded into:**
  - Logging in
  - Creating announcements
  - Sending announcements to users
- **Purpose of Expansion:**  
  To provide a structured way for admins to communicate updates and announcements.

---

### 10. Schedule Management
- **Expanded into:**
  - Logging in
  - Setting booth availability dates
  - Notifying users of schedules
- **Purpose of Expansion:**  
  To give admins control over booth scheduling and ensure users are aware of booth availability.

---

## Data Flow Diagram Level 0

  

1.  **Changed the Arrow "Error Notifications" Direction from Pointing to ‘Payment Gateway’ to Pointing to ‘Booth Management System’**
This change was made to correct the data flow, as the information was intended to go directly into the Booth Management System, ensuring an accurate and efficient workflow representation.
---
2. **Add new entities "MOI"**
The MOI (Ministry of Interior) entity was added to the system to ensure user identity verification by matching names and IDs with official government records. This addition helps prevent fraudulent bookings by validating information and ensures legal compliance with government regulations for identity checks.
---
3. **Revised Data Flow for Enhanced Clarity and Specificity**
The revisions to the data flow were made to enhance clarity and specificity. Previously, terms like "personal information" and "booking activity overview" were too broad and ambiguous, which could lead to confusion about the exact data being collected, transmitted, or processed within the system. By specifying terms such as "name, surname, tel" instead of "personal information," and replacing vague terms with concrete examples of data being exchanged, the system's design becomes more precise and actionable.


## Data Flow Diagram Level 1

### Modifications and Justifications

#### **1. Enhanced Data Flow Specificity**
**Modification**:  
In the second diagram, all data flows are annotated with detailed fields (e.g., *Full Name*, *Telephone No.*, *Booth Image*, etc.), while the first diagram uses general terms like User Data or *Booth Details*.

**Reason for Modification**:  
This change was made to increase clarity and transparency in the data being exchanged between processes. By specifying exact data fields, stakeholders (developers, analysts, or users) can better understand what information is required and ensure compliance with data collection standards.

---

#### **2. Renamed Processes for Clarity**
**Modification**:  
- "Booking Request" (First DFD) was renamed to "Book a Booth" (Second DFD).  
- "Schedules Manage" became *"View Reservation Status"*.  

**Reason for Modification**:  
These renamings aim to make the processes self-explanatory. For instance, "Book a Booth" explicitly states the action being performed, making it easier for users or developers to relate it to their tasks in the system. Similarly, "View Reservation Status" emphasizes user interaction, aligning with expected user actions.

---

#### **3. Added Integration with MOI Verification**
**Modification**:  
In the second diagram, MOI Verification involves interaction with an external MOI User Database for user validation, a layer absent in the first diagram.

**Reason for Modification**:  
This modification ensures that user registration includes identity verification for added security and compliance with regulatory requirements. This step is critical for systems dealing with sensitive or legally protected data.

---

#### **4. Added Explicit Data Stores**
**Modification**:  
The second diagram introduces new data stores such as *User Information*, *Booth Information*, *Payment Information*, and *Reservation Information*.

**Reason for Modification**:  
Adding these data stores improves data management by clearly segregating the storage of different types of information. It enhances the design's modularity, making future system expansions or debugging easier.

---

#### **5. Enhanced "Booth Management" Process**
**Modification**:  
The second diagram includes additional data points in the "Booth Management" process, such as *Booth Image*, *Available Date*, *Facilities*, etc., which were not explicitly defined in the first diagram.

**Reason for Modification**:  
This ensures that all necessary details about booths are centrally managed, improving the system's capability to support diverse user needs and streamlining the management process.

---

#### **6. Added Reporting and Decision Fields**
**Modification**:  
In the second DFD, the Generate Report and Approve/Reject Request processes include more comprehensive inputs like Reservation Information and *Booth Name*.

**Reason for Modification**:  
This allows stakeholders (e.g., Booth Managers) to make better decisions based on complete data and enables the system to generate reports that are richer in detail.

---

#### **7. Simplified General User Interaction**
**Modification**:  
The second diagram organizes user interaction more systematically, grouping related actions and flows (e.g., *Book a Booth*, *Make Payment*, *View Reservation Status*).  

**Reason for Modification**:  
This improves user experience by creating a more intuitive and structured flow of interactions, reducing potential confusion.

---