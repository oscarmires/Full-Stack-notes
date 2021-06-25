# Test Driven Development

TDD is a software development practice that consists of **converting the (functional) software requirements into test cases** before the product is fully developed.

This tests must by done repeatedly.

Mayor contributions were made by **Kent Beck** to this process;

__________

## TDD Life cycle

![TDD Life Cycle](https://upload.wikimedia.org/wikipedia/commons/0/0b/TDD_Global_Lifecycle.png)

## Unit Testing
> unit testing is a software testing method by which individual units of source code are tested to determine whether they are fit for use.

TDD relies heavily on unit testing because they are unit tests which must be written before writing functionality.

A clean test must follow 5 other rules that can be easily memorized using the acronym FIRST:

- **Fast**: a test must be fast to be executed often.
- **Independent**: tests must not depend on each other.
- **Repeatable**: a test must be reproducible in any environment.
- **Self-Validating**: a test must have a binary result (Failure or Success) for a quick and easy conclusion.
- **Timely**: a test must be written at the appropriate time, i.e. just before the production code it will validate.

\* or "fast, complete, reliable, isolated, maintainable, and expressive". 

## Integration Testing
- Takes modules already unit-tested
- Outputs integrated system ready for system testing.