# Javascript

1. high level language = need memory to store variable, in high level language it will be done automatically
   in low level language like c the developer need to manage resource manually.(memory management will be done under the hood)
2. multi paradigm (approach and mindset of structuring code which will direct your coding style and technique)
   procedural, object oriented programming, functional programming
3. object oriented (based on objects, for storing most kinds of data)
4. garbage collected(garbage will be collected automatically)
5. javascript is interpreted or just in time compile.code is converted to machine code 0s and 1s.this step is called compiling or interpreting.this is done in javascript engine.
6. prototype based object oriented
7. first class functions, functions are simply treated as variables.we can pass them into other functions and return them from functions.
8. dynamically typed.
9. single threaded
10. non blocking event loop: handles multiple task at same time. javascript runs in one single thread.so it can only do one thing at a time.so how do we achieve multiple task at a time. answer is event loop. even loop takes long running tasks and executes them in the background. and puts them in the main thread once they are finished.

### Releases

Brendan Eich creates Javascript initially called mocha in 10days in 1995  
mocha changed to livescript in 1996  
1997 Ecmascript 1: first official standard for javascript  
2009 Ecmascript 5: released with lot of new features  
ES2015/ES6: biggest update to the language ever  
Ecmascript changes to annual release cycle inorder to ship less features per upgrade

ES5  
ES2015/ES6  
ES2016/ES7  
...  
ES2020/ES11

#### JS engine

1. program that executes javascript code.
2. v8 in chrome, nodejs
3. js engine has call stack, heap
4. call stack is where the code is executed
5. heap is where the objects are stored.
6. code is parsed and then it is compiled and then it is executed.execution happens in call stack.
   ![js runtime image](./images/jsruntime.png)
7. execution context: global execution context is created. javascript is executed in the execution context.first top level code will be declared eg: variable declaration, functions.after that execution of functions and callback are excuted when event loop tells which one to execute.
8. there are global scope, function scope, block scope.

#### compilation vs Interpretation

compilation: entire code is converted into machine code at once and written to binary file that can be executed by a computer.

Interpretation: runs through the source code and executes it line by line.

Just in time compilation: entire code is converted into machine code at once then executed immediately.

#### imperative vs declarative

1. imperative: how to do things
2. we explain the computer each and every step what to do achieve a result
3. declarative: programmer tells what to do
4. we simply tells the way the computer should achieve the result

#### functional programming

1. declarative programming paradigm
2. combining many pure functions avoiding side effects and mutating data
3. side effect: modification(mutate) of any data outside of the function(mutating external variables, logging to the console, writing to DOM)
4. pure functions: functions without side effects, does not depend on external variables. given the same input always return the same outputs.
5. immutatiblity: state is never modified, instead state is copied and the copy is mutated and returned.
6. use array and object destructuring
7. use spread operator
8. use ternary operator

#### MVC architecture

1. like house we need a structure, the way we organise our code.
2. we need to be able to easily change it in the future.(maintainability)
3. we need to able to add new features
4. components of any architecture business logic, state, http library, application router,presentation logic
5. mvc: model, view, controller

#### paradigm

style of code, how we organize and write our code. to avoid spagetti code we have introduced different paradigms such as oop and functional programming.

1. OOP:we use objects to model real world objects.objects are self contained block of code. by using objects we pack data and the corresponding behaviour into one block.
2. abstraction:Ignoring and hiding the details that dont matter.
3. encapsulation:keeping properties and methods private inside the class so that they are not accessible outside the class. some methods can be exposed as a public interface.
4. Inheritance: making methods and properties available to child class using inheritance. this allows as to reuse common logic.
5. Polymorphism: child class can overrite a method inherited from the parent class

#### OOP in Javascript: prototypes

1. objects are linked to prototype object.
2. prototypal inheritance / delegation: The prototype contains methods that are accessible to all objects that are linked to that prototype.
3. behaviour is delegated to the linked prototype object.
4. when we create object ,we should not add the function to object instead add it like Person.prototype.calcAge=function(){console.log('hello')}. this way the calcAge function is not added as many times an object is created. to avoid copies we add it to the prototype.hasOwnProperty is to check whether the properties or methods are part of the own object.

