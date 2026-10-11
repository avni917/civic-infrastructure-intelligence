# Project Scope and Objectives

## 1. Project Overview

Civic Infrastructure Intelligence is a proposed web-based platform for civic incident management and decision support. It will organize citizen reports, support incident prioritization, recommend responsible departments and repair teams, and provide insights into recurring infrastructure problems.

## 2. Vision

To demonstrate how civic data and computational methods can support more systematic, transparent, and accountable infrastructure incident management.

## 3. Primary Objectives

- Build a web interface for submitting and tracking civic infrastructure issues.
- Organize individual reports into underlying incidents.
- Identify potentially duplicate reports.
- Calculate explainable priority scores.
- Recommend departments based on incident categories.
- Support repair-team recommendations using relevant operational factors.
- Visualize incident locations and recurring problem areas.
- Track assignments, status changes, repair evidence, and feedback.
- Apply selected data structures and algorithms to meaningful problems.
- Evaluate the system through controlled tests and a working demonstration.

## 4. Intended Users

### Citizens
Submit reports, view relevant incident information, track progress, and provide feedback.

### Municipal Officers
Review incidents, prioritize work, manage assignments, and update resolution status.

### Administrators
Manage departments and teams, review system-wide incidents, and monitor performance indicators.

## 5. Functional Scope

### Phase 1: Core Platform
- User registration and login.
- Role-based access.
- Civic issue submission.
- Report storage and retrieval.
- Incident details and status tracking.

### Phase 2: Decision Support
- Duplicate candidate detection.
- Incident priority scoring.
- Department recommendation.
- Incident assignment and status history.

### Phase 3: Geographical and Operational Intelligence
- Map-based incident visualization.
- Repair-team suitability recommendations.
- Basic shortest-path calculations on a simplified graph.
- Incident trend and hotspot analysis.

### Phase 4: Evaluation and Optional Extensions
- Resolution feedback and verification workflow.
- Evaluation of duplicate detection and priority scoring.
- Optional machine-learning experiments.
- Deployment and performance improvements.

## 6. Out of Scope for the Initial Prototype

The initial version will not require:

- Integration with live municipal systems.
- Actual dispatch of repair workers.
- Guaranteed detection of every duplicate.
- Fully automated high-impact decisions without human review.
- A production-grade emergency response system.
- Advanced computer vision or large language models.
- A distributed microservices architecture.

These capabilities may be reconsidered if time, data, and technical requirements justify them.

## 7. Proposed Technology Direction

| Area | Proposed technology |
|---|---|
| Frontend | React, JavaScript, HTML, CSS |
| Backend | Python and FastAPI |
| Database | PostgreSQL |
| Algorithms | C |
| Data analysis | Python, pandas, NumPy |
| Optional machine learning | scikit-learn |
| Mapping | Leaflet and OpenStreetMap |
| Version control | Git and GitHub |

These are initial technology choices. They may be revised during planning if an alternative better fits the team's learning needs or project constraints.

## 8. Success Criteria

The project will aim to demonstrate that:

1. Users can complete the relevant workflows according to their roles.
2. Submitted reports are stored and retrieved correctly.
3. Multiple reports can be associated with one incident without losing their individual records.
4. Priority scores are reproducible and their contributing factors are visible.
5. Department and team recommendations respect defined rules and constraints.
6. Incident status and assignment history can be inspected.
7. Maps and dashboards communicate meaningful information from stored data.
8. Core algorithms pass test cases with known expected results.
9. The application can be set up and demonstrated using documented instructions.
10. The project clearly documents its limitations and evaluation results.

## 9. Constraints

- The project is being developed by two students.
- The initial development period is approximately three months.
- Both developers will need to learn parts of the proposed stack.
- Real municipal operational data may not be available.
- Advanced features will depend on the progress of the core platform.

## 10. Guiding Principle

The project will prioritize a reliable, demonstrable end-to-end system over a large collection of incomplete advanced features.
