# Development Plan

## 1. Project Goal

Build a functional, well-tested civic infrastructure decision-support prototype that combines full-stack development, database design, data structures and algorithms, geographical visualization, and optional machine learning.

The priority is a reliable end-to-end application before adding advanced features.

## 2. Development Principles

- Build the simplest working version of each feature first.
- Keep the frontend, backend, database, and algorithm modules clearly separated.
- Use Git branches and pull requests for collaborative changes.
- Test core logic independently before integrating it.
- Use synthetic or appropriately licensed data during development.
- Keep priority calculations explainable.
- Treat automated recommendations as decision support, not unquestionable decisions.
- Avoid introducing technologies that do not solve a defined project requirement.

## 3. Project Milestones

### Milestone 1: Requirements and Planning

Tasks:
- Finalize the problem statement.
- Agree on user roles and initial features.
- Document the functional and non-functional requirements.
- Design the system architecture and API.
- Identify the core database entities.
- Create GitHub issues for the initial implementation tasks.

Deliverables:
- Problem statement.
- Requirements document.
- Architecture document.
- API design.
- Initial task board.

### Milestone 2: Development Environment and UI

Tasks:
- Set up the frontend project with React.
- Set up the backend project with FastAPI.
- Configure environment variables and `.env.example`.
- Establish code formatting and basic testing conventions.
- Create initial page layouts and navigation.
- Create the initial database schema.

Deliverables:
- Frontend and backend start locally.
- A basic frontend-to-backend health check works.
- Initial database schema is version-controlled.

### Milestone 3: Authentication and Reporting

Tasks:
- Implement registration and login.
- Add role-based authorization.
- Build the citizen reporting form.
- Validate descriptions, categories, and coordinates.
- Support optional photograph uploads.
- Store reports in PostgreSQL.
- Implement report listing and detail views.

Deliverables:
- A citizen can submit and retrieve a report.
- Protected operations enforce permissions.
- Invalid requests are handled safely.

### Milestone 4: Incident Management

Tasks:
- Create the incident entity separately from individual reports.
- Define incident statuses and allowed transitions.
- Link reports to incidents.
- Implement incident details and status history.
- Build the basic officer dashboard.
- Add the first department-routing rules.

Deliverables:
- Multiple reports can support one incident.
- Officers can review and update incident status.
- Status history is preserved.

### Milestone 5: Duplicate Detection and Prioritization

Tasks:
- Calculate geographical distance between reports.
- Compare report categories.
- Implement text similarity using an appropriate method.
- Generate duplicate candidates.
- Add a review mechanism for uncertain matches.
- Implement a configurable priority-scoring formula.
- Display the score and its contributing factors.

Deliverables:
- The system identifies candidate duplicates.
- Priority scores are reproducible and explainable.
- False matches can be reviewed and corrected.

### Milestone 6: Repair-Team Assignment and C Algorithms

Tasks:
- Model departments, team skills, availability, and workload.
- Implement a baseline team-suitability score.
- Implement a binary heap or priority queue in C.
- Represent a simplified road network as a graph.
- Implement and test Dijkstra's shortest-path algorithm.
- Evaluate a basic allocation heuristic.
- Integrate selected C functions with Python.

Deliverables:
- The backend can recommend a suitable repair team.
- The C algorithms have independent tests.
- The integration handles errors and invalid inputs.

### Milestone 7: Maps and Analytics

Tasks:
- Add a map using Leaflet and OpenStreetMap.
- Display incident markers with appropriate filtering.
- Add category and status charts.
- Calculate resolution duration where timestamps are available.
- Identify recurring incidents by area and category.
- Add a basic hotspot visualization.
- Protect private citizen information.

Deliverables:
- Citizens and officers can explore relevant incidents on a map.
- Administrators can view useful summary metrics and trends.

### Milestone 8: Verification, Testing, and Deployment

Tasks:
- Add unit and API integration tests.
- Test role permissions and invalid status transitions.
- Test duplicate-detection edge cases.
- Test priority and allocation algorithms against known examples.
- Test frontend loading, error, and empty states.
- Fix major usability and reliability issues.
- Write setup and deployment instructions.
- Prepare a demonstration dataset and project presentation.
- Deploy a working demonstration if resources permit.

Deliverables:
- A reproducible local setup.
- A tested end-to-end demonstration.
- Updated documentation and screenshots.
- A clear list of limitations and future work.

## 4. Suggested 12-Week Schedule

| Week | Main focus | Expected result |
|---|---|---|
| 1 | Requirements, architecture, repository setup | Documentation and task board |
| 2 | React and FastAPI scaffolding, database design | Working development environment |
| 3 | Authentication and authorization | Protected application routes |
| 4 | Report creation, uploads, retrieval | Citizen reporting workflow |
| 5 | Incident model, departments, status history | Basic officer workflow |
| 6 | Duplicate detection and review | Candidate matching |
| 7 | Priority scoring and explanation | Ranked incident queue |
| 8 | Team assignment and officer dashboard | Assignment workflow |
| 9 | C heap and graph algorithms | Independently tested algorithms |
| 10 | Algorithm integration, maps, analytics | Improved decision support |
| 11 | Integration testing and optional ML | Stable end-to-end prototype |
| 12 | Bug fixes, deployment, documentation, demo | Portfolio-ready release |

