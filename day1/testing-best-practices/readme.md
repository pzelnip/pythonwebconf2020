# Testing Best Practices

## Intro

Started with open discussion on why automated testing is hard.

Tests are 3 things:

* Asset (what we want, make us more productive, good ROI)
* Expense (manual testing ex)
* Liability (automated tests that are brittle or hard to run)

## What can we do to help automated testing be an asset?

Easy to set up:

* Dependencies declared
* service dependencies declared (docker compose)
* simple test instructions

Should be easy to run on a dev machine

Should always be a success or failure, do not live with unreliable or flaky
tests.

Ordering of tests should be irrelevant.

Environment should not affect pass/fail.

Use generators to generate random test data (prefer them over fixtures).
Generators are functions which generate data dynamically, easier to maintain
than static fixtures.

Make them fast.  Be able to run failing tests separately from all tests.

Treat them like any other code, they need refactoring/rearchitecting.

Use code coverage tool to understand where holes in testing exist.  Make goals
for constantly increasing test coverage over time.  Don't worry about the
absolute number, follow the gain over time.

10:30-ish moved to working through examples.


Put `testing_create` method on model class itself.  This feels weird to me, but
I get the power of it.
