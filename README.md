# Smart TravelConnect CRM 🚀  

A Salesforce-based CRM solution for Travel Agencies that improves **lead conversions, customer satisfaction, and business efficiency**.  
This project was built phase-wise to cover the entire Salesforce ecosystem — from **data modeling** to **automation, Apex programming, analytics, and deployment**.  

---

## 📑 Table of Contents
1. [Phase 1: Problem Statement & Goals](#phase-1-problem-statement--goals)  
2. [Phase 2: Salesforce Setup](#phase-2-salesforce-setup)  
3. [Phase 3: Data Modeling & Relationships](#phase-3-data-modeling--relationships)  
4. [Phase 4: Process Automation (Admin)](#phase-4-process-automation-admin)  
5. [Phase 5: Apex Programming (Developer)](#phase-5-apex-programming-developer)  
6. [Phase 6: Integration (API & External Systems)](#phase-6-integration-api--external-systems)  
7. [Phase 7: LWC & UI Enhancements](#phase-7-lwc--ui-enhancements)  
8. [Phase 8: Testing & Deployment](#phase-8-testing--deployment)  
9. [Phase 9: Reporting, Dashboards & Security](#phase-9-reporting-dashboards--security)  
10. [Phase 10: Final Presentation & Demo Day](#phase-10-final-presentation--demo-day)  

---

## Phase 1: Problem Statement & Goals  

### 🎯 Problem Statement  
Travel agencies often struggle with:  
- Managing leads manually  
- Handling multiple booking requests  
- Lack of real-time sales insights  
- Customers not receiving timely updates  

### ✅ Goals  
- Centralize lead, booking, and payment management.  
- Automate repetitive tasks (emails, assignments, status updates).  
- Provide actionable insights with dashboards & reports.  
- Enhance customer experience with loyalty programs and feedback tracking.  

---

## Phase 2: Salesforce Setup  

**Steps Followed:**  
1. Created a **new Salesforce Developer Org**.  
2. Configured **Company Information**:  
   - Company Name: Smart Travel Agency  
   - Currency: INR (₹)  
   - Locale: English (India)  
3. Created **Profiles & Roles**:  
   - Admin  
   - Agent  
   - Customer Support  
   - Manager  
4. Enabled features:  
   - Email Deliverability  
   - Activities (Tasks/Events)  
   - Reports & Dashboards  

---

## Phase 3: Data Modeling & Relationships  

**Custom Objects Created:**  
- **Lead__c** → Fields: Name, Email, Phone, Source, Status  
- **Customer__c** → Fields: Name, Email, Phone, Loyalty Points  
- **Travel_Package__c** → Fields: Destination, Type, Price  
- **Booking__c** → Fields: Customer Lookup, Package Lookup, Travel Dates, Status  
- **Payment__c** → Fields: Booking Lookup, Amount, Mode, Status  

**Relationships:**  
- Customer → Booking = **1:M**  
- Booking → Payment = **1:M**  
- Travel Package ↔ Booking = **M:M (Junction Object if needed)**  

---

## Phase 4: Process Automation (Admin)  

**Automations Implemented:**  
- **Validation Rules**:  
  - Travel Date ≥ Today  
  - Budget > 0  
- **Workflow Rules**:  
  - Send welcome email when a new lead is created  
- **Approval Process**:  
  - Bookings > ₹5,00,000 require Manager approval  
- **Flow Builder**:  
  - Auto-assign leads to Agents by region  
  - Auto-create loyalty points after payment  
  - Update booking status when payment succeeds  

---

## Phase 5: Apex Programming (Developer)  

**Key Implementations:**  
- **Trigger** → Auto-update booking status after payment  
- **SOQL Queries** → Fetch most booked destinations in last 6 months  
- **Batch Apex** → Send monthly travel recommendations to customers  
- **Queueable Apex** → Bulk import leads from campaigns  
- **Scheduled Apex** → Daily unassigned leads report emailed to Admin  
- **Future Methods** → Send SMS/WhatsApp booking confirmations  
- **Test Classes** → 85%+ coverage on triggers & classes  

---

## Phase 6: Integration (API & External Systems)  

**Integrations Implemented:**  
- **REST API** → Fetch live currency exchange rates for dynamic pricing  
- **Email-to-Case** → Convert customer support emails into cases  
- **Third-Party Payment API** → Capture payment confirmation automatically  

---

## Phase 7: LWC & UI Enhancements  

**UI Enhancements Implemented:**  
- **LWC Component (b)** → Display Travel Package Recommendations dynamically  
- **LWC Component (c)** → Show Customer Loyalty Points tracker on Customer Record Page  

---

## Phase 8: Testing & Deployment  

**Steps Taken:**  
- **Sandbox Testing**: Validated automations, Apex classes, and APIs  
- **Deployment via Change Sets**: Migrated from Sandbox → Production  
- **Post-Deployment Checks**:  
  - Verified Reports  
  - Checked Flow executions  
  - Ensured Security Profiles working correctly  

---

## Phase 9: Reporting, Dashboards & Security  

**Reports Created:**  
- Leads by Region  
- Packages by Popularity  
- Revenue by Month  
- Agent Conversion Rate  

**Dashboards:**  
- Business Overview Dashboard  
- Top Destinations Heatmap  
- Customer Loyalty Tracker  

**Security Settings:**  
- OWD: Leads = Private, Bookings = Role Hierarchy based  
- Dynamic Dashboards: Agents see only their data  
- Audit Trail enabled for monitoring changes  

---

## Phase 10: Final Presentation & Demo Day  

**Pitch:**  
Smart TravelConnect CRM increases efficiency by automating tasks, giving real-time insights, and improving customer engagement.  

**Demo Flow:**  
1. Lead Creation  
2. Auto-Assignment to Agent  
3. Package Selection  
4. Booking & Payment  
5. Confirmation Email  
6. Feedback Capture  
7. Dashboard Update  

**Handoff Docs:**  
- Setup Guide (Admin)  
- User Manual (Agents & Customers)  

**Showcase:**  
Shared on LinkedIn as **Smart Travel Agency CRM** to highlight Salesforce skills.  

---

## 👨‍💻 Built With  
- Salesforce Lightning Platform  
- Apex (Triggers, Batch, Queueable, Scheduled)  
- LWC (Lightning Web Components)  
- REST APIs for Integration  
- Reports & Dashboards  

---

## Demo Video
https://drive.google.com/file/d/1B96EnWgjcngBmjXOyYfGzqVGMp-4eMz6/view?usp=drive_link

---

## 📌 Author  
**Yash Dighade**  
B.Tech Final Year | Computer Science Engineering  
Prof. Ram Meghe Institute of Technology and Research, Amravati  
