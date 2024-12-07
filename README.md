# Express.js JSON Body Parsing Error with Empty or Invalid JSON

This repository demonstrates a common issue in Express.js applications where parsing JSON request bodies fails when the body is empty or contains invalid JSON data.  The application incorrectly handles this scenario, resulting in unexpected behavior.

## Problem

The provided Express.js application uses `express.json()` middleware to parse incoming JSON requests.  However, it does not gracefully handle scenarios where the request body is either empty or contains invalid JSON.  This results in either an empty object being logged or an error being thrown, rather than a proper error response to the client.

## Solution

The solution involves adding error handling to catch and appropriately respond to invalid or missing JSON data in the request body.  This ensures the application remains robust and provides informative feedback to the client.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install the dependencies.
3. Run `node bug.js` to start the server.
4. Send a POST request to `/data` with an empty body or an invalid JSON body using a tool like Postman or curl. Observe the server's response and console output.
5. Then run `node bugSolution.js` to see the improved error handling.  Send the same requests and observe the difference.
