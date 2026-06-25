# JRNI Software - Product Analysis

## 1. Product Purpose

- **In-Person Interaction Platform** combining appointment scheduling, queue management, analytics, and experiential events [JR1]
- Enables enterprises to optimize customer engagement across every channel (appointments, walk-ins, digital, events) at scale [JR1][JR2]
- Transforms operational metrics into relationship intelligence for data-driven decision making [JR2]
- Designed to drive increased revenue per customer, improve staff productivity, boost customer retention, and enable clear ROI reporting [JR1]
- Makes every brand moment matter by smoothing the digital-physical handoff between online and in-store experiences [JR1]
- Purpose-built to deliver seamless, personalized service at scale without losing efficiency or insight [JR2]

## 2. Target Customers

- **Primary:** Banks, credit unions, and financial services institutions across North America [JR2][JR3]
- **Named customers:** Oriental Bank (Puerto Rico), Independent Bank (Michigan), Raymond James (wealth management), M&T Bank, Arvest Bank [JR7 - Case Study][JR8 - Case Study][JR9 - Video]
- Financial institutions seeking to improve loan pull-through rates, reduce handle time, and raise customer satisfaction [JR2]
- Organizations with complex branch operations, multiple lines of business, and high-value client journeys [JR2]
- Wealth management firms requiring enterprise-level appointment scheduling for advisors [JR9 - Video]
- **Scale:** 20+ countries, 5 continents, 25+ languages, 20,000+ users enabled, 1,000,000+ engagements facilitated, $2 billion annual commerce through JRNI [JR1]

## 3. Business Capabilities

- **Appointment Scheduling:** Enterprise-grade one-to-one appointment booking with AI matching to drive appointment volume [JR1][JR4]
- **Queue Management:** Virtual and physical queue management to reduce wait times and maximize staff efficiency [JR1][JR5]
- **Event Management:** One-to-many event booking with VIP workflows, guest list management, and QR code check-in [JR1][JR10 - Webinar]
- **Analytics & Insights:** Real-time dashboards, interactive reports, conversational analytics, and ROI tracking [JR1][JR6]
- **Customer Experience Hub:** Kiosk-based check-in for walk-ins and event attendees with QR code scanning [JR10 - Webinar]
- **Coordinator App:** Mobile progressive web app for staff to manage events, guest lists, and on-ground execution [JR10 - Webinar]
- **Security Center:** Centralized administrative console consolidating platform security features [JR10 - Webinar]

## 4. Features

### Appointment Scheduling [JR4]
- AI-powered matching to connect customers with right staff based on expertise, language, and availability
- Multi-staff and multi-service bookings
- Specific staff member selection or automatic assignment
- Holiday and location closure management
- CRM integration with real-time calendar sync
- Automated reminders via SMS and email
- Flexible rescheduling and cancellation
- In-person, video, and phone appointment options
- Custom booking questions and intake forms
- Personalized booking links for email signatures

### Queue Management [JR5]
- Virtual queuing (join from anywhere)
- Physical queue management for walk-in traffic
- Real-time wait time tracking and display
- Next-in-line SMS/email notifications
- Custom intake questions during check-in
- Appointment conversion (walk-in to scheduled)
- Multi-service walk-in support
- Real-time queuing dashboard for operational visibility [JR10 - Webinar]

### Event Management [JR10 - Webinar]
- Template-based HTML invitations with drag-and-drop editor (WYSIWYG arriving Q2 2026)
- Locked invites (VIP-only) or public event registration
- RSVP and registration workflows with pre-filled customer information
- QR code generation for day-of check-in
- Real-time guest list with status tracking (invited, registered, checked in)
- On-site guest addition and registration
- CSV bulk upload for guest lists with timestamp tracking
- Coordinator app for mobile event management
- Experience Hub kiosk integration for check-in

### Analytics & Insights [JR6][JR11 - Webinar]
- Embedded analytics platform integrated directly in Studio (no window switching)
- Role-based access control with SSO support
- Interactive dashboards with self-serve reporting
- Email delivery options for reports (PDF, image formats)
- Headquarters dashboard: YTD/MTD appointments, cancellation percentage, year-over-year analysis
- Appointments by day of week, most popular services, busiest locations
- How appointments were made (website, staff, call center)
- Canceled bookings by service to identify improvement areas
- Average wait time and duration tracking
- Bookings by status (not-yet-started, checked in, being seen, completed, no-show)
- Most engaged staff rankings with filtering
- Days booked in advance and cancellation lead time analysis
- Geographic heat maps for booking density
- Queuing performance metrics per queue/location
- Event analytics: tickets sold, most popular events
- Staff and location utilization tracking
- Demand forecasting and staffing recommendations
- Conversion metrics and lead time tracking

