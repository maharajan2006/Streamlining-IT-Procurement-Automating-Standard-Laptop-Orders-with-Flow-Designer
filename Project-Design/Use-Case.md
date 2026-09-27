# Use Case Design

## Project Title

**Streamlining IT Procurement: Automating Standard Laptop Orders**

## 1. Introduction

A Use Case describes how different users interact with the IT Procurement System to complete specific activities.

The system has four main users: Employee, Manager, Procurement Team, and Administrator.

## 2. Actors

### Employee

The employee can view standard laptops, submit laptop requests, and track request status.

### Manager

The manager reviews employee requests and approves or rejects them.

### Procurement Team

The procurement team processes approved laptop requests and updates the order status.

### Administrator

The administrator monitors users, requests, and procurement activities.

## 3. Use Case Table

| Use Case ID | Use Case Name          | Actor            | Description                                        | Precondition                | Outcome                           |
| ----------- | ---------------------- | ---------------- | -------------------------------------------------- | --------------------------- | --------------------------------- |
| UC-01       | Login                  | All Users        | User logs into the system using valid credentials. | User must have an account.  | User enters the system.           |
| UC-02       | View Laptop Catalog    | Employee         | Employee views available standard laptops.         | Employee must be logged in. | Laptop details are displayed.     |
| UC-03       | Submit Laptop Request  | Employee         | Employee selects a laptop and submits a request.   | Employee must be logged in. | Request is created.               |
| UC-04       | Track Request          | Employee         | Employee checks the request status.                | Request must exist.         | Current status is displayed.      |
| UC-05       | Review Request         | Manager          | Manager reviews employee laptop requests.          | Manager must be logged in.  | Request details are displayed.    |
| UC-06       | Approve Request        | Manager          | Manager approves a laptop request.                 | Request must be pending.    | Request becomes approved.         |
| UC-07       | Reject Request         | Manager          | Manager rejects a laptop request.                  | Request must be pending.    | Request becomes rejected.         |
| UC-08       | View Approved Requests | Procurement Team | Procurement team views approved requests.          | Request must be approved.   | Approved requests are displayed.  |
| UC-09       | Process Order          | Procurement Team | Procurement team processes an approved order.      | Request must be approved.   | Order processing begins.          |
| UC-10       | Update Order Status    | Procurement Team | Procurement team updates order progress.           | Order must exist.           | Order status is updated.          |
| UC-11       | View Statistics        | Administrator    | Administrator views procurement statistics.        | Admin must be logged in.    | Statistics are displayed.         |
| UC-12       | Monitor Requests       | Administrator    | Administrator monitors procurement requests.       | Admin must be logged in.    | Request information is displayed. |

## 4. Use Case Flow Chart

```text
                    START
                      |
                      v
               +--------------+
               |     Login    |
               +--------------+
                      |
                      v
              +---------------+
              | Select User   |
              |     Role      |
              +---------------+
                      |
          +-----------+-----------+-------------+
          |           |           |             |
          v           v           v             v
     +---------+ +---------+ +-----------+ +---------+
     |Employee | | Manager | |Procurement| |  Admin  |
     +---------+ +---------+ +-----------+ +---------+
          |           |           |             |
          v           v           v             v
     View Laptop   Review      View Approved   View
      Catalog      Request       Requests     Statistics
          |           |           |             |
          v           |           v             |
    Submit Request    |       Process Order     |
          |           |           |             |
          v           v           v             v
      Pending     +--------+   Update       Monitor
      Request     |Approve |   Status       Requests
          |       |   /    |      |             |
          |       |Reject  |      v             |
          |       +--------+   Ordered          |
          |          |          |               |
          |          |          v               |
          |          |       Shipped            |
          |          |          |               |
          |          |          v               |
          |          |      Delivered           |
          |          |                          |
          +----------+--------------------------+
                             |
                             v
                       Track Status
                             |
                             v
                            END
```

## 5. Employee Flow

```text
Login
  ↓
View Laptop Catalog
  ↓
Select Laptop
  ↓
Enter Request Details
  ↓
Submit Request
  ↓
Request Pending
  ↓
Track Request Status
```

## 6. Manager Flow

```text
Login
  ↓
View Pending Requests
  ↓
Review Request
  ↓
Decision
  ↓
Approve OR Reject
  ↓
Update Request Status
```

## 7. Procurement Flow

```text
Login
  ↓
View Approved Requests
  ↓
Process Laptop Order
  ↓
Order Placed
  ↓
Shipped
  ↓
Delivered
  ↓
Update Final Status
```

## 8. Administrator Flow

```text
Login
  ↓
Open Admin Dashboard
  ↓
View Users
  ↓
View Requests
  ↓
View Procurement Information
  ↓
View Statistics
  ↓
Monitor System
```

## 9. Overall System Flow

The complete system starts when a user logs into the application.

An employee selects a standard laptop and submits a request. The request is sent to the manager for review.

The manager can approve or reject the request. Approved requests are passed to the procurement team.

The procurement team processes the order and updates the status through the procurement stages until the laptop is delivered.

The employee can track the request status, while the administrator can monitor the overall system activities.

## 10. Conclusion

The Use Case Design provides a clear description of the interactions between system users and the IT Procurement System.

The flow begins with user login and continues through laptop selection, request submission, approval, procurement processing, delivery, and status tracking.
