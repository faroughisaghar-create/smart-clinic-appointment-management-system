## ER Diagram - Smart Clinic Appointment & Management System

The following ER diagram shows the main database entities and their relationships in the Smart Clinic Appointment and Management System.
```mermaid
erDiagram

USER {
int user_id PK
string full_name
string email
string password
string role
string phone
}

PATIENT {
int patient_id PK
int user_id FK
string national_id
date birth_date
string gender
}

DOCTOR {
int doctor_id PK
int user_id FK
string specialization
int clinic_id FK
}

CLINIC {
int clinic_id PK
string name
string address
string phone
}

APPOINTMENT {
int appointment_id PK
int patient_id FK
int doctor_id FK
date appointment_date
string appointment_time
string status
}

SCHEDULE {
int schedule_id PK
int doctor_id FK
string available_day
string start_time
string end_time
}

ADMIN {
int admin_id PK
int user_id FK
string access_level
}

USER ||--|| PATIENT : has
USER ||--|| DOCTOR : has
USER ||--|| ADMIN : has

CLINIC ||--o{ DOCTOR : employs

PATIENT ||--o{ APPOINTMENT : books
DOCTOR ||--o{ APPOINTMENT : receives

DOCTOR ||--o{ SCHEDULE : has



















پmarkdown
## ER Diagram - Smart Clinic Appointment & Management System

![ER Diagram](../images/er-diagram.png)
