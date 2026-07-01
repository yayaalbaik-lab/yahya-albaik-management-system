# Business Rules

This document records approved and candidate business rules.

## Approved Rules

### BRULE-001 Single Branch

The first phase manages one restaurant branch only.

### BRULE-002 No Warehouse Transfers In Phase One

The first phase does not include warehouse-to-warehouse or branch-to-branch transfers.

### BRULE-003 Existing POS Is Not Replaced

The first phase must not replace the existing local POS.

### BRULE-004 POS Database Safety

The POS SQL Server database is treated as an external system. The application must not write to it unless a formal approved decision allows it.

### BRULE-005 Count Records Need User Attribution

Inventory count entries and corrections must be attributable to a user.

### BRULE-006 Phase One Focus

The first phase focuses on daily counts of core inventory items and next-day matching.

### BRULE-007 Initial Phase-One Core Items

For the current phase-one scope, daily inventory counting is limited to:

- Broasted.
- Tikka.
- Zinger.
- Escalope.
- Cola.
- Shanina.
- Water bottles.

## Candidate Rules Pending Clarification

### CBR-001 Matching Rule

The exact meaning of next-day matching is not yet approved.

Possible interpretations:

- Compare today's count directly with previous count.
- Compare expected quantity after sales/usage with actual count.
- Allow manager-approved differences.

### CBR-002 Count Edit Rule

Who may edit or correct submitted counts is not yet approved.

### CBR-003 Offline Rule

Whether the mobile app must work offline inside the restaurant is not yet approved.
