## History

1. 2011 created by facebook
2. 2016 React 15 was released(previous version was .14)
3. Learn once and write everywhere
4. used in webapps,static sites(gatsby),mobile(react native),desktop apps,server rendered(next.js),virtual reality(react VR)

## Core concepts

1. react renderers: renderer is separate from react itself.react-dom is used to render web components in web apps. react native is used to render components in react native friendly environments, and react vr is used to render components in react vr friendly environments.
2. react uses html in js files(angular and vue uses js in html files)
3. why virtual DOM: updating the DOM is expensive, so react minimizes dom changes
4. react testing library: test react components without browser(used node)
5. react goes with one way binding ie if you change a state value in a input, we will have change handler that will update the state value(angular goes with 2 way binding ie less typing, in a input value field will be associated with the state and changes will be automatically updated by the framework)

## workflow

1. JSX is compiled to js through a build step(transpilers like babel compile jsx to js) and webpack combines individual files to single bundle.js
2. client request the initial html from server and then from the html script tag triggers to request server for the bundle.js file

## React :

1. react :library that defines what a component is and how multiple components work together.
2. reactDOM : library knows how to display a component in browser
3. react only cares about showing content and handling events

## JSX

1. inline styles are provided as objects
2. props are written as camelCase autoFocus,maxLength
3. numbers to be mentioned within curly braces(when using with attributes)
4. boolean with truthy value can be written with the name alone

## Component

1. A function that returns a JSX

## import / exports

1. default exports can be renamed in the importing file
2. named exports cannot be renamed

## Events

1. when we click a button an event handler or callback function is attached to it(in simple terms a normal function is attached to it)
2. make sure you pass a reference to the function instead of calling it. if we call it using handleClick() then when we try load the page initially the function will get called. but when we just give the reference it will be called when we click the button.

```
onClick={handleClick}
instead of
onClick={handleClick()}
```

```
onClick={handleClick}
same as
onClick={()=>{console.log("Dias")}}

```

## state

1. when we update a state using setCount() usestate method then the corresponding component will be rerendered.
2. when the second time the component is rerendered(calling the component again) it wont take the default value instead if will take the updated value.

## http error codes

1. 200: success
2. 201: record was created
3. 204: record was deleted
4. 301: url you made request to has changed
5. 400: request was bad
6. 401: unauthorized
7. 403: forbidden
8. 404: not found
9. 500: internal server error.

## axios request

```
import axios from 'axios'

const searchImages = async(term)=>{
const response = await axios.get(url,{
  headers:{
    Authorization: 'Client-ID kjlnknkkjnklklmklmklmklmklmlklkø'
  },
  params:{
    query: term
  }
})
  return response.data.results;
}
```

## async await

1. await keyword tells js to wait until you receive answer from the backend once received the response is returned back.
2. once await is added async keyword should be added for the method which has await keyword.

## Notes

1. when you write javascript code within the braces {} in a javascript file you will get autocomplete support and error messages when you have some typing errors
2. react developer tools extension in chrome => components tab in F12 to check the values of the components passed.
3. while importing an js file we wont give an extension but other than js files, all other files we need to write the extension while importing.
4. when you update state the component and all of its children are rerendered.
5. while iterating we should not have keys generated by uuid or math.random() they will be generated new for each rerender.good one to have is id from backend.
6. when updating an useState object or array. old value and new value should have different object so that react will update properly.

```
const [obj,setObj] =useState([])
obj.push({title:'new obj'}) // this will update the old empty object then it will point the old object
setObj([...obj,{title:'new obj'}]) // this will create new object then react compares the old empty array reference and new object reference, then it is different then it will rerender and update properly
```

7. inserting elements in middle of the array (spread + slice technique)
8. removing element from an object

```
const obj={
  color: "red",
  age: "35"
}
const {color,...rest}=obj
console.log(rest)  // color is removed from object
```

9. random number generation: Math.round(Math.random() \* 99999)
10. component task(say a function) has to be executed in the component alone.if you need it in another component make a new function in the parent component which calls the existing function and pass the new function to the child component.

