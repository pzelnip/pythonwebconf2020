# Testing Best Practices

## Intro

Started with open discussion on why automated testing is hard.

Tests are 3 things:

- Asset (what we want, make us more productive, good ROI)
- Expense (manual testing ex)
- Liability (automated tests that are brittle or hard to run)

## What can we do to help automated testing be an asset?

Easy to set up:

- Dependencies declared
- service dependencies declared (docker compose)
- simple test instructions

Should be easy to run on a dev machine

Should always be a success or failure, do not live with unreliable or flaky
tests.

Ordering of tests should be irrelevant.

Environment should not affect pass/fail.

Use generators to generate random test data (prefer them over fixtures).
Generators are functions which generate data dynamically, easier to maintain
than static fixtures.

Make them fast. Be able to run failing tests separately from all tests.

Treat them like any other code, they need refactoring/rearchitecting.

Use code coverage tool to understand where holes in testing exist. Make goals
for constantly increasing test coverage over time. Don't worry about the
absolute number, follow the gain over time.

10:30-ish moved to working through examples.

Put `testing_create` method on model class itself. This feels weird to me, but
I get the power of it.

---

Principle #1: Just get started (with something trivial)
Principle #2: explicit is better than implicit (especially when it comes to errors)
Principle #3: make tests as close to the "real world" as possible
Principle #4: it's helpful to refactor code to make it easier to test
Principle #5: use mocking as needed to avoid depending on the "real world" for data
Principle #6: it's often useful to create CLI commands that make it easy to run library code
Principle #7: most of the time, your library code & data structures should be "context agnostic"
Principle #8: but, sometimes it makes more sense to share library code and make it adaptable to the context.
Principle #9: it's really easy to only test happy paths, don't do that. Test the unhappy paths too.
Principle #10: ????
Principle #11: when it comes to external services, there can often be multiple ways to test around the service. Pick the method that is most maintainable and least brittle.
Principle #12: tests are responsible for managing expected state (usually at the start of the test)
Principle #13: pytest fixtures can be very useful, but don't abuse them
Principle #14: generators are always better than database data fixtures
Principle #15: magic generators are really cool
