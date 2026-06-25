# OneCX Business Rules and Questions

## Business Rules

### Authentication and Access Control

#### Password Management
- Password expiration default: 90 days
- Password can be changed via My Account page or Forgot Password flow
- Two-factor authentication can be enabled per user

**Source:** 04. Users & My Account Script.docx.md, 12. Global Settings Script.docx.md

#### Session Management
- Default timeout duration: 90 minutes of inactivity
- Timeout duration is configurable in Global Settings

**Source:** 12. Global Settings Script.docx.md

#### Login Eligibility
- Active status required for all users to log in (Lobby Tracker clients)
- Active status AND Login Enabled required for Appointment Concierge clients
- Account can be locked by administrators to prevent access

**Source:** 04. Users & My Account Script.docx.md

#### Permission Assignment
- User can be assigned to only ONE permission group
- User can belong to MULTIPLE notification groups
- Permission groups control feature access
- Notification groups control alert targeting only

**Source:** 03. Permission Groups Script.docx.md

### Location and Hierarchy Rules

#### Location Hierarchy
- Four-tier structure enforced: Organization → Area → Region → Branch
- Parent location must be specified for all non-Organization types
- Child locations inherit parent's time zone unless overridden

**Source:** 06. Locations Script.docx.md

#### Location Access
- User's home location determines accessible location hierarchy
- Users can access home location and all sub-locations
- Float locations grant additional access beyond home hierarchy

**Source:** 04. Users & My Account Script.docx.md, 07. Lobby Script.docx.md

#### Location Activation
- Inactive locations hidden from dropdowns
- Inactive locations cannot be used for appointments or lobby check-ins
- Location activation/deactivation controlled via lock/unlock icon

**Source:** 06. Locations Script.docx.md

#### Geolocation
- Latitude and Longitude auto-generated when address information is completed
- Used for location-based services and mapping

**Source:** 06. Locations Script.docx.md

### Operating Hours and Holidays

#### Operating Hours
- Multiple time slots allowed per day (e.g., 9-12, 1-5 for lunch breaks)
- Days can be marked as non-working by unchecking Open status
- Operating hours determine appointment availability and remote check-in windows

**Source:** 06. Locations Script.docx.md

#### Holiday Management
- Holidays cannot be manually added through UI
- Holidays must be provisioned via Data Import/Export module
- Holidays can be opted in/out at branch level
- Higher-level locations show holidays opted in for at least one child branch
- Holiday settings can be inherited from parent or overridden at branch level
- Holidays support All Day and Blackout flags
- Holidays include start time and end time for partial-day closures

**Source:** 06. Locations Script.docx.md, 15. Data ImportExport & Localization Script.docx.md

### Product and Service Rules

#### Service Configuration
- Service Code must be unique
- Service can be type "Product" or "Service"
- Service must be assigned to a Product Category
- Inactive services not available for selection

**Source:** 05. Products & Services Script.docx.md

#### Opt-In Requirements
- Services must be opted in at location level to be available at that branch
- Services must be opted in at employee level for staff to provide that service
- Opt-in can be configured independently for locations and employees

**Source:** 05. Products & Services Script.docx.md

#### Proficiency Levels
- Employee proficiency range: 0-100 for each service
- Proficiency indicates skill level in providing specific service
- Used for skilled user alert targeting

**Source:** 05. Products & Services Script.docx.md, 10. Alerts Script.docx.md

#### Display Order
- Global Display Order used when "Show Category" is disabled
- Category Display Order used when "Show Category" is enabled
- Display order affects Lobby Check-in, Lobby Wrap-Up, Kiosk, and Widget
- Display order can be customized per branch

**Source:** 05. Products & Services Script.docx.md, 06. Locations Script.docx.md

#### Appointment Settings per Service
- Duration defines default appointment length
- Show in Widget controls appointment booking availability
- Meeting Preferences: In-Person, Phone, and/or Virtual
- Restrict Modify/Cancel prevents customer changes to appointments
- Require Comments mandates customer input during booking
- Settings can be configured per location for same service

