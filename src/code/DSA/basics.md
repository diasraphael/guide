What is a good code, how do we say that it is good code?

1. readable
2. scalable(how we can say it is scalable)
   => we can say it through Big O
   => when the input increases how the code behaves
   => we should not calculate based on the time taken since if computer is powerful it takes less time
   => should be based on no of operations it takes to execute the program or code

Datastructure: ways of storing data

Big O - To describe the performance of the algorithm

## How to calculate the code is efficient or which code is efficient

Faster? speed? find it through time complexity big O notation

Memory extensive? find it through space complexity

Readable?

## Omega Notation ( Ω ) vs Big O Notation ( O ) vs Theta Notation ( θ )

What is the mileage that your car gives?

So let's discuss different scenarios.

Let's say the car gives an average of 12 km/hr in Traffic, an average of 20 km/hr on Highway and an average of 16 km/hr in Normal City Traffic.

Traffic is your worst case, Highway is your best case and Normal City Traffic is your average case.

This is similar to the notations that we use for Algorithm runtime Analysis.

Omega Notation ( Ω ) gives the best case complexity (highway in above case), Big O Notation ( O ) gives the worst case complexity (traffic in above case) and Theta Notation ( θ ) gives the average case complexity of an algorithm (normal city traffic in above case).

Storytelling and real life examples make you understand concepts clearly.

### rule book

1. worst case Big(o)
2. remove constants
3. different terms for inputs o(x+y)
4. drop non dominants ie we will consider the most powerful one O(n +n^2) =O(n^2)

### points

1. when we have 2 for loops one below other then it is big O(x+y) and when we have nested for loops then it is big O(n\*n)=O(n^2)if same array, if diff array then O(x\*y)

### Time complexity:

time taken to execute the program

### Space complexity:

space taken to execute the program

## Big O notation:

to analyze the performance of algorithm

To identify the worst case for an algorithm

O(n!) = nesting loop for each input= wont be used much and it is terrible
O(n2) = quadratic time= very slow
O(n) = linear time= n is the no of the inputs = grows proportionally
O(log n) = logarithmic
O(1) = constant time= calculating only once

Omega best case
Theta average case
Big O worst case

O(n2) , O(n), O(1), O(log n)

O(n) is better than O(n2) since it will be executed n times

Drop constants

ie O(2\*n) = O(n)

O(500) =O(1)

O(13n2) = O(n2)

O(n+10) =O(n)

O(n2 + 500 + 8) =O(n2)

O(n2) = n square

O(n3)= n cube

O(n cube) will be treated as O(n2)

O(n square + n) will be treated as O(n square)

### Order of efficient programming

O(1) = constants

O(log n) = logarithmic(as the inputs increase no of times decrease)

O(n) = linear

O(n2) = quadratic

O(2 pow n) = exponential

### Space complexity:

Auxiliary space complexity means the space taken by the algorithm to execute and not the size of the inputs.
variables
data structures
function call
allocation

## Big O notation for objects and arrays

### Objects

Access : O(1)

Searching: O(n)

Pushing and removing O(1)

### Arrays

Pushing and removing in last O(1)

Pushing and removing in the beginning O(n)(shift,unshift)

Access: O(1)

Searching: O(n)

Splice, slice O(n)

Foreach, map, filter, reduce O(n)

## Algorithm

### Set of steps to solve a task(A plan for solving problems)

Understand the problem

1. restate the problem in own words

2. what are the inputs

3. what are the outputs out from the solution

4. do I have enough information to solve the problem

Explore with examples

1. start with simple examples(simple input and output)

2. progress to more complex examples(complex input and output)

3. explore examples with empty inputs

4. explore examples with invalid inputs

Break your code

1. explicitly write out the steps you need to take

2. clarify the doubts

Solve and simplify

1. find the core difficulty in what we are trying to do

2. temporarily ignore that difficulty

3. write a simplified solution

4. then incorporate that difficulty back in.

refactor

1. can you check the result

2. can you derive the result differently

3. can you improve the performance of your solution

4. can you think of other ways to refactor

5. how other people would have solved this problem

### Master common problem solving patterns

### Data-structures

1. how data is stored

### Datastructures

Arrays:

lookup: O(1)
push: O(1)
pop: O(1)
insert: O(n)(unshift)
delete: O(n)(shift)

static arrays: fixed size of the array ahead of time
dynamic arrays: dynamic size of the array

Stacks:
Queues:
Linked Lists:
Trees:
Tries:
Graphs:
Hash Tables:

Algorithms

1. Sorting
2. Dynamic programming
3. BFS + DFS
4. Recursion
