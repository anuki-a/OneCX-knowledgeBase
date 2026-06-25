# OneCX Product Overview

## Product Purpose

OneCX is a visitor management and customer engagement platform designed for banks and credit unions to streamline lobby operations, appointment scheduling, and customer service delivery across multiple branches.

**Sources:** 01. Login & Introduction Script.docx.md, OneCX.html

## Target Users and Roles

- **Super Users (FMSI Default Users):** Manage multi-tenant client environments, create new clients, switch between clients
- **Client Admins:** Configure system-wide settings, manage locations, users, products/services, and operational parameters
- **Supervisors:** Monitor staff performance, manage team assignments, force sign-outs
- **Staff Members:** Assist visitors, manage lobby queues, handle appointments, sign in/out of branches
- **Customers/Visitors:** Check in via kiosk or staff assistance, schedule appointments, receive notifications
- **Executives:** View SOC reports and analytics

**Sources:** 01. Login & Introduction Script.docx.md, 03. Permission Groups Script.docx.md, 04. Users & My Account Script.docx.md, OneCX.html

## Main Business Areas

### User Management
- User profile creation and maintenance
- Permission group configuration (access control)
- Notification group setup (alert targeting)
- Multi-location access hierarchy

**Sources:** 01. Login & Introduction Script.docx.md, 03. Permission Groups Script.docx.md, 04. Users & My Account Script.docx.md

### Locations & Services
- Hierarchical location structure (Organization → Area → Region → Branch)
- Operating hours and holiday management
- Product/service catalog configuration
- Service checklists and display ordering

**Sources:** 01. Login & Introduction Script.docx.md, 05. Products & Services Script.docx.md, 06. Locations Script.docx.md

### Lobby Management
- Real-time visitor queue management
- Staff status tracking and sign-in/out
- Walk-in and appointment check-ins
- Visitor wrap-up and service completion
- Central views across all branches

**Sources:** 01. Login & Introduction Script.docx.md, 02. Home Script.docx.md, 07. Lobby Script.docx.md

### Appointments
- Appointment scheduling and management
- Exception and event handling
- Action center for appointment workflows
- Appointment reporting and analytics
- Widget-based customer self-service

**Sources:** 01. Login & Introduction Script.docx.md, 06. Locations Script.docx.md, 07. Lobby Script.docx.md

### Configuration
- Global settings (licensing, authentication, branding)
- Kiosk configuration per branch
- Text message templates and automation
- Alert configuration (global and personal)
- Data import/export capabilities
- Localization (English/Spanish)

**Sources:** 01. Login & Introduction Script.docx.md, 12. Global Settings Script.docx.md, 13. Kiosk Configuration Script.docx.md

### Reporting & Analytics
- Lobby activity reports (multiple views)
- Lobby editor for record auditing/editing
- Performance metrics and KPIs
- SOC reports (auto-generated)

**Sources:** 01. Login & Introduction Script.docx.md, 17. Reporting Script.docx.md, OneCX.html

## Main Feature Groups

### Authentication & Access Control
- Username/password or ADFS single sign-on
- Two-factor authentication
- Password expiration policies
- Just-In-Time provisioning for SSO
- Multi-domain support per client
- Session timeout management (default: 90 minutes)

**Sources:** 04. Users & My Account Script.docx.md, 12. Global Settings Script.docx.md, OneCX.html

### Client Management (Multi-Tenancy)
- Multi-tenant architecture with strict data isolation
- Client creation with database allocation and domain mapping
- Legacy data migration from Appointments and Lobby platforms
- Client switching capability for super users
- White-label branding customization

**Sources:** OneCX.html

### Location Hierarchy & Configuration
- Four-tier structure: Organization, Area, Region, Branch
- Time zone management (location-based and user-preferred)
- Contact information and geolocation (latitude/longitude)
- Operating hours with multiple time slots per day
- Holiday provisioning and opt-in/out at branch level
- Product/service opt-in per location

