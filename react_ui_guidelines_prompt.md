# React + TypeScript: Clean Code & Optimization Prompt for Copilot/Cody

Use this prompt daily when generating or reviewing React + TypeScript code via Copilot or Cody:

---

## Prompt

You are helping me write and maintain **clean, optimized, and production-ready React + TypeScript code**. When suggesting or generating code, follow these best practices strictly:

### 1. Component Design & Structure
- Break large components into **smaller reusable components** or **utility functions**.
- Follow **Separation of Concerns**: JSX, state, handlers, effects, and derived values should be clearly separated.
- Avoid bulky render logic—extract parts into helper render methods (`renderHeader()`, `renderListItems()` etc.).
- Prefer **functional components** and modern React conventions.

### 2. Code Readability & Maintainability
- Keep components **under 50 lines** if possible.
- Use **clear and descriptive** names for functions, variables, and props.
- Comment only where logic is non-trivial (prefer JSDoc-style).
- Organize code with logical grouping: **state > effects > handlers > render**.

### 3. Conditional Logic
- Avoid deeply nested `if-else` blocks.
- Use `switch` or **early returns** for better readability.
- Use ternary only for **short expressions**, not multiple layers.

### 4. Function Best Practices
- Do **not mutate arguments**—always return a **new object** or array.
- Prefer **pure functions** for helpers/utilities.
- Abstract reusable logic into `utils/` or `hooks/`.

### 5. Hooks Optimization
- Use `useMemo` and `useCallback` **only when truly necessary** (e.g., expensive computation or stable dependency).
- Avoid wrapping all handlers in `useCallback` by default.
- Prefer computed values in render over redundant state.

### 6. Code Splitting & Performance
- Use `React.lazy` + `Suspense` for **non-critical or heavy components**.
- Apply **code-splitting** where performance is impacted.
- Avoid unnecessary re-renders—**check dependencies** in `useEffect`/`useMemo`.

### 7. Error Handling & Resilience
- Add **fallback UI** for loading and error states.
- Always **validate props and data** defensively.
- Catch and log errors in API calls and async operations.

### 8. Design & Consistency
- Follow **Atomic Design**: Atoms > Molecules > Organisms.
- Prefer consistent styling approach: **CSS Modules**, `styled-components`, or **TailwindCSS**.
- Maintain a clear folder structure:
```
src/
components/
hooks/
utils/
types/
services/
```

---

### Output Expectations
- Provide **clean, readable** code suggestions.
- Avoid overengineering or premature optimizations.
- Add a short explanation when suggesting new structures or patterns.

---

> Use this prompt daily while coding with Copilot/Cody to maintain consistency, readability, and performance in your React + TypeScript apps.