**Source:** 05. Products & Services Script.docx.md

#### Lobby Settings per Service
- Time Standard defines expected service duration in lobby
- Show in Check-In/Wrap-up controls visibility in lobby workflows
- Show in Kiosk controls kiosk display
- Settings can be configured per location for same service

**Source:** 05. Products & Services Script.docx.md

### Lobby Queue Rules

#### Check-In Requirements
- First Name and Last Name are mandatory fields
- Account Number, Phone, Email, DOB, Custom fields are optional (visibility controlled in Global Settings)
- At least one product/service can be selected (mandatory selection configurable in Kiosk settings)
- Staff preference and notification group selection are optional

**Source:** 07. Lobby Script.docx.md, 13. Kiosk Configuration Script.docx.md

#### Text Message Opt-In
- Phone number required for text message opt-in
- Text notification toggle must be enabled in Global Settings
- Customer must check "Receive Text Message" during check-in

**Source:** 07. Lobby Script.docx.md, 12. Global Settings Script.docx.md

#### Interaction Limits
- Maximum 5 interactions per visitor record
- Each "Return to Lobby" counts as one interaction
- On 5th interaction, "Return to Lobby" button disabled
- Staff must wrap up visitor on 5th interaction

**Source:** 07. Lobby Script.docx.md

#### Sign-In Requirements for Assistance
- Staff can check in visitors without being signed into lobby
- Staff must be signed in to appear in staff preference selections
- Unsigned staff can still assist via impersonation

**Source:** 07. Lobby Script.docx.md

### Staff Status Rules

#### Force Sign-Out Restrictions
- User cannot sign out themselves via force sign-out
- Idle users can be signed out immediately
- Assisting users require confirmation before sign-out
- Force sign-out disabled when user is last one signed in at branch
- Force sign-out disabled when assisting record is on 5th interaction

**Source:** 07. Lobby Script.docx.md

#### Float Location Rules
- Float locations visible in Lobby Queue and Appointment Queue filters
- Float locations appear on Home dashboard
- Users can view appointment requests from float branches
- Users can assist float-location visitors through lobby

**Source:** 07. Lobby Script.docx.md

### Impersonation Rules

#### Impersonation Enablement
- Global impersonation setting must be enabled in Global Settings first
- User-level "Enable User Impersonation" allows user to impersonate others
- User-level "Show User for Impersonation" allows user to be impersonated
- Both settings only visible if global impersonation is enabled

**Source:** 08. Impersonation & Transfers Script.docx.md

#### Impersonation Eligibility
- Only signed-out staff can be impersonated
- Staff must have "Show User for Impersonation" enabled
- Impersonating user can assist up to 25 visitors concurrently

**Source:** 08. Impersonation & Transfers Script.docx.md

#### Transfer Rules
- Impersonated assists can be transferred to other eligible users
- Transfer All moves all assists to single user
- Transfer Individually assigns specific assists to different users
- New users receive automatic notification when assists transferred
- Original impersonation identity maintained after transfer

**Source:** 08. Impersonation & Transfers Script.docx.md

### Appointment Rules

#### Scheduling Constraints
- Future Availability Window defines how far ahead appointments can be booked
- Appointment Cut-Off Window defines deadline for edits/cancellations
- Allowed Lead Time defines minimum advance booking period
- Appointments cannot be scheduled outside operating hours (unless override enabled)

**Source:** 06. Locations Script.docx.md

#### Concurrency Rules
- Concurrency Mode controls max appointments per time slot
- Max Number of Appointments per slot configurable (e.g., 2)
- Multiple appointments, exceptions, and resources can occupy same slot based on setting

**Source:** 06. Locations Script.docx.md

#### Float Staff Scheduling
- Float Travel Pad Time adds buffer for staff travel between branches
- Float Assignment Priority Mode determines which staff assigned first (home vs. float)

**Source:** 06. Locations Script.docx.md, 12. Global Settings Script.docx.md

