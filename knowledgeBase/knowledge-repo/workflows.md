# OneCX Workflows

## User Authentication and Access

#### Login and Branch Selection

**Purpose:** Authenticate users and establish their working context within a specific branch.

**Actors:** All users (Client Admin, Staff, Supervisors, Super Users)

**Main Flow:**
1. User enters username and password
2. System authenticates and identifies client (financial institution)
3. Sign-In popup displays accessible branches (home and float locations)
4. User selects branch and signs into lobby queue
5. System displays client name in header and grants access to modules

**Variations:**
- **ADFS Single Sign-On:** User authenticates via identity provider instead of username/password
- **Two-Factor Authentication:** Additional verification step after password entry
- **Super User Client Switching:** Super users can switch between different client organizations
- **Float Location Access:** Users see both home and float locations in branch selection
- **Sign Out and Re-Sign In:** Users can sign out of current branch and select different branch

**Sources:** 01. Login & Introduction Script.docx.md, 12. Global Settings Script.docx.md

---

## User and Permission Management

#### User Profile Management

**Purpose:** Create and maintain user accounts with appropriate access levels and settings.

**Actors:** Client Admin, Supervisors

**Main Flow:**
1. Navigate to User Management → Users
2. Click Add User or Edit existing user
3. Configure Basic Settings (email, permission groups, notification groups, home location, active status)
4. Save user profile

**Variations:**
- **Save and Continue:** Save user and remain in edit mode to configure additional sections
- **Lobby Settings Configuration:** Set supervisor, default view, impersonation settings (Lobby Tracker clients only)
- **Appointment Settings Configuration:** Set time zone, email subscriptions, flexible float, meeting preferences (Appointment Concierge clients only)
- **Availability Template Setup:** Define work days, time slots, locations, multiple rotations
- **Skills Assignment:** Opt-in for products/services by category, set proficiency levels (0-100)
- **Migrating Client:** Existing users automatically imported with permission mappings from legacy platforms
- **Account Locked/Unlocked:** Admin can lock/unlock user accounts
- **Login Enabled Toggle:** Control login capability (Appointment Concierge clients only)

**Sources:** 04. Users & My Account Script.docx.md

#### Permission Group Configuration

**Purpose:** Define access control and notification targeting groups.

**Actors:** Client Admin

**Main Flow:**
1. Navigate to User Management → Permission Groups
2. Click Add to create new group
3. Enter Permission Group Name
4. Uncheck Notification Group checkbox
5. Select permissions across Administrative, Lobby, Analytics, and Appointments categories
6. Save group

**Variations:**
- **Notification Group Creation:** Check Notification Group checkbox; all permission checkboxes disabled; used for alert targeting only
- **Migrating Client:** Pre-existing groups automatically mapped from legacy platforms
- **Edit Existing Group:** Modify permissions or convert between permission/notification group types
- **Select All by Category:** Use category-level or master checkbox for bulk selection

**Sources:** 03. Permission Groups Script.docx.md

#### My Account Self-Service

**Purpose:** Allow users to update their personal information.

**Actors:** All logged-in users

**Main Flow:**
1. Click username in top-right corner
2. Select My Account
3. Edit allowed fields (name, time zone, emails, phone, language, lobby default tab)
4. Save changes

**Variations:**
- **Password Change:** Update password through My Account page
- **Forgot Password:** Use login page to receive password reset email
- **Non-Editable Fields:** Username, permission groups, notification groups, supervisor assignments cannot be changed by user

**Sources:** 04. Users & My Account Script.docx.md

---

## Location and Service Configuration

#### Location Setup

**Purpose:** Configure branch locations with operating parameters.

**Actors:** Client Admin

**Main Flow:**
1. Navigate to Locations & Services → Locations
2. Click Add Location
3. Configure Basic Settings (code, name, type, time zone, parent, contact information)
4. Save and Continue
5. Configure Operating Hours (days, time slots)
6. Configure Holidays (opt-in/out provisioned holidays)
7. Configure Products & Services opt-in
8. Configure Appointment Settings (availability window, cut-off, concurrency, float priority)
9. Configure Lobby Settings (remote check-in options)
10. Save all sections

