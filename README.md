# Java Counter Race Condition Bug

This repository demonstrates a common race condition bug in Java that occurs when multiple threads access and modify a shared resource (in this case, a counter) without proper synchronization. The bug involves two threads concurrently incrementing a counter, leading to an inaccurate final count.

## Description

The code demonstrates a simple counter class (`Counter`) and a main method that creates two threads to increment the counter. Without synchronization, the threads may interfere with each other, causing the final count to be less than the expected value (20000 in this case).

## Solution

The solution involves using the `synchronized` keyword to make the `increment` method thread-safe. This ensures that only one thread can access and modify the counter at any given time, preventing race conditions.