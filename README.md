# Uninitialized Variable in Ada

This repository demonstrates a simple Ada program that contains a common error: using an uninitialized variable. The program calculates the sum of two integers but fails to initialize a variable before using it.  This highlights the importance of proper variable initialization in Ada.

## Bug Description

The `Main` procedure declares an integer variable `Z` without initializing it.  Ada does not automatically initialize variables to zero (unlike some languages). The subsequent assignment `Z := Add_Numbers(X, Y);` works, but if the `Add_Numbers` function were to somehow fail to return a value, `Z` would remain uninitialized, leading to undefined behavior. 

## Solution

The solution involves explicitly initializing `Z` to a default value before its use.