This is a target schedule, not a guarantee. If a milestone slips, prioritize the working end-to-end system over optional ML or advanced optimization.

## 5. Feature Priorities

### P0 — Must Have

- Authentication and role-based authorization.
- Report submission and database persistence.
- Report-to-incident relationships.
- Incident listing and details.
- Department recommendation.
- Explainable priority scoring.
- Status workflow and audit history.
- Basic officer dashboard.
- Automated tests and setup documentation.

### P1 — Important

- Duplicate candidate detection and review.
- Map-based incident visualization.
- Repair-team assignment recommendations.
- Resolution evidence and citizen feedback.
- Administrative analytics.
- At least one meaningful C algorithm integrated with the application.

### P2 — Advanced

- Shortest-path routing over a simplified road graph.
- Team-allocation optimization.
- Advanced hotspot analysis.
- Machine-learning category classification.
- Resolution-time or recurrence-risk prediction.
- Notifications and additional user-experience improvements.

P0 features must be stable before the team commits substantial time to P2 features.

## 6. Suggested Team Responsibilities

The split below is a starting point. Both developers should understand the complete system and review each other's work.

### Developer A: Backend, Data, and Algorithms

- FastAPI endpoints and application services.
- PostgreSQL schema and database integration.
- Incident aggregation and duplicate detection.
- Priority scoring and department-routing rules.
- C algorithm implementations and Python integration.
- Optional ML experiments and model evaluation.
- Backend tests and API documentation.

### Developer B: Frontend and User Experience

- React application structure and navigation.
- Citizen reporting forms and report history.
- Incident detail views.
- Officer and administrator dashboards.
- Maps, charts, filters, and responsive layouts.
- API integration and frontend error handling.
- Frontend tests and usability improvements.

### Shared Responsibilities

- Requirements and architecture decisions.
- Database and API contract reviews.
- Integration testing.
- Pull-request reviews.
- Debugging cross-component issues.
- README, documentation, presentation, and demo preparation.

Responsibilities can change as each developer learns new parts of the stack.

## 7. GitHub Collaboration Workflow

1. Create a GitHub issue for each meaningful task.
2. Assign an owner and define acceptance criteria.
3. Create a feature branch from the latest `main`.
4. Implement the feature in small commits.
5. Run relevant tests before opening a pull request.
6. Request review from the other developer.
7. Merge only after reviewing the changes and resolving conflicts.
8. Update documentation when the behavior or API changes.

Example branch names:

- `feat/citizen-report-form`
- `feat/report-api`
- `feat/incident-priority`
- `feat/duplicate-detection`
- `feat/c-algorithms`
- `test/assignment-engine`

Example commit messages:

- `feat: add civic report creation endpoint`
- `feat: add incident priority scoring`
- `test: cover duplicate matching edge cases`
- `docs: update assignment API contract`

## 8. Testing Strategy

### Unit Tests
Test individual functions such as priority calculation, distance calculation, text similarity, department routing, and C graph algorithms.

### API Tests
Test valid and invalid requests, authentication, role permissions, missing resources, and database behavior.

### Integration Tests
Verify that reports can be created, linked to incidents, prioritized, assigned, and tracked through status changes.

### Frontend Tests
Verify form validation, API error handling, navigation, filters, and role-specific screens.

### Algorithm Evaluation
Use controlled test cases to evaluate:
- Duplicate matches and false matches.
- Priority ranking on known examples.
- Shortest-path correctness.
- Assignment feasibility and workload constraints.

## 9. Optional Machine-Learning Plan

ML is not a prerequisite for completing the core system.

If time and data permit:

1. Choose one task with a measurable purpose.
2. Obtain or create an appropriate, documented dataset.
3. Establish a simple rule-based baseline.
4. Train and evaluate a suitable model.
5. Compare the model against the baseline.
6. Document limitations and failure cases.
7. Integrate it as a recommendation only if it provides measurable value.

Do not claim accurate real-world prediction using arbitrary or unrepresentative sample data.

## 10. Definition of Done

A feature is complete when:
- Its expected behavior is documented.
- Valid and invalid cases have been considered.
- Authorization and input validation are implemented where required.
- Relevant tests pass.
- Frontend and backend contracts agree.
- Error handling is in place.
- The change has been reviewed and merged.
- The documentation is updated when necessary.

## 11. Final Deliverables

The final project should include:
- A working React frontend.
- A FastAPI backend.
- A PostgreSQL schema and setup instructions.
- Civic report and incident workflows.
- Explainable prioritization and department recommendations.
- Repair-team assignment support.
- Tested C algorithms integrated where appropriate.
- Maps and analytics.
- Automated tests.
- Sample data instructions.
- A clear README, architecture documentation, and demonstration.

## 12. Future Scope

Future extensions may include authorized municipal data integrations, multilingual reporting, more advanced geospatial analysis, notification services, image classification, improved resource scheduling, and privacy-preserving analytics.
