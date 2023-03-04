# ClinicalSystemDatabaseManagement

1.	Executive Summary 

The National Family Clinic, a system of clinics across major cities in the United States, requires a relational database system to replace the current file-based system. A relational database system is needed specifically to store and manage data regarding employees including both staff and physicians, patients, appointments, visits, treatments, billing, and insurance. This project’s purpose is to design and implement a database that will fulfill the needs of our team’s client, the National Family Clinic. This report aims to be a comprehensive document of the design and implementation process of the National Family Clinic’s database.
This report is structured to show the process of database development in logical order from requirements gathering to full implementation. First, the goals, context, and scope of the project are described. The report then outlines the data requirements, business rules, and other assumptions necessary for the development of the clinical database. This step is important because it ensures clarity of purpose and understanding of the needs of the client. Included in this report's design process are the conceptual and logical models of the database shown through conceptual and logical Entity-Relationship diagrams and the Relational Schema. Both the two diagrams and the schema are vital elements used by the team to develop a final implementation. 
This report then fully documents the database's implementation. The database code contained in this report has been verified across our team to be replicable. The replicable nature of the commands means that this database can be reliably installed and implemented by our client with ease. After installation, the client can use the database system to generate reports and gather information relevant to the clinic's business and functional needs. To demonstrate the database's power, our team developed a set of complex queries and data manipulation commands to display the database’s utility and versatility. The National Family Clinic’s new database can thus yield valuable information that will aid decision-making at both the clinical and executive level. It is also able to change according to the evolving needs of the National Family Clinic itself, accommodating growth in the clinic’s branches, employees, and patients. 
The result of this project is the creation of a relational database that fulfills the needs of the National Family Clinic. The implementation is consistent with the pre-established requirements and scope. All aspects, from the conceptual level to the code, are documented herein as to provide a resource for the future implementation and management of the database. 

2.	Problem Statement 

a.	Goals

A healthcare clinic for family doctors across the United States would like to create a relational database system for both adult and pediatric patient visits with physicians and clinic staff.

b.	Context 

The healthcare clinic for family doctors has previously been using a file-based system for record keeping. This method unnecessarily duplicates data and is difficult to update, scale up, and maintain consistency. A relational database would solve the problems of duplication and inconsistencies, helping the clinic keep accurate records of patient data. Electronic clinic records for patient medical history ensure legibility and do not incur damage over time, unlike file records that may be hastily handwritten or damaged (“What Is a Clinic Management System?” 2019). A long-lasting system is important for this clinic because family doctors can treat patients throughout their lives. According to Existek blog, a database management system also helps to outline and implement policies, guarantee communication and coordination between employees, automate routine tasks, design patient-oriented workflows, and advertise services (Osetskyi, 2022). An RDBMS would increase staff efficiency and speed, serving as a valuable resource for the clinic to track patient payments and medical history.

c.	Scope 

•	In-scope: The clinic database is accessible to doctors and clinic staff. It contains data regarding patient personal information, physician information, appointments, 	medical history, billing, payment, insurance, treatments, department and clinic branches.

•	Out-scope: The clinic database does not contain data regarding physician personal information, staff personal information, clinic payroll, and staff scheduling. It is not accessible by patients. No walk-ins are permitted at this clinic.

3.	Requirements 

a.	Analysis of Current System 

The healthcare clinic for family doctor's database system reviewed and analyzed as first step to initiate the development and transition of clinical database management from an old traditional paper base to electronic medical record. The current system is a non-relational database system with multiple reporting forms and data entry applications. The nature of data flow in the clinic has introduced a lot of challenges ranging from poor data quality and integrity, erroneous care delivery, poor health outcome, growing cost, and risk to legal issues. This non-relational database model collection and handling process is faced with each department collecting duplication information from the same patient. The clinic data system uses 9 different forms to record patient health information such as demographics, vital signs, lab results, doctor orders, and care plan. The forms are stored in hard copies, as a result, more time is spent pulling out records for patients with follow-up or second visits. 
Patient healthcare information has been recorded into separate databases, the billing department has its accounting software to bill and collect patient health insurance, front desk uses excel spreadsheet to record patient appointments, Physician has an access database to capture patient medical record. These separate databases are not integrated both internally and externally, information is not shared between departments. The use of data to support clinical decisions must be utilized in multiple databases. The growing recognition of the cost, risk of data integrity, and healthcare quality has driven the clinic management to transition its non-relational database system from paper-based to relational database system (electronic medical records) that is designed to collect, store, analyze, and share patient records in a more secure, simple, easy, manner. 


b.	Data requirements 

·	The clinic relational database will capture and track all information about patients visiting the facility irrespective of the visit. It will store information such as patient full name, phone number, patient medical history, patient appointment dates and time, payment information, billing information and insurance.
·	The Philadelphia clinic system has branches in different locations throughout the city. Each branch of the clinic has different departments. The database will      collect data on each branch location and name. 
·	Each branch has different adult and pediatric departments for which the database will store department name and number. 
·	The clinic must collect and maintain patient records including the start date with the clinic and description of each patient's medical history.
·	The insurance information of each patient is stored, including insurance ID and company.
·	The database will collect information about the physician such as physician ID, full name, and specialty.

c.	Business rules and Logic 

·	Each clinic branch can schedule many patients a day with multiple departments
·	Each department can serve many patients a day 
·	The clinic system consists of many branches, each with multiple departments
·	Each department has at least one physician
·	A physician can belong to more than one department
·	Each branch has its own set of staff members
·	Staff members are not physicians
·	Some staff members can be managers, some can be receptionists, some can be neither
·	There is one manager for every branch
·	Physicians can view patient medical history and appointments, but not billing 
·	Patients schedule appointments with the receptionist via phone call
·	Each branch has at least one receptionist 
·	Patients can only have one appointment per day
·	Patients are billed for each treatment they receive
·	Billing is the total amount due 
·	Payments can be made in multiple installments 
·	Patients are scheduled for appointments depending on their physician’s availability

d.	Any other assumption 

·	All patients must have an associated patient history record
·	Insurance information is updated when insurance changes
·	Bills are expected to be paid in full 90 days after the appointment
·	Payment methods can include credit, debit, cash, or check


e.	The way you solved the problem, if relevant 

A few tables instantly popped out as being critical in a database that tracks patients going to the clinic for treatment, arranging appointments to meet the required physician, and making bill payments accordingly: Staff, Treatment, Billing, Payments, and Insurance. Staff was split into Managers and Receptionist. Whereas managers only oversee branches, patients can schedule appointments with receptionists. Another issue that must not be overlooked was Billing, Payment, and Insurance, all of which play a significant role in the database system. Following treatment, a bill will be issued that the patient must pay. Patients may or may not utilize their insurance to pay the bills generated, and in either case, the details of their insurance are vital for the database.

f.	Obtaining data

On the data aspect, we created fictional data value based on our research about healthcare data to meet the database requirements and the scope of this project. Furthermore, we used several data reports such as the Association of American Medical Colleges' report to obtain realistic data value about the specialty of physicians. 

g.	The hardware and software (Personal Oracle, CCI Oracle, LiveSQL, Mysql, Version number) you used and any special features or considerations 

I have used CCI Oracle to implement SQL commands. 



