# Product Requirements

## 1. Product Summary

The product is a process planning platform that turns user-entered workflow information into editable BPMN diagram drafts.

It combines process intake, process structure, BPMN generation, BPMN review, and planning metadata in one platform.

## 2. Core Problem

Organizations often have process knowledge scattered across:

- meetings
- notes
- messages
- spreadsheets
- manual task lists
- undocumented routines

This creates process ambiguity and weak standardization.

Existing tools often fail because they are either:

- too diagram-focused
- too task-focused
- too manual
- too disconnected from actual operating discussions

## 3. Product Goal

The goal is to help users convert process knowledge into structured, editable workflow diagrams and maintain those diagrams in a usable planning environment.

## 4. Key Inputs

The system should support input such as:

- process title
- process objective
- trigger
- participants / roles
- tasks
- dependencies
- decision points
- expected outputs
- notes
- meeting details
- documents or references later

## 5. Key Outputs

The system should produce:

- BPMN draft diagram
- structured process overview
- mapped tasks and roles
- editable process steps
- process metadata for review

## 6. Main Use Cases

### Use Case 1: Create a Process
A user creates a new process record.

### Use Case 2: Enter Process Details
A user provides process structure through forms and notes.

### Use Case 3: Generate BPMN Draft
The system converts the process information into a BPMN draft.

### Use Case 4: Review and Edit BPMN
A user reviews the generated BPMN and corrects it as needed.

### Use Case 5: Manage Planning Metadata
A user updates task-level planning details such as owner, status, and notes.

## 7. MVP Functional Requirements

### 7.1 Process Management
- create process
- list processes
- open process detail
- edit process metadata
- archive or delete process

### 7.2 Process Intake
- process name
- objective
- trigger
- roles / participants
- tasks
- decision points
- expected output
- notes / meeting details

### 7.3 BPMN Draft Generation
- generate BPMN draft from structured inputs
- support start event
- support end event
- support user/service/generic task representation where practical
- support exclusive gateway in simple conditions
- support sequence flows
- support lanes / participants

### 7.4 BPMN Review
- display generated BPMN
- edit labels
- edit task order
- update lane association
- add/remove steps
- save and reload diagram

### 7.5 Planning Layer
- link planning records to generated steps
- set owner
- set status
- set priority
- set notes
- optional due date

## 8. Non-Functional Requirements

- professional and institutional UI
- maintainable architecture
- modular frontend
- stable diagram persistence
- understandable UX
- product clarity over visual gimmicks

## 9. Constraints

- do not depend only on unstructured notes for process truth
- generated BPMN should be treated as a draft
- avoid overbuilding AI scope in MVP
- avoid full enterprise permissions in the first version
- avoid automation engine scope in the first version

## 10. Future Direction

Possible future features:

- AI-assisted ambiguity detection
- AI suggestions for roles and gateways
- role-based access control
- collaboration
- version history
- export/import
- integrations
- analytics
- templates
- process comparison

## 11. Success Criteria

The MVP succeeds if users can:

- describe a process in a structured way
- generate a BPMN draft
- edit and save the BPMN
- maintain related planning details
- use the product without confusion
