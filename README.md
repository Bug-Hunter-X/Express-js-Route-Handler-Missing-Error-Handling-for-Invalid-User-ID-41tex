# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  missing error handling for invalid input. Specifically, the `/users/:id` route attempts to parse the `id` parameter as an integer without checking for non-numeric values.  This can lead to unexpected behavior or crashes.

The `bug.js` file shows the problematic code. The `bugSolution.js` file provides a corrected version with robust error handling. 

## How to reproduce the bug

1. Clone the repository.
2. Run `npm install` to install Express.js.
3. Run `node bug.js`. 
4. Make a request to `/users/abc` (or similar invalid ID).

You'll likely see an error in the console. 

## Solution

The solution involves adding input validation to ensure the `userId` is a number before attempting to parse and use it.  This prevents unexpected errors and provides a more robust API.