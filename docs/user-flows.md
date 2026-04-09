# User Flows

## 1. Create Process Flow

1. user clicks create process
2. user enters process title and objective
3. user saves process shell
4. system opens process detail

## 2. Process Intake Flow

1. user enters roles
2. user enters steps
3. user enters dependencies
4. user enters decision points
5. user optionally enters meeting notes
6. user reviews input summary
7. user clicks generate BPMN draft

## 3. BPMN Draft Generation Flow

1. system validates required fields
2. system builds internal process structure
3. system assigns lanes
4. system creates tasks and gateways
5. system outputs BPMN draft
6. system displays BPMN review screen

## 4. BPMN Review Flow

1. user inspects generated diagram
2. user selects nodes
3. user edits labels or structure
4. user adjusts lane associations if needed
5. user saves BPMN

## 5. Planning Metadata Flow

1. user opens process detail
2. user selects a step
3. user assigns owner, status, notes, priority
4. system stores metadata
5. user sees updated process record

## 6. Process Reopen Flow

1. user opens existing process
2. system loads process metadata
3. system loads BPMN
4. system loads planning data
5. user continues editing