5. we can add new customised method to builtin methods(eg) Array.prototype.unique = function(){}

#### how do we create prototypes? how do we link object to prototype? how can we create new objects without having classes

1. constructor functions: technique to create objects from function. this is how builtin objects like arrays and maps and sets are actually implemented.

2. ES6 Classes: alternative to constructor functions.ES6 classes work exactly like constructor functions but ES6 classes do not behave exactly like classical OOP. when we add a function within a class it will automatically added to prototype. classes are first class citizens that means we can pass the class as a variable.classes are executed in strict mode.getters and setters are not called with getLatest() instead called as getLatest.

private fields will be starting with #  
protected fields will be starting with underscore  
we can also chain the methods in classes by returning this from every method.

3. object.create is the straight forward way of linking an object to prototype object.
   const PersonProto = {
   calcAge: function(){
   return 'Dias'
   }
   }

   const steven = Object.create(PersonProto) // calcAge will be added to the prototype

#### Backward compatibility:

code written in 1997 put in new browser will work  
old features are never removed  
javascript supports backward compatibility

#### forward compatibility:

code written in ES2089 will not work in current browser.  
In production we can use transpilers and polyfilling to support old browsers  
ES5 is support in all browsers eg: works in IE11  
javascript dont support forward compatibility

#### hoisting

variables are lifted to the top of their scope.function declarations are hoisted.var is hoisted .let and const are not hoisted.function expression are hoisted depends on whether it is declared with ler or var.

#### temporal dead zone

accessing variables before declaration is bad practise and should be avoided.

#### Dynamic typing:

we do not manually define type of the value, instead datatypes are determined automatically in javascript.

#### let,var,const

we cannot reassign using const,using let we can reassign.

var allows adding variables without adding var keyword.(notrecommended)

#### Type conversion and coercion

Type conversion: manually converting from one type to another.

coercion: javascript converts the type automatically from one type to another.

Number('Dias') // returns NaN

#### falsy values

0, '', undefined, null, NaN

#### == vs ===

=== will check the type and the value(will not perform coercion).prefer always this operator.
== will perform coercion and checks the value

#### nullish coalescing operator ??

```
const value = 0;
const guest =value ?? 10; // ?? check for null and undefined only
console.log(guest) // prints 0

const value = 0;
const guest =value || 10; // ?? check for truthy value
console.log(guest) // prints 10

guest ??= 10  // this is also possible
```

#### optional chaining

console.log(restaurant.openinghours?.mon?.open)
console.log(restaurant.order?.(0,1) ?? 'method does not exist') //calling methods

#### use strict

it has to be the first line of the code.  
it forbids to introduce new errors.  
it creates visible errors on the developer console otherwise it will fail silently.

#### for of loop

```
for (const item of items)
   console.log(item)

for (const [i,element] of items.entries())
   console.log(`${i}: ${element}`)
```

#### functions

1. function declaration:

```
const value = calculate(5) // works
function calculate(value){
return value;
}
```

we can call the function before the function definition.

2. function expression:

```
const value = calculate(5) // does not work
const calulate = function (value){
return value;
}
```

we cannot call the function before the function definition.

3. arrow function:

```
const calculate = (value)=>value
```

this keyword is not available in arrow function

4. first class

a. first class means functions are simply values(store functions in variables)
b. functions are just another type of object(pass functions as arguments to other functions and return functions from functions)
c. call methods on functions(bind)

5. higher order function

a. function that receives another function as an argument that returns a new function or both.

```
 btnclose.addEventListener('click', greet) // addEventListener is an higher order function and greet as callback function.
```

b. function returning another function

```
function count(){  // higher order function
let counter = 0;
return function(){  // returned function
counter ++;
}
}
```

6. call, apply, bind methods

a. call method is used point to the current this object

7. IIFE(immediately invoked function expression)

```
(function (){
console.log('Hello')
})()

(()=>console.log('HELLO'))()
```

8. Closures

