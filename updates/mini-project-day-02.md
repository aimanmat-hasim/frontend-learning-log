# Mini Project — TaskFlow (Day 2)

**Status:** Day 2 — Core Logic Completed (UI styling later)

Today I completed the core application logic for TaskFlow. The interface is still minimal, but the functionality works end-to-end.

---

## What’s Working Now

### ✅ CRUD + State
- Add tasks (controlled input)
- Toggle done/active state
- Delete tasks
- Clear all completed tasks

### ✅ Filtering (All / Active / Done)
- Filter state: `"all" | "active" | "done"`
- Derived visible list using `useMemo` to avoid re-filtering unnecessarily

### ✅ Persistence (localStorage)
- Load once on mount:
  - read from `localStorage` using a fixed key
  - parse JSON safely with try/catch
- Save whenever `todos` changes:
  - `localStorage.setItem(key, JSON.stringify(todos))`

---

## Components Implemented

- `TodoForm`
  - controlled input + submit handler
  - trims input and blocks empty tasks
- `TodoItem`
  - checkbox toggle + delete button
- `TodoList`
  - list rendering with stable keys
  - empty state message when no tasks exist
- `FilterBar`
  - All / Active / Done buttons
  - remaining vs total counter

---

## Technical Notes / Decisions

- State updates are immutable:
  - add: `[newTodo, ...prev]`
  - toggle: `map()` with new object `{ ...t, done: !t.done }`
  - delete: `filter()`
- Unique ids are generated using timestamp + random hex string
- The UI layer is intentionally minimal until logic is stable

---

## Next Steps (Day 3)
- Improve UI layout (spacing, button styles, typography)
- Add small UX upgrades:
  - disable “Add” when input is empty
  - show active filter state more clearly
- (Optional) Add “Edit task title” feature
