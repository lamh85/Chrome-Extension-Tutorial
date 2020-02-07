# Google's Documentation

Getting Started:
https://developer.chrome.com/extensions/getstarted

Architecture:
https://developer.chrome.com/extensions/overview

# Custom Architecture

## General

```
View <---> Controller <---> Model
```

## Comparisons

Helpful command:
```bash
tree -L 3 -d -I 'node_modules'
```

Rails
* View
* Serializer
* Controller
  * Concern
* External APIs. EG:
  * Marketing apps
  * Stripe
  * Microservices. EG: product pipeline
* Queries
* Workers
* Model
  * Validator
  * Concern
  * Decorator

Redux
* Components
* Containers
* Actions
* Reducers

Common to Both Rails and Redux:
* Helpers
* Constants
* Initializers
  * Config
* Tests
* Dependencies
* Transpiler: webpack, gulp, etc.
* Routes

Logic in Helium 10 Chrome Extension that needs cleaning

* Manifest
* Chrome API
  * Message sending
  * Message listening
  * Querying the tab
  * GET local storage
  * SET local storage
  * Prompt for permissions
* Options page
* Redux library for extensions
* Refreshing the page
* Using jQuery to parse HTML
* Manipulate DOM and click elements
* Different Amazon pages calling the API, and paassing different arguments.
* Helpers: number, array, string, pagination

NOTE - Finished looking at these files:
* `background.js`


## Common Reasons for Abstractions

* Different levels of abstraction. EG: serialized data VS database data
* Different parts of the flow. EG: querying the data VS serializing the data
* Makes the flow asynchronous. EG: workers
* Applicable to different levels of abstraction. EG: tests, helpers, constants, config
* Too much logic that can be grouped to a few general responsibilities. EG: presentational components VS containers
* Conceptualizes the app as a whole. EG: initializers, tests, git ignore, infrastructure logic, transpilers, etc.