# Firebase Snapshot Data Access Before Loading

This repository demonstrates a common error in Firebase applications: accessing data from a Firestore snapshot before it has fully loaded. This often leads to undefined values and unexpected behavior.

## Problem
The `bug.js` file shows how attempting to access data before the snapshot is resolved results in an error.  This is because asynchronous operations in Firebase require proper handling to avoid this race condition.

## Solution
The `bugSolution.js` file presents a corrected approach using promises and `.then()` to ensure data is loaded before access.  Error handling is also included to gracefully manage potential issues.

## How to Run
1.  Ensure you have Node.js and npm installed.
2.  Install the Firebase Admin SDK: `npm install firebase-admin`
3.  Configure your Firebase project (see Firebase documentation).
4.  Run the JavaScript file.  Observe the difference in behavior between the buggy and corrected code.