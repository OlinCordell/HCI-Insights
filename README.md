# Project Title: **HCI Insights**

## Live Demo
**[Visit HCI Insights here...](https://hci-insights-production-a92a.up.railway.app)**

## Problem and Domain

Human-Computer Interaction workflows are sometimes scattered among several different applications and services, limiting scalability and efficiency. A smooth and interactive application is paramount for HCI and UX/UI researchers. HCI Insights operates within the design, management, execution, and analysis of usability studies for different products and services.

## Solution

This web application centralizes the workflow of HCI/UX/UI research teams by facilitating the planning, execution, and analysis of usability studies. It handles participants, tasks, subtasks, sessions, results, studies, users, and analytics - all backed by a MySQL database that is exposed through a secure SpringBoot framework.

## Project Ownership

This project was completed as part of a team-based course. I was responsible for the primary design and implementation of the system, including the database schema, backend architecture, core application logic, and deployment. Other team members contributed primarily through testing and feedback.

## Key Features

- User authentication and authorization
- Study creation and lifecycle management
- Participant enrollment and session assignment
- Task and subtask modeling per study
- Analytics views for study performance and outcomes
- Relational integrity enforced via normalized schema

## Technologies Used

SpringBoot, Mustache, MySQL, Java, Maven, JDBC, Git + Github,
JS, Railway (for deployment), CSS

## System Architecture

HCI Insights follows a traditional server-rendered MVC architecture:

- **Presentation Layer:** Mustache templates rendered server-side
- **Application Layer:** Spring Boot controllers and services handling business logic
- **Data Layer:** MySQL database accessed via JDBC
- **Deployment:** Containerized and deployed to Railway with environment-based configuration

## Database Design

The database schema was designed to facilitate complex relationships between studies, participants, sessions, tasks, and results.

Key Considerations:
- Normalized to reduce redudancy and maintain consistency according to 3NF standards
- Foreign key constraints to enforce relational integrity
- Designed to support multiple studies and concurrent users

## ER Diagram

![ER Diagram](./ER_Diagram_DBMS.pdf)

## Design Considerations

- Chose server-side rendering with Mustache for simplicity and predictable state management
- Used JDBC instead of an ORM to maintain explicit control over SQL queries and schema interactions
- Focused on relational integrity over horizontal scalability, given project constraints
- Prioritized correctness over premature optimization