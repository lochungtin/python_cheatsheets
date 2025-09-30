# The Different Bracket Types

`()`
-
- Isolating arithmetic operations.
- If followed directly after a "word", it is a function call.

`[]`
- 
- Defining lists.
- Indexing a list or a dictionary.

`{}`
- 
- Defining dictionaries.

## Interpreting Chained or Nested Brackets
- Read from inside out, then left to right.

Example
```py
fn(({"a": 1, "b": 2, "c": 3}["a"] + 3) * 2)
```

1. Defining a dictionary.
2. Indexing the dictionary with `"a"`, which returns `1`.
3. Adding `3` to the indexed `1`, then multiply by `2`, which gives `8`.
4. Inputting `8` as the parameter to the function `fn`.

# Blocks, and the use of ":"

A code "block" is defined by indentation. The indented code belongs to the line immediately **above** it.

Always have a `:` after the top line of a block.

Examples:
- An `if-else` condition.
```py
if something == another_thing:
    # whatever is here is belongs to the condition above
```
- A for or while loop.
```py
for i in range(n):
    # whatever is here is part of the for loop

while condition:
    # whatever is here is part of the while loop
```

- A function definition.
```py
def fn(params):
    # whatever is here is part of the function definition
```