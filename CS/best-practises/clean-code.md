# Clean Code

Readable and meaningful and understandable code

Should be concise and to the point

Should avoid complex nesting, big code blocks

Should follow common practices and pattern

Should be slim

It should be fun and easy to understand

## Names

Classes

Functions

Variables/constants

Names should be meaningful

Use nouns or short phrases with adjective(userData, isValid)

Boolean names: isValid, isCorrect

Variables : user, customer(it has to be specific)

Methods: getUserByEmail,saveUser

Classed: User,Admin

Function should be verbs or short phrases with adjective(sendData, inputIsValid)

Classes should be nouns or short phrases with nouns(User, RequestBody)

Be consistent: getUsers or fetchUser or retrieveUsers, getProducts or fetchProducts

If you have choosed get follow consistently (getUsers, getProducts)

### Name Casing

Snake case

is_valid ---- for variables, methods,

camelCase

isValid --- for variables and methods

PascalCase

AdminRole --- for the classes

Kebab case

<side-drawer> --we use in html

## Structure and comments

Code formatting

Improves code readability

Spaces between methods

Spaces after import

Keep related methods close to each other

Try to reduce the line which needs scroll (horizontal scroll in editor)

Good and bad comments

Names of the variables, methods should be self explainable by that will not need the comments

We could add a regex, for which we can add comments what it really does

// To do need to add implementation, comment can be added

Generally we should avoid comments

## Functions

Length of the code

Functions should be small

Function should do one thing

Stay dry (don’t repeat yourself)

Split functions reasonably

Try keep functions pure

For Same input we will always get same output

### No side effects

Side effect is an operation which does not just act on function inputs and change the function output but which instead changes the overall system /program state.

Side effects are not automatically bad- we do need them in our programs. But unexpected side effects should be avoidable.

If there are side effects then we can try to split the function

Parameters

Minimise the no of parameters(3 is more,max of 2)

When there is 3 parameters we can pass this is as an object so that we can avoid order which we need to pass to the function.

## Conditionals

Deep nesting

Check if the value exists if not return or throw error

Avoid magic number and strings

/https://github.com/academind/clean-code-course-code/blob/control-extra-attachments/Control-Structures-Summary.pdf

Error Handling

Missing error handling

Classes and datastructure

Missing distinction

Bloated classes

/https://github.com/academind/clean-code-course-code/blob/obj-extra-attachments/Objects-Summary.pdf

## Notes

How to write the code

Focus on single files

You will always find ways of improving the code

Question a old code and refactor a lot

Codebase can only survive and stay maintainable if it is continuously improved

Whenever you try to add something new , try to improve the existing code along the way

Clean architecture

Where to write which code

Focus on the project as a whole
