# Appointment Booking System Analysis

  

## 1. What the Code Does

  

### Task 1: Basic Appointment Display

 

The first section demonstrates:

 

- **Variables** to store appointment information.

- **Output statements (`print`)** to display information on the screen.

- **Formatted strings (f-strings)** to combine text and variables into a readable message.

 

Example:

 

```python

patient1_name = 'Alice Smith'

practitioner1_name = 'Dr. John Doe'

appointment1_time = '2024-07-20 10:00 AM'

```

 

These variables store details for one appointment.

 

The statement:

 

```python

print(f"Patient: {patient1_name} | Practitioner: {practitioner1_name} | Time: {appointment1_time}")

```

  

prints the appointment information in a user-friendly format.

 

The same process is repeated for a second appointment.

 

---

 

### Task 1 Enhanced: Lists, Dictionaries and Functions

 

This version improves the design of the program.

 

#### List

 

```python

appointments = []

```

 

A list is created to store multiple appointments.

 

---

 

#### Function: `book_appointment()`

 

```python

def book_appointment(patient_name, practitioner_name, appointment_time):

```

 

This function:

 

1. Receives appointment details as parameters.

2. Checks whether the patient name is empty.

3. Creates a dictionary containing the appointment information.

4. Adds the dictionary to the appointments list.

 

The validation:

 

```python

if not patient_name:

raise ValueError("Patient name cannot be empty")

```

 

prevents appointments from being created without a patient name.

 

---

 

#### Dictionary

 

```python

appointment = {

"patient": patient_name,

"practitioner": practitioner_name,

"time": appointment_time

}

```

 

The dictionary stores related appointment data using key-value pairs.

 

---

 

#### Function: `display_appointments()`

 

```python

def display_appointments():

```

 

This function:

 

1. Checks if the appointments list is empty.

2. Displays a message if no appointments exist.

3. Loops through the list and prints every appointment.

 

The loop:

 

```python

for appointment in appointments:

```

 

allows all stored appointments to be displayed.

 

---

 

#### Program Execution

 

The program then:

 

```python

book_appointment('Alice Smith', 'Dr. John Doe', '2024-07-20 10:00 AM')

book_appointment('Bob Johnson', 'Dr. Jane Roe', '2024-07-20 11:30 AM')

```

 

creates two appointments and stores them in the list.

 

Finally:

 

```python

display_appointments()

```

 

prints all recorded appointments.

 

---

 

## 2. Three Limitations

 

### 1. No User Input

 

The appointments are hard-coded into the program.

 

```python

book_appointment('Alice Smith', ...)

```

 

A real system would allow users to enter appointment details themselves.

  

---

 

### 2. Limited Validation

 

Only the patient name is checked.

 

```python

if not patient_name:

```

 

The program does not verify:

 

- Practitioner name

- Appointment date format

- Appointment time format

- Future versus past dates

 

---

 

### 3. No Duplicate Booking Checks

 

The system allows multiple appointments to be booked at the same time with the same practitioner.

 

For example, two patients could be booked with Dr. John Doe at 10:00 AM.

 

---

 

## 3. Suggested Improvements

 

### Improvement 1: Add User Input

 

Use the `input()` function so users can enter:

 

- Patient name 

- Practitioner name

- Appointment time

 

This would make the system interactive.

 

---

 

### Improvement 2: Improve Validation

 

Check that:

 

- Practitioner names are not empty.

- Dates and times follow a valid format.

- Appointment dates are not in the past.

 

This would improve data quality.

 

---

 

### Improvement 3: Prevent Scheduling Conflicts

 

Before adding an appointment, check whether the practitioner already has an appointment at the requested time.

 

This would reduce booking errors.

 

---

 

### Additional Possible Improvements

 

- Allow appointments to be cancelled.

- Search for appointments by patient name.

- Save appointments to a file so data remains after the program closes.

- Sort appointments by date and time.

- Create a simple menu system for users.

 

---

 

## 4. Questions to Test Understanding

 

### Question 1

 

What is the purpose of the `appointments` list, and why is it useful compared with storing every appointment in separate variables?

- The purpose of making appointments as a list is to store every appointment in one place\
rather than having appointments stored in multiple places. It also meas that a new variable\
does not need to be made for each appointment.
 

---

 

### Question 2

 

In the `book_appointment()` function, what happens when this statement is executed?

 

```python

appointments.append(appointment)

```

 

Explain what is being added and where it is being stored.
- This command will add an appointment to the end of the list which allows the program to\
keep track of appointments

## AI Beginner Friendly Python Code
```python
def book_appointment(patient_name, practitioner_name, appointment_time):

    appointment = {

        "patient": patient_name,

        "practitioner": practitioner_name,

    "time": appointment_time

    }

 

    print("Appointment Booked")

    print(f"Patient: {appointment['patient']}")

    print(f"Practitioner: {appointment['practitioner']}")

    print(f"Time: {appointment['time']}")

 

# Example usage

book_appointment("Alice Smith", "Dr. John Doe", "20 July 2024, 10:00 AM")
```