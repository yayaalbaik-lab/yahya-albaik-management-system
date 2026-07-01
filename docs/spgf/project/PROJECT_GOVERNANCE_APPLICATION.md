# Project Governance Application

This document explains how the general SPGF Constitution applies to this project.

## Applied Profile

Initial profile: `Standard`

This is a lightweight `Standard` application: enough governance to protect operational inventory data and permissions, without applying unnecessary `Enterprise` process.

## Current Project Context

- One restaurant branch.
- No transfer between warehouses or branches.
- Existing local/basic POS will not be replaced in the first phase.
- The existing POS uses SQL Server installed on the cashier computer.
- Initial system focus is daily inventory counting and next-day matching.
- Future phases may include waste, profitability, and delivery-app reconciliation.
- Users include owner, manager, cashier, and relevant employees, each with different permissions.

## Required Governance Documents

For the initial project phase:

- Project charter.
- Business glossary.
- Business rules.
- Open questions, assumptions, and constraints.
- Out of scope.
- SRS for Must Have features.
- Engineering standards application.
- Technical debt register when shortcuts are accepted.

Documents may remain compact while the project is in discovery. The priority is clarity of business rules and sensitive workflows, not creating a large document set.

## Initial Scope

Must Have for the first phase:

- Define core inventory items.
- Record daily counts.
- Track who entered or edited a count.
- Compare count data across days.
- Show mismatches that require review.
- Apply basic permissions by role.

Should Have for later phases:

- Waste tracking.
- Profitability and cost reports.
- Delivery-app reconciliation.
- Direct integration with POS sales data.

Out of scope for the first phase:

- Replacing the existing POS.
- Multi-branch management.
- Warehouse transfers.
- Full accounting.
- Automated supplier purchasing.

## Quality Gates

Quality gates are applied as formal approval points, not as blockers for all exploration.

- Discovery and business rules may proceed in parallel with early UI or technical spikes.
- Production development for sensitive workflows must wait until the relevant business rules are clear.
- Must Have requirements should be traceable to a business need.
- SQL Server integration must not be treated as production-critical until the connection method, permissions, and data ownership boundaries are understood.

## Non-Negotiables

- Do not break an existing working flow.
- Register accepted shortcuts as technical debt.
- Use ADRs for decisions that are hard to reverse or affect core architecture.
- Protect sensitive operational data from unsafe hard deletion.
- Do not write to the POS SQL Server database unless an explicit approved decision allows it.
- Inventory count edits must be attributable to a user.
