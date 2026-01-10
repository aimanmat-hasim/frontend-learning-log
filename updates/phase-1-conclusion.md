# Phase 1 — Frontend Fundamentals (React + TypeScript)

This marks the conclusion of **Phase 1** in my frontend learning journey, focused on building strong mental models before scaling into projects.

## Core Concepts Covered

### React Foundations
- React as a **declarative UI library**
- Components as **functions returning JSX**
- Understanding the role of `main.tsx` vs `App.tsx`
- Virtual DOM and why React re-renders efficiently

### JSX Mental Model
- JSX as JavaScript syntax, not HTML
- One parent element rule
- Embedding JavaScript using `{}` 
- camelCase props and event handlers

### State & Events (Core React Loop)
- `useState` as React’s memory system
- Why state updates must go through setter functions
- Re-rendering as a function re-execution, not a page reload
- Event → handler → state update → re-render → UI update

### Data Flow & Props
- One-way data flow (parent → child)
- Props as function arguments
- State ownership living in the parent
- Child-to-parent communication via callback functions

### useEffect (Conceptual Understanding)
- Side effects vs rendering logic
- Dependency array patterns:
  - `[]` → run once
  - `[state]` → run on change
- Clear separation between events and effects
- Cleanup functions to prevent memory leaks

### TypeScript in React
- Type inference vs explicit typing
- Typing props and state when necessary
- Understanding `:` as type annotation, not assignment

---

## Key Takeaways
- React is predictable when the mental model is clear
- State drives UI, events trigger state, effects respond to changes
- Strong fundamentals reduce future complexity
- Avoiding premature abstractions is intentional

---

## Next Phase
**Phase 2** will focus on:
- Guided React + TypeScript projects
- Component composition
- Real-world UI patterns
- Cleaner GitHub-ready codebases

This repository serves as a learning log and progress tracker before publishing production-ready projects.
