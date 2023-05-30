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

## Notes

1. when you write javascript code within the braces {} in a javascript file you will get autocomplete support and error messages when you have some typing errors

## context

1. alternative to props is context
2. share data and function through context

### sharing data in context

1. create the context

```
import {createContext } from react;
const BooksContext =createContext();
booksContext will have provider(component used to specify what data we want to share) and consumer(component used to get access to data)
```

2. specify the data that will be shared
3. consume the data in a component

4. on top of this booksContext we will create a provider which we will have the object and functions to share so that values and functions can used and modified by other component under the provider

5. useContext: allows a component to access values stored in context.

### Custom Hooks

1. functions we write to make reusable bits of logic
2. can do a lot or very little
3. usually reuse a basic hooks like useState, useEffect

### useCallbacks

1. hook to help you let tell react that your function isnt actually changing over the period of time.
2. fixes bugs around useeffect
