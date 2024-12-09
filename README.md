# Expo Managed Workflow App Intermittent Crashes

This repository demonstrates a bug I encountered in an Expo managed workflow application. The application would crash intermittently without providing clear error messages. The crashes seem to be related to asynchronous operations and the use of AsyncStorage.

## Bug Description

The application crashes randomly, with no specific error messages in the console. The crashes appear correlated with read/write operations to AsyncStorage. Standard debugging techniques proved ineffective in identifying the root cause.

## Reproduction Steps

1. Clone the repository.
2. Run `npm install`.
3. Run `expo start`.
4. Interact with the application, performing actions that trigger data persistence using AsyncStorage.  Crashes will occur intermittently.

## Solution

A solution is provided in `bugSolution.js` that addresses the issue by properly handling potential errors within asynchronous operations and adding more robust error handling to AsyncStorage operations. 