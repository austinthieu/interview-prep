# Stack

## Overview

A **stack** is a linear data structure that follows **LIFO (Last In, First Out)**:

- The last element added is the first one removed.

### Common Use Cases

- Matching pairs (parentheses, brackets, braces)
- DFS traversal
- Undo/redo operations
- Expression evaluation
- Backtracking patterns

---

## Core Idea (Valid Parentheses Pattern)

For problems like **Valid Parentheses**, a stack is used to:

- Track opening brackets
- Match them with closing brackets
- Maintain correct order and nesting

---

## Key Insight

When encountering a closing bracket:

1. If stack is empty → invalid
2. Pop the top element
3. Check if it matches the expected opening bracket

At the end:

- Stack must be empty → valid
- If not empty → invalid

---

## Mapping Strategy

Use a hash map to match closing → opening brackets:

```python
pairs = {
    ')': '(',
    ']': '[',
    '}': '{'
}
