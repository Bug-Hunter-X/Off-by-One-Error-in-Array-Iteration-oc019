# Off-by-One Error in Java Array Iteration

This repository demonstrates a common off-by-one error in Java when iterating over arrays.  The error occurs when the loop condition is incorrect, causing an attempt to access an index beyond the array's bounds.  This results in an `ArrayIndexOutOfBoundsException`.

## Bug Description

The original code contains a loop that iterates from 0 up to and *including* `array.length`.  Since array indices are zero-based, the valid indices range from 0 to `array.length - 1`. Accessing `array[array.length]` leads to the exception.

## Solution

The solution corrects the loop condition to iterate only up to `array.length - 1`. This ensures that the loop accesses only valid array indices.