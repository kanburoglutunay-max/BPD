# BPMN Generation Rules

## Purpose

This document defines the initial logic for turning structured process input into a BPMN draft.

## Important Principle

Generated BPMN is a draft.  
It should be editable and should not be treated as guaranteed perfect truth.

## Expected Inputs

The generation logic may use:

- process objective
- trigger
- roles
- tasks
- dependencies
- decision points
- expected output
- notes

## Initial Interpretation Rules

### 1. Start Event
Create a start event when the process has a trigger or an implied beginning.

### 2. End Event
Create an end event when there is a defined final output or completion state.

### 3. Tasks
Create BPMN tasks from structured process steps.

### 4. Lanes
Create lanes from defined roles or participants.

### 5. Sequence Flow
Use explicit task ordering and dependencies to create sequence flow.

### 6. Exclusive Gateway
Use a simple exclusive gateway when the input clearly describes a conditional branch such as:
- approved / rejected
- available / unavailable
- yes / no

### 7. Parallel Logic
Do not aggressively infer parallel logic in MVP unless it is explicitly stated.

### 8. Ambiguity
If task order or role ownership is unclear, preserve the ambiguity for user review instead of inventing certainty.

## MVP BPMN Coverage

Support at minimum:

- start event
- end event
- task
- exclusive gateway
- sequence flow
- lanes

## Not Required for MVP

- boundary events
- escalation
- compensation
- complex message choreography
- deep subprocess orchestration

## Quality Rule

Prefer simpler BPMN that users can refine over complex BPMN that is likely wrong.
