# Experiment 1: Entity-Relationship (ER) Diagram

## 🎯 Objective:
To understand and apply the concepts of ER modeling by creating an ER diagram for a real-world application.

## 📚 Purpose:
The purpose of this workshop is to gain hands-on experience in designing ER diagrams that visually represent the structure of a database including entities, relationships, attributes, and constraints.

---

## 🧪 Choose One Scenario:

### 🔹 Scenario 1: University Database
Design a database to manage students, instructors, programs, courses, and student enrollments. Include prerequisites for courses.

**User Requirements:**
- Academic programs grouped under departments.
- Students have admission number, name, DOB, contact info.
- Instructors with staff number, contact info, etc.
- Courses have number, name, credits.
- Track course enrollments by students and enrollment date.
- Add support for prerequisites (some courses require others).

---

### 🔹 Scenario 2: Hospital Database
Design a database for patient management, appointments, medical records, and billing.

**User Requirements:**
- Patient details including contact and insurance.
- Doctors and their departments, contact info, specialization.
- Appointments with reason, time, patient-doctor link.
- Medical records with treatments, diagnosis, test results.
- Billing and payment details for each appointment.

---

## 📝 Tasks:
1. Identify entities, relationships, and attributes.
2. Draw the ER diagram using any tool (draw.io, dbdiagram.io, hand-drawn and scanned).
3. Include:
   - Cardinality & participation constraints
   - Prerequisites for University OR Billing for Hospital
4. Explain:
   - Why you chose the entities and relationships.
   - How you modeled prerequisites or billing.

# ER Diagram Submission - Abdur Rahman Basil (212223040002)

## Scenario Chosen:
University / Hospital (choose one)

## ER Diagram:
![Hospital ER](https://github.com/user-attachments/assets/5890c2bb-9551-497d-8ddd-759dad4110d9)

## Entities and Attributes:
- Department of Specialization - Department ID, Head of Department, Department Name
- Doctor - Name (First name, Last name), Specialization, Contact (Email, Phone No.)
- Patient - Patient ID, Full Name, Contact (Email, Phone No.)
- Appointments - Appointment ID, Patient Name, Doctor Name, Date and Time
- Medical Records - Medical Record ID, Patient Name, Doctor Name, Diagnoses, Medication
...

## Relationships and Constraints:
Relationship1: consists of
Entities involved: Department of Specialization — Doctor
Cardinality:
One Department consists of many Doctors (1:N)
One Doctor belongs to one Department (N:1)

Relationship2: treats
Entities involved: Doctor — Patient
Cardinality:
One Doctor can treat many Patients (1:N)
One Patient can be treated by one Doctor (N:1)

Relationship3: schedules
Entities involved: Patient — Appointments
Cardinality:
One Patient can schedule many Appointments (1:N)
One Appointment is scheduled by one Patient (N:1)

Relationship4: collect 
Entities involved: Appointments — Medical Records
Cardinality:
One Appointment can collect many Medical Records (1:N)
One Medical Record is linked to one Appointment (N:1)
...

## Extension (Prerequisite / Billing):
For prerequisites, the design includes a relationship between Appointments and Medical Records to model the sequence of steps in medical treatment. In this context, the Medical Records are created after the Appointment takes place, which ensures the correct order of events and the proper documentation of the patient's treatment.

## Design Choices:
Entities:
Department of Specialization: This is included to group doctors into different specialties and link them to the relevant department. It helps organize the hospital's operations into meaningful divisions.
Doctor: This entity captures important details about medical staff, such as their specialization and contact details, which are crucial for identifying the right doctor for a patient's needs.
Patient: This entity stores patient information, ensuring a proper linkage to appointments and medical records.
Appointments: This entity models the scheduling of visits between patients and doctors, capturing necessary details like date, time, and the involved individuals.
Medical Records: This stores the diagnoses and medication prescribed to patients, linked to specific appointments and doctors.

Relationships:
Department of Specialization — Doctor (1:N): This relationship ensures that doctors are associated with their respective departments. One department can have many doctors, but each doctor belongs to a single department, simplifying the management of medical staff.
Doctor — Patient (1:N): This relationship ensures that one doctor can treat multiple patients but that each patient is linked to a specific doctor for treatment continuity.
Patient — Appointments (1:N): The patient can schedule multiple appointments, and each appointment is associated with a specific patient. This relationship also allows easy tracking of the patient's visit history.
Appointments — Medical Records (1:N): Each appointment results in medical records that document the diagnoses and treatments prescribed by the doctor. This relationship reflects the logical flow of medical treatment.

Assumptions:
No Ambiguity in Specializations: Doctors have only one specialization, and patients are treated by doctors based on their conditions and the doctor's expertise.
Appointments and Medical Records: Each appointment generates a single medical record. A patient could have multiple appointments, but each one will have its own associated medical record.
Patients and Billing: The Billing entity is assumed to be handled after each appointment, reflecting the services provided during the visit.

## RESULT:
Hence, the concepts of ER modeling is understood and applied by creating an ER diagram for a real-world application.