**Variations:**
- **Multiple Time Slots per Day:** Add multiple time ranges for breaks (e.g., 9-12, 1-5)
- **Non-Working Days:** Uncheck Open status for closed days
- **Higher-Level Locations:** Organization/Area/Region show aggregated holidays and services from child branches
- **Holiday Inheritance:** Holidays can be inherited from parent or overridden at branch level
- **Set Display Order:** Customize product/service display order for branch (global or category-based)
- **Activate/Deactivate Location:** Use lock/unlock icon to change location status

**Sources:** 06. Locations Script.docx.md

#### Product and Service Configuration

**Purpose:** Define and organize service offerings available to customers.

**Actors:** Client Admin

**Main Flow:**
1. Navigate to Locations & Services → Product Categories
2. Create categories with display names, codes, and icons
3. Set display order for categories
4. Navigate to Products & Services
5. Click Add Product or Service
6. Configure Basic Settings (name, code, category, type, language, active status)
7. Save and Continue
8. Configure Opt In Settings (per location)
9. Configure Employee Settings (per employee, with proficiency 0-100)
10. Configure Appointment Settings (duration, widget visibility, meeting preferences, restrictions)
11. Configure Lobby Settings (time standard, check-in/wrap-up visibility, kiosk visibility)
12. Set global or category display order

**Variations:**
- **Multi-Language Support:** Create separate entries for English and Spanish
- **Show in Widget Toggle:** Control appointment booking availability
- **Meeting Preferences:** Enable In-Person, Phone, and/or Virtual options
- **Restrict Modify/Cancel:** Prevent customers from changing appointments
- **Require Comments:** Mandate customer comments during booking
- **Appointment Checklists:** Add checklist items for confirmation emails
- **Apply to Multiple Branches:** Replicate settings across selected locations
- **Category-Based Display:** Show services grouped by category or in global order
- **Deactivate/Activate Service:** Toggle active status without deletion

**Sources:** 05. Products & Services Script.docx.md, 06. Locations Script.docx.md

#### Checklist Management

**Purpose:** Define service-specific checklists for staff to complete during wrap-up.

**Actors:** Client Admin

**Main Flow:**
1. Navigate to Locations & Services → Checklists
2. Filter by Product Category
3. Click Plus icon for product/service
4. Add checklist items with internal name and display text
5. Reorder items via drag-and-drop
6. Save checklist

**Variations:**
- **Edit Existing Checklist:** Modify checklist items for configured services
- **Delete Checklist or Items:** Remove entire checklist or individual items
- **No Checklist:** Services without checklists proceed to wrap-up without checklist step

**Sources:** 09. LWA & Checklists Script.docx.md

---

## Lobby Operations

#### Visitor Check-In

**Purpose:** Register visitors into the lobby queue for service.

**Actors:** Staff members, Kiosk (self-service)

**Main Flow:**
1. Click Check-In button (available from any module)
2. Enter visitor information (first name, last name - mandatory)
3. Enter optional fields (account number, phone, email, DOB, custom fields based on Global Settings)
4. Select products/services (grouped by category if enabled)
5. Select staff preference or notification group
6. Check Spanish speaker preference if applicable
7. Check receive text message if phone provided
8. Add notes (non-sensitive information only)
9. Submit check-in

**Variations:**
- **Add to Lobby:** Add visitor to queue without immediate assist
- **Instant Assist:** Begin assisting visitor immediately after check-in
- **Instant Assist (Impersonate):** Assist visitor while impersonating another staff member
- **Today's Appointments:** View appointment queue for signed-in branch
- **Kiosk Self-Service:** Customer performs check-in independently via kiosk
- **Remote Check-In:** Customer checks in remotely before arriving (if enabled for location)
- **Appointment Check-In:** Validate appointment via confirmation number or last name + time

**Sources:** 07. Lobby Script.docx.md, 14. Kiosk Script.docx.md

#### Staff Sign-In to Lobby

**Purpose:** Make staff available to assist visitors in a specific branch.

**Actors:** Staff members

**Main Flow:**
1. Log into application
2. Sign-In popup displays accessible branches (home and float locations)
3. Select branch
4. Click Sign In to Lobby Queue
5. System marks staff as signed in and available

**Variations:**
- **Sign Out:** Click Sign Out of Lobby button in header
- **Change Signed-In Location:** Select different location in Lobby/Appointment Status dropdown
- **Float Location Sign-In:** Sign into non-home location where user has float access
- **Already Signed In:** If signed in, can directly access lobby queue

