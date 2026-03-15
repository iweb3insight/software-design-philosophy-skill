# Design Methodology (Actionable)

## 1. System Thinking
- Principle: design is the whole system, not just modules.
- Methods:
1. Draw a system landscape early (components, data flow, dependencies).
2. Prioritize clear boundaries and interface contracts.
3. Run a global consistency check (style, naming, error handling).
- Example: large open-source projects define boundaries and contracts early to sustain scalability.

## 2. Modularity and Layering
- Principle: independent modules and clear layers reduce coupling and improve reuse.
- Methods:
1. Split by function and dependency (presentation, business, data).
2. High cohesion inside modules, low coupling between modules.
3. Separate common libraries from business libraries to avoid cycles.
- Example: commercial systems separate data access and business logic for long-term evolution.

## 3. Progressive Design and Iteration
- Principle: design evolves with requirements and technology.
- Methods:
1. Avoid over-design; implement only what is needed (YAGNI).
2. Refactor key modules regularly for performance and maintainability.
3. Use reviews and user feedback to adjust architecture.
- Example: microservices boundaries are refined over multiple iterations.

## 4. Understandability and Maintainability
- Principle: code and docs are communication tools.
- Methods:
1. Clear naming to reduce ambiguity.
2. Simple interfaces that hide internal complexity.
3. Use patterns and templates to improve readability.
- Example: frameworks like Django are easy to adopt due to clear APIs.

## 5. Experience and Feedback Loop
- Principle: design improves with practice and feedback.
- Methods:
1. Extract patterns from successful cases.
2. Run root-cause analysis on failures.
3. Build review and monitoring loops (decisions, architecture reviews, performance).
- Example: commercial systems use regular architecture reviews to keep systems healthy.
