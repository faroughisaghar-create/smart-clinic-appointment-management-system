sequenceDiagram
    actor Patient
    participant System
    participant Clinic
    participant Doctor
    participant Appointment

    Patient->>System: Login / Register
    System-->>Patient: Login Successful

    Patient->>System: Search Clinics
    System->>Clinic: Request clinic list
    Clinic-->>System: Return clinic list
    System-->>Patient: Display clinics

    Patient->>System: Select Clinic
    System->>Doctor: Request doctor list
    Doctor-->>System: Return doctor list
    System-->>Patient: Display doctors

    Patient->>System: Select Doctor
    Patient->>System: Choose appointment slot
    System->>Appointment: Create appointment
    Appointment-->>System: Appointment confirmed
    System-->>Patient: Show confirmation