**Sources:** 07. Lobby Script.docx.md

#### Visitor Assistance and Wrap-Up

**Purpose:** Provide service to visitors and record completed services.

**Actors:** Staff members

**Main Flow:**
1. From Lobby Queue, click Assist icon on visitor record
2. System opens Wrap-Up view with visitor details
3. Select requested or additional services to mark as completed
4. For services with checklists, click checklist icon and check off all items
5. Enter service reference numbers if applicable
6. Add required comments
7. Click Wrap Up to complete service

**Variations:**
- **Return to Lobby:** Send visitor back to queue (up to 5 interactions maximum)
- **Book Follow-Up Appointment:** Schedule future appointment during wrap-up
- **Multiple Interactions:** Track each assist session separately; 5th interaction forces wrap-up
- **Impersonation Assist:** Assist visitor on behalf of another staff member
- **Edit Lobby Record:** Update visitor details or service requests before/during assist
- **Wrap-Up Button Access:** Access ongoing wrap-up from anywhere in application
- **Running Interaction Time:** View elapsed time and assisted-by details

**Sources:** 07. Lobby Script.docx.md

#### Left Without Assistance

**Purpose:** Record when visitors leave before being served.

**Actors:** Staff members

**Main Flow:**
1. From Lobby Queue, click Left Without Assistance icon
2. Select predefined reason from popup
3. Optionally enter description
4. Save
5. System removes record from queue

**Variations:**
- **Custom Reasons:** Admin can add/edit/delete LWA reasons in Configuration module
- **Default Reason:** System provides "Left without Assistance" reason by default

**Sources:** 07. Lobby Script.docx.md, 09. LWA & Checklists Script.docx.md

#### Text on Demand

**Purpose:** Send ad-hoc text messages to waiting visitors.

**Actors:** Staff members

**Main Flow:**
1. From Lobby Queue, click Text on Demand icon (visible if visitor opted in)
2. Enter custom message (up to 350 characters)
3. Click Send
4. Message delivered to visitor's phone

**Variations:**
- **Message History:** All sent messages logged in Text On Demand History section

**Sources:** 07. Lobby Script.docx.md, 11. Text Messages Script.docx.md

#### Staff Status Monitoring

**Purpose:** Monitor staff availability and current activities.

**Actors:** Supervisors, Staff members

**Main Flow:**
1. Navigate to Lobby → Staff Status tab
2. View staff signed in at selected location
3. See status (assisting/idle), duration, current visitor, and services being provided

**Variations:**
- **View Interaction Details:** Click information icon to see assist start time, current assist time
- **Force Sign Out:** Click sign-out icon to remove staff from lobby (disabled for last signed-in staff or 5th interaction)
- **Filter by Assist Type:** View all staff or filter by specific assist types
- **Central Staff Status View:** View all staff across all accessible branches

**Sources:** 07. Lobby Script.docx.md

#### Central Views Monitoring

**Purpose:** Monitor lobby activity across all branches.

**Actors:** Supervisors, Client Admin

**Main Flow:**
1. Navigate to Lobby → Central Views tab
2. Select view type (Central Lobby, Central Staff Status, or Central Location)
3. View aggregated data across all accessible branches

**Variations:**
- **Central Lobby View:** All visitors checked in across all branches
- **Central Staff Status View:** All signed-in staff across all branches
- **Central Location View:** Performance metrics by location (wait time, visitors waiting, assists, average times, abandons)
- **Filter by Location:** Narrow view to specific branches
- **Filter by Spanish Speaker:** Filter lobby records by language preference

**Sources:** 07. Lobby Script.docx.md

---

## Impersonation and Transfers

#### Staff Impersonation Setup

**Purpose:** Enable staff to assist visitors on behalf of other staff members.

**Actors:** Client Admin

**Main Flow:**
1. Navigate to Configuration → Global Settings
2. Enable "Enable User Impersonation" in Lobby Settings section
3. Save global settings
4. Navigate to User Management → Users
5. Select user and open Lobby Settings
6. Check "Enable User Impersonation" (user can impersonate others)
7. Check "Show User for Impersonation" (user can be impersonated)
8. Save user settings

