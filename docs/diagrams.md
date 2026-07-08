sequenceDiagram
    actor Patient
    participant System
    participant Clinic
    participant Doctor
    participant Appointment

    Patient->>System: Login / Register

    Patient->>System: Search Clinics
    System->>Clinic: Get clinic list
    Clinic-->>System: Return clinic details

    Patient->>System: View Doctors
    System->>Doctor: Get doctor list
    Doctor-->>System: Return doctor details

    Patient->>System: Select appointment slot
    System->>Appointment: Create appointment
    Appointment-->>System: Appointment confirmed

    System-->>Patient: Show confirmation











