# Refactoring

You've been asked to refactor the function `deterministicPartitionKey` in [`dpk.js`](dpk.js) to make it easier to read and understand without changing its functionality. For this task, you should:

1. Write unit tests to cover the existing functionality and ensure that your refactor doesn't break it. We typically use `jest`, but if you have another library you prefer, feel free to use it.
2. Refactor the function to be as "clean" and "readable" as possible. There are many valid ways to define those words - use your own personal definitions, but be prepared to defend them. Note that we do like to use the latest JS language features when applicable.
3. Write up a brief (~1 paragraph) explanation of why you made the choices you did and why specifically your version is more "readable" than the original.

You will be graded on the exhaustiveness and quality of your unit tests, the depth of your refactor, and the level of insight into your thought process provided by the written explanation.

## Your Explanation Here

- In the dpk.js file, I've added another function called `deterministicPartitionKey` - this is the refactored version of the original function
- In the refactored code, I have used the following concepts to make the code cleaner and more readable:
  - Short-circuiting - in the cases where the answer is trivial, we should try to return from the function as early as possible
  - Use of `const` in place of `var` - in general, it is harder to keep track of variables that change state throughout a code flow. Changing the code design to immutable `consts` reduces some of this overhead in trying to understand the code. 
  - Modular code: break up a large function into smaller more logically compact functions, improves readability and easier debugging.
  - Performing null-checks early in the function and handling it ensures that the following code can treat the input as being well-formed input.
  - TDD: writing out the possible patterns of input to the function, as to test the function on the full wide range of inputs that can possibly exist - reduces chances of errors/bugs.