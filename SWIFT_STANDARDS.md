## Swift Standards

1. **Design APIs for clarity at the point of use.**
   - Follow Swift API Design Guidelines. Names and APIs should read naturally at the call site and communicate intent clearly.
   - Optimize APIs for clarity at the point of use. Call sites must clearly communicate the operation and its intent.
   - Prefer clarity over brevity. Do not shorten names when doing so reduces understanding.
   - Include all words needed to avoid ambiguity. Names and argument labels must make the meaning of a call clear.
   - Omit needless words. Do not repeat information already conveyed by types or surrounding context.
   - Make API usage read fluently. Method names and argument labels should form natural, grammatical phrases at the call site.

2. **Prefer value semantics unless identity is required.**
   Use `struct` by default; use `class` when shared identity, reference semantics, lifecycle, or inheritance is required.

3. **Use access control deliberately.**
   - Keep implementation details `private` or `internal`; expose only what callers need.
   - do not omit the `internal` access control at declaration of internal types, properties, or functions.
   

4. **Protect shared mutable state and respect Swift concurrency isolation.**
   - Shared mutable state must have a clearly defined synchronization or actor-isolation boundary.
   - Do not bypass actor isolation or sendability requirements merely to silence diagnostics.
   - Use `@unchecked Sendable` only when thread safety can be verified and guaranteed.

5. **Prefer structured concurrency and manage long-lived task lifecycles explicitly.**
   - Use scoped tasks, child tasks, and task groups instead of detached or unmanaged work where practical.
   - Tasks whose lifetime exceeds a local scope must have clear ownership and cancellation behavior.

6. **Use typed errors when callers need to distinguish failure cases.**

7. **Avoid force unwraps and force casts unless an invariant guarantees success.**

8. **Use `guard` for prerequisites and early exits when it improves control-flow clarity.**

9. **Avoid unnecessary copying of expensive values.**
   Pay particular attention to buffers, `Data`, images, and large collections.

10. **Prefer domain types over magic values.**
    Use enums, option sets, typed identifiers, and dedicated types where they improve correctness.

11. **Document public APIs and non-obvious behavioral requirements.**
    - Document public API declarations. Documentation should begin with a concise summary describing the declaration.
    - Document non-obvious ownership, concurrency, and lifecycle requirements of public APIs.

12. **Follow Swift naming conventions and established terminology.**
    - Name methods according to their side effects. Use noun-like names for non-mutating operations and imperative verbs for mutating operations.
    - Name mutating and non-mutating operation pairs consistently. Use forms such as `sort()` / `sorted()` and `reverse()` / `reversed()`.
    - Use established terminology correctly. Prefer accepted terms of art and do not redefine their established meaning.
    - Avoid obscure terminology and nonstandard abbreviations. Prefer familiar terminology unless a technical term conveys necessary precision.
    - Use `UpperCamelCase` for types and protocols and `lowerCamelCase` for other declarations.

13. **Prefer methods and properties over free functions.**
    Use free functions only when there is no natural `self` or established notation justifies them.

14. **Design argument labels and parameter ordering for clear call sites.**
    - Design argument labels to clarify parameter roles. Omit labels only when arguments cannot be usefully distinguished or when Swift conventions specifically call for it.
    - Place parameters with default values after essential parameters. Preserve a stable and understandable primary call pattern.
