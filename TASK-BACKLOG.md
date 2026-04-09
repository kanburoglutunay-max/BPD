# Task Backlog

## Purpose

This backlog breaks the MVP into practical tasks.  
Tasks should be completed in sequence where dependencies exist.

---

# Epic 1 — Repository and Project Setup

- [ ] Initialize Next.js project
- [ ] Configure TypeScript
- [ ] Configure Tailwind CSS
- [ ] Install shadcn/ui
- [ ] Install Lucide icons
- [ ] Install Zustand
- [ ] Install React Hook Form
- [ ] Install Zod
- [ ] Install bpmn-js
- [ ] Create base folder structure
- [ ] Add initial environment setup if needed
- [ ] Add ESLint / Prettier configuration
- [ ] Add base theme variables

---

# Epic 2 — App Shell and Branding

- [ ] Build sidebar layout
- [ ] Build topbar
- [ ] Build page wrapper
- [ ] Add dark premium theme
- [ ] Add branded color tokens
- [ ] Add typography rules
- [ ] Create reusable button component
- [ ] Create reusable input component
- [ ] Create reusable card component
- [ ] Create reusable table component
- [ ] Create reusable dialog/sheet component

---

# Epic 3 — Types and Schemas

- [ ] Define Process type
- [ ] Define Role type
- [ ] Define ProcessStep type
- [ ] Define DecisionPoint type
- [ ] Define Dependency type
- [ ] Define Diagram type
- [ ] Define BPMNNodeMapping type
- [ ] Define Note type
- [ ] Create Zod schema for process creation
- [ ] Create Zod schema for process intake
- [ ] Create form-safe default values

---

# Epic 4 — Process Management

- [ ] Build dashboard placeholder
- [ ] Build process list page
- [ ] Build create process modal/page
- [ ] Build process detail shell
- [ ] Build process summary section
- [ ] Add empty state for no processes
- [ ] Add simple search UI
- [ ] Add simple status filter UI

---

# Epic 5 — Structured Process Intake

- [ ] Build process objective section
- [ ] Build trigger section
- [ ] Build roles section
- [ ] Build task list section
- [ ] Build dependency input section
- [ ] Build decision point input section
- [ ] Build expected output section
- [ ] Build notes / meeting details section
- [ ] Add dynamic add/remove item controls
- [ ] Add validation messages
- [ ] Build intake review summary

---

# Epic 6 — Internal Process Structuring

- [ ] Create normalized process input utility
- [ ] Create role-to-lane mapping utility
- [ ] Create step ordering utility
- [ ] Create dependency resolver
- [ ] Create decision-point transformer
- [ ] Create start event inference
- [ ] Create end event inference
- [ ] Define internal process graph type
- [ ] Build process graph from input

---

# Epic 7 — BPMN Generation

- [ ] Create BPMN generation service
- [ ] Map start event
- [ ] Map end event
- [ ] Map lanes
- [ ] Map tasks
- [ ] Map exclusive gateways
- [ ] Map sequence flows
- [ ] Generate BPMN model output
- [ ] Create basic BPMN validation checks
- [ ] Generate node mapping records

---

# Epic 8 — BPMN Viewer and Editing

- [ ] Build BPMN viewer wrapper
- [ ] Load BPMN output into editor
- [ ] Add BPMN canvas container
- [ ] Add node selection handling
- [ ] Add selected node side panel
- [ ] Add save BPMN action
- [ ] Add reset/reload action
- [ ] Add edit label support
- [ ] Add lane review support

---

# Epic 9 — Planning Metadata

- [ ] Build step detail panel
- [ ] Add owner field
- [ ] Add status field
- [ ] Add priority field
- [ ] Add notes field
- [ ] Add optional due date field
- [ ] Build planning table view
- [ ] Link BPMN node selection to planning detail
- [ ] Persist node-to-step mappings

---

# Epic 10 — Persistence

- [ ] Create persistence model
- [ ] Save process metadata
- [ ] Save process intake data
- [ ] Save BPMN XML
- [ ] Save planning metadata
- [ ] Save mappings
- [ ] Load process detail on open
- [ ] Load BPMN on reopen
- [ ] Load planning data on reopen

---

# Epic 11 — UX and Quality

- [ ] Add loading states
- [ ] Add empty states
- [ ] Add error states
- [ ] Improve form clarity
- [ ] Improve BPMN review clarity
- [ ] Improve navigation between tabs/sections
- [ ] Improve mobile/tablet fallback as practical
- [ ] Remove visual clutter
- [ ] Align all screens with brand language

---

# Epic 12 — MVP Hardening

- [ ] Review process graph edge cases
- [ ] Review BPMN generation edge cases
- [ ] Test save/reload consistency
- [ ] Test mapping stability
- [ ] Fix critical bugs
- [ ] Clean dead code
- [ ] Update README if implementation changes
- [ ] Update architecture doc if structure changes
- [ ] Prepare demo-ready sample data

---

# Nice-to-Have After MVP

- [ ] Process templates
- [ ] Ambiguity warnings
- [ ] AI suggestion layer
- [ ] Export BPMN
- [ ] Import process input
- [ ] Role-based access
- [ ] Version history
- [ ] Collaboration comments

---

## Prioritization Rule

When priorities conflict, choose tasks that improve this core flow:

1. create process
2. enter structured input
3. generate BPMN draft
4. review/edit BPMN
5. save and reopen process
