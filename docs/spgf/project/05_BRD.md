# Business Requirements Document

## Business Context

The restaurant currently has a local/basic POS. The first system phase will not replace the POS. Instead, the application will focus on daily inventory counting and matching count records across days.

## Business Need

The business needs a practical way to:

- Count core inventory items daily.
- Preserve who entered each count and when.
- Compare count records across days.
- Detect mismatches that need review.
- Control access by user role.

## Users And Roles

Initial roles:

- Owner: full access and management visibility.
- Manager: operational review and management actions.
- Cashier: limited access related to cashier/POS-adjacent workflows.
- Relevant employees: limited task-specific access.

Final permissions are not yet approved and must be defined before implementation.

## Phase One Business Requirements

### BR-001 Daily Core Item Count

The business must be able to record daily counts for core inventory items.

Current phase-one core items:

- Broasted.
- Tikka.
- Zinger.
- Escalope.
- Cola.
- Shanina.
- Water bottles.

### BR-002 Count History

The business must preserve historical count records by date, item, and user.

### BR-003 Next-Day Matching

The business must be able to compare inventory count records across days to detect mismatches.

### BR-004 Role-Based Access

The business must restrict system capabilities based on user role.

### BR-005 POS Non-Replacement

The first phase must not replace the existing local POS.

### BR-006 SQL Server Boundary

The existing POS SQL Server database must be treated as an external system until integration rules are formally approved.

## Future Business Capabilities

Potential future phases:

- Waste tracking.
- Profitability and cost reports.
- Delivery-app reconciliation.
- Direct read integration with POS sales/consumption data.

## Business Constraints

- Single branch only.
- No warehouse transfer workflow in phase one.
- POS is installed locally on the cashier computer.
- POS disruption is not acceptable.
