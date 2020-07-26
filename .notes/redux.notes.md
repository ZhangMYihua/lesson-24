redux pretty much this.state
redux replaces this.state and has it happen in redux library

doesnt completely replace this.state can and will be used together

https://www.npmjs.com/package/react-redux
https://www.npmjs.com/package/redux
https://www.npmjs.com/package/redux-logger

used to avoid prop drilling able to access user and props from one location

<h1 redux flow></h1>

*Action*-gos to reducer, action can hit middle ware before hitting reducer
        clicking on button
*Middleware*- what it does with action is entirely up to middleware
    redux-logger-middleware-logs action that get fired before and after action
*Root Reducer*- propagates changes and gos to store
    function that recieves an input which is an action and creates an output(state or store in redux)
*Store* - results in dom changes in right components store gets updated {state/store of app}
    <react notices state change and makes changes to the view layer>

**Dom Changes**-view layer
<p ActionMiddleWare></p><p RootReducer></p><p Store></p><p React></p><p DomChanges></p>

**Flux Pattern Flow  vs MVC**(action-controller-model-view)
VVVVVVVVVVVVVVVVV
unidirectional data flow
solve problems in logical sense and organized fashion
<Action>
V
<Dispatcher>- dispatches action to store
V
<Store>- updates view
V
<View>

1. components have props and fire actions 

2. actions update state in Reducer
    fore example and state regarding User would be in a User reducer
    and state regarding home would be in Home reducer
    and state regarding shop would be in the shop reducer

3. all of these reducers would live in one state object called the Root Reducer

4. the root reducer will give this information to components as props as they need to display in order for our components to function.


**user flow**

--reducer is an object
--root reducer is a big abject that holds all reducers
--reducers will be seperated by component
--together will be combined in the root reducer

--actions are objects
    {
        type: string
        payload: any
    }

1. actions go to reducers
        *Middleware*- what it does with action is entirely up to middleware
                    redux-logger-middleware-logs action that get fired before and after action
2. reducers check that type of action and if its aplicable to that reducer,
   1.  if we want to update the user only the user reducer cares about that option the other    reducers arent going to care and they will know because of the action.type prop, and will set the user with action.payload

3. than User Reducer passes that into component as a Prop to the component

    --Reducers 
        --are function that take in a state and an action
        --the state is the previous state that it was in or current state
        --propery equal to pay action.payload

