# ER Diagram Workshop – Submission Template

## Objective
To understand and apply ER modeling concepts by creating ER diagrams for real-world applications.

## Purpose
Gain hands-on experience in designing ER diagrams that represent database structure including entities, relationships, attributes, and constraints.

---

# Scenario A: City Fitness Club Management

**Business Context:**  
FlexiFit Gym wants a database to manage its members, trainers, and fitness programs.

**Requirements:**  
- Members register with name, membership type, and start date.  
- Each member can join multiple programs (Yoga, Zumba, Weight Training).  
- Trainers assigned to programs; a program may have multiple trainers.  
- Members may book personal training sessions with trainers.  
- Attendance recorded for each session.  
- Payments tracked for memberships and sessions.

### ER Diagram:
*Paste or attach your diagram here*  
<img width="662" height="412" alt="image" src="https://github.com/user-attachments/assets/bcfe5322-1fb9-41bf-af39-a7122ed704db" />


### Entities and Attributes
<img width="669" height="408" alt="image" src="https://github.com/user-attachments/assets/c5d68d66-dd66-4b8e-b6af-2be809056adc" />


### Relationships and Constraints

<img width="670" height="346" alt="image" src="https://github.com/user-attachments/assets/bb41df72-f112-489a-96e2-90a15df10bd0" />

### Assumptions
* Each member has a unique MemberID and can join multiple fitness programs.

* Each trainer can teach multiple programs and conduct multiple personal training sessions.

* Every payment is made by one member and attendance is recorded for every training session.

---

# Scenario B: City Library Event & Book Lending System

**Business Context:**  
The Central Library wants to manage book lending and cultural events.

**Requirements:**  
- Members borrow books, with loan and return dates tracked.  
- Each book has title, author, and category.  
- Library organizes events; members can register.  
- Each event has one or more speakers/authors.  
- Rooms are booked for events and study.  
- Overdue fines apply for late returns.

### ER Diagram:
<img width="660" height="459" alt="image" src="https://github.com/user-attachments/assets/624c269c-048c-48de-bd94-42121812085c" />

### Entities and Attributes
<img width="666" height="398" alt="image" src="https://github.com/user-attachments/assets/e5c37d05-a4ba-43b6-bbbd-24bd14a23d48" />

### Relationships and Constraints
<img width="670" height="288" alt="image" src="https://github.com/user-attachments/assets/e6eb89f1-731a-4de3-9569-39af86cf4b30" />

### Assumptions
*Each member can borrow multiple books, but each loan record belongs to one member and one book.
*Every event is conducted in one room and may have one or more speakers.
*Overdue fines are applied only when a borrowed book is returned after its due date.
# Scenario C: Restaurant Table Reservation & Ordering

**Business Context:**  
A popular restaurant wants to manage reservations, orders, and billing.

**Requirements:**  
- Customers can reserve tables or walk in.  
- Each reservation includes date, time, and number of guests.  
- Customers place food orders linked to reservations.  
- Each order contains multiple dishes; dishes belong to categories (starter, main, dessert).  
- Bills generated per reservation, including food and service charges.  
- Waiters assigned to serve reservations.

### ER Diagram:
*Paste or attach your diagram here*  
<img width="664" height="266" alt="image" src="https://github.com/user-attachments/assets/d46a1006-48a1-4af9-a4c8-f7e4f9ab2c9e" />


### Entities and Attributes
<img width="669" height="401" alt="image" src="https://github.com/user-attachments/assets/a02aa736-166c-4189-9829-a86239a4caa9" />

### Relationships and Constraints
<img width="667" height="358" alt="image" src="https://github.com/user-attachments/assets/20f80691-a186-4e21-9976-dd598ebf0a65" />

### Assumptions
- A customer can make multiple reservations, but each reservation belongs to only one customer.
- Every reservation is assigned to one table and one waiter.
- Each reservation generates one bill, and an order can contain multiple dishes.
---
done by:LEKSHMEENDHRA S,212225040198
## Instructions for Students

1. Complete **all three scenarios** (A, B, C).  
2. Identify entities, relationships, and attributes for each.  
3. Draw ER diagrams using **draw.io / diagrams.net** or hand-drawn & scanned.  
4. Fill in all tables and assumptions for each scenario.  
5. Export the completed Markdown (with diagrams) as **a single PDF**