### Security Center [JR10 - Webinar]
- Centralized administrative console for all security features
- Protection against platform abuse and attacks
- Version 1 features deployed with additional capabilities coming soon

### Integration & API [JR12 - API Documentation][JR13 - Developer Hub]
- Comprehensive REST API with Public, Member, and Admin endpoints
- Public APIs for scheduling appointments and service information
- Member APIs for authenticated customer booking management
- Admin APIs for configuration, reporting, and validation bypass
- Real-time booking notification webhooks for custom email/SMS providers
- Webhook payload customization using Liquid templating
- Bulk Import API for staff, schedules, and locations
- Seamless embedding in customer apps and websites
- CRM data sync capabilities (S3, Azure, Google Cloud, SFTP, webhooks)

## 5. User Workflows

### Client Appointment Booking Workflow [JR2][JR4]
1. Client accesses booking via website, digital banking platform, or personalized booking link
2. Selects location, service type, and preferred date/time
3. System shows available advisors based on service and expertise (AI matching)
4. Client completes custom questions/forms
5. Receives confirmation and automated reminders
6. Joins appointment (in-branch, video, or phone)

### Walk-in Queue Management Workflow [JR5]
1. Client arrives at branch or joins virtual queue remotely
2. Checks in via kiosk, staff tablet, or mobile device
3. Answers custom intake questions
4. Receives wait time estimate
5. Gets next-in-line notification via SMS/email
6. Staff sees real-time queue status and customer information

### Event Lifecycle Workflow [JR10 - Webinar]
1. **Invitation:** Customer receives personalized HTML invite (VIP or public)
2. **RSVP & Registration:** Customer taps RSVP, information pre-filled, grants consent, confirms
3. **Confirmation:** Customer receives email with booking details and QR code
4. **Day-of Check-In:** Customer arrives and checks in via Experience Hub kiosk using QR code
5. **Real-time Tracking:** Check-in status reflected immediately in staff Coordinator App

### Staff Event Management Workflow [JR10 - Webinar]
1. Access Coordinator App (progressive web app, no installation)
2. View full guest list with real-time status
3. Add new guests on-site (search existing or create new)
4. Invite, register, or check in guests with single tap
5. Scan QR codes for check-in directly from app
6. Upload guest lists via CSV template
7. Monitor all uploads with timestamps

## 6. User Roles

- **Customers/Clients:** Book appointments, join queues, RSVP to events, check in via kiosks [JR2][JR4][JR5][JR10 - Webinar]
- **Branch Staff/Advisors:** Take appointments, serve walk-ins, view customer information and service history [JR2]
- **Event Coordinators:** Manage events, guest lists, invitations, and on-site check-ins via Coordinator App [JR10 - Webinar]
- **Administrators:** Configure services, staff, locations, security settings, and system-wide parameters [JR12 - API Documentation]
- **Managers/Analysts:** Access analytics dashboards, generate reports, monitor performance across locations [JR6][JR11 - Webinar]
- **Developers/Integration Teams:** Use REST APIs, webhooks, and bulk import tools for system integration [JR12 - API Documentation][JR13 - Developer Hub]
- **Technical Account Managers (TAM):** Perform deep-level analysis of booking data for appointments, events, and optimization [JR10 - Webinar]

## 7. AI Capabilities

- **AI Matching:** Intelligent routing of clients to right advisor based on expertise, language, relationship value, and availability [JR1][JR4]
- **Demand Forecasting:** AI-driven predictions for daily, weekly, and monthly appointment and walk-in demand [JR2]
- **Smart Scheduling:** AI recommendations for optimal staffing based on forecasted demand patterns [JR2]
- **Conversational Analytics:** Plain-language queries to extract insights from data without technical knowledge [JR6][JR11 - Webinar]
- **Behavioral Insights:** AI analysis of customer patterns including arrival time, check-in status, areas of interest, and product preferences [JR1]

## 8. Reporting & Analytics