a. A function has access to the variable environment of the execution context in which it was created.
b. closure gives a function access to all the variables of its parent function even after the parent function has returned.
c. closure makes sure that a function doesnt loose connection to variables that existed at the functions birth place.

#### Arrays

push method returns the length of the array

```
const arrayName = ['Raphael']
const length = arrayName.push('Dias') // 2
```

pop method returns the deleted element

```
const deletedElement = arrayName.pop('Raphael') // Raphael
```

includes method returns whether the element exist in the array or not

indexOf method returns index of the element where it is present
const arr = ['a', 'b' ,'c' ,'d', 'e']

1. slice method array.slice(2) // returns a new array with the elements ['c' ,'d', 'e']

2. splice method modifies the original array.

3. reverse method modifies the original array.

4. at method returns the value using the index value

### forEach and for of

#### Objects

Accessing dynamic value

```
obj ={
firstName:'Dias',
lastName:'Raphael',
birthYear: 1988,
calcAge: function(){
return currentYear - this.birthYear;
}
}

const namekey = 'Name'

console.log(obj['first'+nameKey])
console.log(obj['calcAge']())  // calling method using bracket syntax

Object.keys(obj) will give ['firstName','lastName','birthYear']
Object.values(obj) will give ['Dias','Raphael','1988']
Object.entries(obj) will give [key,value]
```

#### sets

1. will contain unique values
2. has,add,delete,for of to print the values,size

#### maps

1. keys can be of any type but in object it can be only string that is the big difference between object and map
2. set() method to add new element in map
3. get(key) to retrieve the corresponding element
4. has method to check if the element exist
5. size to get length
6. alternate for set
7. to iterate use for(const [key, value] of question)

```
const map= new Map([['question','what is your name'],['1','java']])
```

#### when to use maps vs object and arrays vs set

1. arrays - when we need ordered data and can be duplicates
2. sets - when data is unique

3. objects -when you use strings as keys, when you need function within object, when you need to convert to json
4. maps -can use any type as keys, simply need to map key and values

#### strings

methods: indexOf, slice, lastIndexOf, toLowerCase, toUpperCase, trim(), replace(used to replace currency to another currency, comma to dot), includes(), startsWith(), endsWith(), split(), join(), padStart(to mask number to \*)

#### DOM

1. DOM is the complete representation of the HTML page we write
2. we can modify the html structure using document object
3. DOM methods and properties not part of javascript instead they are the apis of browsers
4. timers, fetch api is also from browser apis
5. dom manipulation methods innerHtml,insertAdjacentHTMLElements(check the name)
6. In DOM there are different types of nodes.some are html elements and some are just text.every single type of element is a node and each node represent a javascript object.
7. An element type has internally an HTML element(HTMLButtonElement, HTMLDivElement) child type.

#### Data Transformations(direction towards functional programming(using the below methods))

1. map - similar to foreach(modifies the original array) but returns new array
2. filter - returns a new filtered array
3. reduce - reduce all array elements down to a single value(adding all elements together)
4. find - method finds the first element which satisfies the condition
5. findIndex- method returns the corresponding index of the array
6. some -
7. every - every element in the array satisfies the condition then returns true
8. flat - this will help to flat the nested array within a array(it goes 1 level deep ie flat(1))
9. flatmap - flat + map (always does 1 level deep)
10. fill - method used to fill the array with numbers(Array.from({length:7},()=>1) also used for this purpose)

#### sorting

1. sort method will help you to sort the strings
2. to sort the number pass the callback function to sort it based on asc or desc

#### copying objects using Object.assign({},obj)

object.assign will do a shallow copy of the object

```
let obj = {
firstName: 'Dias',
lastName: 'raphael',
friends:['x','y','z']
}
let newObj = Object.assign({},obj)
newObj.firstName = 'anie';
console.log(obj) // will print an obj with firstname as Dias
console.log(newObj)  // will print an obj with firstname as anie
newObj.friends.push('ac')
console.log(obj) // will print an obj with friends as ['x','y','z', 'ac'] , both will point to the same updated object
console.log(newObj)  // will print an obj with firstname as ['x','y','z', 'ac'v]
```

