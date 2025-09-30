# Conditions

## What are Conditions?

- Selecting cases or sections of code to run based on whether on not certain conditions are met

```py
if condition:
    # do something if the condition is true
elif another_condition:
    # do something else if another_condition is true
else:
    # do this if none of the above is true
```

## Rules and Practices

- You must start with an `if`.
- You can have as many `elif`s as you want.
- A good practice is to have an `else` to catch any unforeseen cases (only if applicable).
    - If you are sure that uncaught cases just continues to program, do not add an `else`.
- All code that belongs to that case (block) must be **indented**.

## Conditions

- Checking for equality
    - `==` double equals checks for equality
    - **DO NOT MISTAKE DOUBLE EQUALS (FOR CHECKING) WITH SINGLE EQUALS (FOR ASSIGNING VALUES TO VARIABLES)**
    - e.g. `var_a == var_b`
- Checking for inequality
    - `<`, `>`, `<=`, `>=`
    - e.g. `var_a > var_b`
- Checking for not equality
    - `!=`
    - e.g. `var_a != var_b`

These expressions will evaluate to a `boolean` value.

## Logical Predicates

Predicates combine logical expressions to form a different logical expression.

- `and`, both expressions must be true for the entire expression to be true
- `or`, only one expression needs to be true for the entire expression to be true
- `not`, inverts to polarity of the expression

```py
var_a = True
var_b = False

var_a and var_b # this is False
var_a or var_b  # this is True
not var_a       # this is False
```

## Bad (could be optimised) Code

You don't need to check the true value of a boolean variable for the condition.
```py
some_boolean_variable = True

# bad example
if some_boolean_variable == True:
    pass

# instead you can simply the code to this
if some_boolean_variable:
    pass
```
