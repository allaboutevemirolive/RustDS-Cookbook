Here's an exhaustive list of functions and methods in Rust that are commonly used for error handling:

1. `panic!` macro:
   - Syntax: `panic!("Error message");`
   - Description: Generates a runtime panic with an error message and terminates the program.

2. `Result<T, E>` type:
   - Description: Represents the result of an operation that can either be `Ok(value)` with a successful result of type `T`, or `Err(error)` with an error of type `E`.

3. `unwrap` method:
   - Syntax: `Result<T, E>.unwrap()`
   - Description: Extracts the value from a `Result`, returning it if it is `Ok`, or panics with the error if it is `Err`.

4. `expect` method:
   - Syntax: `Result<T, E>.expect("Error message")`
   - Description: Extracts the value from a `Result`, returning it if it is `Ok`, or panics with a custom error message if it is `Err`.

5. `unwrap_or` method:
   - Syntax: `Result<T, E>.unwrap_or(default_value)`
   - Description: Extracts the value from a `Result`, returning it if it is `Ok`, or returns a default value if it is `Err`.

6. `unwrap_or_else` method:
   - Syntax: `Result<T, E>.unwrap_or_else(|| { ... })`
   - Description: Extracts the value from a `Result`, returning it if it is `Ok`, or executes a fallback closure to compute a default value if it is `Err`.

7. `match` expression:
   - Syntax: `match result { Ok(value) => { ... }, Err(error) => { ... } }`
   - Description: Matches a `Result` against its variants (`Ok` and `Err`) and executes different blocks of code based on the variant.

8. `if let` statement:
   - Syntax: `if let Ok(value) = result { ... }`
   - Description: Matches a `Result` against the `Ok` variant and executes a block of code if it matches.

9. `unwrap_err` method:
   - Syntax: `Result<T, E>.unwrap_err()`
   - Description: Extracts the error from a `Result`, returning it if it is `Err`, or panics with the value if it is `Ok`.

10. `unwrap_err_or_else` method:
    - Syntax: `Result<T, E>.unwrap_err_or_else(|| { ... })`
    - Description: Extracts the error from a `Result`, returning it if it is `Err`, or executes a fallback closure to compute a default error if it is `Ok`.

11. `map` method:
    - Syntax: `Result<T, E>.map(|value| { ... })`
    - Description: Transforms a `Result` by applying a function to the inner value if it is `Ok`, otherwise returns the `Err` unchanged.

12. `and_then` method:
    - Syntax: `Result<T, E>.and_then(|value| { ... })`
    - Description: Chains a sequence of computations on a `Result`, passing the inner value to the next computation if it is `Ok`, otherwise returns the `Err` unchanged.

13. `or` method:
    - Syntax: `Result<T, E>.or(other_result)`
    - Description: Returns the `Ok` value if the `Result` is `Ok`, otherwise returns the `other_result`.

14. `unwrap_or_default` method:
    - Syntax: `Option<T>.unwrap_or_default()`
    - Description: Extracts the value from an `Option`, returning it if it is `Some`, or returns the default value of the type if it is `None`.

15. `Option` type:
    - Description: Represents an optional value that can either be `Some(value)` with a value of type `T`, or `None` indicating the absence of a value.

16. `Some(value)`:
    - Description: Constructs an `Option` with a non-null value of type `T`.

17. `None`:
    - Description: Represents the absence of a value in an `Option`.

These are some of the common functions, methods, and types in Rust that are used for error handling. They provide mechanisms to handle and propagate errors, allowing you to write robust and reliable code.