**Sources:** 08. Impersonation & Transfers Script.docx.md

#### Impersonating Staff in Lobby

**Purpose:** Assist visitors while acting as another staff member.

**Actors:** Staff with impersonation enabled

**Main Flow:**
1. Sign into lobby
2. Check in visitor or select visitor from Lobby Queue
3. Click Instant Assist (Impersonate) or Impersonate Assist icon
4. Select staff member to impersonate from popup (shows signed-out staff with impersonation enabled)
5. Begin assisting visitor as impersonated staff member

**Variations:**
- **Multiple Concurrent Impersonations:** Assist up to 25 visitors simultaneously while impersonating
- **Transfer Impersonated Assists:** Use Transfer Assists button to move impersonated assists to other eligible users
- **Transfer All:** Move all impersonated assists to single user
- **Transfer Individually:** Assign specific assists to different users
- **Notifications:** New users receive automatic notification when assists are transferred

**Sources:** 08. Impersonation & Transfers Script.docx.md

---

## Appointment Management

#### Appointment Scheduling

**Purpose:** Book future appointments for customers.

**Actors:** Staff members, Customers (via widget)

**Main Flow:**
1. Access Appointments Web Widget (from kiosk or web)
2. Select location
3. Select product/service
4. Choose meeting preference (In-Person, Phone, Virtual)
5. Select available date and time slot
6. Optionally request specific staff member (if enabled)
7. Enter customer details and comments
8. Confirm appointment
9. Receive confirmation number and email

**Variations:**
- **Staff-Assisted Booking:** Staff books appointment on behalf of customer via portal
- **Follow-Up Appointment:** Book during lobby wrap-up process
- **Restrict Staff Request:** Widget setting can disable staff selection
- **Restrict Modify/Cancel:** Service setting can prevent customer changes
- **Require Comments:** Service setting can mandate customer comments
- **Concurrency Mode:** Multiple appointments can be scheduled in same slot based on location settings
- **Float Staff Availability:** Float staff appear in scheduling based on travel pad time

**Sources:** 06. Locations Script.docx.md, 07. Lobby Script.docx.md, 14. Kiosk Script.docx.md

#### Appointment Check-In

**Purpose:** Register appointment arrival and add to lobby queue.

**Actors:** Staff members, Customers (via kiosk)

**Main Flow:**
1. From Lobby → Appointment Queue tab, locate appointment
2. Click check-in icon
3. Visitor added to Lobby Queue with appointment details

**Variations:**
- **Kiosk Check-In:** Customer validates appointment via confirmation number or last name + time
- **Remote Check-In:** Customer checks in remotely before arriving (if enabled)
- **Restrict Remote Check-In Outside Hours:** Block remote check-ins outside operating hours
- **Edit Appointment:** Modify appointment details before check-in
- **Mark No-Show:** Record appointment as no-show if customer doesn't arrive

**Sources:** 07. Lobby Script.docx.md, 14. Kiosk Script.docx.md

---

## Alert and Notification Management

#### Global Alert Configuration

**Purpose:** Set up automated notifications for lobby activity.

**Actors:** Client Admin

**Main Flow:**
1. Navigate to Configuration → Global Alerts
2. Click Add Alert
3. Select who to notify (individuals, groups, skilled users, or email lists)
4. Select delivery method (System Alert, Email, SMS, or All)
5. Set trigger timing (immediately or after wait time threshold)
6. Filter by request type (all requests, no requests, or custom users/groups/services)
7. Configure Notify Offline option
8. Save alert

**Variations:**
- **Edit Alert:** Modify existing alert configuration inline
- **Delete Alert:** Remove alert from system
- **Skilled Users Targeting:** Alert staff proficient in specific service when requested
- **Wait Time Threshold:** Trigger only when customer wait exceeds defined minutes
- **Multiple Phone Numbers:** Add additional SMS recipients beyond user profiles

**Sources:** 10. Alerts Script.docx.md

#### Personal Alert Configuration

**Purpose:** Set up individual notification preferences.

**Actors:** All users

**Main Flow:**
1. Click username in header
2. Select My Alerts
3. Click Add Alert
4. Configure alert settings (same options as Global Alerts)
5. Save alert

