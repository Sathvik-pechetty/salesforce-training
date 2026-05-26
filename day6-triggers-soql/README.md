
# 1. What is SOQL?

SOQL (Salesforce Object Query Language) is a query language used in Salesforce to retrieve data from objects. It is similar to SQL but designed specifically for Salesforce data.

### Example:

```sql
SELECT Name, Email FROM Student__c
```

This query retrieves the Name and Email fields from the Student object.

---

# 2. What is an Apex Trigger?

An Apex Trigger is code that automatically executes before or after events occur on Salesforce records, such as insert, update, delete, or undelete.

Triggers help automate business logic inside Salesforce.

### Example:

```apex
trigger StudentTrigger on Student__c (before insert) {
    System.debug('New student record created');
}
```

---

# 3. Difference

## Flow vs Trigger

| Flow                           | Trigger                   |
| ------------------------------ | ------------------------- |
| Declarative (No-code/Low-code) | Programmatic (Code-based) |
| Easier to build                | Requires Apex coding      |
| Best for simple automation     | Best for complex logic    |
| Limited flexibility            | Highly customizable       |
| Faster for admins              | Better for developers     |

---

## Before Trigger vs After Trigger

| Before Trigger                            | After Trigger                             |
| ----------------------------------------- | ----------------------------------------- |
| Executes before data is saved             | Executes after data is saved              |
| Used for validation and updating fields   | Used for related records and integrations |
| Faster because changes happen before save | Used when record ID is needed             |
| Example: Set default values               | Example: Send notifications               |

---

# 4. Trigger Use Cases (5 Examples)

### 1. Auto Generate Student ID

When a new student record is created, automatically generate a unique student ID.

---

### 2. Prevent Duplicate Email

Before saving a student record, check whether the email already exists.

---

### 3. Send Notification After Admission

After admission is confirmed, automatically send a welcome email.

---

### 4. Update Remaining Seats

When a student enrolls in a course, automatically reduce available seats.

---

### 5. Attendance Warning System

If attendance falls below 75%, automatically create a warning notification.

---

# 5. Query Examples (Question + Answer)

### Q1: Retrieve all student names

```sql
SELECT Name FROM Student__c
```

---

### Q2: Retrieve student email and phone number

```sql
SELECT Email__c, Phone__c FROM Student__c
```

---

### Q3: Find students with attendance below 75%

```sql
SELECT Name FROM Student__c WHERE Attendance__c < 75
```

---

### Q4: Retrieve all courses with available seats

```sql
SELECT Name, Remaining_Seats__c FROM Course__c
```

---

### Q5: Find students from CSE department

```sql
SELECT Name FROM Student__c WHERE Department__c = 'CSE'
```

---

### Q6: Retrieve top 5 students by marks

```sql
SELECT Name, Marks__c FROM Student__c ORDER BY Marks__c DESC LIMIT 5
```
