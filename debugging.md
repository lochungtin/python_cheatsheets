# General Steps for Debugging

*Only to be referenced, don't take this as an definitive guide to solve every problem.*

1. Look at the error message
    `File "the/file/path/of/your/python/file.py", line X, in <module>`
    The error occurs in line `X`.

2. If the error is not immediately obvious, expand the line, and print out each sub-step.
    Example line:`answer = fn(round(x, 2), (list1 + list2)[2:4])[0]`
    Breakdown the line from **inside-out** from the brackets, then **left-to-right**.
    ```py
    step1 = round(x, 2)
    print(step1)

    step2 = list1 + list2
    print(step2)

    step3 = step2[2:4]
    print(step3)

    step4 = fn(step1, step3)
    print(step4)

    answer = step4[0]
    print(answer)
    ```
    When you run this again, the error message will appear at a specific step and the results of the steps above will be own, then you can diagnose the problem as an isolated step.

## Common Errors
- Indexing a list beyond its length.
    - Remember we count from zero.
- Removing an item that doesn't exist in a list, set, or dictionary.
    - Check before popping, removing, or deleting.
- Tuples are immutable.
    - Check the type of your collection before mutating them.
- Name errors.
    - Using a local variable outside of its block.
- `sequence item 0: expected str instance, int found` in a line with the `"".join` function.
    - Joining requires strings, map the list to `str` before the `join`.