**Variations:**
- **View Global Alerts:** See alerts assigned to user by admin
- **Edit/Delete Personal Alerts:** Manage own alert configurations

**Sources:** 10. Alerts Script.docx.md

---

## Text Message Management

#### Automated Text Message Configuration

**Purpose:** Set up automated SMS notifications for lobby events.

**Actors:** Client Admin

**Main Flow:**
1. Navigate to Configuration → Text Messages
2. Select Text Message Type (Walk-in, Appointment, Remote Check-In, Queue)
3. Enable via Opt In checkbox
4. Click Edit icon to customize message content
5. Drag and drop dynamic chips (CustomerFirstName, LocationDisplayName, etc.)
6. Save message template

**Variations:**
- **Reset to Default:** Restore original message template
- **Queue Position Trigger:** Set queue position number for notification (e.g., notify when next in line)
- **Language Support:** Currently English only

**Sources:** 11. Text Messages Script.docx.md

---

## Kiosk Configuration and Usage

#### Kiosk Setup

**Purpose:** Configure self-service kiosk behavior for a branch.

**Actors:** Client Admin

**Main Flow:**
1. Navigate to Configuration → Kiosks
2. Click plus icon for branch without kiosk
3. Configure Check-in Display Options (sign-in, check-in, appointment cards)
4. Configure Optional Input Fields (account number, phone, email, DOB, custom)
5. Configure Staff Preference Options
6. Configure Product/Service Options (visibility, sorting, categories, mandatory selection)
7. Configure Wait Time & Queue Display Options
8. Configure Additional Settings (welcome/thank-you messages, refresh interval, language)
9. Save configuration

**Variations:**
- **Edit Existing Kiosk:** Modify configuration for already-configured branch
- **Copy Configuration:** Duplicate settings from one kiosk to another branch
- **Launch Kiosk:** Test kiosk configuration
- **Delete Kiosk:** Remove kiosk configuration
- **Show Categories:** Group products/services by category in kiosk display
- **Wait Time Calculation:** Choose method (average over time, visitors served, or real-time queue)

**Sources:** 13. Kiosk Configuration Script.docx.md

#### Customer Self-Service via Kiosk

**Purpose:** Enable customers to check in independently.

**Actors:** Customers/Visitors

**Main Flow:**
1. Kiosk displays home page with available cards
2. Customer selects Sign In
3. Selects products/services (by category if enabled)
4. Enters personal details (first name, last name, optional fields)
5. Opts in for text messages if desired
6. Selects staff or group preference if enabled
7. Completes sign-in
8. Views confirmation screen with position and estimated wait time

**Variations:**
- **Appointment Check-In:** Validate existing appointment via confirmation number or last name + time
- **Schedule Future Appointment:** Launch Appointments Web Widget from kiosk
- **Spanish Language:** Select Spanish if enabled in kiosk settings
- **Auto-Return to Home:** Kiosk returns to home screen after configured timeout

**Sources:** 14. Kiosk Script.docx.md

---

## Data Management

#### Bulk Data Import

**Purpose:** Upload configuration data in bulk.

**Actors:** Client Admin

**Main Flow:**
1. Navigate to Configuration → Data Import/Export
2. Select file type from dropdown (Locations, Holidays, Operating Hours, Product Categories, Products & Services, User Availability, User Skills, Users)
3. Upload CSV file via Select File or drag-and-drop
4. Click Submit File
5. Review Import Logs for success/failure details

**Variations:**
- **Error Correction:** Review failed records in logs and resubmit corrected file
- **Holiday Provisioning:** Holidays must be imported; cannot be manually added in UI

**Sources:** 15. Data ImportExport & Localization Script.docx.md

#### Data Export

**Purpose:** Extract system data for external use.

**Actors:** Client Admin

**Main Flow:**
1. Navigate to Configuration → Data Import/Export → Data Export tab
2. Select file type (Users, Locations, Products & Services, etc.)
3. Click Data Export button
4. Download CSV file

**Sources:** 15. Data ImportExport & Localization Script.docx.md

#### Localization Customization

**Purpose:** Customize text displayed in different applications and languages.

**Actors:** Client Admin

**Main Flow:**
1. Navigate to Configuration → Localization
2. Select Application (FMSI OneCX, Kiosk, Remote Check-In Web Page)
3. Select Language (English or Spanish)
4. Locate text key in grid
5. Click Edit icon
6. Modify display text
7. Save changes

