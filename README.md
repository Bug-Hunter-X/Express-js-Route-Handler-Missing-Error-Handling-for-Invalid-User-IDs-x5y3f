# Express.js Route Handler Missing Error Handling for Invalid User IDs

This repository demonstrates a common error in Express.js route handlers:  missing error handling for invalid or unexpected input. Specifically, this example showcases a route that fetches a user by ID but lacks proper checks to handle cases where the ID is not a valid number.

## Bug

The `bug.js` file contains the flawed code.  The route handler attempts to parse the user ID as an integer using `parseInt()` without any validation.  If the `userId` parameter is not a number (e.g., a string), `parseInt()` will return `NaN`, leading to a potential crash or unexpected behavior when the code attempts to use it in comparisons.

## Solution

The `bugSolution.js` file provides a corrected version of the code. It includes error handling to check if the `userId` parameter is a valid number before attempting to use it.  If it is not, a suitable error message is returned to the client.