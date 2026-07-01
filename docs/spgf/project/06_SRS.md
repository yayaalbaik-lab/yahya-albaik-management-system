# Software Requirements Specification

## System Overview

The system is intended to be a mobile-first application for daily inventory counting and operational review. Flutter is the preferred mobile app candidate, pending final technical confirmation.

## Candidate Technology Direction

- Mobile app candidate: Flutter.
- Existing POS data source: SQL Server on cashier computer.
- Backend/API: undecided.
- Project database: undecided.

## Functional Requirements

### FR-001 Manage Core Inventory Items

The system shall allow authorized users to define or use a list of core inventory items for daily counting.

Linked business requirement: `BR-001`

Initial phase-one item list:

- Broasted.
- Tikka.
- Zinger.
- Escalope.
- Cola.
- Shanina.
- Water bottles.

### FR-002 Record Daily Inventory Count

The system shall allow authorized users to enter daily counts for core inventory items.

Linked business requirement: `BR-001`

### FR-003 Store Count Metadata

The system shall store count date, item, entered quantity, user, and timestamp for each count record.

Linked business requirement: `BR-002`

### FR-004 Compare Count Records Across Days

The system shall compare count records across days and identify mismatches requiring review.

Linked business requirement: `BR-003`

### FR-005 User Authentication

The system shall authenticate users before allowing access to protected features.

Linked business requirement: `BR-004`

### FR-006 Role-Based Authorization

The system shall restrict actions based on the user role.

Linked business requirement: `BR-004`

### FR-007 Preserve Count History

The system shall preserve inventory count history and avoid destructive deletion after records are used for matching or reporting.

Linked business requirements: `BR-002`, `BR-003`

### FR-008 POS SQL Server Read Boundary

The system shall not write to the POS SQL Server database unless a formally approved decision allows it.

Linked business requirement: `BR-006`

## Non-Functional Requirements

### NFR-001 Data Integrity

Inventory count records must preserve history and user attribution.

### NFR-002 Auditability

Corrections or edits to sensitive inventory records must be attributable to a user and timestamp.

### NFR-003 POS Safety

The system must not disrupt the existing local POS workflow.

### NFR-004 Mobile-First Experience

The user experience should be suitable for mobile inventory workflows.

## Open Technical Questions

- Should Flutter be confirmed as the mobile framework?
- Does the app need offline support inside the restaurant?
- Will phase one read any data from SQL Server, or only prepare for future integration?
- What backend/API approach best fits local SQL Server access and mobile usage?
