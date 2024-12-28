# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling for invalid input.  Specifically, the `/users/:id` route attempts to parse the `id` parameter as an integer without validating that it's actually a number. This can lead to crashes or unexpected behavior if the `id` is not a valid integer.

## Bug Report
The provided `bug.js` file contains the problematic route handler.  The `parseInt(userId)` call can throw an error if the userId is not a valid number.  Also, the code doesn't handle the scenario where a user is not found.

## Solution
The `bugSolution.js` file provides a corrected version of the route handler. It includes error handling for both non-numeric IDs and missing users.