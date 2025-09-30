# Integers

Any positive and negative whole number, no decimals points.

The `int()` function converts any **VALID** variable into an integer.

- Valid conditions:
    - The variable is a float
        - `int(3.14)` is `3`
    - The variable is a string AND contains only numbers (no decimal points)
        - `int("3")` is `3`
    - The variable is a boolean
        - `int(False)` is `0`
        - `int(True)` is `1`

# Floats

Any real number, with decimal points.

The `float()` function converts any **VALID** variable into an floating point number.

- Valid conditions:
    - The variable is a integer
        - `float(3)` is `3.0`
    - The variable is a string AND contains only numbers (decimal points optional)
        - `float("3.14")` is `3.14`
    - The variable is a boolean
        - `float(False)` is `0.0`
        - `float(True)` is `1.0`

## Useful built-in functions

`round(n)`, rounds `n` to the nearest integer.
    - e.g. `round(2.46)` is `2`
`round(n, z)`, rounds `n` to the neareest `z` decimal points.
    - e.g. `round(2.46, 1)` is `2.5`

# Booleans

A type with only 2 values, `True` and `False`.
Used mostly during conditions.

# Strings