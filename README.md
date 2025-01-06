# PHP Ternary Operator Array Issue

This repository demonstrates a subtle bug in PHP involving the use of the ternary operator when returning array values.  When the ternary operator's condition evaluates to false, the array is unexpectedly overwritten instead of having new key-value pairs appended.

## Description
The core problem is the behavior of PHP's ternary operator in array contexts. It does not perform an array merge operation if the condition is false; it replaces the array entirely. This can lead to unexpected results and data loss.

## How to Reproduce
1. Clone this repository.
2. Run `bug.php`.
3. Observe the output, demonstrating the incorrect behavior.
4. Run `bugSolution.php` to see the corrected implementation.

## Solution
The solution involves avoiding the ternary operator in this specific scenario or using explicit array merging using `array_merge` or array union with the `+` operator.