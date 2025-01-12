# Silent Promise Rejection in React Native Fetch

This example demonstrates a common issue in React Native applications: unhandled promise rejections during asynchronous operations, specifically with `fetch`.  The application fetches data from an API but lacks proper error handling for failed requests, resulting in silent failures.  The solution adds comprehensive error handling to catch and report these rejections.

## Bug
The `bug.js` file shows the flawed code, where a network error or any rejection during `fetch` won't trigger an error in the UI or the console (unless you're using a debugger that's actively catching unhandled rejections).  The application will simply show a loading indicator indefinitely. 

## Solution
The `bugSolution.js` file demonstrates the improved error handling using a `try...catch` block within the `useEffect`'s asynchronous function.  It provides the user feedback via UI and also logs the error to the console for debugging purposes.