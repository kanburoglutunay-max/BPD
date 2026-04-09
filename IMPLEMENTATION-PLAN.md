
---

# `IMPLEMENTATION-PLAN.md`

```md
# Implementation Plan

## Purpose

This document defines the practical implementation sequence for the Process Planning Platform MVP.

The objective is to avoid random development and keep the build aligned with product logic.

---

## Phase 0 — Project Setup

## Goal
Establish the technical and documentation foundation.

## Tasks
- initialize Next.js project
- configure TypeScript
- configure Tailwind CSS
- set up base linting/formatting
- install shadcn/ui
- install Lucide icons
- install Zustand
- install React Hook Form
- install Zod
- install bpmn-js
- prepare folder structure
- prepare shared types folder

## Deliverable
A clean starter project with structure, dependencies, and documentation in place.

---

## Phase 1 — Design System and App Shell

## Goal
Create the branded frontend foundation aligned with the company logo and product direction.

## Tasks
- implement dark premium theme
- define global colors, spacing, typography
- build sidebar
- build topbar
- build page container layout
- build reusable card, button, input, dialog, table components
- ensure UI matches brand direction

## Deliverable
A clean, professional shell that can host all product features.

---

## Phase 2 — Core Data Model and Validation

## Goal
Create the internal structure needed for process intake and BPMN generation.

## Tasks
- define TypeScript types for Process, Role, Step, DecisionPoint, Diagram, Mapping
- create Zod schemas for process intake forms
- create utility functions for normalized process input
- define draft-safe default states
- prepare validation rules for required process generation fields

## Deliverable
A typed and validated process data model.

---

## Phase 3 — Process Management Foundation

## Goal
Allow users to create and manage process records.

## Tasks
- build process list page
- build process creation flow
- build process detail shell
- add process metadata editing
- add basic search/filter UI
- prepare empty states

## Deliverable
Users can create and open process records.

---

## Phase 4 — Structured Process Intake

## Goal
Capture process information in a way that supports BPMN generation.

## Tasks
- build intake form sections:
  - process info
  - objective
  - trigger
  - roles
  - tasks
  - dependencies
  - decision points
  - expected output
  - notes / meeting details
- add add/remove dynamic inputs
- validate required fields
- build intake summary view

## Deliverable
Users can enter structured process information.

---

## Phase 5 — Internal Process Graph Builder

## Goal
Transform structured user input into a machine-usable process structure.

## Tasks
- create role-to-lane mapping logic
- create step ordering logic
- create dependency resolution logic
- create decision point modeling logic
- create start/end inference logic
- define internal process graph structure

## Deliverable
A normalized internal process graph that can feed BPMN generation.

---

## Phase 6 — BPMN Draft Generation

## Goal
Generate an editable BPMN draft from the internal process graph.

## Tasks
- define BPMN generation rules
- map start event
- map end event
- map tasks
- map lanes
- map exclusive gateways
- map sequence flows
- generate BPMN XML or equivalent model format
- validate output structure

## Deliverable
The system produces initial BPMN drafts.

---

## Phase 7 — BPMN Viewer and Editor Integration

## Goal
Allow users to inspect and edit the generated BPMN.

## Tasks
- build BPMN viewer/editor wrapper component
- load generated BPMN into viewer
- support save/update
- support selection state
- connect selected node to side properties panel
- handle basic edit actions safely

## Deliverable
Generated BPMN is viewable and editable.

---

## Phase 8 — Planning Metadata Layer

## Goal
Attach operational planning data to process steps and BPMN nodes.

## Tasks
- build step properties panel
- support owner assignment
- support status assignment
- support priority
- support notes
- optional due date
- persist node-to-step mappings
- show planning table

## Deliverable
The product becomes more than a diagram editor.

---

## Phase 9 — Persistence Layer

## Goal
Persist process, BPMN, and metadata reliably.

## Tasks
- create storage schema
- save process metadata
- save structured intake data
- save BPMN XML
- save step metadata
- save node mappings
- load all related records on reopen

## Deliverable
Users can save and reopen complete process records.

---

## Phase 10 — UX Refinement

## Goal
Improve usability and visual clarity.

## Tasks
- reduce screen clutter
- improve empty states
- improve validation messages
- improve loading states
- improve navigation between intake and BPMN review
- refine spacing and hierarchy
- ensure strong visual coherence with brand

## Deliverable
A more professional and usable MVP.

---

## Phase 11 — MVP Hardening

## Goal
Make the MVP stable enough for demonstration or internal pilot usage.

## Tasks
- fix critical bugs
- test BPMN generation edge cases
- test save/load integrity
- review process-to-node mapping consistency
- clean up obvious UI inconsistencies
- remove dead code
- update documentation

## Deliverable
An MVP that is credible, not just visually impressive.

---

## Practical Delivery Order

If development capacity is limited, build in this exact order:

1. app shell
2. process list and process detail shell
3. process intake forms
4. internal process graph builder
5. BPMN draft generation
6. BPMN editor integration
7. planning metadata panel
8. persistence
9. UX refinement

---

## Discipline Rule

Do not start advanced AI features before the structured process intake and BPMN generation pipeline works reliably.
