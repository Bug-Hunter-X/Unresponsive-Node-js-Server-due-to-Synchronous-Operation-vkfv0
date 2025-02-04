# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in a request handler blocks the event loop, making the server unresponsive.  The `bug.js` file contains the problematic code. The `bugSolution.js` provides a solution using asynchronous operations.

## Bug

The server simulates a long-running task (5 seconds) using a `while` loop inside the request handler. This blocks the event loop, preventing the server from handling other requests.

## Solution

The solution involves using asynchronous operations to avoid blocking the event loop.  This example uses `setTimeout` to simulate a long-running task asynchronously.  For real-world applications, you'll likely use other asynchronous methods such as database interactions or API calls.

## How to run

1. Clone the repository.
2. Navigate to the repository directory.
3. Run `node bug.js` to observe the unresponsive server. 
4. Run `node bugSolution.js` to see the corrected asynchronous version.