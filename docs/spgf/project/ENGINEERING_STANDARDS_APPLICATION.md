# Engineering Standards Application

This document explains how the general Engineering Standards apply to this project.

## Applied Level

`Standard`

The implementation should stay lean inside the `Standard` profile: strong protection for inventory data, permissions, and auditability, without adding unnecessary enterprise infrastructure.

## Initial Engineering Expectations

- Use a clear project structure that separates UI, business logic, and data access.
- Use migrations for database changes.
- Protect sensitive changes with audit trail where needed.
- Use soft delete or archival for records that enter operational history.
- Add tests for critical business rules.
- Use clear commit messages and avoid mixing large refactors with feature work.
- Treat the existing POS SQL Server database as an external system.
- Avoid direct writes to the POS database unless formally approved.
- Keep daily inventory count records immutable where possible; corrections should be tracked.

## Areas Requiring Project Decisions

The following decisions must be made before production development:

- Tech stack.
- Database engine.
- Authentication and authorization model.
- Backup and restore approach.
- Deployment target.
- Test strategy for critical workflows.
- POS SQL Server connection method and read/write boundaries.
- Mobile app offline behavior, if any.

## Project-Specific Standards

### Candidate Tech Stack

- Mobile app candidate: Flutter.
- Existing POS data source: SQL Server on cashier computer.
- Backend/API: undecided.
- Project database: undecided.

Flutter is a strong candidate because the first intended user experience is mobile. The final decision should consider local network access, SQL Server integration, offline needs, and deployment simplicity.

### Data Integrity Rules

- Inventory counts are operational records and must preserve history.
- Count edits require user attribution and timestamp.
- Destructive deletion is not allowed for count records after they are used for matching or reporting.
- Matching logic must be covered by tests before production use.

### Permission Rules

At minimum, the project should distinguish:

- Owner: full access and reports.
- Manager: operational management and review.
- Cashier: limited access depending on POS and inventory workflow.
- Employee: limited count entry or task-specific access.

Final permissions must be documented before implementation.
