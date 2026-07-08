# UML and Database Diagrams

This document contains the main diagrams for the Smart Clinic Appointment & Management System.

## Diagrams List

1. Use Case Diagram
2. Class Diagram
3. Sequence Diagram
4. Activity Diagram
5. ER Diagram

## Use Case Diagram
flowchart LR
Patient[Patient]
Receptionist[Receptionist]
Doctor[Doctor]
Admin[System Admin]

UC1((Register / Login))
UC2((Search Clinics))
UC3((View Doctors))
UC4((Book Appointment))
UC5((Cancel Appointment))
UC6((View Medical Record))
UC7((Manage Schedule))
UC8((Confirm Appointment))
UC9((Manage Users))
UC10((Generate Reports))

Patient --> UC1
Patient --> UC2
Patient --> UC3
Patient --> UC4
Patient --> UC5
Patient --> UC6



Receptionist --> UC2
Receptionist --> UC3
Receptionist --> UC4
Receptionist --> UC8



Doctor --> UC6
Doctor --> UC7



Admin --> UC9
Admin --> UC10










## Class Diagram

mermaid
classDiagram
class User {
+int userId
+string fullName
+string email
+string password
+string phoneNumber
+login()
+logout()
}

class Patient {
+int patientId
+string nationalCode
+string dateOfBirth
+viewMedicalRecord()
+bookAppointment()
+cancelAppointment()
}

class Doctor {
+int doctorId
+string specialty
+string medicalLicenseNumber
+manageSchedule()
+viewAppointments()
}

class Receptionist {
+int receptionistId
+confirmAppointment()
+manageAppointments()
}

class SystemAdmin {
+int adminId
+manageUsers()
+generateReports()
}

class Clinic {
+int clinicId
+string clinicName
+string address
+string phoneNumber
}

class Appointment {
+int appointmentId
+string appointmentDate
+string appointmentTime
+string status
+createAppointment()
+cancelAppointment()
+confirmAppointment()
}

class MedicalRecord {
+int recordId
+string diagnosis
+string prescription
+string visitDate
+updateRecord()
+viewRecord()
}

User <|-- Patient
User <|-- Doctor
User <|-- Receptionist
User <|-- SystemAdmin

Clinic "1" --> "many" Doctor
Patient "1" --> "many" Appointment
Doctor "1" --> "many" Appointment
Appointment "1" --> "1" MedicalRecord
Patient "1" --> "many" MedicalRecord
Doctor "1" --> "many" MedicalRecord


`

```markdown
## Class Diagram



markdown
Admin --> UC10## Class Diagram


`markdown
Admin --> UC10

## Class Diagram
`


```text
Fix Mermaid diagrams formatting

`


```markdown
Admin --> UC10
