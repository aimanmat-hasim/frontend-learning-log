# Mini Project — TaskFlow (Day 1)

**Project:** TaskFlow (Todo App with React + TypeScript)  
**Status:** Day 1 — Setup & Core Architecture Planning

This entry documents Day 1 of my first React + TypeScript mini project.  
The focus was on **environment setup, architecture planning, and understanding core logic** before completing the full implementation.

---

## Project Goal
Build a simple but realistic task management app with:

- Add task (controlled input)
- Toggle task completion
- Delete task
- Filter tasks (All / Active / Done)
- Persist data using `localStorage` via `useEffect`

This project is designed to apply concepts learned in Phase 2:  
state, immutability, controlled inputs, lists, keys, and effects.

---

## Day 1 Focus

### 1. Project Setup (Vite + React + TypeScript)
- Initialized project using Vite for fast development:
  ```bash
  npm create vite@latest taskflow -- --template react-ts
  cd taskflow
  npm install
  npm run dev
Confirmed Hot Module Replacement (HMR) for instant feedback

Reviewed default Vite + React project structure

2. Core Types & Data Models
Defined clear TypeScript types early:

Filter: "all" | "active" | "done"

Todo object:

id (unique identifier)

title (task description)

done (completion state)

createdAt (timestamp)

Early typing helps avoid logic errors later in the project.

3. React Hooks Planning
Planned hook usage before full implementation:

useState

manage task list

manage input value

useEffect

sync tasks with browser localStorage

useMemo

optimize filtered task lists

This reinforces separation between state, derived data, and side effects.

4. Controlled Form Design
Designed the TodoForm component with:

Controlled input (value + onChange)

preventDefault() on submit

Input trimming to avoid empty tasks

Callback (onAdd) passed from parent

This matches the standard React data flow:
input → event → state → re-render → UI

5. Component Responsibility Planning
Planned component responsibilities clearly:

TodoForm

handles user input

emits clean task titles upward

TodoItem

displays task

handles toggle & delete via callbacks

Parent component

owns state

handles logic

persists data

This avoids tight coupling and keeps components reusable.

Day 1 Takeaways
Writing types first improves clarity

Planning component boundaries early prevents refactoring later

Controlled inputs are essential for predictable behavior

useEffect should handle persistence, not rendering logic

Next Steps (Day 2)
Complete task list rendering

Implement filtering logic

Connect localStorage persistence

Finalize toggle and delete behavior

Refactor and prepare for public release
