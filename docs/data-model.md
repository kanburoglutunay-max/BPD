# Data Model

## Purpose

This document outlines the suggested initial conceptual data model for the platform.

## Core Entities

### Process
Represents a process record.

Suggested fields:
- id
- name
- objective
- trigger
- expectedOutput
- category
- status
- createdAt
- updatedAt

### ProcessInput
Represents raw or semi-structured user-provided input used to generate BPMN.

Suggested fields:
- id
- processId
- meetingSummary
- notes
- assumptions
- rawText
- createdAt

### Role
Represents a participant or lane candidate.

Suggested fields:
- id
- processId
- name
- type
- description

### ProcessStep
Represents a structured process task.

Suggested fields:
- id
- processId
- title
- description
- roleId
- orderIndex
- status
- priority
- dueDate
- note

### DecisionPoint
Represents process branching logic.

Suggested fields:
- id
- processId
- label
- conditionText
- sourceStepId

### Dependency
Represents a relationship between steps.

Suggested fields:
- id
- processId
- fromStepId
- toStepId
- dependencyType

### Diagram
Represents the BPMN model content.

Suggested fields:
- id
- processId
- bpmnXml
- version
- generatedBy
- createdAt
- updatedAt

### BPMNNodeMapping
Maps BPMN nodes to structured process records.

Suggested fields:
- id
- processId
- bpmnNodeId
- stepId
- mappingType

### Note
Represents user notes or comments.

Suggested fields:
- id
- processId
- relatedStepId
- content
- createdAt

## Key Relationship Rule

The mapping between structured process steps and BPMN nodes must remain explicit.

This is one of the core product requirements.
