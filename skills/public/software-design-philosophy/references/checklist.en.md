# Software Design Best-Practice Checklist

## 1. System Thinking
1. Draw the system landscape
- Action: produce component, data-flow, and dependency diagrams early.
- Tip: mark boundaries and interface contracts.
2. Check global consistency
- Action: review naming, style, and error handling for consistency.
- Tip: enforce via reviews or static analysis.
3. Design module boundaries first
- Action: define responsibilities, interfaces, and dependencies.
- Tip: internal complexity should not leak outward.

## 2. Modularity and Layering
4. Split by function
- Action: separate presentation, business, and data layers.
- Tip: each layer has a single responsibility.
5. High cohesion, low coupling
- Action: keep logic cohesive and dependencies minimal.
- Tip: use interfaces to hide implementations.
6. Separate common and business libraries
- Action: keep shared utilities independent of business logic.
- Tip: prevent circular dependencies.

## 3. Progressive Design
7. Follow YAGNI
- Action: implement only current needs.
- Tip: evolve later when requirements change.
8. Refactor key modules regularly
- Action: identify high-complexity modules and simplify them.
- Tip: keep modules small and maintainable.
9. Review and feedback loop
- Action: conduct architecture reviews after iterations.
- Tip: schedule reviews by milestone.

## 4. Understandability and Maintainability
10. Clear, intuitive naming
- Action: keep names unambiguous.
- Tip: use team-wide naming conventions.
11. Simple module interfaces
- Action: expose only necessary methods.
- Tip: document params, returns, and errors.
12. Use patterns and templates
- Action: apply proven patterns in key scenarios.
- Tip: reduce repeated design work.

## 5. Experience and Feedback
13. Extract patterns from successes
- Action: derive patterns from open-source or prior projects.
- Tip: focus on reusable, scalable practices.
14. Analyze failures
- Action: document root causes.
- Tip: build a lessons-learned library.
15. Establish review mechanisms
- Action: record design decisions and monitor performance.
- Tip: run post-release reviews.
