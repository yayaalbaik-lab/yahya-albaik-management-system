# Project Charter

## Project Name

Yahya Albaik Management System

## Project Purpose

Build a mobile-first operational management system for Yahya Albaik restaurant, starting with daily inventory counting and next-day matching for core items.

## Business Objective

Improve control over daily inventory by recording counts, preserving history, and highlighting mismatches that require review.

## Initial Scope

The first phase includes:

- Daily counting of core inventory items.
- Saving count snapshots by date, item, and user.
- Reviewing mismatches between inventory count records.
- Basic role-based access for owner, manager, cashier, and relevant employees.

## Out Of Scope For Phase One

- Replacing the existing local POS.
- Multi-branch management.
- Warehouse-to-warehouse transfers.
- Full accounting.
- Waste tracking.
- Profitability calculations.
- Delivery-app reconciliation.
- Automated supplier purchasing.

## Stakeholders

- Restaurant owner.
- Manager.
- Cashier.
- Relevant operational employees.

## Project Profile

Initial SPGF profile: `Standard`

## Profile Rationale

The project handles operationally sensitive inventory data and user permissions. It is limited to one branch and does not currently require `Enterprise` governance.

## Key Constraints

- The project is for one branch only.
- There are no warehouse transfers in phase one.
- The existing POS is local/basic and remains in place.
- The POS database is SQL Server installed on the cashier computer.

