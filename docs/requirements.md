# Software Requirements Specification

## 1. Purpose

This document defines the functional and non-functional requirements of Civic Infrastructure Intelligence, a web-based civic incident management and decision-support platform.

The purpose of the system is to help organize civic infrastructure reports, identify related incidents, prioritize repairs, recommend responsible departments, coordinate repair teams, and monitor resolution outcomes.

## 2. Project Scope

The initial version will be a functional prototype that simulates the workflow of a civic infrastructure management system. It will support citizen submissions, incident processing, officer workflows, and administrative analytics using sample or demonstration data.

The project will not directly dispatch real municipal workers or replace official reporting channels.

## 3. User Roles

### 3.1 Citizen

A citizen can:
- Register and log in.
- Submit a civic issue with a category, description, and location.
- Upload a supporting photograph when available.
- View their submitted reports and current status.
- View relevant public incident information.
- Submit feedback about a reported issue.
- Request reconsideration when an issue appears unresolved, subject to system rules.

### 3.2 Municipal Officer

An officer can:
- View incidents assigned to their department.
- Review incident descriptions, locations, and supporting reports.
- View priority scores and the factors contributing to them.
- Update incident status.
- Assign or recommend repair teams, subject to permissions.
- Record repair notes and upload resolution evidence.
- Review feedback and reopened incidents.

### 3.3 Administrator

An administrator can:
- Manage departments and repair teams.
- View and manage incidents across departments.
- Review duplicate-detection suggestions.
- Configure priority-scoring weights.
- Monitor unresolved, overdue, and recurring incidents.
- Access analytical dashboards and system-level summaries.

## 4. Functional Requirements

### FR-01: Authentication and Authorization
The system shall allow users to register and log in. Access to citizen, officer, and administrator operations shall be controlled by user roles.

### FR-02: Civic Issue Reporting
The system shall allow a citizen to submit an issue with a category, description, location, and optional photograph.

### FR-03: Report Storage
The system shall persist reports and their submission timestamps in the database.

### FR-04: Report Tracking
Citizens shall be able to view their reports and the latest status associated with them.

### FR-05: Incident Aggregation
The system shall distinguish individual reports from underlying real-world incidents. Multiple reports may be linked to one incident.

### FR-06: Duplicate Detection
The system shall identify potentially duplicate reports using factors such as geographical distance, category, and textual similarity. Suggested matches shall be reviewable, and uncertain matches shall not be merged automatically without appropriate safeguards.

### FR-07: Priority Scoring
The system shall calculate an explainable incident priority score using configurable factors such as severity, safety risk, recurrence, affected population, and waiting time.

### FR-08: Department Recommendation
The system shall recommend a responsible department based on the incident category and configurable routing rules.

### FR-09: Repair-Team Allocation
The system shall recommend suitable repair teams based on required skills, availability, workload, distance, and incident priority.

### FR-10: Incident Status Management
The system shall support a defined status workflow and record status changes with timestamps and the responsible user.

### FR-11: Resolution Verification
The system shall support repair evidence, citizen feedback, and a mechanism to flag an incident for review when the issue remains unresolved.

### FR-12: Map Visualization
The system shall display incident locations on a map using geographical coordinates.

### FR-13: Analytics Dashboard
The system shall summarize incident counts, categories, priorities, resolution times, overdue incidents, reopened incidents, and recurring problem areas.

### FR-14: Audit History
The system shall maintain an appropriate history of incident status changes and assignment actions.

### FR-15: Optional Machine Learning
If suitable data is available, the project may include a machine-learning model for category classification or another clearly defined task. ML predictions shall be treated as recommendations and evaluated before use.

## 5. Non-Functional Requirements

### NFR-01: Usability
The interface should be understandable to users with basic web browsing skills.

### NFR-02: Performance
Common API operations should respond within a reasonable time under the expected demonstration workload. Performance shall be measured during testing rather than assumed.

### NFR-03: Security
Passwords shall be stored using a suitable password-hashing algorithm. Protected endpoints shall enforce authentication and role-based authorization.

### NFR-04: Data Integrity
Database constraints shall prevent invalid relationships and inconsistent records where possible.

### NFR-05: Maintainability
The frontend, backend, database definitions, algorithms, and optional ML experiments shall be organized into clearly defined modules.

### NFR-06: Reliability
The application shall validate inputs, handle expected errors, and avoid silently losing report or status information.

### NFR-07: Explainability
Priority scores and automated recommendations shall expose the principal factors behind their results.

### NFR-08: Privacy
The system shall collect only the personal information required for the prototype. Credentials, private configuration, and sensitive personal data shall not be committed to the public repository.

### NFR-09: Testability
Core business rules and algorithms shall have repeatable tests using controlled sample data.

### NFR-10: Accessibility and Responsiveness
The interface should support common desktop and mobile screen sizes, with readable text, keyboard-accessible controls, and clear form errors.

## 6. Constraints and Assumptions

- The project will initially use sample or synthetic civic incident data.
- Real municipal integrations are outside the initial scope.
- Map services and geocoding providers may have usage limits and terms that must be respected.
- Image uploads will be subject to file type and size validation.
- Team availability and repair duration may be simulated for the prototype.
- ML functionality is optional and depends on data quality and project time.
- Human review will remain available for uncertain duplicate matches and important allocation decisions.

## 7. Acceptance Criteria

The initial prototype will be considered functionally complete when:

1. A citizen can register, log in, and submit a valid report.
2. A report is saved and can be retrieved from the database.
3. Related reports can be linked to a common incident without losing their individual records.
4. Incidents receive priority scores with visible explanations.
5. The system recommends an appropriate department.
6. Authorized officers can assign incidents and update statuses.
7. Status history and resolution evidence can be recorded.
8. The dashboard displays meaningful summaries from stored data.
9. Core workflows and algorithms pass their defined tests.
10. Setup instructions allow another developer to run the prototype locally.

## 8. Future Enhancements

Possible extensions include image-based issue classification, resolution-time prediction, recurrence-risk prediction, notifications, multilingual reporting, and integration with authorized municipal datasets.
