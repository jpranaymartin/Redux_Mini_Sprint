### Redux Mini Sprint

This sprint is intended to familiraze yourself with the Redux workflow before modularization and before connecting it with React in Recast.ly-Redux

navigate to ./src/store.js

All of your work can be done in this file; however, it will also be useful to explore App.js and index.js to see how React and Redux connect with one another.

### Actions and Action Creators

Actions are objects that must always have a type property and will often have a payload property containing data. Action creators can be synchronous or asynchronous functions that eventually deliver the data to the store. Our application will contain 2 action creators which will eventually result in 3 unique sets of data in our store.

Start by filling in a type for the first provided "studentActionCreator". Types are always strings and the naming convention is to use "ALL_CAPS_SEPARATED_BY_UNDERSCORES".

Write a second action creator, playListActionCreator, which will return an object with an artist and songTitle property.

### Reducers

Under the hood, reducers receive the action objects delivered by action creators as an argument; however, you will not directly provide this argument. Redux will take care of this and we will write the function to handle the incoming objects.

Action types are available to all reducers so that they can all be handled as needed, which is why we need a switch statement.

Write a playListReducer so that it returns an array containing all song objects created by the playList action creator.

### Root Reducer

Add the studentsReducer with property name 'students' and playListReducer with property name 'playList' to the rootReducer. Notice that the function 'combineReducers' is imported from redux.
The properties of the object argument inside this function directly reflect the properties maintained in your store (an object that holds the somplete state of our application). At this point, we still have not shipped any data to our store or even created our actual store. We have only set up our Redux flow to ship data to the store.

### Store

The createStore function is imported from Redux. For our purposes createStore takes two arguments:
our root reducer and a preloaded, initial state.