#### Auto-Wrap Up
- Appointments auto-update status at configured time if not manually wrapped
- Status options: Completed or No Show
- Auto-wrap up time configurable per location

**Source:** 06. Locations Script.docx.md

#### Staff Request Rules
- "Allow Widget User to Request Staff" setting controls customer staff selection
- If disabled, staff assigned automatically
- Staff must be opted in for service and available during time slot

**Source:** 06. Locations Script.docx.md

#### Remote Check-In Rules
- "Allow Remote Check-In" must be enabled at location level
- "Restrict Remote Check-In Outside of Operating Hours" blocks check-ins outside branch hours
- Remote check-in available for appointments only

**Source:** 06. Locations Script.docx.md

### Alert Rules

#### Alert Triggering
- Alerts can trigger immediately upon check-in or after wait time threshold
- Wait time threshold specified in minutes
- Alerts can be filtered by requested users, groups, or products/services
- "All Requests at Location" triggers for any check-in
- "No Requests" triggers when no staff/group/service specified

**Source:** 10. Alerts Script.docx.md

#### Alert Delivery
- Delivery methods: System Alert, Email, SMS, or All
- SMS requires phone number in user profile or additional numbers specified
- Notify Offline option sends alerts even when users not signed into portal
- Notify Offline not applicable for email list notifiers

**Source:** 10. Alerts Script.docx.md

#### Skilled User Alerts
- Alerts can target users proficient in specific product/service
- System identifies staff with service opt-in and proficiency > 0

**Source:** 10. Alerts Script.docx.md

### Text Message Rules

#### Automated Text Types
- Walk-in: Triggered when walk-in customer checks in
- Appointment: Triggered when appointment customer checks in
- Remote Check-In: Triggered when customer performs remote check-in
- Queue: Triggered based on queue position (e.g., position = 1 means next in line)

**Source:** 11. Text Messages Script.docx.md

#### Text on Demand
- Available only for visitors who opted in for text messages
- Character limit: 350 characters
- All messages logged in Text On Demand History
- History filterable by date range, location, staff member, keyword

**Source:** 11. Text Messages Script.docx.md

#### Message Customization
- Templates support dynamic chips (CustomerFirstName, LocationDisplayName, etc.)
- Chips vary by message type
- Reset to Default restores original template (irreversible)
- Currently English language only

**Source:** 11. Text Messages Script.docx.md

### Kiosk Rules

#### Display Options
- Sign In, Appointment Check-In, and Schedule Appointment cards controlled by configuration
- Optional fields can be marked as visible, mandatory, or both
- Service selection can be made mandatory
- Show Categories groups products/services by category

**Source:** 13. Kiosk Configuration Script.docx.md

#### Wait Time Display
- Wait time calculation methods: average over time, visitors served, or real-time queue
- Wait time can be shown on home page and/or confirmation screen
- Queue position can be displayed alongside wait time

**Source:** 13. Kiosk Configuration Script.docx.md

#### Auto-Refresh
- Kiosk returns to home screen after configured refresh interval
- Refresh interval specified in kiosk settings

**Source:** 13. Kiosk Configuration Script.docx.md, 14. Kiosk Script.docx.md

### Data Import Rules

#### Import File Types
- Supported types: Locations, Holidays, Operating Hours, Product Categories, Products & Services, User Availability, User Skills, Users
- Files must be in CSV format
- Import Logs provide success/failure feedback per record

**Source:** 15. Data ImportExport & Localization Script.docx.md

### Reporting Rules

#### Filter Templates
- Templates can be saved and reused
- Templates can be shared with other users
- One template can be marked as Default (auto-applied on report open)
- Templates apply to both Lobby Activity and Lobby Editor reports

**Source:** 17. Reporting Script.docx.md

#### Lobby Editor Restrictions
- Records can be edited after the fact for auditing purposes
- Customer information, interaction details, and services provided are editable
- Multiple interactions shown separately for multi-interaction records
- Records can be deleted individually or in bulk

**Source:** 17. Reporting Script.docx.md

### Status Transitions

