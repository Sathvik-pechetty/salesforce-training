##DAY 3 data-modeling
# 1. What is the difference between App, Object, Record, and Field?

An App is a collection of related objects and tools used for a business purpose. An Object is like a table that stores data. A Record is one row of data inside an object, and a Field is a single property or column inside the object.

Example: Student is an object. Name, Age, and Email are fields. Rahul, 20, and [rahul@gmail.com](mailto:rahul@gmail.com) together form one record.

---

# 2. What is the difference between Standard and Custom Objects?

Standard Objects are already available in Salesforce for common CRM tasks. Examples are Account and Contact. Custom Objects are created by users based on business needs. Examples are Student and Course.

---

# 3. Explain your College Management System Data Model.

The College Management System contains objects like Student, Faculty, Course, and Department. One department can have many faculty members and many courses. One faculty member can teach many courses, and one course can have many students.

The Student object contains fields like Student Name, Age, Email, and Course. The Faculty object contains Faculty Name, Email, and Department. The Course object contains Course Name, Course Code, and Total Seats. The Department object contains Department Name and HOD Name.

---

# 4. Give 3 Formula Fields with explanation.

The first formula field is Full Name, which combines First Name and Last Name automatically. This saves time and reduces mistakes.

The second formula field is Remaining Seats, which calculates available seats automatically by subtracting enrolled students from total seats. This helps prevent overbooking.

The third formula field is Percentage, which automatically calculates marks percentage. This avoids manual calculations and improves accuracy.

---

# 5. Give 3 Validation Rules with explanation.

The first validation rule is Email Cannot Be Empty. This prevents missing contact information.

The second validation rule is Student Age Cannot Be Negative. This prevents invalid data entry.

The third validation rule is Course Seats Cannot Exceed Limit. This prevents admission errors and maintains proper seat count.

---

# 6. Why is structured data important?

Structured data is important because it reduces duplicate data, improves reporting, and maintains relationships between data. It also helps companies manage large amounts of information easily.

Spreadsheets become difficult to manage when many users work on large datasets. Structured systems help maintain accuracy and organization.
