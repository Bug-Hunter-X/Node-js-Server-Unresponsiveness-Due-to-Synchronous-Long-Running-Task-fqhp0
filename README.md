# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in the request handler causes the server to become unresponsive. The `server.js` file shows the problematic code, while `serverSolution.js` provides a solution using asynchronous operations.

## Problem

The `server.js` file contains a `while` loop that simulates a long-running task.  This blocks the event loop, preventing the server from handling new requests.  As a result, the server becomes unresponsive and new connections are dropped.

## Solution

The `serverSolution.js` file demonstrates a solution using asynchronous operations. Instead of blocking the event loop with a synchronous task, the solution uses asynchronous I/O or task scheduling, allowing other tasks to run and prevent the server from hanging.