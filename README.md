# JavaScript Algorithm Challenges

This repository contains a couple of small algorithmic problems implemented in
plain JavaScript (Node). They focus on iterative sequences and working with
very large integers represented as digit arrays.

---

## Problem 1 – Longest Collatz Chain

Consider the Collatz sequence defined for positive integers:

- If `n` is even, `n → n / 2`
- If `n` is odd, `n → 3n + 1`

Starting from a given `n`, the sequence ends when it reaches 1. This problem
asks:

> For starting values less than one million, which starting number produces the **longest** Collatz chain?

Key ideas:

- Implementing the Collatz step function
- Iterating sequences until they reach 1
- Using memoization (caching) to avoid recomputing chain lengths for values
  we’ve already seen

File: `src/problem01_longestCollatz.js`

---

## Problem 2 – Factorial Digit Sum

For a positive integer `n`, the factorial `n!` is defined as:

\[
n! = n \times (n-1) \times \cdots \times 3 \times 2 \times 1
\]

This problem asks:

> Compute `100!` and find the **sum of the digits** of that number.

Since `100!` is larger than JavaScript’s safe integer range, the solution:

- Represents big integers as arrays of digits
- Implements manual multiplication for factorial
- Sums the digits of the final result

File: `src/problem02_factorialDigitSum.js`

---

## Running the Code

From the project root:

```bash
node src/problem01_longestCollatz.js
node src/problem02_factorialDigitSum.js
