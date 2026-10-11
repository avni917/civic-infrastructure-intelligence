# Development Roadmap

## 1. Purpose

This roadmap outlines the planned development of Civic Infrastructure Intelligence from initial research and design to a working, tested prototype.

The project will be developed incrementally by two students. The exact timeline may change as requirements are refined and technical challenges are discovered.

## 2. Development Phases

### Phase 1: Research and Project Definition

**Goals**
- Study existing civic reporting platforms.
- Understand the problems faced in civic incident management.
- Identify the proposed contribution of the project.
- Finalize the target users and primary use cases.
- Define the initial scope and success criteria.

**Expected outcome:** A documented problem, research findings, and an agreed project scope.

### Phase 2: System Design and Learning Preparation

**Goals**
- Define the system architecture.
- Identify the main application modules.
- Draft the database entities and their relationships.
- Agree on the initial API contract.
- Identify technology-specific learning requirements.
- Establish GitHub collaboration practices.

**Expected outcome:** A shared design that both developers understand before implementation begins.

### Phase 3: Core Full-Stack Application

**Goals**
- Set up the React frontend.
- Set up the FastAPI backend.
- Connect the application to PostgreSQL.
- Implement authentication and role-based access.
- Build citizen report submission and retrieval.
- Add basic officer views and incident status tracking.

**Expected outcome:** A working application that can save, retrieve, and manage civic reports.

### Phase 4: Incident Intelligence

**Goals**
- Separate individual reports from underlying incidents.
- Implement duplicate candidate detection.
- Add incident priority scoring.
- Recommend the responsible department.
- Record relevant status and assignment history.

**Expected outcome:** A system that organizes reports and supports explainable incident prioritization.

### Phase 5: Resource Coordination and Algorithms

**Goals**
- Model departments, repair teams, skills, availability, and workload.
- Develop a baseline team-recommendation method.
- Implement selected data structures and graph algorithms in C.
- Test the algorithms independently.
- Integrate appropriate algorithms with the Python backend.

**Expected outcome:** A working demonstration of algorithmic decision support and resource recommendations.

### Phase 6: Maps and Analytics

**Goals**
- Display incidents on an interactive map.
- Add category, status, and priority filters.
- Visualize incident counts and trends.
- Analyze recurring problems by area.
- Add useful administrative dashboard metrics.

**Expected outcome:** A platform that communicates both individual incident information and broader patterns.

### Phase 7: Evaluation and Optional Advanced Features

**Goals**
- Test the main user workflows.
- Evaluate duplicate matching and priority ranking.
- Measure algorithm correctness and performance.
- Explore one optional machine-learning feature if the core application is stable.
- Document limitations and possible improvements.

**Expected outcome:** A tested prototype with evidence supporting its design decisions.

### Phase 8: Finalization and Demonstration

**Goals**
- Fix major bugs and usability issues.
- Prepare reproducible setup instructions.
- Complete the documentation.
- Deploy the application if suitable hosting is available.
- Prepare a demonstration using sample data.
- Publish the final project status and known limitations.

**Expected outcome:** A portfolio-ready project that another developer can understand, run, and evaluate.

## 3. Tentative Timeline

| Period | Primary focus |
|---|---|
| Weeks 1–2 | Research, requirements, scope, and system design |
| Weeks 3–4 | Frontend/backend setup, database, and authentication |
| Weeks 5–6 | Reporting, incident management, and duplicate detection |
| Weeks 7–8 | Priority scoring, department routing, and team recommendations |
| Weeks 9–10 | C algorithms, integration, maps, and analytics |
| Week 11 | Testing, evaluation, and optional ML |
| Week 12 | Refinement, documentation, and demonstration |

The timeline is indicative. Core reporting and incident workflows take priority if the project falls behind schedule.

## 4. Initial Division of Responsibilities

Responsibilities will be divided according to interest and current strengths, with shared reviews and integration.

### Developer A: Backend and Algorithms

Potential responsibilities:
- FastAPI and backend services.
- Database integration.
- Incident processing and prioritization.
- Duplicate detection and department routing.
- C algorithm implementation and integration.
- Backend tests.

### Developer B: Frontend and Interface

Potential responsibilities:
- React application structure.
- Citizen reporting interface.
- Incident and status views.
- Officer and administrator dashboards.
- Maps, charts, and filters.
- Frontend API integration and tests.

### Shared Responsibilities

Both developers will contribute to:
- Requirements and architecture.
- API and database design reviews.
- Testing and debugging.
- Pull-request reviews.
- Documentation and demonstrations.
- Learning unfamiliar technologies as required.

This division is provisional and may change as implementation progresses.

## 5. Development and Collaboration Practices

- Track tasks using GitHub Issues and Projects.
- Create feature branches for individual changes.
- Use clear, descriptive commit messages.
- Review code before merging substantial changes.
- Keep configuration secrets out of Git.
- Maintain sample data and setup instructions.
- Update documentation when project decisions change.
- Test each module before integrating it into the complete application.

## 6. Prioritization Rules

The team will follow these priorities:

1. Establish a working end-to-end application.
2. Ensure the database and incident relationships are correct.
3. Implement transparent priority scoring and department routing.
4. Add resource recommendations and selected C algorithms.
5. Add maps, analytics, and resolution verification.
6. Attempt optional machine learning only when sufficient time and appropriate data are available.

## 7. Completion Criteria

The project will be ready for its final demonstration when the core workflow can be completed using the documented setup and sample data, relevant tests pass, major limitations are recorded, and both developers can explain the architecture and their contributions.

## 8. Future Development

After the initial prototype, the team may explore improved allocation strategies, more advanced geographical analysis, model-based predictions, additional user feedback mechanisms, and integrations with authorized external datasets.