to avoid this we need to do a deep copy which is not easy.TODO to know more

#### Destructuring arrays

1. unpacking of elements and original array is not modified

```
   const [a,b,c] = [1,2,3]
   console.log(a,b,c) // prints 1 2 3

   let [main, , secondary] = ['apple', 'banana', 'mango']
   console.log(main, secondary)

```

2. switching between variables

```
   const temp = main;
   main = secondary;
   secondary = main; // old way

[main, secondary] =[secondary, main] // new way to switching values without temproary variable
```

3. return 2 values from the function

```
   function result(){
   return [1, 2]
   }
   const [main, secondary] = result()
   console.log(main, secondary) // prints 1, 2
```

#### Destructuring objects

```
const restaurant ={
name: 'cook with comali',
openinghours: 'friday'
}
```

const {name, openingHours} = restaurant;

1. renaming
   `const {name: restaurantName, openingHours: hours}= restaurant`
2. default values
   `const {name: restaurantName = 'KFC', openingHours: hours = '9am'}= restaurant`

#### spread operator

to unpack the elements and it will be on the right side of the =(assignment operator)

1. copy arrays( shallow copy the elements just like assign())

```
   const a = [1,2]
   const b = [3,4]
   const c = [...a]
   console.log(c)  // prints [1, 2]

```

2. Join 2 arrays

```
   const a = [1,2]
   const b = [3,4]

   const c = [...a, ...b]
   console.log(c)  // prints [1,2,3,4]
```

#### rest operator

to pack the elements and it will be on the left side of the =(assignment operator). and rest element must be the last.

```
function add(...numbers){
console.log(numbers.length) // 6
}
add(1,1,4,3,4,6);

```

#### Numbers

1. Number('23') // will convert to number 23
2. console.log(+'23') will convert to number 23
3. to check if a value is number use Number.isFinite()
4. to check if a value is integer use Number.isInteger()
5. toFixed() will always return string
6. math.round() returns rounded value for eg 23.6 will give 24
7. math.ceil() returns rounded value for eg 23.6 will give 24
8. math.floor() returns rounded value for eg 23.6 will give 23
9. const a =783456349856n // to represent numbers in bigInt

#### numeric separators

const num = 98*237_098_237_489 // we can use * to separate the numbers

#### Dates

Z in the date means coordinated universal time without any time zone in london without any day light savings

```
const date = new Date();
console.log(date.toISOString())
```

To get the timestamp

```
console.log(date.getTime())
```

To display date like day/month/year

```
const now = new Date();
const day = `${now.getDate()}`.padStart(2,0);
const month = `${now.getMonth() + 1}`.padStart(2,0); // +1 due to month starts from 0
const year = now.getFullYear();
const hour = now.getHours();
const min = now.getMinutes();

labeldate.textContent =`${day}/${month}/${year}, ${hour}:${minutes}`
```

#### Internationalization

```
const now = new Date();
const options={
hour: 'numeric',
minute: 'numeric',
day: 'numeric',
month: 'long',
year:'numeric',
weekday: 'long'
}

const local = navigator.language;  // or
const localCopy = 'en-US'  // or

labelDate.textContent = new Intl.DateTimeFormat(local,options).format(now)
```

#### events && event handlers

mouseEvent

#### Bubbling & capturing

In the capturing phase the click traverses from the parent element to the target element. it does not goes through sibling

In the bubbling phase, the event then traverse back to the root element. when you dont want the event to bubble up in their parent element we can use e.stopPropagation

#### event delegation

1. add event listener to the common parent
2. determine from what element originated the event
3. can be used in nav bar click implementation where there are many links and to avoid performance issues by not to add as many event listeners to all the links available.

```
document.querySelector('.nav__links').addEventListener('click',function(e){
e.preventDefault();
if(e.target.classList.contains('nav__link)){
const id=e.target.getAttribute('href');
document.querySelector(id).scrollIntoView({behaviour: 'smooth'})
}
})
```

#### lifecycle DOM Events