**Variations:**
- **Appointment Localization:** Access via Appointments → Administration → Localization tab
- **Default Values:** System provides default English values; Spanish can be customized

**Sources:** 15. Data ImportExport & Localization Script.docx.md

---

## Reporting and Analytics

#### Lobby Activity Reporting

**Purpose:** Analyze lobby performance and service delivery.

**Actors:** Client Admin, Supervisors, Executives

**Main Flow:**
1. Navigate to Reports → Lobby Activity
2. Select View type (Location Comparison, Traffic & Wait Time, Products & Services, Employee, Details, Staff Signed In/Out)
3. Apply filters via Filter Options (locations, dates, staff, services, status)
4. Review data in grid
5. Expand rows for detailed interactions
6. Export to Excel

**Variations:**
- **Save Filter Templates:** Create reusable filter configurations
- **Share Templates:** Make templates available to other users
- **Set Default Template:** Auto-apply template when opening report
- **Drill-Down Analysis:** Expand rows to see granular interaction details
- **Multiple Filter Dimensions:** Combine location, time, staff, service, and status filters

**Sources:** 17. Reporting Script.docx.md

#### Lobby Editor for Data Correction

**Purpose:** Audit and correct historical lobby records.

**Actors:** Client Admin, Supervisors

**Main Flow:**
1. Navigate to Reports → Lobby Editor
2. Set date range (From/To dates)
3. Click Run Report
4. Review records in grid
5. Click Edit icon on record to modify
6. Update customer information, interaction details, or services provided
7. Add or remove products/services
8. Save changes

**Variations:**
- **Expand All Records:** View all interaction details simultaneously
- **Delete Selected Records:** Bulk delete using checkboxes
- **Filter Templates:** Apply saved filters for targeted auditing
- **Multiple Interactions:** View and edit each interaction separately for multi-interaction records
- **Export Data:** Download filtered records to Excel

**Sources:** 17. Reporting Script.docx.md

---

## System Configuration

#### Global Settings Management

**Purpose:** Configure system-wide defaults and behaviors.

**Actors:** Client Admin, Super Users

**Main Flow:**
1. Navigate to Configuration → Global Settings
2. Configure Basic Settings (client display name, email settings, timeout duration, text notifications, logo upload)
3. Configure Authentication Settings (username/password vs. ADFS, password expiration, two-factor authentication, domain configuration)
4. Configure Appointment Settings (float travel pad time, widget appointments, confirmation email settings)
5. Configure Lobby Settings (default tab, alert chime, staff status text, mandatory comments, reference numbers, impersonation, field visibility, data regeneration day)
6. Save settings

**Variations:**
- **Single Sign-On Configuration:** Set up ADFS with identity provider and domain mappings
- **Just-In-Time Provisioning:** Enable automatic user creation during SSO
- **Multi-Domain Support:** Configure multiple domains with default designation
- **Custom Field Visibility:** Control which optional fields appear in lobby and kiosk

**Sources:** 12. Global Settings Script.docx.md

#### Client Management (Super Users Only)

**Purpose:** Create and manage multi-tenant client environments.

**Actors:** Super Users (FMSI Default Users)

**Main Flow:**
1. Navigate to Client Management page
2. Click create new client
3. Specify client code, solution ID, domain name
4. Configure database name and server name
5. Enable client migration from legacy platforms if applicable
6. Save client configuration

**Variations:**
- **View Existing Clients:** Review details of already-created clients
- **Change Client:** Switch between client organizations using client selection feature

**Sources:** OneCX.html

---

## Left Without Assistance Configuration

#### LWA Reason Management

**Purpose:** Define reasons for visitors leaving without service.

**Actors:** Client Admin

**Main Flow:**
1. Navigate to Configuration → Left Without Assistance
2. View default reason ("Left without Assistance")
3. Click Add Reason to create custom reason
4. Enter reason text
5. Click Save icon

**Variations:**
- **Edit Reason:** Modify existing reason text
- **Delete Reason:** Remove custom or default reasons
- **Usage in Lobby:** Reasons appear in LWA popup when marking visitors

**Sources:** 09. LWA & Checklists Script.docx.md