- **Insight Hub:** Embedded analytics platform with interactive dashboards integrated directly in Studio [JR6][JR11 - Webinar]
- **Pre-built Dashboards:** Headquarters dashboard, appointments dashboard, queuing dashboard, events dashboard [JR11 - Webinar]
- **Key Metrics Tracked:**
  - Total appointments (YTD, MTD), cancellation percentage, year-over-year comparisons [JR11 - Webinar]
  - Appointments by day of week, most popular services, busiest locations [JR11 - Webinar]
  - How appointments were made (website 70%, staff 30%, call center <1%) [JR11 - Webinar]
  - Canceled bookings by service [JR11 - Webinar]
  - Average wait time and duration [JR11 - Webinar]
  - Bookings by status (not-yet-started, checked in, being seen, completed, no-show) [JR11 - Webinar]
  - Most engaged staff and most booked services [JR11 - Webinar]
  - Days booked in advance and cancellation lead time [JR11 - Webinar]
  - Geographic heat maps for booking density [JR11 - Webinar]
  - Queue performance, event tickets sold, staff utilization [JR11 - Webinar]
- **Core KPIs:** Volume, velocity, leakage, productivity, conversion rates, NPS tracking, no-show rates [JR1][JR2]
- **Sharing Options:** Secure web links, downloads, email delivery in PDF or image formats [JR11 - Webinar]
- **Role-Based Access:** Data segregated by role (store managers see only their store, HQ sees all) [JR11 - Webinar]
- **Customization:** Date range filtering, custom chart additions, threshold filtering [JR11 - Webinar]
- **TAM Program:** Technical Account Manager team provides deep-level analysis of booking data [JR10 - Webinar]

## 9. Integrations

- **CRM Systems:** Real-time calendar sync with Microsoft Exchange and Outlook [JR2]
- **Data Connections:** S3, Azure, Google Cloud, SFTP, webhooks for data sync [JR2]
- **E-signature:** DocuSign, OneSpan integration (mentioned for video banking context) [JR2]
- **Video Conferencing:** Zoom partnership for remote appointments [JR8 - Case Study]
- **Core Banking Platforms:**
  - Backbase Engagement Banking Platform (composable banking integration) [JR14 - Integration]
  - Temenos Exchange marketplace availability [JR14 - Integration]
- **Custom Integrations:** REST API with Public, Member, and Admin endpoints [JR12 - API Documentation]
- **Webhooks:** Real-time booking notifications for custom email/SMS providers [JR13 - Developer Hub]
- **Bulk Import API:** Automated staff, schedule, and location management [JR13 - Developer Hub]
- **SSO Support:** Single sign-on for analytics and platform access [JR11 - Webinar]

## 10. Configuration & Customization

- **Configurable Workflows:** Tailored to retail, commercial, and wealth management environments [JR2]
- **Custom Booking Questions:** Personalized intake forms for appointments and walk-ins [JR4][JR5]
- **Service Configuration:** Multi-service appointments, service-specific settings, custom durations [JR4]
- **Staff Management:** Individual staff profiles, expertise tags, language capabilities, availability schedules [JR4]
- **Location Management:** Multi-location support, holiday closures, location-specific settings [JR4]
- **Invitation Templates:** HTML-designed event invitations with drag-and-drop editor (WYSIWYG coming Q2 2026) [JR10 - Webinar]
- **Branding:** Custom branded backgrounds for video appointments [JR2]
- **Access Control:** Role-based permissions for staff, managers, and administrators [JR11 - Webinar]
- **Queue Settings:** Virtual vs. physical queuing, wait time display preferences, notification triggers [JR5]
- **Analytics Customization:** Custom reports, date range filters, threshold settings, chart additions [JR11 - Webinar]
- **Webhook Customization:** Liquid templating for webhook payload design [JR13 - Developer Hub]
- **Security Settings:** Centralized Security Center for platform-wide security configuration [JR10 - Webinar]

## 11. Strengths & Weaknesses

