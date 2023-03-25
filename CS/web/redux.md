## redux

action => dispatch function => reducer functions => state

## RTK

1. earlier redux <=> react app is the old style

2. RTK is the wrapper around plain redux

3. redux <=> redux toolkit <=> react app

4. simplifies the action types creation process

## Slices

1. defines some initial state

2. combine mini reducers in to big reducer

3. creates a set of action creator functions

4. slices are what saves us from having to write out all of this boilerplate code

## changing state

1. Add a reducer to one of your slices that changes state in some particular way

2. export the action creator that the slice automatically creates

3. find the component that you want to dispatch from

4. import the action creator function and usedispatch from react-redux

5. call the usedispatch hook to get access to the dispatch function

## Accessing state

1. find the component that needs to access some state

2. import the useSelector hook from react-redux

3. call the hook passing in a selector function

4. use the state, anytime state changes the component will rerender.

## when we have multiple slices and we want to perform an action when another action takes place

1. we can have reducer function in both slices and call both the actions using dispatch but it will be multiple dispatch calls.It will work but its not redux way of doing it

2. we can avoid this using extraReducers where we want to listen to other action when it takes place.but there is a dependency between both the slices.

3. we can avoid this by creating standalone action created using actionCreator from redux toolkit for both slices as common onetime and use extrareducers to listen for that action and return appropriate value.

## create a RTK query api

1. find different kinds of query we need to make and categorize

2. make a new file that will create api
