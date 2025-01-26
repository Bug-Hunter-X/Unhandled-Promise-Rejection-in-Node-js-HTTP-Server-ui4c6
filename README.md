# Unhandled Promise Rejection in Node.js HTTP Server

This repository demonstrates a common error in Node.js: unhandled promise rejections in asynchronous operations within an HTTP server.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides the corrected version.

## Problem

The `bug.js` file showcases a server that performs an asynchronous operation. If this operation fails (throws an error), the server crashes without any graceful error handling. This results in unexpected downtime and makes debugging difficult.

## Solution

The `bugSolution.js` file addresses this by properly handling the potential error within the `.catch` block of the promise.  This prevents crashes and allows for better error logging and recovery.

## How to reproduce

1. Clone this repository
2. Run `node bug.js`
3. Observe the crash after a few seconds.  Then run `node bugSolution.js` to observe the proper handling of the error.