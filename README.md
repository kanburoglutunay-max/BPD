# Process Planning Platform

A process planning platform that transforms user-entered tasks, process details, meeting objectives, workflow notes, and structured operational input into editable BPMN diagrams automatically.

## Overview

This project is being built as a professional process planning platform with integrated BPMN generation and BPMN editing capabilities.

The platform is not intended to be only a BPMN drawing tool.  
Its main value is converting process knowledge into structured, editable workflow diagrams.

Users should be able to enter:

- process goals
- roles and participants
- tasks and dependencies
- decision points
- meeting notes
- expected outputs

The system should interpret these inputs and generate an editable BPMN draft.

## Core Value Proposition

Most workflow tools fall into one of two weak categories:

- diagram-first tools that are weak in operational planning
- task/project tools that are weak in process modeling

This product aims to bridge that gap by combining:

- process intake
- structured planning
- BPMN draft generation
- BPMN review and editing
- process visibility

## Product Vision

Build a process intelligence platform that helps organizations turn semi-structured process input into reliable visual workflows.

The long-term goal is to support:

- process capture
- process modeling
- process review
- process standardization
- future automation readiness

## Main Capabilities

### 1. Process Intake
Users enter process-related information through structured and semi-structured forms.

### 2. Process Interpretation
The system identifies:

- roles
- tasks
- sequence
- conditions
- outputs
- lane candidates

### 3. BPMN Draft Generation
The system generates a BPMN draft with:

- lanes / participants
- tasks
- gateways
- sequence flows
- start and end events

### 4. BPMN Review and Editing
Users refine the generated diagram and correct logic if needed.

### 5. Process Planning Layer
Each process and step can retain metadata such as:

- owner
- status
- priority
- notes
- due date
- dependencies

## Initial MVP

The first version should support:

- process creation
- process list and detail pages
- structured process intake
- BPMN draft generation from structured inputs
- BPMN editor/viewer integration
- step-to-node mapping
- saving and reloading process data
- editing process metadata and planning records

## Not in Initial MVP

The first version should not attempt to fully solve:

- real-time collaboration
- advanced permissions
- full workflow automation execution
- AI-only generation from completely messy notes
- advanced analytics
- enterprise integration complexity
- deep version comparison

## Brand Direction

The frontend should reflect the existing corporate logo and brand language:

- dark premium interface
- controlled gold accent usage
- clean, structured layout
- professional and institutional tone
- no playful or over-stylized UI

See `docs/design-system.md` and `docs/frontend-style-guide.md`.

## Repository Documents

- `AGENTS.md` → working rules for AI coding agents
- `docs/product-requirements.md` → product intent and requirements
- `docs/architecture.md` → technical architecture direction
- `docs/roadmap.md` → phased execution plan
- `docs/design-system.md` → visual system and brand rules
- `docs/frontend-style-guide.md` → layout and UX direction
- `docs/data-model.md` → suggested entities and relationships
- `docs/user-flows.md` → core product flows
- `docs/mvp-scope.md` → strict MVP boundaries
- `prompts/bpmn-generation-rules.md` → BPMN generation logic rules

## Working Principles

- prefer modularity over one-page complexity
- keep process logic separate from diagram rendering logic
- build a usable product, not only a visual demo
- do not overpromise AI capabilities in the first version
- treat generated BPMN as an editable draft, not unquestionable truth
- document important decisions as the project evolves

## Suggested Next Technical Decisions

Before starting implementation, define:

- frontend framework
- BPMN library
- persistence strategy
- backend scope for MVP
- authentication scope for MVP
- hosting / deployment direction

## Success Criteria for MVP

The MVP is successful if a user can:

- create a process
- enter structured process details
- generate a BPMN draft
- review and edit the BPMN
- save and reopen the process
- understand the UI without confusion

## License

Add your preferred license here.
