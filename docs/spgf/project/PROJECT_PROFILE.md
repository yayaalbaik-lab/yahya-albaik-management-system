# Project Profile

## Project Name

Yahya Albaik Management System

## Initial SPGF Profile

`Standard`

## Why Standard

This project is a single-branch operational management system focused first on daily inventory counting and next-day matching. It is `Standard` because it handles operationally sensitive data such as:

- Inventory quantities.
- Daily inventory count records.
- Item matching differences between days.
- User permissions.
- Operational and management reports.
- Future waste, profitability, and delivery-app reconciliation data.

The project does not currently require `Enterprise` because it is limited to one branch, does not include warehouse-to-warehouse transfers, and does not yet involve critical external integrations.

## Initial MVP Focus

The first release focuses on:

- Daily count of core items.
- Saving count snapshots by date, user, and item.
- Comparing today's opening/expected quantities against the previous count.
- Highlighting mismatches for review.
- Basic role-based access for owner, manager, cashier, and relevant employees.

The first release does not attempt to replace the existing local POS.

## Profile Boundaries

The project should not start as `Enterprise` unless one or more of the following become true:

- Multiple independent teams work on the system.
- External integrations become operationally critical.
- Strict legal or regulatory compliance requirements appear.
- The system becomes multi-branch or multi-tenant with high operational risk.
- Warehouse transfers or multi-location stock movement are introduced.

## Review Trigger

Reassess the profile at the end of discovery and before development begins.

Also reassess the profile before adding:

- Waste tracking.
- Profitability calculations.
- Delivery-app reconciliation.
- Automated integration with the local POS SQL Server database.
