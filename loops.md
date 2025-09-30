# For loops

## When to use

When the number of cycles you want to loop is **KNOWN**.
- e.g. Flip a coin N number of times.

### Type 1:

Counts up until **BUT NOT REACHING** `how_many_times` from 0, increasing 1 each time.
Effectively, counts `how_many_times` number of times.
```py
for counter in range(how_many_times):
    pass
```

### Type 2:

Counts up until **BUT NOT REACHING** `ending_count` from `starting_point`, increasing 1 each time.
```py
for counter in range(starting_count, ending_count):
    pass
```

### Type 3:

Counts up until **BUT NOT REACHING** `ending_count` from `starting_point`, increasing by `increment` each time.
```py
for counter in range(starting_count, ending_count, increment):
    pass
```

# While loops

## When to use

When the number of cycles you want to loop is **UNKNOWN**.
- e.g. Do something until the game ends.

Runs the block of code as long as `condition` is `True`.

```py
while condition:
    # keep doing this block of code
```

**!! VERY IMPORNANT !!** 

Make sure to manipulate the value of the condition **INSIDE** the loop or use `break` based on some condition, or else this would be a forever loop.

```py
while True:
    # keep doing this block of code
    if not condition:
        break
```