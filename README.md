# Internship Tracker – Salesforce Project

**Industry:** Education  
**Project Type:** Salesforce CRM Implementation  
**Target Users:** Placement Officers, Students, and Recruiters/Companies  

---

## 📌 Problem Statement
A university placement cell faces challenges in tracking internship opportunities, student applications, and recruiter interactions. Currently, records are maintained in spreadsheets and emails, leading to:  
- Missed deadlines  
- Miscommunication  
- Poor placement outcomes  

**Solution:** A Salesforce-based system to:  
- Manage internship postings  
- Allow students to apply and track applications  
- Enable recruiters to shortlist and finalize candidates  
- Provide real-time dashboards for placement officers  

---

## 📊 Use Cases
- **Internship Posting:** Recruiters/Placement Officers add opportunities into the system  
- **Student Applications:** Students apply for internships and receive notifications  
- **Review & Shortlisting:** Placement Officers review and forward shortlisted students  
- **Recruiter Selection:** Recruiters finalize candidates and update statuses  
- **Reporting:** Placement Officers monitor student applications, recruiter participation, and placement rates  

---

## ⚙️ Project Phases

### Phase 1 – Problem Understanding & Industry Analysis
- **Requirement Gathering:** Identify problems with manual tracking, missed deadlines, lack of transparency  
- **Stakeholder Analysis:** Placement Officer, Students, Recruiters  
- **Business Process Mapping:** Internship Posting → Applications → Review → Shortlisting → Final Selection  
- **Industry-specific Use Case Analysis:** Universities, Colleges, EdTech platforms  
- **AppExchange Exploration:** Education Cloud & Recruitment apps exist but not customized for internships  

---

### Phase 2 – Org Setup & Configuration
- Salesforce Edition: Developer Org for implementation  
- Company Profile Setup: University/Institute details  
- Business Hours & Holidays: Placement office schedule  
- User Setup: Placement Officer, Student, Recruiter roles  
- Profiles & Permission Sets: Access restrictions based on user type  
- Roles: Placement Officer (top), Students (below), Recruiters (parallel)  
- OWD & Sharing Rules: Private for Students, hierarchical for Officer  
- Sandbox & Deployment Basics: Use Sandbox for testing before deployment  

---

### Phase 3 – Data Modeling & Relationships
- Custom Objects: Student, Company, Internship, Application, Interview  
- Fields: Skills, Stipend, Status, Role, Package  
- Record Types: Internship status (Open, Closed, Shortlisted)  
- Page Layouts: Student Profile, Internship Details  
- Schema Builder: Validate relationships  
- Relationships: Lookup (Student–Application), Master-Detail (Application–Internship)  
- Junction Object: Interview between Student and Company  

---

### Phase 4 – Process Automation (Admin)
- Validation Rules: Prevent duplicate applications, ensure stipend > 0  
- Workflow Rules: Email recruiter when internship is created  
- Process Builder: Auto-update application status  
- Approval Process: Packages above threshold require approval  
- Flow Builder: Auto-create Interview record when shortlisted  
- Email Alerts: Notify students of status changes  
- Custom Notifications: Placement Officer alert for deadlines  

---

### Phase 5 – Apex Programming (Developer)
- Apex Classes: ApplicationManager, PlacementReportGenerator  
- Triggers: Prevent duplicate student applications  
- SOQL & SOSL: Fetch student skills and internship matches  
- Collections: Store shortlisted students in List/Map  
- Batch Apex: Bulk update internship statuses  
- Queueable Apex: Async recruiter updates  
- Scheduled Apex: Nightly status update jobs  
- Exception Handling & Test Classes (75% coverage)  

---

### Phase 6 – User Interface Development
- Lightning App Builder: Create Internship Tracker App  
- Record Pages: Customized for Student, Internship, Company  
- Tabs: For all custom objects  
- Utility Bar: Quick access to dashboards  
- LWC: Component for Upcoming Interviews for Students  
- Events in LWC: Notify on student application updates  
- Wire Adapters & Imperative Apex: Fetch internships dynamically  
- Navigation Service: Redirect users to relevant records  

---

### Phase 7 – Integration & External Access
- Named Credentials: Store API endpoints  
- External Services: Connect with recruiter portals  
- REST Callouts: Fetch recruiter data (mock)  
- Platform Events: Notify students on application status  
- Change Data Capture: Track Internship updates  
- Salesforce Connect: Connect to external student DB  
- OAuth & Authentication: Secure recruiter access  

---

### Phase 8 – Data Management & Deployment
- Data Import Wizard: Import Student/Company records  
- Data Loader: Bulk Internship upload  
- Duplicate Rules: Prevent duplicate students  
- Data Export: Weekly backup of student applications  
- Change Sets: Deploy to Production  
- Managed vs Unmanaged Packages: Solution distribution  
- VS Code & SFDX: Version control  

---

### Phase 9 – Reporting, Dashboards & Security Review
- Reports: Applications by Internship, Recruiter Participation, Success Rate  
- Dashboards: Placement Overview Dashboard  
- Dynamic Dashboards: Role-based for Placement Officer/Recruiter  
- Field Level Security: Restrict sensitive student data  
- Sharing Rules: Define recruiter vs student access  
- Audit Trail & Login IP Ranges: Security compliance  

---

### Phase 10 – Final Presentation & Demo Day
- Pitch Presentation: Highlight problem, solution, and outcomes  
- Demo Walkthrough: Student applies → Interview auto-created → Recruiter selects → Dashboard updates  
- Feedback Collection: Mentor/Stakeholder inputs  
- Handoff Documentation: ERD, Flow Diagrams, Guides  
- LinkedIn/Portfolio Showcase: Highlight project  

---

## 📂 Repository Structure
Internship-Tracker/
├─ README.md
├─ 01_Phase_Problem_Analysis/
├─ 02_Phase_Org_Setup/
├─ 03_Phase_Data_Modeling/
├─ 04_Phase_Process_Automation/
├─ 05_Phase_Apex_Programming/
├─ 06_Phase_UI_Development/
├─ 07_Phase_Integration/
├─ 08_Phase_Data_Deployment/
├─ 09_Phase_Reporting/
└─ 10_Phase_Presentation/
