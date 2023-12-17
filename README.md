# gh-execution-flow

## Description

Controlling execution flow in GitHub Actions using conditional expressions.

### How-to

Set an id for each step you want to control the execution flow of.

Use the id in the `if` condition of the step you want to control the execution flow of.

## Usage

```yaml
id: run-tests

if: failure() && steps.run-tests.outcome == 'failure'
```

## Special Conditional Functions

### failure()

Returns true if the previous step failed.

### success()

Returns true if the previous step succeeded.

### cancelled()

Returns true if the previous step was cancelled.

### always()

Returns true.

## Reusable Workflows