#### Lobby Record Status
- Possible statuses: Waiting, Assisting, Completed, Left Without Assistance, No Show
- Status changes based on staff actions (assist, wrap up, LWA, etc.)
- Auto-wrap up can transition to Completed or No Show

**Source:** 07. Lobby Script.docx.md, 17. Reporting Script.docx.md

#### Appointment Status
- Statuses include: Scheduled, Checked In, Assisting, Completed, No Show, Cancelled
- Check-in transitions appointment to lobby queue
- Manual wrap-up or auto-wrap up transitions to Completed or No Show

**Source:** 07. Lobby Script.docx.md, 06. Locations Script.docx.md

### Validation Rules

#### User Validation
- Email address used as username (must be unique)
- Permission group required for user creation
- Home location required for user creation
- Active status required for login (all clients)
- Login Enabled required for Appointment Concierge clients

**Source:** 04. Users & My Account Script.docx.md

#### Location Validation
- Location Code must be unique
- Location Type must be specified (Organization, Area, Region, Branch)
- Time Zone required
- Parent required for non-Organization types

**Source:** 06. Locations Script.docx.md

#### Service Validation
- Service Name and Service Code required
- Category assignment required
- Type (Product or Service) required
- Language selection required

**Source:** 05. Products & Services Script.docx.md

#### Appointment Validation (Kiosk Check-In)
- Confirmation number OR (last name + appointment time) required
- Details must match existing appointment
- Error shown if validation fails

**Source:** 14. Kiosk Script.docx.md

---

## Customization

### Tenant Customization
- **Client Display Name:** Customizable in Global Settings, appears across UI, emails, browser tabs
- **Client Logo:** Uploadable in Global Settings, auto-adjusted for all platforms/devices
- **Email Settings:** Customizable From Display Name, Reply Address, From Email, Sender Address, Admin Email
- **Timeout Duration:** Configurable session timeout
- **Default Location Address:** Displayed when location sharing disabled (Widget only)

**Source:** 12. Global Settings Script.docx.md

### Workflow Customization
- **Default Lobby Tab:** Configurable per user (Lobby Queue, Appointment Status, Central Views)
- **Float Assignment Priority Mode:** Determines home vs. float staff priority
- **Concurrency Mode:** Controls appointment slot capacity
- **Auto-Wrap Up Behavior:** Choose Completed or No Show status
- **Impersonation Enablement:** Global and per-user control

**Source:** 04. Users & My Account Script.docx.md, 06. Locations Script.docx.md, 12. Global Settings Script.docx.md

### Role Customization
- **Permission Groups:** Fully customizable feature-level access across Administrative, Lobby, Analytics, Appointments
- **Notification Groups:** Custom groups for alert targeting
- **Supervisor Assignments:** Configurable per user
- **Eligible Supervisor:** Users can be marked as eligible supervisors

**Source:** 03. Permission Groups Script.docx.md, 04. Users & My Account Script.docx.md

### Form Customization
- **Optional Fields Visibility:** Control display of Account Number, Phone, Email, DOB, Custom fields in Lobby and Kiosk
- **Mandatory Field Configuration:** Mark optional fields as mandatory in Kiosk settings
- **Custom Fields:** Support for custom data fields in check-in forms
- **Checklist Customization:** Define service-specific checklists with custom items and display text

**Source:** 07. Lobby Script.docx.md, 09. LWA & Checklists Script.docx.md, 12. Global Settings Script.docx.md, 13. Kiosk Configuration Script.docx.md

### Branding Customization
- **Kiosk Branding:** Customizable through backend (not Admin Portal)
- **Admin Portal Branding:** Fixed to FMSI branding
- **Welcome/Thank-You Messages:** Customizable per kiosk
- **Alert Chime:** Customizable notification sound

**Source:** OneCX.html, 12. Global Settings Script.docx.md, 13. Kiosk Configuration Script.docx.md

### Localization Customization
- **Multi-Language Support:** English and Spanish
- **Application-Specific Text:** Customize text for FMSI OneCX, Kiosk, Remote Check-In Web Page
- **Appointment Localization:** Separate localization tab under Appointments → Administration
- **System Text Keys:** All UI text customizable via Localization module

