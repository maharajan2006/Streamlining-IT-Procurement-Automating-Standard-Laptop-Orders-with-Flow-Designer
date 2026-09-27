# Phase 5 – Project Development

## Project Title

**Streamlining IT Procurement: Automating Standard Laptop Orders**

## 1. Introduction

The Project Development phase focuses on implementing the proposed IT Procurement Automation System. The system is developed as a web-based application that automates the process of requesting, approving, and processing standard laptop orders.

The application consists of a frontend interface, FastAPI backend, and database. These components work together to provide a complete procurement workflow.

## 2. Development Technologies

The following technologies are used to develop the application:

* **HTML** – Used to create the frontend structure.
* **CSS** – Used to design and style the application.
* **JavaScript** – Used to provide client-side interaction and communicate with the backend.
* **Python** – Used for backend development.
* **FastAPI** – Used to create REST API endpoints.
* **SQLite** – Used to store application data.
* **Uvicorn** – Used to run the FastAPI application.
* **Visual Studio Code** – Used as the development environment.

## 3. Frontend Development

The frontend provides the user interface for the IT procurement system.

The main frontend pages include:

* Home Page
* Login Page
* Employee Dashboard
* Laptop Request Page
* Request Status Page
* Manager Dashboard
* Procurement Dashboard
* Administrator Dashboard

HTML is used to create forms, buttons, navigation menus, tables, and dashboard sections.

CSS is used to provide a consistent layout and improve the appearance of the application.

JavaScript is used to perform actions such as login, submitting laptop requests, retrieving request information, and communicating with the FastAPI backend.

## 4. Backend Development

The backend is developed using Python and FastAPI.

The backend handles the main application operations, including:

* User authentication
* Laptop information
* Laptop request creation
* Request retrieval
* Manager approval
* Manager rejection
* Procurement status updates
* Administrator statistics

FastAPI provides API endpoints that allow the frontend to communicate with the backend.

The backend receives data from the frontend, processes the request, communicates with the database, and returns the required result.

## 5. Database Development

SQLite is used as the database for the application.

The database stores information required for the procurement process.

The main database entities are:

### Users

Stores user information such as:

* User ID
* Name
* Email
* Password
* Role

### Laptops

Stores standard laptop information such as:

* Laptop ID
* Model Name
* Processor
* RAM
* Storage
* Operating System
* Price

### Requests

Stores laptop procurement request information such as:

* Request ID
* Employee ID
* Laptop ID
* Request Reason
* Request Date
* Approval Status
* Manager Comment
* Procurement Status

## 6. API Development

The FastAPI backend provides API endpoints for communication between the frontend and database.

The main API operations include:

| API Operation        | Purpose                      |
| -------------------- | ---------------------------- |
| Login API            | Authenticates users          |
| Laptop API           | Retrieves available laptops  |
| Create Request API   | Creates a laptop request     |
| User Requests API    | Retrieves employee requests  |
| All Requests API     | Retrieves all requests       |
| Request Decision API | Approves or rejects requests |
| Procurement API      | Updates procurement status   |
| Statistics API       | Retrieves system statistics  |

## 7. Login Coding

The login functionality accepts the user's email and password.

The frontend sends the login information to the FastAPI backend. The backend checks the credentials against the user information stored in the database.

If the credentials are correct, the user's role and account information are returned. The user is then redirected to the appropriate dashboard.

## 8. Laptop Request Coding

The employee can view the available standard laptops and select a suitable laptop.

The employee enters the reason for requesting the laptop and submits the form.

JavaScript sends the request information to the FastAPI backend.

The backend validates the information and stores the request in the SQLite database with an initial status of **Pending**.

## 9. Manager Approval Coding

The manager dashboard retrieves submitted laptop requests from the backend.

The manager can review the employee, laptop, and request details.

The manager can either approve or reject the request.

When approved, the request status changes to **Approved**.

When rejected, the request status changes to **Rejected**.

The manager can also provide a comment when processing the request.

## 10. Procurement Coding

Approved requests are displayed to the procurement team.

The procurement team processes the approved laptop order and updates its procurement status.

The procurement workflow can contain the following stages:

```text
Not Started
     ↓
Ordered
     ↓
Shipped
     ↓
Delivered
```

Each status update is stored in the database.

## 11. Request Tracking

Employees can view the current status of their submitted requests.

The system displays information such as:

* Laptop model
* Request date
* Approval status
* Manager comment
* Procurement status

This allows employees to monitor the progress of their laptop request.

## 12. Administrator Functionality

The administrator dashboard provides an overview of procurement activities.

The system can display:

* Total Requests
* Pending Requests
* Approved Requests
* Rejected Requests
* Delivered Orders

This information helps administrators monitor the overall system activity.

## 13. Complete Application Workflow

The complete application workflow is:

```text
User Login
     ↓
Role Identification
     ↓
Employee
     ↓
View Standard Laptops
     ↓
Submit Laptop Request
     ↓
Request Stored in Database
     ↓
Manager Reviews Request
     ↓
Approve / Reject
     ↓
If Approved
     ↓
Procurement Team
     ↓
Order Processing
     ↓
Ordered
     ↓
Shipped
     ↓
Delivered
     ↓
Employee Tracks Status
```

## 14. Coding Integration

The frontend, backend, and database are integrated to create a complete working system.

The frontend sends requests using JavaScript. FastAPI receives and processes these requests. The backend communicates with SQLite to store or retrieve information. The response is then sent back to the frontend and displayed to the user.

Therefore, the application follows the following architecture:

```text
Frontend
HTML + CSS + JavaScript
        ↓
FastAPI Backend
        ↓
Application Logic
        ↓
SQLite Database
        ↓
Response
        ↓
Frontend
```

## 15. Project Folder Structure

The development files are organized as follows:

```text
05-Project-Development/
│
├── backend/
│   ├── main.py
│   ├── database.py
│   ├── models.py
│   ├── schemas.py
│   └── crud.py
│
├── frontend/
│   ├── index.html
│   ├── login.html
│   ├── dashboard.html
│   ├── request.html
│   ├── requests.html
│   ├── manager.html
│   ├── procurement.html
│   ├── admin.html
│   ├── css/
│   │   └── style.css
│   └── js/
│       └── script.js
│
├── database/
│   └── procurement.db
│
├── requirements.txt
└── README.md
```

## 16. Testing During Development

During development, the main functions are checked to ensure that they work correctly.

The following functions are tested:

* User login
* Laptop catalog
* Laptop request submission
* Database insertion
* Request retrieval
* Manager approval
* Manager rejection
* Procurement status update
* Request tracking
* Administrator statistics

Errors identified during development are corrected before the final project demonstration.

## 17. Expected Output

The completed application provides a centralized platform for managing standard laptop procurement.

Employees can submit and track requests, managers can process requests, procurement teams can manage orders, and administrators can monitor procurement activities.

## 18. Conclusion

The Project Development phase converts the requirements and design into a functional IT procurement automation system.

The integration of HTML, CSS, JavaScript, Python, FastAPI, and SQLite provides a complete application for managing standard laptop requests from submission through delivery.

The developed system reduces manual procurement activities and provides a structured workflow for laptop request, approval, procurement, and tracking.
