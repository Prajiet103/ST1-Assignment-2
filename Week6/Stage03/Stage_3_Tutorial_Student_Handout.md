# Assignment 2 - Case Study
## Stage 3 Tutorial Activities: From Requirements to Domain Models
**Week 6 | 60 minutes**

---

### Candidate Concepts

| Candidate | Class? | Reason                                                                                                                        |
| :--- |:-------|:------------------------------------------------------------------------------------------------------------------------------|
| Patient | Yes    | Patients are a domian since they have their own behaviours and attributes                                                     |
| Practitioner | Yes    | Doctors are a domian that is different to patients since they have attributes and behaviours completely different to patients |
| Appointment | Yes    | Appointments are a domian since they have attributes unique to what it is                                                     |
| Name | No     | No beacause names are an attribute within a domain                                                                            |
| Clinic | Yes    | Yes because its a seperate entity                                                                                             |
| Database | No     | databases are an infrastructure not a class                                                                                   |
| Cancellation | No     | this is and action which is not a class                                                                                       |
| Status | No     | this is an event which is not a class                                                                                         |

---

### CRC Cards

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

---

### Relationship Reasoning
1. **Patient to Appointment:** Which relationship and why?: Their relationship is association the appointment needs to know the patient but the patient just makes the appointment within the system.
2. **Practitioner to Appointment:** What multiplicity?: 
3. **Should Appointment inherit from Patient?:** Partially since the Appointment needs some of the patient info
4. **Does Clinic need to own every object?:** yes in order to be able to properly track and store all information within the clinic

---

### AI Model Critique
Critique the following AI proposals:
* `PatientManager`- Good, something that is able to manage patient information could be quite handy.
* `PractitionerManager`- Good, handling personnel info is important so any way to make this function as strong as possible should be taken into consideration.
* `AppointmentManager`- Good, Makes tracking appointments easy
* `ClinicController`- Bad, out of scope and unnecessary
* `NotificationManager`- Bad, out of scope and unnecessary
* `ScheduleEngine`- Good, but out of scope