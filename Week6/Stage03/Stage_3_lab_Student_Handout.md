# Assignment 2 - Case Study
## Stage 3 Lab Activities: SmartCare Domain Modelling
**Workflow:** AI OFF -> AI ON -> COMPARE -> VERIFY | **Duration:** 1 hour

---

### Activities

#### A - Requirements Review
Highlight nouns, verbs and business rules in SmartCare v0.2.

<mark style="background-color: #00ff00">The smart care clinic</mark> has been <mark style="background-color: #48cae4"> doing all their management on paper for quite a while, and they are seeing quite\
frustrating mistakes occur.</mark> To <mark style="background-color: #ff4d00">combat</mark> this, they have tasked us with <mark style="background-color: #ff4d00">creating</mark> <mark style="background-color: #48cae4">a small system for their\
receptionist to easily book and keep track of appointments for their patients.</mark> The clinic would also like to have\
a way of <mark style="background-color: #ff4d00">storing</mark> <mark style="background-color: #00ff00">patient</mark> and <mark style="background-color: #00ff00">personnel</mark> information in a <mark style="background-color: #48cae4"> non-complex database</mark> which personnel will have access to,\
for them to better perform their jobs.

##### Legend
<mark style="background-color: #48cae4"> Business rules</mark>
<mark style="background-color: #00ff00">Nouns</mark>
<mark style="background-color: #ff4d00">Verbs</mark>


#### B - Candidate Classes
Record candidate concepts, supporting requirements, state and behaviour.

#### C - CRC Cards
Create CRC cards for `Patient`, `Practitioner`, and `Appointment`.

#### Patient
| Responsibilities                                                                | Collaborators |
|:--------------------------------------------------------------------------------|:--------------|
| Providing health information and current health status                          | Practitioner  |
| Providing personal details, preffered doctor and preferred time for appointment | Appointment   |

#### Practitioner
| Responsibilities | Collaborators                       |
|:-----------------|:------------------------------------|
| Patient          | Providing medical counselling       |
| Appointment      | Review and prepare for appointments |

#### Appointment
| Responsibilities | Collaborators                                                                                            |
|:-----------------|:---------------------------------------------------------------------------------------------------------|
| Patient          | Logging and keeping track of upcoming and past appointments                                              |
| Practitioner     | Notifiying practioners about upcoming appointments and other relevant info in respect to the appointment |


#### D - UML Model
Draw classes, attributes, operations, associations, and multiplicities.

#### E - AI Design Review
Ask AI to suggest classes and relationships using only confirmed requirements; require supporting requirement IDs.

#### F - Compare and Decide
Record at least one accepted, modified, and rejected AI suggestion.
* `PatientManager`- Good, something that is able to manage patient information could be quite handy.
* `ScheduleEngine`- Good, but out of scope
* `NotificationManager`- Bad, out of scope and unnecessary

#### G - Python Skeletons
Create simple `Patient`, `Practitioner`, and `Appointment` class skeletons.
# SmartCare Python Class Skeletons


from datetime import datetime
from typing import List, Optional


class Patient:
    Represents a patient within the SmartCare system.

    def __init__(self, patient_id: str, name: str, contact_info: str):
        self.patient_id: str = patient_id
        self.name: str = name
        self.contact_info: str = contact_info

    def get_medical_history(self) -> List[str]:
        """Retrieves patient medical history records."""
        pass

    def book_appointment(self, appointment: "Appointment") -> bool:
        """Schedules a new appointment for the patient."""
        pass


class Practitioner:
    Represents a healthcare practitioner in the SmartCare system.

    def __init__(self, practitioner_id: str, name: str, specialization: str):
        self.practitioner_id: str = practitioner_id
        self.name: str = name
        self.specialization: str = specialization

    def get_availability(self) -> List[datetime]:
        """Returns available time slots for appointments."""
        pass


class Appointment:
    Represents an appointment between a Patient and a Practitioner.

    def __init__(
        self,
        appointment_id: str,
        date_time: datetime,
        patient: Patient,
        practitioner: Practitioner,
        status: str = "Scheduled",
    ):
        self.appointment_id: str = appointment_id
        self.date_time: datetime = date_time
        self.patient: Patient = patient
        self.practitioner: Practitioner = practitioner
        self.status: str = status

    def cancel(self) -> bool:
        """Cancels the scheduled appointment."""
        pass

    def reschedule(self, new_time: datetime) -> bool:
        """Reschedules the appointment to a new date and time."""
        pass


#### H - Consistency Check
Check model-code consistency; do not implement full behaviour yet.

---

### Reflection
* What modelling decision was hardest?
* Where did AI over-design? wanting to replace staff with AI
* What evidence supported your final choices?the way current clinics run