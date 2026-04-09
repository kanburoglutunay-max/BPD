# Tech Stack

## Purpose

This document defines the recommended initial technology stack for the Process Planning Platform MVP.

The goal is not to choose the most fashionable stack.  
The goal is to choose a stack that is stable, maintainable, fast enough to build with, and suitable for BPMN integration.

---

## 1. Recommended MVP Stack

### Frontend
- Next.js
- React
- TypeScript
- Tailwind CSS

### UI Components
- shadcn/ui
- Lucide icons

### BPMN
- bpmn-js

### State Management
- Zustand for local/global app state
- React Hook Form for forms

### Validation
- Zod

### Data Fetching
- Native fetch or TanStack Query if needed later

### Backend for MVP
Two realistic options:

#### Option A — Fastest MVP
- Next.js app with local persistence or mock JSON data
- no real backend at first

#### Option B — Better MVP
- Next.js frontend
- Supabase for database and auth

### Database
Recommended:
- PostgreSQL via Supabase

### Authentication
Recommended later for MVP+:
- Supabase Auth

### Hosting
Recommended:
- Vercel for frontend
- Supabase for backend/database

---

## 2. Why This Stack

## Next.js
Good choice because:
- fast project setup
- production-grade React framework
- clean routing model
- easy deployment
- flexible enough for future backend/API usage

## TypeScript
Required because:
- this project will have structured process entities
- BPMN mapping logic will get messy without typing
- safer refactoring
- clearer architecture

## Tailwind CSS
Useful because:
- fast UI implementation
- easy dark theme management
- clean design system enforcement
- easy component consistency

## shadcn/ui
Useful because:
- avoids building every base component from scratch
- can still be customized to match premium brand design
- better than random component libraries for this kind of product

## bpmn-js
This is the obvious BPMN choice for MVP because:
- widely used
- mature
- built for BPMN rendering/editing
- supports BPMN XML workflows
- much more realistic than building custom BPMN from scratch

## Zustand
Recommended because:
- simpler than Redux
- enough for MVP complexity
- good for UI/process state separation if used carefully

## Zod
Needed because:
- structured process intake requires validation
- important for process input quality
- useful for both frontend and backend consistency

---

## 3. Recommended MVP Architecture Choice

## Best practical choice
- Next.js
- TypeScript
- Tailwind
- shadcn/ui
- bpmn-js
- Zustand
- Zod
- Supabase

This is the most balanced route.

---

## 4. Suggested Folder Direction

```text
src/
  app/
  components/
    ui/
    layout/
    process/
    bpmn/
  features/
    process-intake/
    process-list/
    process-detail/
    bpmn-review/
    planning-layer/
  lib/
    bpmn/
    validation/
    utils/
  store/
  types/
  services/
