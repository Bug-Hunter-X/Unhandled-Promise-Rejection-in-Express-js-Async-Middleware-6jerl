# Unhandled Promise Rejection in Express.js Async Middleware

This repository demonstrates a common error in Express.js applications: unhandled promise rejections within asynchronous middleware.  The error is logged to the console, but the client receives no error response.

The `bug.js` file contains the problematic code. The `bugSolution.js` file shows how to fix the issue using proper error handling.

## How to reproduce:

1. Clone this repository.
2. Run `npm install express`.
3. Run `node bug.js`.
4. Refresh the page a few times.  You will notice the server sometimes logs errors, but no error response is sent to the client.

## Solution:

The solution is to always handle promise rejections in your asynchronous middleware.  The `bugSolution.js` file demonstrates this using a `try...catch` block.  This ensures that errors are handled gracefully and that appropriate error responses are sent to the client.