1. DOMContentLoaded: when all the scripts and styles are loaded this will be executed but it wont wait for images and fonts to get loaded
2. this is not needed in regular javascript since script.js file will be present in the bottom so all the DOM content will be loaded before th script js is loaded.
3. load : when all script, styles, images, fonts are loaded this will be executed
4. beforeUnload: when user leaves the page this will be fired

#### Regular vs async vs defer

1. regular: scripts are fetched and executed after the HTML is completely parsed.
2. async : scripts are asynchronously and executed immediately.DOMContentLoaded does not wait for the async scripts.
3. defer: scripts are fetched asynchronously and executed after the HTML is completely parsed.DOMContentLoaded event fires after defer script is executed. scripts are executed in order

### Asynchronous Javascript

1. synchronous code: code executed line by line
2. each lines wait for the previous lines to finish(eg:alert)
3. asynchronous code: is executed after a task that runs in the background is finished.
4. asynchronous code is non blocking
5. execution does not wait for the asynchronous task to finish its work

### AJAX

1. Asynchronous Javascript and XML: allows to communicate with remote web servers in an asynchronous way.
2. with ajax calls we can request data from web servers dynamically.
3. json data we get from api calls is json text string.to convert from json text to javascript object we need to use JSON.parse(jsontext)
4. default port no for https = 443
5. default port no for http = 80
6. 404 means page not found

#### Callback hell

when we have nested callbacks in order to execute asynchronous task in sequence.it will become more hard to maintain.In order to avoid this we move to promise.

#### promise

when we call a fetch api we will store it in a variable which will have a promise instead of a value.The promise is an object that is used as a placeholder for the future result of an asynchronous operation.A container for asynchronously delivered value.A container for future value. Instead of nesting callbacks we can chain promises for a sequence of asynchronous operations, escaping callback hells.Its an es6 feature(ES2015)

#### promise lifecycle

1. before the future value its pending
2. once asynchronous task is completed the state is settled(fullfilled,rejected)
3. once fullfilled we will get the response. response data will be a promise so we need to use response.json() and in the next then() we can get the actual value.
4. using the then() method we can chain multiple asynchronous sequentially.
5. important thing to remember in promise is there will be one level of chaining

```
const getCountryData = function(){
fetch()
.then(response=>response.json(),error=>alert(error))
.then(data=>{
   return fetch(using data of previous result);  // correct
   fetch(using data of previous result).then(response=>response.json()) // incorrect returning to old callback hell ie nesting  method within the then method
})
.then(response=>response.json(),error=>alert(error))//Instead of having error block in all then blocks we can have catch block in the end to handle error.
.then(data)
}
```

6. instead of having error block in all the then block we can have a catch block at the end.
7. it has a finally block which will be inserted.
8. throw new error will throw the error and the block which has the catch or error handler will handle the error.

#### Asynchronous behind the scenes: The event loop

1. in javascript there is not multitasking, it is single threaded
2. it can do one thing at a time.
3. java can do more than one task at a time but not javascript
4. event loop takes callback from the callback queue and puts in call stack and from there it gets executed.
5. how does javascript execute asynchronous non blocking code? image load, timer , ajax call all gets executed in web api environment.it does not get executed in the call stack and not in the main thread.
6. event loop does the entire orchestration of the javascript engine.moving the code from callback queue to call stack.
7. promise works a little bit different, fetch call gets executed in the call stack and it then waits in the web api environment and once response is recieved its not moved to callback queue instead its put in the micro tasks queue.its a priority queue. the tasks in the priority queue is executed atonce so it will be moved back to call stack to continue execution.

#### Async await

1. syntactic sugar over the promises
2. use try/catch with async await
3. await can be used without async from 2022, when used as the top level code, it blocks the entire module in a synchronous manner.(it works in script type = module)

```
(async function(){
try{
const city = await whereamI()
console.log(`${city}`)
}catch(err){
console.log(err.message)
}
})
```

```
const data = await Promise.all([fetch(),fetch(),fetch()]) // parallel calls
```

