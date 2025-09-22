# Smart TravelConnect CRM

**Author:** Yash Dighade  
**Date:** 22-Sep-2025  
**Technology Stack:** Salesforce Lightning, Apex, LWC, Reports & Dashboards  

---

## Project Overview

Smart TravelConnect CRM is a Salesforce-based solution for mid-sized travel agencies to streamline lead management, travel package booking, payments, customer engagement, and reporting. This project demonstrates end-to-end CRM implementation in Salesforce Lightning, including automation, Apex programming, UI design, integrations, and analytics.

---

## Phase-wise Breakdown

### Phase 1 — Problem Understanding & Industry Analysis
- Gathered requirements: lead capture, package management, booking automation, customer updates via email/SMS/WhatsApp.
- Identified stakeholders: Admin, Sales Agent, Customer, Finance Manager, Marketing Manager.
- Mapped business process: Lead Capture → Qualification → Package Selection → Booking → Payment → Confirmation → Customer Update → Feedback → Reporting.
- Studied industry use cases: MakeMyTrip, Yatra, Thomas Cook.
- Explored Salesforce Travel & Hospitality Cloud; decided to build a simplified, custom solution.

---

### Phase 2 — Org Setup & Configuration
- Created Developer Org: **Smart TravelConnect CRM**.
- Set company profile: Smart Travel Agency Pvt. Ltd., 24x7 business hours.
- Created users: Admin, Sales Agent, Marketing Manager, Finance Manager.
- Configured Profiles & Roles for controlled access.
- Set Organization-Wide Defaults (OWD): Leads = Private, Bookings = Controlled by Role.
- Created Sandbox for testing flows and Apex before production.

---

### Phase 3 — Data Modeling & Relationships
- Created custom objects: Customer__c, Travel_Package__c, Booking__c, Payment__c, Feedback__c, (Optional) Booking_Package__c for M:M relationships.
- Configured fields (text, number, picklist, formula, roll-up summaries).
- Established relationships: Customer → Booking (1:M), Booking → Payment (1:M), Booking ↔ Travel_Package (M:M via junction object).
- Validation rules: Travel start date ≥ Today, End Date ≥ Start Date, Payment Amount > 0.
- Created Record Types & Page Layouts: Individual / Group bookings, Full / Partial payments.
- Used Schema Builder to visualize all relationships.

---

### Phase 4 — Process Automation
> Skipped for simplicity in the basic project version.

---

### Phase 5 — Apex Programming
- Implemented Triggers: Update Booking Status when Payment is received.
- Implemented SOQL Queries for fetching data (example: top destinations).
- Skipped Batch Apex, Queueable Apex, Scheduled Apex, Future Methods in basic version.
- Created Test Classes to cover triggers.

---

### Phase 6 — User Interface Development
- Created Lightning App: **Smart TravelConnect**.
- Configured Tabs: Leads, Customers, Travel Packages, Bookings, Payments, Feedback.
- Designed Record Pages: Customer travel history, Booking details, Payment summary.
- Skipped custom LWC components for simplicity.

---

### Phase 7 — Integration & External Access
- Implemented Payment gateway simulation (Razorpay/PayPal demo).
- Implemented Google Maps API (optional, if configured).
- Skipped Flight & Hotel API integration, Experience Cloud portal, OAuth login.

---

### Phase 8 — Data Management & Deployment
- Used Data Import Wizard to import leads from CSV.
- Used Data Loader to import travel packages in bulk.
- Configured Duplicate Rules to prevent duplicate customers.
- Managed deployment using Change Sets / VS Code + SFDX.

---

### Phase 9 — Reporting & Dashboards
- Created Reports:  
  - **New Travel Packages Report**: Active travel packages list.  
  - **New Leads Report**: Recently created leads.  
- Dashboards: Basic dashboard layout (optional in simple version).  
- Security: OWD applied, Audit Trail enabled.

---

### Phase 10 — Final Presentation & Demo
- Prepared Demo Flow: Lead → Auto-assign → Package Selection → Booking → Payment → Confirmation → Feedback → Dashboard update.
- Created Handoff Documents: Setup guide, User manuals for Agents & Customers.
- Added LinkedIn Showcase: Highlighted Salesforce skills.
- Recorded demo video without audio showing end-to-end navigation.
- Demo Video Link: https://drive.google.com/file/d/1B96EnWgjcngBmjXOyYfGzqVGMp-4eMz6/view?usp=drive_link

---

## Project Outcome
- Fully functional Salesforce CRM for travel agencies (basic version).
- Automated Booking-Payment linkage with triggers.
- Reports and dashboards provide insights.
- Ready for demo, documentation, and showcase.

---

## Skills Demonstrated
- Salesforce Lightning  
- Custom Objects & Relationships  
- Apex Triggers  
- Validation Rules  
- Reports & Dashboards  
- Basic Payment Simulation  

---

