Salesforce Day 3 – Data Modeling
1. Difference Between App, Object, Record, and Field
Term	Meaning
App	Collection of related tools and objects
Object	Database table that stores data
Record	Single row/data entry inside object
Field	Single column/property in object
Example
Object:

Student

Fields:
Student Name
Age
Email
Record:
Student Name	Age	Email
Rahul	20	rahul@gmail.com
2. Standard vs Custom Objects
Standard Objects	Custom Objects
Already provided by Salesforce	Created by users/developers
Example: Account, Contact	Example: Student, Course
Used for common CRM needs	Used for business-specific needs
3. College Management System Data Model

The task asks you to create these objects:

Student
Faculty
Course
Department
Objects and Relationships
Department Object

Fields:

Department Name
HOD Name
Faculty Object

Fields:

Faculty Name
Email
Department (Lookup)

Relationship:

One Department → Many Faculty
Course Object

Fields:

Course Name
Course Code
Total Seats
Department (Lookup)
Faculty (Lookup)

Relationship:

One Faculty → Many Courses
One Department → Many Courses
Student Object

Fields:

Student Name
Age
Email
Course (Lookup)

Relationship:

One Course → Many Students
Simple Relationship Diagram
Department
   |
   |---- Faculty
   |
   |---- Course
             |
             |---- Student
4. Formula Fields

The PDF asks for 3 examples with explanation.

Formula Field 1: Full Name

Formula:

First_Name + Last_Name

Why automatic?

Avoids manual typing
Reduces mistakes
Saves time
Formula Field 2: Remaining Seats

Formula:

Total Seats - Enrolled Students

Why automatic?

Updates instantly
Helps avoid overbooking
Formula Field 3: Percentage

Formula:

(Obtained Marks / Total Marks) * 100

Why automatic?

No manual calculation
Faster report generation
5. Validation Rules

The PDF asks for 3 rules with explanation.

Validation Rule 1: Email Cannot Be Empty

Why?

Prevents missing communication data
Validation Rule 2: Student Age Cannot Be Negative

Why?

Prevents invalid data entry
Validation Rule 3: Course Seats Cannot Exceed Limit

Why?

Prevents system inconsistency
Avoids admission errors
6. Reflection: Why Structured Data Matters

Companies cannot rely only on spreadsheets because:

Data becomes duplicated
Hard to maintain relationships
Difficult to generate reports
Multiple users create confusion
Errors increase
Security becomes difficult

Structured enterprise systems help:

Maintain clean data
Build relationships
Automate processes
Generate analytics and reports
