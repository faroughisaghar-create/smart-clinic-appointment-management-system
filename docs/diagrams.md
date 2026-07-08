
## Class Diagram
```mermaid
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
+bookAppointment()
+cancelAppointment()
+viewMedicalRecord()
}

class Receptionist {
+confirmAppointment()
+manageBooking()
}

class Doctor {
+string specialization
+manageSchedule()
+viewPatientRecord()
}

class Admin {
+manageUsers()
+generateReports()
}

class Clinic {
+int clinicId
+string clinicName
+string address
}

class Appointment {
+int appointmentId
+date appointmentDate
+string status
+createAppointment()
+cancelAppointment()
}

class MedicalRecord {
+int recordId
+string diagnosis
+string prescription
+viewRecord()
}

User <|-- Patient
User <|-- Receptionist
User <|-- Doctor
User <|-- Admin

Patient "1" --> "0..*" Appointment : books
Doctor "1" --> "0..*" Appointment : handles
Clinic "1" --> "0..*" Doctor : has
Patient "1" --> "0..*" MedicalRecord : owns
Doctor "1" --> "0..*" MedicalRecord : updates
`





text


text
## Class Diagram

## Commit message
text
Add class diagram



