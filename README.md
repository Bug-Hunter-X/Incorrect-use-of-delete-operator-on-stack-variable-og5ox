# Incorrect Use of delete Operator in C++
This repository demonstrates a common error in C++: attempting to use the `delete` operator on a stack-allocated variable.  The `delete` operator is intended for deallocating memory allocated on the heap using `new`. Using it on stack variables results in undefined behavior, potentially causing crashes or other unpredictable issues.

## Bug Description
The provided C++ code snippet attempts to use `delete` on an integer variable (`x`) allocated on the stack. This is incorrect.  The `delete` operator should only be applied to pointers pointing to memory dynamically allocated with `new`.

## Solution
The corrected code removes the erroneous `delete` operation. Stack-allocated variables are automatically deallocated when they go out of scope.