**Source:** 15. Data ImportExport & Localization Script.docx.md

### Display Customization
- **Product/Service Display Order:** Global and category-based ordering per branch
- **Product Category Display Order:** Drag-and-drop ordering for categories
- **Checklist Item Order:** Drag-and-drop ordering for checklist items
- **Staff Status Display Text:** Customizable in Global Settings
- **Kiosk Font Size:** Configurable for product/service display

**Source:** 05. Products & Services Script.docx.md, 06. Locations Script.docx.md, 09. LWA & Checklists Script.docx.md, 12. Global Settings Script.docx.md, 13. Kiosk Configuration Script.docx.md

### Notification Customization
- **Text Message Templates:** Customizable with dynamic chips per message type
- **Email Templates:** Appointment confirmation, reminder, update emails with checklist integration
- **Reminder Timing:** Configurable hours before appointment for email and SMS reminders
- **Summary Email Time:** Configurable time of day for daily appointment summaries
- **Confirmation Email Sender:** Can be sent from assigned employee (configurable)

**Source:** 05. Products & Services Script.docx.md, 06. Locations Script.docx.md, 11. Text Messages Script.docx.md, 12. Global Settings Script.docx.md

---

## Open Questions

### Question 1: Permission Group Migration Mapping
**Question:** What is the exact mapping logic when migrating permission groups from Appointment Concierge and Lobby Tracker to OneCX?

**Reason:** The script mentions "permissions from these platforms are automatically mapped to equivalent permissions in OneCX" but doesn't specify the mapping rules or how conflicts are resolved.

**Source:** 03. Permission Groups Script.docx.md

### Question 2: Kiosk Branding Backend Configuration
**Question:** What is the process and interface for customizing kiosk branding through the backend, since it's not available in the Admin Portal?

**Reason:** OneCX.html states "Kiosk branding is customizable through the backend" but no backend configuration process is documented in the BA scripts.

**Source:** OneCX.html

### Question 3: Client Migration Data Scope
**Question:** When enabling "client migration from Appointments and Lobby" during client creation, what specific data is migrated and what is excluded?

**Reason:** Client creation mentions migration enablement but doesn't detail which entities, configurations, or historical data are included in the migration.

**Source:** OneCX.html

### Question 4: SOC Report Generation and Distribution
**Question:** What is the exact schedule, content, and recipient configuration for auto-generated SOC reports?

**Reason:** SOC reports are mentioned as "auto-generated at a time specified from the backend and automatically emailed to users" but timing, content, and recipient configuration are not documented.

**Source:** OneCX.html

### Question 5: Custom Field Configuration
**Question:** How are custom fields defined, configured, and managed in the system?

**Reason:** Multiple scripts reference "custom fields" as optional input fields in lobby and kiosk, but no configuration workflow or field definition process is documented.

**Source:** 07. Lobby Script.docx.md, 13. Kiosk Configuration Script.docx.md, 17. Reporting Script.docx.md

### Question 6: Just-In-Time Provisioning Details
**Question:** What are the specific rules and field mappings for Just-In-Time user provisioning during SSO authentication?

**Reason:** Global Settings mentions JIT provisioning configuration and domain mapping, but the actual provisioning logic, default permission assignments, and field mappings are not specified.

**Source:** 12. Global Settings Script.docx.md

### Question 7: Analytics and Scheduler File Export
**Question:** What is the "Analytics and Scheduler File Export" referenced in Global Settings, and what data does it contain?

**Reason:** Global Settings mentions "Day To Regenerate Previous Month's Data for Analytics and Scheduler File Export" but the purpose, format, and content of this export are not explained.

**Source:** 12. Global Settings Script.docx.md

### Question 8: Appointment Web Widget Hosting
**Question:** Is the Appointments Web Widget hosted separately from OneCX, and how is it configured and deployed?

**Reason:** Widget is referenced as customer-facing interface accessible from kiosk and web, but hosting, URL structure, and deployment process are not documented.

