# 1. What is the difference between App, Object, Record, and Field?

| Term   | Simple Meaning                          |
| ------ | --------------------------------------- |
| App    | Collection of related objects and tools |
| Object | Table that stores data                  |
| Record | One row of data inside object           |
| Field  | One column/property inside object       |

### Example:

* Object → Student
* Fields → Name, Age, Email
* Record → Rahul, 20, [rahul@gmail.com](mailto:rahul@gmail.com)

---

# 2. What is the difference between Standard and Custom Objects?

| Standard Objects                | Custom Objects                 |
| ------------------------------- | ------------------------------ |
| Already available in Salesforce | Created by users               |
| Example: Account, Contact       | Example: Student, Course       |
| Used for common CRM work        | Used for custom business needs |

---

# 3. Explain your College Management System Data Model.

### Objects:

* Student
* Faculty
* Course
* Department

### Relationships:

* One Department has many Faculty
* One Department has many Courses
* One Faculty teaches many Courses
* One Course has many Students

### Student Fields:

* Student Name
* Age
* Email
* Course

### Faculty Fields:

* Faculty Name
* Email
* Department

### Course Fields:

* Course Name
* Course Code
* Total Seats

### Department Fields:

* Department Name
* HOD Name

---

# 4. Give 3 Formula Fields with explanation.

## Formula Field 1: Full Name

Formula:

```text id="dxb78u"
First_Name + Last_Name
```

Why?

* Automatically combines names
* Saves time
* Reduces mistakes

---

## Formula Field 2: Remaining Seats

Formula:

```text id="t1n0yc"
Total Seats - Enrolled Students
```

Why?

* Updates automatically
* Prevents overbooking

---

## Formula Field 3: Percentage

Formula:

```text id="5e3c2d"
(Obtained Marks / Total Marks) * 100
```

Why?

* Calculates marks automatically
* Avoids manual calculation

---

# 5. Give 3 Validation Rules with explanation.

## Validation Rule 1: Email Cannot Be Empty

Why?

* Prevents missing contact information

---

## Validation Rule 2: Student Age Cannot Be Negative

Why?

* Prevents invalid data entry

---

## Validation Rule 3: Course Seats Cannot Exceed Limit

Why?

* Prevents admission errors
* Maintains correct seat count

---

# 6. Why is structured data important?

Structured data is important because:

* It avoids duplicate data
* Makes reports easier
* Maintains relationships between data
* Reduces errors
* Helps companies manage large data easily

Spreadsheets become difficult when many users and large amounts of data are involved.
