EventX – Online Event Management System

 Project Overview

EventX is an Online Event Management System designed to simplify the discovery, organization, and registration of college events. The platform provides a user-friendly interface where students can explore campus events, view event details, and manage their registrations.

The project aims to integrate a modern web interface with a Java-based backend and a MySQL database to demonstrate full-stack development, Object-Oriented Programming, database connectivity, and web application development.

 Problem Statement

College event information is often distributed across multiple platforms, making it difficult for students to discover events and manage registrations efficiently. Organizers also need a centralized system to manage event details and participant information.

EventX aims to address these challenges by providing a centralized platform for event discovery, registration, and administration.

 Proposed Solution

EventX brings students and event organizers together through a single web application. It is designed to support event browsing, registration management, centralized data storage, and administrative operations.

 Key Features

Student Features

- Browse and explore college events.
- View event details, dates, venues, and descriptions.
- Register for events.
- View registration information.
- Submit feedback for events.

Admin and Organizer Features

- Create and manage events.
- Update event information.
- View registered participants.
- Manage event registrations.
- Monitor event information and participation.

The availability of each feature depends on its implementation and successful integration.

🛠️ Technology Stack

Frontend

- HTML
- CSS
- TypeScript
- Responsive web interface

Backend — Integration Target

- Java
- Java Servlets
- JDBC
- Core Java and Object-Oriented Programming

Database — Integration Target

- MySQL

Development Tools

- Replit
- Git
- GitHub
- Node.js and pnpm for frontend tooling

 System Architecture

The planned application architecture separates the user interface, request handling, business logic, and database operations.

Student / Admin
       |
       v
Frontend Interface
       |
       v
Java Servlets
       |
       v
Service / Business Logic
       |
       v
DAO (Data Access Objects)
       |
       v
JDBC
       |
       v
MySQL Database

This layered design improves code organization, maintainability, and separation of responsibilities.

 Core Java Concepts

The Java implementation is intended to demonstrate the following concepts required by the university project rubric.

1. Object-Oriented Programming

- Classes and objects
- Encapsulation
- Inheritance
- Polymorphism
- Abstraction
- Interfaces

2. Exception Handling

- try-catch-finally
- throw and throws
- Custom exception classes
- Handling database and application errors

3. Collections and Generics

- List, ArrayList, and Map
- Type-safe collections
- Generic classes and methods
- Managing event and registration data

4. Multithreading and Synchronization

- Thread creation and execution
- Runnable interface
- Synchronization for shared resources
- Safe handling of concurrent operations where required

5. Database Operations

- JDBC connectivity
- PreparedStatement and ResultSet
- CRUD operations
- DAO classes
- Transaction management where appropriate

6. Web Integration

- Java Servlets
- HTTP request and response handling
- Frontend and backend communication
- Server-side validation

These concepts should be considered complete only after they have been implemented and verified in the source code.

 Database Design

The planned MySQL database includes the following entities.

Users

Stores user information and account roles.

Possible fields:

- user_id
- name
- email
- password_hash
- role

Events

Stores information about college events.

Possible fields:

- event_id
- title
- description
- event_date
- venue
- organizer_id

Registrations

Stores student registrations for events.

Possible fields:

- registration_id
- user_id
- event_id
- registration_date
- status

Feedback

Stores feedback submitted by participants.

Possible fields:

- feedback_id
- user_id
- event_id
- rating
- comments

The final schema should define primary keys, foreign keys, suitable constraints, and relationships between tables.

 Repository Structure

The repository currently contains frontend-related files and configuration. The structure below describes the intended organization as the Java backend and database are added.

EventX-Event-Hub/
│
├── artifacts/
├── attached_assets/
├── lib/
├── scripts/
├── src/
│   └── main/
│       ├── java/
│       │   └── eventx/
│       │       ├── model/
│       │       ├── dao/
│       │       ├── service/
│       │       ├── servlet/
│       │       └── util/
│       └── webapp/
│
├── database/
│   └── event_management.sql
│
├── package.json
├── pnpm-lock.yaml
├── .gitignore
├── pom.xml
└── README.md

This is the target structure, not a claim that every directory or file already exists.

⚙️ Requirements

Frontend

- Node.js
- pnpm, if required by the project

Java Backend

- A compatible JDK
- Apache Tomcat or another compatible Servlet container
- Maven, if the project uses Maven

Database

- MySQL Server
- A MySQL client for database setup and inspection

Exact versions and dependencies should be documented after the final configuration is confirmed.

 Getting Started

1. Clone the Repository

git clone https://github.com/AtharvGupta/EventX-Event-Hub.git
cd EventX-Event-Hub

2. Install Frontend Dependencies

If the root "package.json" contains the appropriate scripts, run:

pnpm install
pnpm run dev

Use the actual scripts defined in "package.json" if these commands differ.

3. Configure the MySQL Database

After the database schema has been added:

1. Start MySQL Server.
2. Create the EventX database.
3. Import the SQL schema.
4. Configure the database connection using environment variables or a secure local configuration.
5. Verify the database connection.

Example database name:

event_management

4. Configure the Java Backend

After the backend has been implemented:

1. Install the required JDK and build tools.
2. Configure the Servlet container.
3. Set the database connection properties securely.
4. Build and deploy the Java application.
5. Verify the backend endpoints.

The exact build and deployment commands will depend on the final project configuration.

5. Test the Application

- Open the frontend in a browser.
- Test event browsing and navigation.
- Test registration and validation.
- Verify backend responses.
- Verify database insert, read, update, and delete operations.
- Test error handling and relevant concurrent operations.

 Security

- Do not commit database passwords, API keys, access tokens, or other secrets.
- Store credentials in environment variables or an appropriate secret manager.
- Use PreparedStatement for parameterized SQL queries.
- Store password hashes rather than plain-text passwords.
- Validate input on the server.
- Apply authorization checks to administrative operations.

 Testing Strategy

Testing should cover:

- Frontend navigation and user interactions.
- Event creation and updating.
- Student registration.
- Input validation and exception handling.
- JDBC connectivity and database operations.
- Servlet request and response handling.
- Authentication and role-based access, when implemented.
- Multithreading and synchronization requirements, where applicable.

 University Project Evaluation

The project will be developed and verified against the following areas of the university marking rubric.

Evaluation Area| Maximum Marks
Solution Design| 8
Core Java and OOP| 10
JDBC and Database Integration| 8
Servlets and Web Integration| 7
Total| 33

The final implementation and demonstration must provide evidence for each category. The README itself does not establish that these marks or requirements have been achieved.

 Future Enhancements

- Complete Java backend integration.
- MySQL database persistence.
- Secure student and administrator authentication.
- Event creation and management.
- Registration tracking.
- Participant management.
- Feedback and ratings.
- Improved validation, testing, and error handling.

 Project Status

The EventX frontend is available in the repository. Java backend development, database connectivity, and full integration must be verified against the current source code before being considered complete.

📄 License

No license has been selected for this project yet. A suitable license can be added if the project is intended for public reuse.
