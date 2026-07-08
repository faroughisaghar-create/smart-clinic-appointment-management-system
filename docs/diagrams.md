
## Sequence Diagram
mermaid
sequenceDiagram
actor Patient
participant System
participant Clinic
participant Doctor
participant Appointment

Patient->>System: Login / Register
Patient->>System: Search Clinics
System->>Clinic: Get clinic list
Clinic-->>System: Clinic details

Patient->>System: View Doctors
System->>Doctor: Get doctor list
Doctor-->>System: Doctor details

Patient->>System: Select appointment slot
System->>Appointment: Create appointment
Appointment-->>System: Appointment confirmed
System-->>Patient: Show confirmation


:

1. Use Case Diagram
2. Class Diagram
3. Sequence Diagram

## Commit message
text
Add sequence diagram


