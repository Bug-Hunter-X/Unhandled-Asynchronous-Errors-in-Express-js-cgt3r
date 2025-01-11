# Unhandled Asynchronous Errors in Express.js

This repository demonstrates a common issue in Node.js Express.js applications: unhandled asynchronous errors during request processing.

The `bug.js` file shows an Express.js application with an asynchronous operation that might throw an error. The error is caught, logged to the console, but the request isn't properly handled, leading to hanging requests.

The `bugSolution.js` file provides a solution using Express.js's error handling middleware to gracefully handle these errors and send an appropriate response to the client.

## How to Reproduce

1. Clone the repository.
2. Run `npm install` to install the dependencies.
3. Run `node bug.js`. Make multiple requests to the server.
4. Observe that roughly half of the requests will hang.
5. Run `node bugSolution.js`.  Observe that all requests are handled properly, and errors are gracefully handled.