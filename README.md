# ReactReduxDemo

## Install React redux

```command
npm install redux react-redux
```

## Create a new store

[src/store/index.js](src/store/index.js )


## Provide store to the application

[src/index.js ](src/index.js )

```javascript
import { Provider } from 'react-redux';

import store from './store/index';


.....


ReactDOM.render( <Provider store = {store}><App /></Provider> , document.getElementById('root'));

```

## Accessing (Subscribe) or updating (dispatch)

[src/components/Counter.js](src/components/Counter.js)

```javascript

import { useSelector, useDispatch } from 'react-redux';

...

//here we get dispatch hook into constant
const dispatch = useDispatch();

//Here we subscribe only counter state of store data
const counter =  useSelector(state => state.counter);

const incrementHandler = () => {

//we called dispatch action here with type key into dispatch object
    dispatch({type:'increment'})
  };
  

....

// Here we are using subscribed counter state
<div className={classes.value}>{counter}</div>

```
