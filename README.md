# Node.js Server Crash Under High Load

This repository demonstrates a common issue in Node.js servers: crashing under high load. The `server.js` file contains a basic HTTP server that's susceptible to crashing when bombarded with many requests simultaneously.  The `serverSolution.js` file provides a solution using the `cluster` module for improved performance and stability.

## Problem

The original server uses a single thread to handle all incoming requests. This becomes a bottleneck when dealing with a large number of concurrent requests, leading to instability and potential crashes. 

## Solution

The solution leverages Node.js's `cluster` module to create a cluster of worker processes. Each worker handles a subset of the incoming requests, distributing the load and improving the server's ability to handle high concurrency.