**Sources:** 06. Locations Script.docx.md, OneCX.html

### Product & Service Management
- Product categories with icons and display names
- Service types: Product vs. Service
- Multi-language support (English/Spanish)
- Proficiency-based skill assignment (0-100 scale)
- Display order customization (global and category-based)
- Opt-in settings per location and employee
- Appointment settings (duration, meeting preferences, restrictions)
- Lobby settings (time standards, visibility controls)

**Sources:** 05. Products & Services Script.docx.md, 06. Locations Script.docx.md

### Lobby Operations
- Multiple check-in sources: staff-assisted, kiosk, remote
- Queue management with wait time tracking
- Staff preference and group selection
- Spanish speaker preference
- Service checklists during wrap-up
- Reference number tracking per service
- Up to 5 interactions per visitor record
- Left Without Assistance (LWA) tracking with reasons
- Text on Demand for ad-hoc customer messaging

**Sources:** 07. Lobby Script.docx.md, 09. LWA & Checklists Script.docx.md, 11. Text Messages Script.docx.md

### Appointment Management
- Future availability window configuration
- Appointment cut-off window for edits/cancellations
- Concurrency mode (max appointments per slot)
- Float assignment priority modes
- Auto-wrap up with status transitions
- Staff request capability in widget
- Remote check-in for appointments
- Reminder emails and SMS notifications
- Summary email scheduling

**Sources:** 06. Locations Script.docx.md, 07. Lobby Script.docx.md

### Staff Management
- Home location and float location assignments
- Availability templates with multiple rotations
- Meeting preferences (In-Person, Phone, Virtual)
- Supervisor assignments and eligibility
- Impersonation capabilities (up to 25 concurrent)
- Transfer assists between staff members
- Flexible float capabilities
- Daily/summary email subscriptions

**Sources:** 04. Users & My Account Script.docx.md, 08. Impersonation & Transfers Script.docx.md

### Kiosk Self-Service
- Customizable check-in display options
- Optional input fields (account number, phone, email, DOB, custom)
- Staff and group preference selection
- Product/service selection with category grouping
- Wait time and queue position display
- Welcome and thank-you message customization
- Language preferences (English/Spanish)
- Appointment validation and check-in
- Integration with Appointments Web Widget

**Sources:** 13. Kiosk Configuration Script.docx.md, 14. Kiosk Script.docx.md

### Alerts & Notifications
- Global alerts (assigned to users/groups)
- Personal alerts (My Alerts)
- Multiple delivery methods: System Alert, Email, SMS
- Trigger conditions: immediate or wait-time threshold
- Request-based filtering (users, groups, products/services)
- Offline notification support
- Notification group targeting
- Alert chime customization

**Sources:** 10. Alerts Script.docx.md

### Text Messaging
- Automated SMS for walk-in, appointment, remote check-in, queue position
- Customizable message templates with dynamic chips
- Text on Demand for ad-hoc staff-to-customer messaging
- Text notification opt-in at check-in
- Message history tracking
- Character limit: 350 characters for ad-hoc messages

**Sources:** 11. Text Messages Script.docx.md

### Data Management
- Bulk import via CSV (locations, holidays, hours, categories, products, users, availability, skills)
- Import logs with success/failure tracking
- Data export for system data retrieval
- Localization for multiple applications (OneCX, Kiosk, Remote Check-In)
- Multi-language text customization

**Sources:** 15. Data ImportExport & Localization Script.docx.md

### Reporting & Analytics
- **Location Comparison:** Branch performance benchmarking
- **Traffic & Wait Time:** Peak analysis by hour/day/week/month
- **Products & Services:** Service demand analysis
- **Employee:** Individual staff performance tracking
- **Details:** Granular interaction-level data
- **Staff Signed In/Out:** Presence and time tracking
- Filter templates (savable, shareable, default)
- Drill-down capabilities
- Excel export functionality
- Lobby Editor for record auditing and correction

**Sources:** 17. Reporting Script.docx.md

