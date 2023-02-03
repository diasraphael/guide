# Testing

Verify if something as intended

## Manual Testing

Doing it by manually

Need to check all the possible scenarios all time if not

Tedious

Often incomplete

## Automated testing

We write a couple of test that will test the feature

Initial effort, no effort afterwards

predictable, consistent

Complete code and coverage scenario can be achieved

Its needs a test runner and assertion library

### Test runner

Runs the testcases you have written

Automatically detects testing code

Display results

Eg Jest, Karma, vitest

### Assertion library

Checks whether the expectation are met

Supports all kinds of expectations(sync/async)

Eg: Jest, Chai, vitest

#### VITEST

Vitest is latest tool to run the testcases as well as use it as assertion libaray(it supports the jest syntaxes so you can use vitest as test runner and use jest syntax). It has the latest ES6 syntax. (In Jest they are using ES6 as experimental features due to that we can use VITEST to get the latest (ES6 imports for example))

## Testing Fundamentals

Need to find the smallest unit(for eg functions)

Files will have an extension (math.test.js or math.spec.js)

test or it both are same(in unit test file)it is preferable

Should follow AAA principle

Arrange = to define the values in the beginning of the test

Act = to call the actual method which we want to test

Assert = to assert whether the value is expected

Should test with incorrect values as well

If you expect a function to throw error then you can use expect with .toThrow()

(.toBe

.no.toBe)

Test what you want to test

beforeAll, afterAll, beforeEach, afterEach

Concurrent execution

describe.concurrent()

It.concurrent()

Organize the structure using describe and corresponding it within the describe block

### Spies & Mocks:

To test your code instead of the third party code we have spies and mocks

Spies:

To check whether the method has been called

To check if the method has been called with certain arguments

Can also check how many times it is called.

Spies are wrappers around functions or empty replacement for function that allow you to track and how the function is called.

Const logger = vi.fn()

GenerateReport(logger)

Expect(logger).tobeCalled()

Mocks

We can mock the 3rd party functions and make it not to call them. Instead call our own method to provide the expected output that comes out of it.

Can have custom method to be executed instead of the original call to the api.

are replacement for an api that may provide some test specific behaviour instead.

Custom replacement code can be placed under **mocks**

Code specific:

In Jest the jest.mock should be wriiten on the top

In vitest vi.mock that will be automatically hoisted to the top

Vi.stubGlobal('fetch')

you can mock that library as you learned in the previous section (i.e., use vi.mock('axios'), provide a **mocks**/axios.js file if necessary etc.).

Can consider using mockImplementation, mockImplementationonce

Side effects to avoid we can use spies and mocks

### Notes

.toBe vs .toEqual
toEqual does deep comparison ({} == {}) true

toBe checks the shllow ({} == {}) false // it checks the memory location of the object hence it will be different

Asynchronous callback
Use done in the argument of the it method and use it after the expect(assertion)

done()

Returning Promises In Tests
Even though the test worked as expected in the previous lecture, you should actually return the promise assertion in your tests:

it('should generate a token value', () => {

const testUserEmail = 'test@test.com';

return expect(generateTokenPromise(testUserEmail)).resolves.toBeDefined();

});

This guarantees that Vitest / Jest wait for the promise to be resolved.

You don't need to return when using async / await (since a function annotated with async returns a promise implicitly

### Unit Testing

Smallest building block

Eg function, class, component

App- combination of building blocks

Every building block is tested standalone

Quickly spot the failure

Why unit testing

Code changes are tested against all scenarios instantly

Write cleaner and better code

Avoids endless amount of manual testing

### Integration Testing

Test of combination of building blocks

Verify if the building blocks are work together

Spotting the exact the issue can be tricky

### End to End Testing

Test the entire flows and and the application features

Test the actual things users would do

### Test Driven Development

Write failing test first and then implement the code to make the test succeed

Project setup

Testing setup can be integrated along with the project setup

Based on webpack, vite

### Writing good tests

Good tests are short and concise

Advanced testing concepts

Mocks & spies

### Testing The DOM

Accessing the DOM from inside Tests

Testing of the testcases can be done in many environments nodejs, jsdom, happydom

Nodejs environment will not have dom packages

To write complex testcases which is dom specific we can use testing library

## Best Practises

use AAA principle
Don’t hardcode

Use the constants and set the value in the beginning of the test

use the variable during assertion

Try to derive the expected value also(instead of just hardcoding)

Should not have only one test
Should also get different value when incorrect value is passed

Only test one thing

Keep the assertions as low as possible(count= 1)

Test one behaviour in one test

Only test your code and don’t test any 3rd party code and don’t test any dom methods, and test any nodejs packages
For testing api we need to test different responses and errors
Split or refactor the big function to simple individual simple function which does a single job
Function which does a single task or a job goes in unit testing . Function which contains multiple functions called inside then it goes inside integration testing category
To test a function which throws error
Const cleanFn=()=> cleanNumbers(values)

Expect(cleanFn).toThrow()
