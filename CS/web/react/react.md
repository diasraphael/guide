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