**Source:** 06. Locations Script.docx.md, 14. Kiosk Script.docx.md

### Question 9: Reference Number Usage
**Question:** What is the business purpose and downstream usage of service reference numbers entered during wrap-up?

**Reason:** Reference numbers are mentioned as optional fields during wrap-up and in reporting, but their purpose, format requirements, and how they're used in business processes are not explained.

**Source:** 07. Lobby Script.docx.md, 17. Reporting Script.docx.md

### Question 10: Multi-Domain SSO Behavior
**Question:** When multiple domains are configured for a client with one marked as default, how does the system determine which domain to use during authentication?

**Reason:** Global Settings mentions multi-domain support with default designation, but the authentication flow and domain selection logic are not specified.

**Source:** 12. Global Settings Script.docx.md

### Question 11: Interaction Alert Configuration
**Question:** What are "interaction alerts" mentioned in Global Settings Lobby Settings, and how are they configured?

**Reason:** Global Settings references "interaction alerts" as a configurable option but provides no details on what triggers them or how they function.

**Source:** 12. Global Settings Script.docx.md

### Question 12: Browser Pop-Up Configuration
**Question:** What is the "browser pop up" setting in Global Settings Lobby Settings, and what does it control?

**Reason:** Mentioned as a configurable option but no explanation of its purpose or behavior is provided.

**Source:** 12. Global Settings Script.docx.md

### Question 13: Event Scheduling vs. Appointments
**Question:** What is the difference between "events" and "appointments" in the system, and how do they function differently?

**Reason:** Multiple references to "Use Events" settings for locations and users, but the distinction between events and appointments is not explained.

**Source:** 04. Users & My Account Script.docx.md, 06. Locations Script.docx.md

### Question 14: Appointment Action Center
**Question:** What is the "Action Center" mentioned in the Appointments module, and what workflows does it support?

**Reason:** Introduction script mentions "view action center" under Appointments but no details on its purpose or functionality are provided.

**Source:** 01. Login & Introduction Script.docx.md

### Question 15: Appointment Exceptions
**Question:** What are "appointment exceptions" and how are they created, managed, and resolved?

**Reason:** Appointments module mentions "exceptions and events" management but exception types, creation process, and resolution workflows are not documented.

**Source:** 01. Login & Introduction Script.docx.md

### Question 16: Proficiency Scoring Logic
**Question:** Is there a specific algorithm or business rule for how proficiency scores (0-100) affect staff assignment or scheduling priority?

**Reason:** Proficiency is used for skilled user alerts and employee settings, but whether higher proficiency affects automatic assignment or is purely informational is unclear.

**Source:** 05. Products & Services Script.docx.md, 10. Alerts Script.docx.md

### Question 17: Lobby vs. Appointment Licensing
**Question:** How does licensing work when a location has both Lobby Tracker and Appointment Concierge enabled? Are there feature conflicts or dependencies?

**Reason:** Locations can have one or both licenses, and some features are license-specific, but interaction between the two is not fully explained.

**Source:** 06. Locations Script.docx.md

### Question 18: Time Zone Conflict Resolution
**Question:** When a user's preferred time zone differs from their location's time zone, which takes precedence for appointment scheduling and display?

**Reason:** OneCX.html mentions both Location Time Zones and User Preferred Time Zones but doesn't specify conflict resolution rules.

**Source:** OneCX.html

### Question 19: Restrict Scheduling Outside Operating Hours
**Question:** What happens when "restrict user being scheduled outside operating hours" is enabled but the user has availability defined outside those hours?

**Reason:** User settings mention this restriction but the interaction with availability templates is not clarified.

**Source:** 04. Users & My Account Script.docx.md

### Question 20: Default Notification Group in Kiosk
**Question:** How does the "default group notification" setting in kiosk Additional Settings affect check-in behavior?

**Reason:** Setting is mentioned but its impact on staff assignment or alert triggering is not explained.

**Source:** 13. Kiosk Configuration Script.docx.md
