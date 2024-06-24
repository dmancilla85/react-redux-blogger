# Redux Essentials Tutorial Example

This project contains the setup and code from the "Redux Essentials" tutorial in the Redux docs ( https://redux.js.org/tutorials/essentials/part-1-overview-concepts ).

The `master` branch has a single commit that already has the initial project configuration in place. You can use this to follow along with the instructions from the tutorial.

The `tutorial-steps` branch has the actual code commits from the tutorial. You can look at these to see how the official tutorial actually implements each piece of functionality along the way.

This project was bootstrapped with [Vite](https://vitejs.dev/), and is based on the [official Redux Toolkit + Vite template](https://github.com/reduxjs/redux-templates/tree/master/packages/vite-template-redux).

## Available Scripts

In the project directory, you can run:

### `yarn dev`

Runs the app in the development mode.<br />
Open [http://localhost:4173](http://localhost:4173) to view it in the browser.

The page will reload if you make edits.<br />

### `yarn build`

Builds the app for production to the `dist` folder.<br />
It correctly bundles React in production mode and optimizes the build for the best performance.

## Learn More

You can learn more about building and deploying in the [Vite docs](https://vitejs.dev/).

To learn React, check out the [React documentation](https://react.dev).

## RTK Query: Comparing Transformation Approaches
We've now seen three different ways that we can manage transforming responses:

* Keep original response in cache, read full result in component and derive values
* Keep original response in cache, read derived result with selectFromResult
* Transform response before storing in cache

Each of these approaches can be useful in different situations. Here's some suggestions for when you should consider using them:

* transformResponse: all consumers of the endpoint want a specific format, such as normalizing the response to enable faster lookups by ID
* selectFromResult: some consumers of the endpoint only need partial data, such as a filtered list
* per-component / useMemo: when only some specific components need to transform the cached data