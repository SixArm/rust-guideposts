# Source-based code coverage

<https://doc.rust-lang.org/rustc/instrument-coverage.html>

In Rust, source-based code coverage is a way of measuring how much of a Rust codebase is executed during a test suite. This type of coverage analysis works by instrumenting the Rust code and tracking which lines of code are executed during a test run.

The process of generating source-based coverage typically involves the following steps:

* Instrumentation: The Rust code is modified to include extra code that tracks which lines of code are executed.

* Test Execution: The test suite is run against the instrumented code.

* Coverage Report Generation: The data collected during the test run generates a report that shows which lines of code were executed and which were not.

The resulting coverage report provides developers with insights into the effectiveness of their tests and helps identify areas of the code that are not being sufficiently exercised by the test suite.

One key advantage of Rust source-based coverage is that it can provide more accurate coverage measurements than alternative methods, such as binary-based coverage. This is because source-based coverage is able to account for control structures, such as branches and loops, which can lead to different paths through the code being executed.

To run unit tests with coverage:

```sh
RUSTFLAGS="-C instrument-coverage" cargo test --tests
```

After the tests run, there are a variety of ways to use the output files and view the coverage reports. The steps are detailed, so please see the link above for specifics.
