# Architecture

## 1. Overview

The application should be built as a modular process planning system with clear separation between:

- frontend UI
- process intake logic
- process interpretation logic
- BPMN generation logic
- BPMN rendering / editing
- persistence

## 2. Core Domains

### A. Intake Domain
Responsible for collecting process-related input from the user.

### B. Interpretation Domain
Responsible for translating input into structured process logic.

### C. BPMN Domain
Responsible for converting process structure into BPMN-compatible diagram data.

### D. Planning Domain
Responsible for operational metadata such as owner, status, notes, and dependencies.

## 3. Key Architectural Principle

Do not collapse all product behavior into one large page or one large state tree.

The architecture should support distinct modules with clean interfaces.

## 4. Suggested Frontend Modules

- app shell
- dashboard
- process list
- process detail
- process intake form
- BPMN draft review
- BPMN editor
- step properties panel
- shared component library

## 5. Suggested Service Modules

- process service
- BPMN generation service
- BPMN serialization service
- process mapping service
- validation / ambiguity service later

## 6. Suggested Entity Model

Core entities should likely include:

- Process
- ProcessInput
- Role
- ProcessStep
- DecisionPoint
- Diagram
- BPMNNodeMapping
- Note

## 7. State Separation

Separate at least:

- process metadata state
- intake state
- BPMN diagram state
- planning metadata state
- UI state

Avoid placing diagram internals and business planning data in one uncontrolled structure.

## 8. Persistence Strategy

The system should be able to persist:

- process metadata
- intake records
- generated BPMN data
- step mappings
- planning metadata

The persistence model must preserve traceability between generated BPMN and process records.

## 9. Frontend Layout Strategy

The interface should remain modular.

Preferred patterns:

- list + detail layouts
- split panels
- tabs
- contextual property panel
- clear separation between process input and diagram review

Avoid giant all-in-one screens.

## 10. Risks

- BPMN becomes visually disconnected from process planning
- interpretation logic becomes hidden and untraceable
- UI becomes overloaded
- node-to-step mapping becomes fragile
- AI logic becomes too vague too early

## 11. Architecture Rule

Any structural change should improve at least one of:

- clarity
- maintainability
- modularity
- BPMN generation traceability
- UX quality
