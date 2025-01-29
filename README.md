# Node.js Server Hang

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in a request handler can cause the server to hang.  The event loop is blocked, resulting in unresponsive behavior.

## Bug
The `bug.js` file contains a simple HTTP server with a request handler that performs a computationally intensive loop, effectively halting the server until it completes. 

## Solution
The `bugSolution.js` demonstrates the solution by using asynchronous operations. This offloads the long task from the main thread and keeps the server responsive.

## How to run
1. Clone the repository: `git clone <repo_url>`
2. Navigate to the directory: `cd node-server-hang`
3. Install dependencies (none required in this case)
4. Run the bug example: `node bug.js` (Observe the unresponsive behavior)
5. Run the solution: `node bugSolution.js` (Observe that the server remains responsive)
