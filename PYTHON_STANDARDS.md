## Python Coding Standards

1. **Optimize for readability, clarity, and simplicity.**
   - Prefer explicit code over implicit behavior.
   - Prefer simple designs over unnecessarily complex ones.
   - Avoid excessive nesting and dense expressions when clearer alternatives exist.
   - If an implementation is difficult to explain, reconsider the design.

2. **Follow PEP 8 naming conventions consistently.**
   - Use `snake_case` for functions, methods, and variables.
   - Use `CapWords` for classes.
   - Use `UPPER_CASE` for constants.
   - Use leading underscores to communicate non-public implementation details.

3. **Keep public interfaces clear and intentional.**
   - Expose only what callers need.
   - Distinguish public and internal interfaces deliberately.
   - Avoid compatibility-breaking changes to public APIs without justification.

4. **Keep functions and classes focused.**
   - Prefer small units with clear responsibilities.
   - Separate unrelated behavior rather than accumulating responsibilities in one function or class.

5. **Handle errors explicitly and precisely.**
   - Do not silently ignore errors unless suppression is intentional.
   - Catch specific exceptions rather than overly broad exceptions.
   - Raise exceptions that accurately represent the failure.
   - Preserve useful exception context when translating errors.

6. **Manage resource lifetimes explicitly.**
   - Prefer `with` and context managers for files, locks, connections, and other scoped resources.
   - Ensure cleanup occurs reliably on success, failure, and early exit.

7. **Avoid unsafe or ambiguous defaults.**
   - Do not use mutable objects as default argument values unless shared state is explicitly intended.
   - Use `None` or factories when a fresh mutable value is required for each call or instance.

8. **Prefer Python's native abstractions and idioms.**
   - Prefer iteration over index-based access when indices are unnecessary.
   - Prefer comprehensions when they remain clear.
   - Use unpacking, generators, context managers, and standard-library abstractions where they improve clarity.
   - Do not reproduce language or library functionality unnecessarily.

9. **Use comprehensions and expressions only while they remain readable.**
   - Avoid deeply nested comprehensions.
   - Do not compress substantial control flow into a single expression merely to reduce line count.

10. **Use imports deliberately and predictably.**
    - Place imports near the top of the module unless delayed import is intentional.
    - Group standard-library, third-party, and local imports separately.
    - Avoid wildcard imports except where an API explicitly requires them.
    - Prefer absolute imports unless an explicit relative import improves package clarity.

11. **Use type annotations where they improve API clarity and tooling.**
    - Type public interfaces and important boundaries where useful.
    - Prefer precise domain types over overly broad annotations.
    - Do not use annotations merely to satisfy tooling when they obscure the real contract.

12. **Document public modules, classes, functions, and methods.**
    - Follow PEP 257 docstring conventions.
    - Start with a concise summary.
    - Document relevant arguments, return values, side effects, raised exceptions, and usage restrictions.
    - Avoid comments and docstrings that merely restate obvious code.

13. **Keep control flow explicit and easy to follow.**
    - Prefer early exits where they reduce nesting.
    - Avoid unnecessary `else` blocks after unconditional `return`, `raise`, `break`, or `continue`.
    - Do not rely on clever control-flow tricks that obscure intent.

14. **Use comparisons and Python semantics correctly.**
    - Use `is` / `is not` for identity checks such as `None`.
    - Use truth-value testing where appropriate instead of redundant comparisons.
    - Do not depend on implementation-specific behavior when language-defined behavior is available.

15. **Prefer practicality and consistency over rigid rule-following.**
    - Follow established project conventions where consistency improves maintainability.
    - Deviate from a style rule when applying it would materially reduce readability or correctness.
