# Seolad School Management System — Project Portfolio

A full-stack school management system I designed, built, and deployed for **Seolad International School** in Mowe, Ogun State, Nigeria. It replaced manual, paper-based record keeping with a secure platform for managing students, academic sessions and terms, assessments, results, report cards and promotions.

> **Note:** The source code is kept in a private repository to protect the school's data and systems. This portfolio shows the system's scope, architecture, and features using non-sensitive information only.

---

## At a Glance

| | |
|---|---|
| **Status** | Live in production since September 2026 |
| **Users** | 460+ students, 280+ parents, 53 teachers, 4 administrators (as of October 2026) |
| **Target scale** | Full enrollment of 600+ students and 300+ parents |
| **My role** | Sole full-stack developer: development, design, deployment, and maintenance |

---

## Tech Stack

- **Frontend:** React.js (Vite), Tailwind CSS, React Router
- **Backend:** Node.js, Express.js (RESTful API)
- **Database:** MongoDB with Mongoose
- **Media storage:** Cloudinary (student and staff photos)
- **Authentication:** JWT stored in HTTP-only cookies

---

## Four Role-Based Portals

Each user has its own portal and can only see and do what their role allows.

**Super Admin**
- Creates and manages administrator accounts
- Performs corrections to assessments, results and reports after they have been published

**Admin**
- Manages academic sessions, terms, classes, and subjects
- Registers and manages students, teachers, and parents
- Assigns subject teachers to classes
- Assigns subjects to classes for Recption to JSS classes
- Assigns subjects to SS students individually
- Creates assessments, results and report cards if needed
- Reviews and publishes assessments created by subject teachers for parents to view for their child/children only
- Lock/unlock results created by subject teachers and/or admin
- Reviews and publishes report cards for parents to view for their child/children only
- Handles end-of-session student promotions

**Teacher**
- Subject Teachers: Create assessments, record student scores, and manage results for their assigned subjects and classes.
- Class Teachers: Generate report, manage attendance, student ratings, add comments and review report cards for students in their assigned class.

**Parent**
- Views their children's academic records, assessments, and report cards

---

## Data Privacy and Security

The system stores sensitive information about students, teachers and parents, so protecting it was a core design priority:

- **Role-based access control:** every page and API route checks the user's role, so users can only access data they are authorized to see (e.g, subject teachers can only manage assessments and results for subjects and classes assigned to them).
- **Secure authentication:** use JSON Web Tokens (JWTs) stored in HTTP-only cookies to prevent client-side JavaScript from directly accessing authentication tokens.
- **Input validation:** validate submitted forms to prevent duplicate and invalid records of names, emails, Nigerian phone numbers, admission numbers, dates of birth, etc.
- **Controlled corrections:** changes to finalized results go through super admin correction workflow rather than direct edits, protecting the integrity of academic records.
- **Database Transactions:** use MongoDB transactions for operations requiring multiple database changes, which helps to maintain data consistency.

These principles are also relevant to health information systems where protecting sensitive patient records requires strict access control, secure authentication, and data integrity.

---

## Screenshots

*All screenshots use demo data. No real student, parent, or staff information is shown.*

[View Seolad SMS Application Screenshots](screenshots/)

---

## Challenges and What I Learned

- **Modelling the academic year:** designing sessions, terms, classes, and promotions so data flows correctly from one academic year to the next.
- **Designing user permissions:** making sure each role sees and performs only what it needs.
- **Preparing for production:** full code review and cleanup before launch, including shared utilities and components to keep the codebase consistent and maintainable.
- **Maintaining data integrity:** ensuring that published assessments, result and report cards are safe during corrections workflow.
- **Building maintainable applications:** I learnt the importance of writing reusable components, separating business logic from controllers, and organizing code to make debugging, testing, and future maintenance easier.
- **Designing systems around real-world usage:** I learnt how important it is to understand users' needs and existing workflows before implementing features, especially when different user roles depend on one another to complete tasks.

---

## Contact

**Adeola Faith Olajide**  
Email: adeolaolajide871@gmail.com  
GitHub: [@adeolafaitholajide](https://github.com/adeolafaitholajide)