3. promise.all will short circuit when one of the api got rejected
4. promise.race will resolve once any of the promise got resolved
5. promise.settled will not short circuit it returns all the fullfilled and rejected response
6. promise.any

### Modern javascript development

1. the code is splitted into separate modules
2. and this separate modules are bundled into a single file(done by webpack or parcel)
3. and this single file is transpiled and polyfilled using babel to be usable by the browser

#### Module

1. resusable piece of code that encapsulates implementation details
2. usually a standalone file but it doesnt have to be.
3. modules naturally lead to a more organised codebase.
4. modules allows us to easily reuse the same code even across multiple projects
5. modules can developed in isolation without thinking about the entire codebase.
6. es6 modules are scoped to module
7. script- top level variables are global
8. default strict mode for esmodule
9. import and export in es6 modules
10. <script type= module></script> in es6

#### commonjs module

1. using require to import modules

#### polyfilling

1. to polyfill array methods we need to import core.js
2. to polyfill async functions we need to import regenerator runtime js

## Notes:

1. Javascript can be used in the web servers(run outside of browsers eg: nodejs)
2. Javascript can be used in the native mobile applications(ionic, react)
3. Javascript can be used in the native desktop applications(electron)
4. instead of multiple if else block we can include switch so we can avoid multiple conditions and switch will be much more clear.
5. function should always receive an argument and should not work on the global value
6. use early return
7. use ternary instead of if
8. use multiple if instead of if else
9. use array methods instead of for loop

## links

1. https://github.com/jonasschmedtmann/complete-javascript-course

## Techniques

#### Smooth Scrolling

```
const btn =document.querySelector('.btn');
const section1 =document.querySelector('.section1')
btn.addEventListener('click',function(e){
const coordinates = section1.getBoundingClientRect()

window.scrollTo({
left:coordinates.left +window.pageXOffset,
top:coordinates.top +window.pageYOffset,
behaviour: smooth
})

or

window.scrollIntoView({behaviour :'smooth'})
})
```

#### Scroll event(implementing sticky navigation)

method1:(low performance)

const initialCoordinates = section1.getBoundingClientRect()
window.addEventListener('scroll', function(){
if(window.scrolly> initialCoordinates.top)
nav.classList.add('sticky')
else
nav.classList.remove('sticky')
})

The intersection observer api:

const obsCallback = function(entries, observer){
entries.forEach(entry=>{
console.log(entry)
})
}

const obsOption = {
root: null,
threshold:[0,0.2]
}
const observer = new IntersectionObserver(obsCallback,obsOptions);
observer.observe(section1)

#### revealing elements on scroll

.section-hidden{
opacity: 0;
transform:translateY(8rem);
}

1. reveal section

```
   const allSections = document.querySelectorAll('.section')
   const revealSection =function(entries, observer){
   const [entry] =entries
   if(!entry.intersecting)
   return
   entry.target.classList.remove('section-hidden')

   observer.unobserve(entry.target)
   }
   const sectionObserver = new IntersectionObserver(revealSection, {
   root: null,
   threshold: .15
   })
   allSections.forEach(function(section){
   sectionObserver.observe(section)
   section.classList.add('section-hidden')
   })
```

#### lazy loading with observer api

```
const imgTargets = document.querySelectorAll('img[data-src]');

const loadImg =function (entries, observer){
const [entry] =entries

if(!entry.isIntersecting)
return

entry.target.src = entry.target.dataset.src

entry.target.addEventListener('load', function(){
entry.target.classList.remove('lazy-img')
})

observer.unobserve(entry.target)
}

const imgObserver = new IntersectionObserver(loadImg, {root: null,threshold: 0, rootMargin: 200px})
imgTargets.forEach(img=>imgObserver.observe(img))
```

## points to remember

1. JavaScript clearly has the ability to manipulate page elements and do calculations on-the-fly.
   We could use this to create an environment which behaves extensibility. However, it considered bad mo-jo to handle page layout with JavaScript.
   I agree with this in general, but I do believe you can use JavaScript in this way as long you do so unobtrusively and take care to ensure the page will fall back to a usable layout with JavaScript disabled.
