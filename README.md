# react-redux-firebase-typscript

Project to start any projects based on front-end stack with:

-   TypeScript
-   React
-   Redux
-   React Router DOM
-   Styled Components
-   Firebase

## Auth state

Auth state is a basic object to control an application's state. Has a few properties:

-   `connected: ConnectionType` -> `true` if firebase gives feedback when is connected with app
-   `logged: LoggedType` -> `true` when `onAuthStateChanged` from `AuthWatcher` returns user object
-   `user: UserType` -> is `null` or truncated firebase user object

## Basic components

### AuthWatcher

This component controls Auth state. If has a flag `showState` then it renders a table of Auth state.

### ConnectedRout

This component redirect to "/" if `connected === false`.

### PrivateRoute

This component redirect to "/sign-in" if `connected === true` and `logged === false`.

### SwitchGroup and View

These components are prepared for adding a transition animation between pages. Recommended `Framer motion`.

## Helpers

### storageAPI

An API to better handling localStorage. It adds a prefix into a passed localStorage key.

### getCssVar

This function returns a value of specific CSS variable.

### sortHelper

This function handles sorting objects by specific params. The type of a param value can be `string` or `number`.

### convertTimestamp

Conver an firebase `Timestamp` object into simple microtimestamp.

### transformFirebaseDate

Transform Firebase Date inside a specific object into `number`, microtimestamp.

## Types

### routingPaths

A two type of paths for better controlling routing. These paths are:

-   `connectedPaths`
-   `privatePaths`