### Strengths
- **Unified Platform:** Single platform for appointments, queuing, events, and analytics eliminates need for multiple vendors [JR1]
- **Enterprise Scale:** Proven at scale with 20,000+ users, 1M+ engagements, $2B annual commerce [JR1]
- **AI-Powered Intelligence:** Smart matching, demand forecasting, and conversational analytics drive efficiency [JR1][JR2][JR6]
- **Embedded Analytics:** Insight Hub integrated directly in Studio eliminates window switching and simplifies access [JR6][JR11 - Webinar]
- **Mobile Staff Experience:** Coordinator App (progressive web app) enables on-ground event management without app installation [JR10 - Webinar]
- **Proven ROI:** Oriental Bank reduced wait times 50%+ (3 min vs 13-14 min), 13K+ monthly bookings [JR7 - Case Study]
- **Enterprise Security:** SOC 2, GDPR, ISO 27001 compliance with centralized Security Center [JR2][JR10 - Webinar]
- **Global Reach:** 20+ countries, 5 continents, 25+ languages supported [JR1]
- **Comprehensive API:** REST API with Public, Member, Admin endpoints plus webhooks and bulk import [JR12 - API Documentation][JR13 - Developer Hub]
- **Financial Services Focus:** Deep expertise in banking, wealth management, and financial institutions [JR2][JR3]
- **No-Show Reduction:** Automated reminders reduce missed appointments by up to 80%, improving confirmed meetings by 25-35% [JR2]
- **Real-Time Visibility:** Live dashboards for queue status, appointment flow, and event check-ins [JR5][JR10 - Webinar][JR11 - Webinar]

### Weaknesses
- **PDF Documentation Accessibility:** Appointments datasheet PDF was unreadable/corrupted, limiting detailed feature documentation access [JR15 - PDF Datasheet]
- **WYSIWYG Editor Delay:** Drag-and-drop invitation editor not available until Q2 2026, requiring HTML knowledge for event invitations [JR10 - Webinar]
- **Limited Industry Diversification:** Heavy focus on financial services may indicate less maturity in other verticals [JR2][JR3]
- **Video Banking Features:** Video banking capabilities (DocuSign, e-signature, screen sharing) mentioned but not deeply documented as core platform features [JR2]
- **Queuing Dashboard Maturity:** Queuing analytics described as having "major improvements soon," suggesting current limitations [JR11 - Webinar]
- **Geographic Heat Maps:** Color-coded density "in progress during beta," indicating incomplete feature [JR11 - Webinar]

## 12. Interesting Ideas

- **Appointment-Driven Culture Shift:** Independent Bank used JRNI to transform from reactive to appointment-driven operations, making banking easier and more convenient [JR8 - Case Study]
- **Digital Delivery First (DDF):** Independent Bank's strategy of designing everything for digital customer experience while maintaining personal touch [JR8 - Case Study]
- **8 Hours/Week Savings:** Raymond James advisors saved 8 hours per week on scheduling, freeing assistants for more productive work [JR9 - Video]
- **25-35% of Branch Services Booked:** Industry data shows quarter to third of banking services are appointment-based, creating significant optimization opportunity [JR2]
- **Interaction Data as Revenue Driver:** Every appointment becomes a source of actionable data for forecasting, staffing, and conversion optimization [JR2]
- **Continuous Improvement System:** Oriental Bank uses real-time data to ensure process changes stick long-term, preventing staff from falling into bad habits [JR7 - Case Study]
- **Channel Fluidity:** JRNI tracks when and why appointments move between channels (in-branch, phone, video) to optimize customer journeys [JR7 - Case Study]
- **QR Code Check-In:** Seamless day-of event check-in via QR codes in confirmation emails, reducing friction [JR10 - Webinar]
- **Progressive Web App:** Coordinator App requires no installation, works on any device, enabling instant staff access [JR10 - Webinar]
- **CSV Upload with Timestamps:** Guest list uploads tracked with timestamps for audit trail and accountability [JR10 - Webinar]
- **Locked Invites:** VIP events can prevent forwarding, ensuring exclusivity [JR10 - Webinar]
- **Centralized Security Console:** Security Center consolidates all security features to protect against platform abuse [JR10 - Webinar]

## 13. Known Limitations & Gaps

