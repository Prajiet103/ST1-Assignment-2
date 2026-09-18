# SmartCare v0.3 - Domain Model Workbook
**Week 6 Student Resource**

---

## Requirement-to-Concept Trace

| Requirement | Concept                                 | State/behaviour                 | Decision |
|:------------|:----------------------------------------|:--------------------------------|:---------|
| Small       | small data size, simple and easy to use | Logging system for receptionist |          |
|             |                                         |                                 |          |
|             |                                         |                                 |          |
|             |                                         |                                 |          |
|             |                                         |                                 |          |
|             |                                         |                                 |          |
|             |                                         |                                 |          |
|             |                                         |                                 |          |
|             |                                         |                                 |          |
|             |                                         |                                 |          |

---

## CRC Cards

### Patient
| Responsibilities                                                                | Collaborators |
|:--------------------------------------------------------------------------------|:--------------|
| Providing health information and current health status                          | Practitioner  |
| Providing personal details, preffered doctor and preferred time for appointment | Appointment   |


### Practitioner
| Responsibilities | Collaborators                       |
|:-----------------|:------------------------------------|
| Patient          | Providing medical counselling       |
| Appointment      | Review and prepare for appointments |

### Appointment
| Responsibilities | Collaborators                                                                                            |
|:-----------------|:---------------------------------------------------------------------------------------------------------|
| Patient          | Logging and keeping track of upcoming and past appointments                                              |
| Practitioner     | Notifiying practioners about upcoming appointments and other relevant info in respect to the appointment |


### Optional class
| Responsibilities | Collaborators |
| :--- | :--- |
| | |
| | |

---

## UML Class Diagram
*(Insert/draw UML here. Include defensible relationships and multiplicities.)*
# SmartCare UML 

### Domain Classes & Features

| Class Name       | Attributes                                                              | Operations (Methods)                     |
|:-----------------|:------------------------------------------------------------------------|:-----------------------------------------|
| **Patient**      | `patientId: Integer`<br>`name: String`<br>`contactInfo: String`         | `getMedHistory()`<br>`bookAppointment()` |
| **Practitioner** | `practitionerId: Integer`<br>`name: String`<br>`specialization: String` | `getAvailability()`                      |
| **Appointment**  | `appointmentId: Integer`<br>`dateTime: String`<br>`status: String`      | `cancel()`<br>`reschedule()`             |

---

## Design Rationale
*(Explain class selection, responsibility allocation and key relationships.)*

All the classes that where made where all unique and are the three most important pieces of information for the system.

---

## AI Design Review Record

| AI Suggestion           | Evidence | Decision | Reason | Model Change |
|:------------------------| :--- | :--- | :--- | :--- |
| **NotificationManager** | | | | |
| **ScheduleEngine**      | | | | |
| **AppointmentStatus**   | | | | |
| **ClinicController**    | | | | |