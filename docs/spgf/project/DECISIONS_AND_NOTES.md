# Decisions And Notes

This file temporarily combines:

- Open questions.
- Assumptions.
- Constraints.
- Early technical notes.

It may be split into separate registers later if the project grows.

## Open Questions

- What does "matching the next day" mean exactly: same quantity, expected quantity after sales, or manager-approved difference?
- Will the first phase use only manual counts, or will it read sales/consumption data from SQL Server?
- Is SQL Server integration read-only in all cases?
- Will the mobile app need to work offline inside the restaurant?
- Who is allowed to edit or correct a submitted count?
- What roles are required in the first release: owner, manager, cashier, employee, or more?
- What reports are required from day one?
- Should Flutter be confirmed as the mobile app framework?

## Assumptions

- Initial project profile is `Standard`.
- The project is for one branch only.
- There is no warehouse transfer workflow in the first phase.
- The existing POS remains in place and will not be replaced in the first phase.
- The existing POS stores data in SQL Server on the cashier computer.
- The first phase focuses on daily counting of core items and next-day matching.
- Current phase-one core items are Broasted, Tikka, Zinger, Escalope, Cola, Shanina, and Water bottles.
- Flutter is the preferred mobile app candidate unless discovery reveals a better fit.

## Constraints

- Existing POS is local/basic and must not be disrupted.
- SQL Server is installed on the cashier computer.
- Any direct POS database integration must be designed carefully and preferably read-only at first.

## Notes

- Keep general SPGF documents unchanged.
- Future phases may include waste, profitability, and delivery-app reconciliation.
- From this point forward, new information should be classified and written directly into the correct document: Charter, BRD, SRS, or this notes file.
- No project-relevant information should remain only in chat. Each new statement must be classified and recorded in the correct document, or captured as an open question/assumption if not yet clear.

## Early Decisions

- Project-specific SPGF profile starts as `Standard`.
- General SPGF documents remain reference-only under `docs/spgf/general`.
- Codex working behavior is governed by `CODEX_WORKING_AGREEMENT.md`, under the authority of SPGF and the project-specific application documents.

## Information Classification Rule

- Charter: project purpose, scope, stakeholders, constraints, profile, and success direction.
- BRD: business needs, business processes, users, role expectations, business rules, and future capabilities.
- SRS: functional requirements, non-functional requirements, system behavior, interfaces, and technical constraints.
- Glossary: terms and definitions used by the business and system.
- Business Rules: approved or candidate business rules.
- RTM: links between business requirements and software requirements.
- Out Of Scope: deferred or excluded capabilities.
- Decisions And Notes: open questions, assumptions, constraints not yet approved, and early decisions.

## Mandatory Intake Procedure

For each new project-relevant user message:

1. Classify each distinct piece of information.
2. Update the correct document immediately.
3. Update RTM if BRD/SRS requirements are added or changed.
4. Record unresolved ambiguity as an open question.
5. Mention the classification and updated document(s) in the response.