- **WYSIWYG Editor Unavailable:** Drag-and-drop invitation editor for events not available until Q2 2026, requiring HTML knowledge for customization [JR10 - Webinar]
- **Queuing Analytics Incomplete:** Queuing dashboard has "major improvements soon," indicating current feature gaps [JR11 - Webinar]
- **Geographic Heat Maps In Progress:** Color-coded density visualization still in beta development [JR11 - Webinar]
- **Custom Chart Catalog Limited:** Chart catalog expansion and custom chart creation planned but not yet available [JR11 - Webinar]
- **Programs Feature in Prototype:** Programs capability shown as preview in prototype stage, not production-ready [JR10 - Webinar]
- **Queuing Enhancements Pending:** Express queue and appointment waitlist for high-demand scenarios coming in Q2 2026 [JR10 - Webinar]
- **Coupons Not Yet Available:** Coupons for appointments planned for Q2 2026 [JR10 - Webinar]
- **Unified Service Model Pending:** Unified service model across multiple modes coming in Q2 2026 [JR10 - Webinar]
- **Insights Hub V2 In Development:** Next version of analytics platform under development for Q2 2026 [JR10 - Webinar]
- **No Explicit Workforce Management:** Unlike competitors (e.g., Coconut Software's bWFM), JRNI does not explicitly mention dedicated workforce management or shift planning features [JR2]
- **Video Banking Not Core:** Video banking features mentioned in context but not positioned as core platform capability like appointments/queuing [JR2]
- **No Explicit Mobile Customer App:** Customer interactions via web/kiosk; no mention of dedicated mobile app for customers [JR4][JR5]

---

## Reference Catalog

### Official Product Pages
- **[JR1]** JRNI Homepage - https://www.jrni.com/ - Enterprise appointments, queue management, events platform overview with global scale metrics (20+ countries, 1M+ engagements, $2B commerce)
- **[JR2]** JRNI for Banks - https://www.jrni.com/banks/ - Banking solution page covering appointments, queuing, analytics, ROI metrics, no-show reduction strategies, and key differentiators for financial institutions
- **[JR3]** JRNI for Financial Services - https://www.jrni.com/financial-services/ - Broader financial services overview including wealth management, insurance, and lending use cases
- **[JR4]** Appointment Scheduling - https://www.jrni.com/platform/appointment-scheduling/ - Enterprise appointment scheduling features including AI matching, multi-staff bookings, CRM integration
- **[JR5]** Queue Management - https://www.jrni.com/platform/queue-management/ - Virtual and physical queue management capabilities, wait time reduction, staff efficiency optimization
- **[JR6]** Analytics Platform - https://www.jrni.com/platform/analytics/ - Analytics and insights capabilities overview, real-time dashboards, behavioral insights, KPI tracking

### Customer Case Studies & Success Stories
- **[JR7 - Case Study]** Oriental Bank Case Study - https://www.jrni.com/resources/oriental-bank/ - 50%+ wait time reduction (3 min vs 13-14 min), 13,000+ monthly bookings, continuous improvement system, channel management insights
- **[JR8 - Case Study]** Independent Bank Case Study - https://www.jrni.com/blog/independent-bank-on-putting-customer-convenience-first/ - Digital Delivery First (DDF) strategy, appointment-driven culture transformation, customer convenience focus, Zoom integration
- **[JR9 - Video]** Raymond James Video Case Study - https://www.jrni.com/resources/raymond-james/ - Wealth management firm's enterprise scheduling rollout, 8 hours/week advisor time savings, assistant productivity improvements

### Webinars & Product Demos
- **[JR10 - Webinar]** March 2026 Product Update - https://www.jrni.com/resources/march-product-2026/ - Latest product releases including Coordinator App (mobile staff experience), Security Center, event management features, Q1/Q2 roadmap, QR code check-in
- **[JR11 - Webinar]** Insight Hub Release Webinar - https://www.jrni.com/resources/insight-hub-release-webinar/ - Analytics platform demo showing embedded dashboards, KQL queries, ROI tracking, role-based access, sharing capabilities

### Developer & API Documentation
- **[JR12 - API Documentation]** JRNI REST API Documentation - https://api-docs.jrni.com/ - Comprehensive API documentation with Public, Member, and Admin endpoints for scheduling, booking management, and configuration
- **[JR13 - Developer Hub]** JRNI Developer Hub - https://dev.jrni.com/ - Developer documentation covering webhooks, bulk import API, integration recipes, Liquid templating for custom notifications

### Integration & Partnership Resources
- **[JR14 - Integration]** Backbase & Temenos Integrations - https://www.jrni.com/news/jrni-now-available-on-the-backbase-engagement-banking-platform/ - JRNI availability on Backbase Engagement Banking Platform and Temenos Exchange marketplace for core banking integration

### Product Datasheets
- **[JR15 - PDF Datasheet]** Appointments Module Datasheet - https://www.jrni.com/wp-content/uploads/2024/07/JRNI_Appointments_Datasheet_2024-2.pdf - 2024 appointments datasheet (Note: File was unreadable/corrupted during research)
