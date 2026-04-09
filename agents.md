# AGENTS.md

## Purpose

This repository is for a process planning platform with automatic BPMN draft generation and BPMN editing support.

Agents working in this repository must preserve product clarity, UX coherence, and code maintainability.

## Source of Truth

Before making changes, review:

1. `README.md`
2. `docs/product-requirements.md`
3. `docs/architecture.md`
4. `docs/mvp-scope.md`
5. `docs/design-system.md`
6. `docs/frontend-style-guide.md`

If code and documentation conflict, do not guess silently.  
Prefer documented product intent unless the docs are clearly outdated.

## Product Intent

This is not a generic diagram editor.

This is a process planning platform where users provide process information and the system generates an editable BPMN draft.

The BPMN diagram is a core feature, but it must remain connected to planning data and process structure.

## Working Rules

- make small, focused, reversible changes
- avoid unnecessary rewrites
- preserve working functionality
- keep UI logic, process logic, and BPMN logic separated
- do not over-engineer early abstractions
- document major product or architecture changes
- do not silently invent requirements

## Frontend Rules

- avoid overloaded single-page layouts
- prefer modular screen composition
- use split panels, tabs, or drawers when appropriate
- keep the interface professional and premium
- maintain alignment with the brand system
- prioritize usability over visual gimmicks

## BPMN Rules

- BPMN generation must be modular
- BPMN rendering should not contain unrelated business logic
- generated nodes should remain linked to planning records where applicable
- generated BPMN must be editable
- treat generated BPMN as a draft that can be refined by the user

## AI / Interpretation Rules

- do not claim perfect process understanding
- use structured inputs whenever possible
- messy meeting notes alone should not be treated as sufficient truth
- when logic is unclear, surface ambiguity instead of hiding it
- preserve traceability between user input and generated process structure

## Data Modeling Rules

Keep these concepts explicit:

- Process
- ProcessInput
- Role
- ProcessStep
- DecisionPoint
- Diagram
- BPMNNodeMapping
- Note
- Dependency

Avoid hiding key relationships inside vague generic objects.

## Refactoring Rules

Refactor only when it improves one or more of the following:

- readability
- modularity
- maintainability
- testability
- BPMN generation clarity
- UX coherence

Do not refactor only for style preference.

## Forbidden Behavior

- do not fabricate requirements
- do not silently remove product capabilities
- do not add random dependencies
- do not rebuild large areas without reason
- do not couple everything into one screen
- do not treat BPMN generation as separate from planning logic
- do not overstate AI reliability

## Expected Change Summary

When proposing or implementing changes, clearly state:

- what changed
- why it changed
- affected files
- risks or follow-up needs
