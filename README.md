📘 Electronic Medical Records (EMR) Management System

A Role-Based Healthcare Database & Application built using Python and MySQL

📌 Overview

This project is a complete Electronic Medical Records (EMR) Management System designed for healthcare environments. It provides a secure, role-based interface for Patients, Doctors, Receptionists, and Staff to interact with clinical, billing, and administrative data.

The system integrates:

A fully normalized MySQL database

SQL scripts for schema creation, indexes, views, triggers, and stored procedures

A Python application that uses MySQL Connector for authentication and role-based operations

CRUD operations across all major healthcare modules

Audit logging for compliance and traceability

🏗️ Project Structure
📂 EMR-Management-System
│── DBCreation.sql
│── DataInsertion.sql
│── Indexes.sql
│── Views.sql
│── Stored procedures.sql
│── Triggers.sql
│── Queries.sql
│── emr.py
└── README.md

⚙️ Features
🔐 Role-Based Login (Patient, Doctor, Receptionist, Staff)

Implemented using the Users table and the stored procedure CheckLogin 

Stored procedures

.

👨‍⚕️ Clinical Management

Doctors can:

View all patients

Create clinical records

Update clinical records
(All operations powered by stored procedures like CreateClinicalRecord and UpdateClinicalRecord 

Stored procedures

.)

🧾 Appointments & Reception Operations

Receptionists can create and manage appointments using procedures such as CreateAppointment 

Stored procedures

.

🧪 Diagnostics, Prescriptions & Visits

MySQL procedures support CRUD for:

Prescriptions

Tests

Visits
(See Stored procedures.sql for all modules 

Stored procedures

.)

💳 Billing & Finance

Billing operations supported with View_Billing_Summary view and billing procedures.
Citations:

Billing Table Definition: 

DBCreation

Billing SPs: 

Stored procedures

Billing View: 

Views

🗄️ Database Views for Reports

Helpful views for reporting include:

View_Patient_BasicInfo

View_Appointment_Details

View_ClinicalRecord_Summary

View_Visit_History

(All defined in Views.sql 

Views

.)

📝 Audit Logging System

Every UPDATE and DELETE action on critical tables triggers audit entries, improving security & compliance (Triggers.sql).
Examples:

BeforeUpdatePatient

BeforeDeleteVisit

BeforeUpdateBilling

(All defined in Triggers.sql 

Triggers

.)

🛠️ Technologies Used
Backend & Database

MySQL – relational schema with indexing, triggers, and stored procedures

SQL – for complex queries, joins, and optimization

Programming

Python (mysql.connector) – authentication, role-based menus, DB operations

Source: emr.py 

emr

Database Optimization

Indexing applied to all key fields for speed (Indexes.sql) 

Indexes

🗃️ Database Schema Summary

The database includes the following core tables:

Patient

Provider

Visit

Appointment

ClinicalCare

Billing

Insurance

Room

Users

Schema defined in DBCreation.sql 

DBCreation

.

🧪 Sample Queries

Complex and analytical SQL queries included in Queries.sql 

Queries

:

Patient visit count

Average patient age

Billing analysis

Room assignment queries

Insurance statistics

These are useful for reports, dashboards, and analytics.

▶️ How to Run the Project
1. Create the Database
SOURCE DBCreation.sql;
SOURCE DataInsertion.sql;
SOURCE Indexes.sql;
SOURCE Views.sql;
SOURCE Stored procedures.sql;
SOURCE Triggers.sql;

2. Configure MySQL Credentials in Python

In emr.py update:

user='root'
password='Localhost!12'
database='emr'

3. Run the Python Program
python emr.py

4. Log in with Sample Credentials

Examples from DataInsertion.sql:

Receptionist: reception1 / password123

Doctor: doctor1 / password123

Patient: patient1 / password123

Staff: staff1 / password123

🧠 Application Menus
👩‍⚕️ Doctor Menu

View patient info

Create clinical record

Update clinical record

View all patients

🧑 Receptionist Menu

Create patient

Create appointment

View appointments

👤 Patient Menu

View personal info

View appointments

View prescriptions

👨‍🔧 Staff Menu

View patient info

View all clinical records

View billing information

📈 Future Enhancements

Add a GUI using Flask or React

Implement JWT-based authentication

Add role-based dashboards

Add exportable reports (PDF/Excel)

Add HL7/FHIR API integration

👨‍💻 Author

Mohammed Waseem Tabrez
Master’s in Information Technology – UNCC
