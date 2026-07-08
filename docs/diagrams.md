## 5. ER Diagram - Smart Clinic Appointment and Management System

This ER diagram represents the main database entities and relationships of the Smart Clinic Appointment and Management System.
```mermaid
erDiagram

USERS {
int user_id PK
string full_name
string email
string password_hash
string phone_number
string role
datetime created_at
}

PATIENTS {
int patient_id PK
int user_id FK
string national_code
date date_of_birth
string gender
string address
}

DOCTORS {
int doctor_id PK
int user_id FK
int clinic_id FK
string specialization
string medical_license_number
int experience_years
}

ADMINS {
int admin_id PK
int user_id FK
string access_level
}

CLINICS {
int clinic_id PK
string clinic_name
string address
string phone_number
string email
}

SCHEDULES {
int schedule_id PK
int doctor_id FK
string day_of_week
time start_time
time end_time
int visit_duration
boolean is_available
}

APPOINTMENTS {
int appointment_id PK
int patient_id FK
int doctor_id FK
int schedule_id FK
date appointment_date
time appointment_time
string status
datetime created_at
}

USERS ||--|| PATIENTS : has
USERS ||--|| DOCTORS : has
USERS ||--|| ADMINS : has

CLINICS ||--o{ DOCTORS : includes

DOCTORS ||--o{ SCHEDULES : defines

PATIENTS ||--o{ APPOINTMENTS : books
DOCTORS ||--o{ APPOINTMENTS : receives
SCHEDULES ||--o{ APPOINTMENTS : used_for






markdown

mermaid



Mermaid 

mermaid
erDiagram

    USERS {
        int user_id PK
        string full_name
        string email
        string password_hash
        string phone_number
        string role
        datetime created_at
    }

    PATIENTS {
        int patient_id PK
        int user_id FK
        string national_code
        date date_of_birth
        string gender
        string address
    }

    DOCTORS {
        int doctor_id PK
        int user_id FK
        int clinic_id FK
        string specialization
        string medical_license_number
        int experience_years
    }

    ADMINS {
        int admin_id PK
        int user_id FK
        string access_level
    }

    CLINICS {
        int clinic_id PK
        string clinic_name
        string address
        string phone_number
        string email
    }

    SCHEDULES {
        int schedule_id PK
        int doctor_id FK
        string day_of_week
        time start_time
        time end_time
        int visit_duration
        boolean is_available
    }

    APPOINTMENTS {
        int appointment_id PK
        int patient_id FK
        int doctor_id FK
        int schedule_id FK
        date appointment_date
        time appointment_time
        string status
        datetime created_at
    }

    USERS ||--|| PATIENTS : has
    USERS ||--|| DOCTORS : has
    USERS ||--|| ADMINS : has

    CLINICS ||--o{ DOCTORS : includes
    DOCTORS ||--o{ SCHEDULES : defines

    PATIENTS ||--o{ APPOINTMENTS : books
    DOCTORS ||--o{ APPOINTMENTS : receives
    SCHEDULES ||--o{ APPOINTMENTS : used_for

