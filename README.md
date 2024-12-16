# MongoDB: Incorrect Use of $inc Operator

This repository demonstrates a common error when using the `$inc` operator in MongoDB update queries.  The `$inc` operator is intended to increment or decrement a numeric field by a specified value.  However, providing a string value instead of a number results in unexpected behavior and can corrupt your data.

## Bug
The original code incorrectly passes a string value to the `$inc` operator.  This prevents the intended numeric increment and may lead to unexpected results or data loss.

## Solution
The corrected code ensures that the value provided to `$inc` is a valid number (integer or float).