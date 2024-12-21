# Expo CLI: Handling Unexpected JSON Errors in package.json

This repository demonstrates a common but often cryptic error encountered when using the Expo CLI.  The error arises from invalid JSON within the project's `package.json` file. The error message itself often isn't very helpful, making it difficult to pinpoint the exact cause. 

This example showcases how an improperly formatted `package.json` can lead to an `Unexpected token in JSON` error and provides a solution for identifying and correcting the JSON issue.

## Steps to Reproduce

1. Clone this repository.
2. Examine the `bug.json` file; it contains intentionally malformed JSON.
3. Attempt to run an Expo CLI command (e.g., `expo start`) in the project directory.
4. Observe the `Unexpected token in JSON` error.

## Solution

The solution lies in carefully reviewing the `package.json` file for any syntax errors. Common issues include:

* **Missing commas:**  Ensure commas separate each key-value pair in objects and each element in arrays.
* **Mismatched brackets:** Check for correct pairing of curly braces `{}` for objects and square brackets `[]` for arrays.
* **Incorrect quotes:** Verify that strings are enclosed in double quotes `"`.
* **Extra characters:** Remove any extraneous characters or whitespace.

The corrected `package.json` is provided in `bugSolution.json`. Use a JSON validator if necessary to detect further errors.