## High-Level System Capabilities

- **Real-time Operations:** Live queue management, KPI tracking, staff status monitoring
- **Multi-Channel Access:** Admin portal, kiosk, web widget, remote check-in
- **Cross-Location Visibility:** Central views aggregating data across all accessible branches
- **Customization:** Per-branch configuration for kiosks, products, services, and workflows
- **Migration Support:** Automatic permission mapping from legacy Appointment Concierge and Lobby Tracker platforms
- **Scalability:** Multi-tenant architecture supporting multiple financial institutions
- **Compliance:** SOC reporting, audit trails, data isolation
- **Accessibility:** Multi-language support, timezone awareness, mobile-responsive interfaces

**Sources:** 01. Login & Introduction Script.docx.md, 02. Home Script.docx.md, 07. Lobby Script.docx.md, OneCX.html

## Relationships Between Business Areas

- **User Management ↔ Locations:** Users assigned to home locations with hierarchical access to sub-locations
- **Locations ↔ Products/Services:** Products/services opt-in at location level; display order customizable per branch
- **Users ↔ Products/Services:** Skill-based proficiency assignments; employee opt-in per service
- **Lobby ↔ Appointments:** Appointment queue visible in lobby; appointments can check into lobby
- **Permission Groups ↔ Alerts:** Notification groups used for alert targeting
- **Kiosk ↔ Configuration:** Kiosk behavior driven by branch-specific configuration settings
- **Lobby ↔ Reporting:** All lobby interactions feed into reporting and analytics
- **Global Settings ↔ All Modules:** System-wide defaults cascade to location and user levels

**Sources:** 03. Permission Groups Script.docx.md, 04. Users & My Account Script.docx.md, 05. Products & Services Script.docx.md, 06. Locations Script.docx.md, 07. Lobby Script.docx.md

## Important Terminology and Definitions

- **Branch:** Physical service location where customers are served
- **Float Location:** Additional locations where a staff member can assist customers beyond their home location
- **Home Location:** Primary location assigned to a user, determining their access hierarchy
- **Lobby Queue:** Real-time list of visitors waiting for assistance
- **Appointment Queue:** List of scheduled appointments for a given day/location
- **Check-In:** Process of adding a visitor to the lobby queue (walk-in or appointment arrival)
- **Wrap-Up:** Process of completing service delivery and recording services provided
- **Assist:** Active service interaction between staff and visitor
- **Interaction:** Single assist session; visitors can have up to 5 interactions before mandatory wrap-up
- **Left Without Assistance (LWA):** Visitor who leaves before being served, with tracked reason
- **Impersonation:** Staff member assisting visitors on behalf of another staff member
- **Permission Group:** Role-based access control defining feature-level permissions
- **Notification Group:** Group of users targeted for alert notifications
- **Product/Service (P/S):** Offerings available for customer selection during check-in or appointments
- **Proficiency:** Skill level (0-100) indicating staff expertise in providing a service
- **Opt-In:** Configuration flag enabling a feature, service, or location for use
- **Concurrency Mode:** Setting controlling how many appointments can occur simultaneously
- **Time Standard:** Expected duration for service delivery in lobby context
- **Remote Check-In:** Customer checking into lobby before physically arriving at branch
- **Widget:** Customer-facing web interface for appointment scheduling
- **Central Views:** Aggregated cross-location views of lobby, staff, and performance metrics
- **SOC Reports:** System and Organization Controls compliance reports
- **Just-In-Time Provisioning:** Automatic user account creation during SSO authentication
- **Multi-Tenancy:** Architecture supporting multiple isolated client environments in single system

**Sources:** 01. Login & Introduction Script.docx.md, 03. Permission Groups Script.docx.md, 04. Users & My Account Script.docx.md, 05. Products & Services Script.docx.md, 06. Locations Script.docx.md, 07. Lobby Script.docx.md, 08. Impersonation & Transfers Script.docx.md, 09. LWA & Checklists Script.docx.md, OneCX.html
