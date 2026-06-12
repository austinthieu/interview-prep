# Arrays

## Overview

Arrays store elements in contiguous memory and provide O(1) access by index.

Examples:

* Python: list
* JavaScript: Array
* C#: Array, List<T>
* Go: array, slice

---

## Time Complexity

| Operation           | Complexity |
| ------------------- | ---------- |
| Access              | O(1)       |
| Search              | O(n)       |
| Insert at End       | O(1)*      |
| Insert at Beginning | O(n)       |
| Delete at End       | O(1)       |
| Delete at Beginning | O(n)       |

* Amortized O(1) for dynamic arrays.

---

## Common Patterns

### Iteration

When:

* Need to visit every element.

Template:

```python
for num in nums:
    print(num)
```

---

### Frequency Counting

When:

* Counting occurrences.
* Detecting duplicates.

Template:

```python
count = {}

for num in nums:
    count[num] = count.get(num, 0) + 1
```

Problems:

* Contains Duplicate
* Top K Frequent Elements

---

### Prefix Sum

When:

* Need fast range sums.

Template:

```python
prefix = [0]

for num in nums:
    prefix.append(prefix[-1] + num)
```

Problems:

* Range Sum Query
* Subarray Sum Equals K

---

## Key Interview Questions

### Two Sum

Pattern:
Hash Map

Difficulty:
Easy

Key Insight:
Store previous numbers in a hash map and check if the complement exists.

Time:
O(n)

Space:
O(n)

Status:
✅ Solved

Solution:
<https://www.youtube.com/watch?v=KLlXCFG5TnA>

---

### Contains Duplicate

Pattern:
Hash Set

Key Insight:
If an element already exists in the set, a duplicate is found.

Time:
O(n)

Space:
O(n)

Status:
✅ Solved

Solution:
<https://www.youtube.com/watch?v=3OamzN90kPg>

---

### Valid Anagram

Pattern:
Frequency Counting

Key Insight:
Both strings must have identical character counts.

Time:
O(n)

Space:
O(1) or O(n)

Status:
✅ Solved

Solution:
<https://www.youtube.com/watch?v=9UtInBqnCgA>

---

## Mistakes I Made

### Two Sum

* Storing difference instead of index in hashmap

### Contains Duplicate

* Forgot that to use hashset instead of hashmap since sets store only unique elements

### Valid Anagram

* Used two dictionaries instead of one - instead of comparing two dictionaries we can use 1 dictionary and increment/decrement
the character's values
* If all the values are 0 then it is an Anagram
* Base case of comparing length of both strings to get an early return

### groupAnagrams

* Use an array of 26 to count frequency of all lowercase latters
* Get the ASCII value of a character using ord()
* Use a tuple as the key instead of a list because only immutable data types can be key

---

## Review Notes

Things to remember:

* Arrays provide O(1) index access.
* Use hash maps for fast lookups.
* Use sets to detect duplicates.
* Always consider time complexity before coding.

---

## Problems Completed

* [x] Two Sum
* [x] Contains Duplicate
* [x] Valid Anagram
* [x] Group Anagrams
* [ ] Top K Frequent Elements
* [ ] Product of Array Except Self
* [ ] Encode and Decode Strings
* [ ] Longest Consecutive Sequence