11. when updating a book in a list of book objects do this to avoid simultanously changed data by different users.

```

do this

if(book.id === id){
return {...book, ...response.data}
}


instead of

if(book.id === id){
return {...book, title: newTitle}
}

```

### JSON server

1. when using JSON server with react app, our react app will be running in 3000 and server will be running in some other port say 3001, we should hit the api 3001 port running in local.

## Task Notes

1. create a tree diagram as components, find the root component and see what components will the root component have. what all methods will the root component have and how its passed to the child component as event handler. write what each component will do and split the components

## review

1. event handler or callback function or simple function attached to an event(onClick) we can name as handleClick or onClick

## context

1. alternative to props is context
2. share data and function through context

### sharing data in context

1. create the context

```
import {createContext } from react;
const BooksContext =createContext();

booksContext will have  2 component

  1. provider(component used to specify what data we want to share)
  2. consumer(component used to get access to data)

```

2. specify the data that will be shared

```
<BookContext.Provider value={5}>
  <MyComponent>  // will have access to the value shared in the context
</BookContext.Provider>
```

3. consume the data in a component(function for accessing the data)
   ```
    const num = useContext(BookContext)
    return <div>{num}</div>  // 5 will be rendered
   ```
4. on top of this booksContext we will create a provider which we will have the object and functions to share so that values and functions can used and modified by other component under the provider

5. useContext: allows a component to access values stored in context.

6. to pass state values and functions we need to have a provider on top of existing one

```
function BookProvider({children}){
  const [count , setCount] = useState(0);
  const valueToShare={
    count:count,
    incrementCount:()=>{
      setCount(count+1)
    }
  }
  return (
    <BookContext.Provider value={5}>
     {children} // will have access to the value shared in the context
    </BookContext.Provider>
    )
}

</BookProvider>
```

### Custom Hooks

1. functions we write to make reusable bits of logic
2. can do a lot or very little
3. usually reuse a basic hooks like useState, useEffect

### useCallbacks

1. hook to help you let tell react that your function isnt actually changing over the period of time.
2. fixes bugs around useeffect

### useeffect

1. useeffect clean up function triggers before the next time the useeffect function is called.so if we have the dependency array as [] then the clean up function wont be triggered.

### Notes

#### form tag

1. when we have input element and when we wrap it with form tag, and when we type something in input element and press enter, an onsubmit event from form tag will be triggered.

```
<form onSubmit={handleSubmit}>
  <label>Email</label>
  <input type="text" name="email">
</form>
```

2. onclick of enter button onsubmit function will triggered and url will be updated and page gets refreshed
   name attribute with value will be appended in the url(in normal html and js)

```
myapp.com?email=dias@gmail.com
```

3. to avoid this behaviour (page refresh and url value getting appended)

```
const handleSubmit=(event)=>{
  event.preventDefault()   // preventing the form submission
}
```

4. dont get value from an input using document.querySelector('input').value in react

instead, do this react way of getting values from input(we are changing the input from uncontrolled input to controlled input using react state)

```
const [term, setTerm] = useState('')
const handleChange = (event)=>{
  setTerm(event.target.value)
}
<form onSubmit={handleSubmit}>
  <label>Email</label>
  <input value={term} onChange={handleChange}>
</form>
```

### input tag

1. when input text is added in a form always set the value and onChange using usestate values
2. you can just add the button and onClick can be added in onSubmit of the form

```
const handleSubmit=(title)=>{
  event.preventDefault()  // prevent refresh
  onCreate(title)
  setTitle('')  // reseting the input box
}
<form onSubmit={handleSubmit}>
  <label>Title</label>
  <input value={title} onChange={handleChange}>
  <button>Create<button>
</form>

```

2. ECONNREFUSED 127.0.0.1:3001 Errors in VSCode
   "server" : "json-server --port 3001 --watch db.json --host 127.0.0.1"
   Please be sure to restart your JSON server after making this change.

3. rest client can be used as backend server which returns the response we configure with api.http file local