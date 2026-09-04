## General Coding Standards

1. **Optimize for readability**
   - Write code primarily for humans.
   - Prefer clear, explicit intent over cleverness or implicit behavior.

2. **Keep code simple**
   - Avoid accidental complexity, unnecessary indirection, and premature optimization.
   - Prefer straightforward solutions that are easy to understand and modify.

3. **Use intention-revealing names**
   - Names should communicate purpose, role, or behavior.
   - Use consistent terminology and avoid misleading names, unnecessary abbreviations, and encodings.

4. **Keep functions focused**
   - A function should do one thing at one level of abstraction.
   - Keep functions small and minimize parameters.
   - Avoid boolean control flags and hidden side effects.

5. **Separate queries from mutations**
   - Code that answers a question should normally not modify state.
   - Make state changes explicit and predictable.

6. **Keep related code together**
   - Favor local reasoning and keep strongly related concepts close.
   - Organize code from high-level intent toward implementation details.

7. **Keep abstractions purposeful**
   - Introduce abstractions only when they improve clarity, cohesion, reuse, or isolation.
   - Remove or inline abstractions that no longer justify their complexity.

8. **Eliminate duplication**
   - Do not maintain duplicated logic without a strong reason.
   - Prefer a single clear expression of shared behavior.

9. **Use comments for rationale, not explanation of poor code**
   - Prefer expressive names and structure over explanatory comments.
   - Comment non-obvious intent, constraints, warnings, protocols, and important design rationale.

10. **Keep control flow easy to follow**
    - Avoid deep nesting, excessive conditionals, and clever control flow.
    - Refactor complex paths into clearer structures.

11. **Make error handling explicit**
    - Keep the happy path readable.
    - Use meaningful error types and provide useful diagnostic context.
    - Keep error-handling concerns from obscuring primary logic.

12. **Minimize shared mutable state**
    - Prefer immutability, clear ownership, and explicit state transitions.
    - Introduce concurrency only when it provides a concrete benefit.

13. **Keep interfaces small**
    - Expose only what callers need.
    - Hide implementation details and make APIs difficult to misuse.

14. **Refactor incrementally**
    - Improve structure in small, behavior-preserving steps.
    - Remove dead code, duplication, misleading abstractions, and unnecessary complexity.

15. **Leave touched code cleaner**
    - Improve weak names, structure, duplication, and readability while working in an area.
    - Keep cleanup proportional to the task.

## Language-specific standards

In addition to the general standards above:

- **Swift:** For Swift code, read and apply [Swift Standards](SWIFT_STANDARDS.md).
- **Python:** For Python code, read and apply [Python Standards](PYTHON_STANDARDS.md).
