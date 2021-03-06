react-redux-app-container
=========================

## Installation

Install the package:
```
npm install --save react-redux-app-container
```

## Usage

```
// index.js

import React from 'react'
import ReactDOM from 'react-dom'
import { ReactReduxAppContainer } from 'react-redux-app-container'
import createStore from './store'
import App from './App'

const store = createStore()

ReactDOM.render(
    <ReactReduxAppContainer store={store}>
        <App />
    </ReactReduxAppContainer>,
    document.getElementById('root')
)
```

```
// store.js

import { createStore } from 'react-redux-app-container'

export default () => {
    const initialState = {}
    const reducers = {}
    const middlewares = []
    const enhancers = []

    return createStore(initialState, reducers, middlewares, enhancers)
}
```

## Devtools

The [Redux DevTools Extension](https://github.com/zalmoxisus/redux-devtools-extension) is automatically recognized.
