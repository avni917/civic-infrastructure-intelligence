# Proposed Solution

## 1. Overview

Civic Infrastructure Intelligence proposes a web-based civic decision-support platform that converts citizen submissions into structured infrastructure incidents and supports their prioritization, assignment, tracking, and analysis.

The platform will combine a citizen-facing reporting interface with officer and administrator tools. Its central contribution is the planned intelligence layer that supports decisions beyond simply collecting complaints.

## 2. Core Concept

The system will distinguish between two entities:

- **Report:** An individual submission made by a citizen.
- **Incident:** The underlying real-world infrastructure problem that may be represented by multiple reports.

For example, five citizens may report the same pothole. The system should preserve all five submissions while allowing officers to manage the underlying pothole as one incident.

Duplicate matching will initially produce candidate matches based on location, category, and description similarity. Uncertain matches will be available for review.

## 3. Proposed Workflow

### Step 1: Citizen Reporting

A citizen submits a report containing:
- Issue category.
- Description.
- Geographical location.
- Optional photograph.
- Submission timestamp.

The system validates the information and stores the report.

### Step 2: Incident Matching

The platform compares the new report with relevant existing incidents.

Potential matching factors include:
- Distance between geographical coordinates.
- Similarity of issue categories.
- Text similarity between descriptions.
- Time between submissions.

A matching score or set of rules will identify possible duplicates. The system will avoid assuming that two reports describe the same issue merely because they are nearby.

### Step 3: Incident Creation or Association

The system either:
- Links the report to an existing incident when the match is sufficiently reliable under the defined rules, or
- Creates a new incident or sends the candidate match for review.

The original report remains available in the system.

### Step 4: Priority Assessment

The platform calculates a priority score using configurable factors such as:
- Reported severity.
- Potential safety risk.
- Number of supporting reports.
- Recurrence of the problem.
- Importance of the affected location.
- Time spent unresolved.

The initial scoring engine will be rule-based and explainable. Each incident's score will show which factors contributed to its ranking.

### Step 5: Department Recommendation

The system recommends a department using configurable routing rules.

Examples:
- Potholes and damaged roads → road maintenance or public works.
- Blocked drains → drainage or sanitation.
- Broken streetlights → electrical maintenance.
- Water leakage → water supply or the relevant utility.

The actual department names and mappings will depend on the configuration used in the demonstration.

### Step 6: Repair-Team Recommendation

The platform identifies candidate teams and evaluates factors such as:
- Required technical skills.
- Team availability.
- Current workload.
- Geographical distance.
- Incident priority.

A simple baseline allocation method will be implemented first. More advanced allocation and route optimization may be introduced later.

Recommendations will be subject to officer review.

### Step 7: Progress Tracking

Authorized officers update the incident status as work progresses.

The system records status changes, assignment details, timestamps, and relevant remarks. Citizens can view the information made available to them.

### Step 8: Resolution Verification

When repair work is reported as complete, the officer may submit notes and supporting evidence.

Citizen feedback or an authorized review may flag an issue that appears unresolved. The incident can then enter a review or reopening workflow according to the configured rules.

### Step 9: Analytics and Insights

The platform aggregates historical incident data to display:
- Incident counts by category and area.
- High-priority and overdue incidents.
- Resolution-time summaries.
- Reopened and recurring incidents.
- Geographical concentrations of reported problems.
- Department and team workload indicators.

These insights are intended to help users understand patterns and evaluate operational performance.

## 4. Main System Modules

### Citizen Module
Provides registration, reporting, report history, incident tracking, and feedback.

### Incident Intelligence Module
Supports duplicate candidate detection, report-to-incident relationships, and incident organization.

### Priority and Routing Module
Calculates priority scores and recommends the appropriate department.

### Resource Allocation Module
Recommends teams according to skills, availability, workload, and distance.

### Officer Module
Provides incident review, assignments, status updates, and resolution evidence.

### Analytics Module
Summarizes incidents and visualizes geographical and historical patterns.

### Algorithm Module
Provides selected C implementations for priority queues, graph operations, and shortest-path calculations.

### Optional ML Module
Explores a narrowly defined prediction or classification task when suitable data and sufficient development time are available.

## 5. Role of Algorithms and Machine Learning

The project will distinguish deterministic algorithms from machine-learning predictions.

### Rule-Based Algorithms
These will be used for:
- Priority scoring.
- Department routing.
- Candidate-team filtering.
- Basic resource-allocation heuristics.

### C Algorithms
Selected data structures and graph algorithms will be implemented in C and integrated into the Python backend where useful.

### Optional Machine Learning
A small model, such as text-based issue category classification, may be explored if it improves on a simple baseline. The model's performance and limitations will be measured and documented.

Machine learning is not required for the initial system to operate.

## 6. Expected Benefits

The prototype aims to demonstrate:
- Better organization of repeated reports.
- More consistent incident prioritization.
- More systematic department and team recommendations.
- Improved visibility into incident progress.
- Better understanding of recurring problem areas.
- Greater transparency through recorded decisions and status history.

These are intended benefits that must be evaluated; they are not guaranteed real-world outcomes.

## 7. Limitations

- Report quality depends on the information supplied by citizens.
- Location and text similarity may produce false matches.
- Rule-based priority scores depend on the chosen weights and assumptions.
- Team recommendations depend on the accuracy of simulated availability and workload data.
- Hotspot maps may reflect reporting activity rather than the true distribution of infrastructure problems.
- The prototype will not replace official municipal decision-making.

## 8. Future Improvements

Potential future extensions include multilingual reporting, authorized municipal data integration, more advanced geospatial analysis, notification services, image-based classification, and improved team scheduling.

## 9. Expected Deliverable

The expected deliverable is a working full-stack prototype that demonstrates the complete journey from citizen report submission to incident organization, prioritization, assignment, resolution tracking, and analytics.
