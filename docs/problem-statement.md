# Problem Statement

## 1. Project Title

**Civic Infrastructure Intelligence: A Civic Decision-Support Platform**

## 2. Background

Cities face recurring infrastructure problems such as potholes, damaged roads, broken streetlights, blocked drainage systems, water leakage, and garbage accumulation.

Citizens may report these problems through online portals or other communication channels. However, several reports may describe the same physical issue. Authorities must determine which issues require urgent attention, identify the responsible department, allocate limited repair resources, and verify whether reported problems have actually been resolved.

A platform that collects reports alone does not necessarily provide the analytical support required to make these decisions efficiently.

## 3. Problem Definition

The project addresses five key challenges:

1. **Duplicate reports:** Multiple citizens may report the same infrastructure issue, making it difficult to estimate the actual number of incidents.
2. **Unclear prioritization:** Authorities need a consistent way to rank incidents according to severity, safety risks, recurrence, and potential public impact.
3. **Department and team assignment:** Incidents must be directed to suitable departments and repair teams.
4. **Limited resources:** Repair teams have limited availability, skills, time, and geographical coverage.
5. **Resolution accountability:** An incident marked as resolved may remain unresolved or recur, making verification and historical tracking important.

These challenges motivate the development of an intelligent decision-support layer for civic infrastructure management.

## 4. Proposed Solution

Civic Infrastructure Intelligence is a web-based prototype that converts individual citizen reports into actionable infrastructure incidents.

The platform will collect issue descriptions, categories, photographs, and geographical locations. It will identify potentially duplicate reports, combine related reports into incidents, calculate transparent priority scores, recommend responsible departments, and support repair-team allocation.

The system will also maintain incident status history, support resolution evidence and citizen feedback, and provide dashboards that help identify recurring issues and infrastructure hotspots.

The platform is intended to assist human decision-makers rather than replace municipal authorities.

## 5. Project Objectives

- Provide a structured interface for submitting and tracking civic issues.
- Identify potentially duplicate reports using location, category, and text similarity.
- Rank incidents using a configurable, explainable priority-scoring algorithm.
- Recommend the appropriate department for each incident.
- Support resource allocation based on team skills, availability, distance, and incident priority.
- Use data structures and algorithms implemented in C where appropriate.
- Visualize incidents, trends, and recurring problem areas.
- Maintain transparent status history and resolution verification.
- Explore machine-learning techniques for selected tasks when sufficient data is available.

## 6. Scope

### Included in the prototype

- Citizen, officer, and administrator roles.
- Issue reporting with location and optional photographs.
- Incident aggregation and duplicate detection.
- Rule-based priority scoring.
- Department recommendations.
- Repair-team assignment and status tracking.
- Map-based incident visualization.
- Administrative analytics and hotspot identification.
- Selected C algorithms integrated with the Python backend.
- Optional machine-learning experiments using suitable datasets.

### Outside the initial scope

- Direct integration with live municipal systems.
- Automatic dispatch of real repair teams.
- Guaranteed detection of every duplicate report.
- Fully automated decisions without human oversight.
- Production deployment for emergency response.
- Advanced image recognition unless time and data permit.

## 7. Intended Users

- **Citizens:** Submit reports, track progress, and provide feedback.
- **Municipal officers:** Review incidents, prioritize work, assign teams, and update statuses.
- **Administrators:** Manage departments and teams and monitor overall performance.

## 8. Expected Outcome

The expected outcome is a working full-stack prototype demonstrating how software engineering, algorithms, geographical data, and optional machine learning can improve civic incident management.

The prototype will be evaluated using functional correctness, duplicate-detection quality, prioritization explainability, assignment efficiency, usability, and test coverage.

## 9. Important Distinction

A citizen report is an individual submission, whereas an incident represents an underlying real-world problem. Multiple reports may be associated with one incident.

This distinction is central to the system's data model and deduplication workflow.

## 10. Disclaimer

This is an independent educational and portfolio project. It is not affiliated with any municipal authority and does not replace official civic reporting or emergency services.
