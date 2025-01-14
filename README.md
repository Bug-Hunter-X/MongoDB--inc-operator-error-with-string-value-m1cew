# MongoDB $inc Operator Error with String Value

This repository demonstrates an uncommon error encountered when using the `$inc` operator in MongoDB update operations. The issue arises from providing a string value instead of a numeric value to the `$inc` operator.

## Bug Description

The `$inc` operator in MongoDB is designed to increment a numeric field by a specified value.  When a string is supplied as the increment value, the update operation might not work as expected, potentially leading to incorrect data. 

## Reproduction Steps

1. Create a MongoDB collection.
2. Insert a document with a numeric field, e.g., `counter`.
3. Attempt to update the `counter` using `$inc` with a string value.
4. Observe the result; the `counter` may not be incremented as anticipated.

## Solution

Ensure that the value passed to the `$inc` operator is a number, not a string. Correct usage involves providing numeric values (integer or float).