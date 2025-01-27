# Unresponsive Node.js Server: Synchronous Long-Running Task

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in a request handler can cause the server to become unresponsive.  The provided `bug.js` file showcases this problem, and `bugSolution.js` offers a solution using asynchronous programming.

## Problem

Node.js is single-threaded.  A synchronous operation that takes a long time (like a complex calculation or I/O operation) will block the main thread, preventing the server from handling other requests. This leads to an unresponsive server and poor user experience.

## Solution

The solution involves using asynchronous techniques to avoid blocking the main thread.  This allows the server to continue processing other requests while the long-running task executes in the background.