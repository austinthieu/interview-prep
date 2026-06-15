# Two Pointers

## Overview

Two Pointers is a technique that uses two indices to traverse data efficiently.

Goal:

* Reduce O(n²) brute force solutions to O(n)
* Avoid nested loops
* Process data from both ends or maintain a moving window

---

## When to Use

Look for:

* Sorted arrays
* Palindrome problems
* Pair sum problems
* Problems involving opposite ends of an array/string

Questions to ask:

* Can I use a left and right pointer?
* Is the input sorted?
* Do I need to compare elements from both ends?

---

## Time Complexity

| Approach     | Complexity |
| ------------ | ---------- |
| Brute Force  | O(n²)      |
| Two Pointers | O(n)       |

Space Complexity:

* Usually O(1)

---

## Common Template

```python
left = 0
right = len(nums) - 1

while left < right:
    if condition:
        left += 1
    elif other_condition:
        right -= 1
    else:
        return result
```

---

## Key Interview Questions

### Two Integer Sum II

Pattern:
Opposite Direction Two Pointers

Difficulty:
Medium

Key Insight:
Because the array is sorted, we can eliminate half the search space after each comparison.

Algorithm:

1. Start with left at beginning.
2. Start with right at end.
3. Calculate current sum.
4. If sum is too small:

   * Move left pointer right.
5. If sum is too large:

   * Move right pointer left.
6. If sum equals target:

   * Return answer.

Time:
O(n)

Space:
O(1)

Why it Works:
The sorted array guarantees that moving pointers changes the sum predictably.

Status:
✅ Solved

---

### Valid Palindrome

Pattern:
Two Pointers on String

Difficulty:
Easy

Key Insight:
Compare characters from both ends while skipping non-alphanumeric characters.

Algorithm:

1. Place pointers at both ends.
2. Skip invalid characters.
3. Compare lowercase versions.
4. If mismatch occurs:

   * Not a palindrome.
5. Continue until pointers cross.

Time:
O(n)

Space:
O(1)

Status:
✅ Solved

---

## Mistakes I Made

### Two Integer Sum II

* This one was easy
* Didn't make sum variable to hold numbers[l] + numbers[r]
* Don't forget to return [l + 1, r + 1] because indices start at 0

### Valid Palindrome

* Can check if alphanumeric using .isalnum() function
* Can check alphanumeric inside while loop instead of creating new string to save space complexity

---

## Pattern Recognition

### Sorted Array + Pair Sum

Think:
Two Pointers

Examples:

* Two Integer Sum II
* Container With Most Water

### Compare Opposite Ends

Think:
Two Pointers

Examples:

* Valid Palindrome
* Reverse String

---

## Problems Completed

* [x] Two Integer Sum II
* [x] Valid Palindrome
* [ ] Container With Most Water
* [ ] 3Sum
* [ ] Trapping Rain Water
