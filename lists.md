# Lists

## What are Lists?

An **ordered** collection of items of any type.

Duplicate items are **allowed** in lists.

## Initialisation

Defining items explicitly.
```py
l = [1, 2, 3, 4]
```

Using the class constructor, creates a list with **no** items.
```py
l = list()
```

Using syntax abuse to create a list with **n** of the same item.

```py
l = [0] * 10 # creates a list with 10 zeros
```

## Indexing

```py
l = ['a', 'b', 'c', 'd']
l[0]    # a
l[2]    # c
l[-1]   # d
```

- Start counting at 0.
- Negative indices count from the back, starting from -1.
- Indexing beyond the length of the list with give an **error**. `l[4]` will give an error.

## Methods

Getting the length of the list.
```py
l = [1, 2, 3, 4]
len(l) # returns 4
```
---

App**end** - Adding items to the **back**.
```py
l = [1, 2, 3, 4]
l.append(5) # l is now [1, 2, 3, 4, 5]
```

**In**sert - Adding items to **any position**.
```py
l = [1, 2, 3, 4]
l.insert(5, 0) # l is now [5, 1, 2, 3, 4]
l.insert(6, 2) # l is now [5, 1, 6, 2, 3, 4]
```
---

Checking if an item is in the list.
```py
l = [1, 2, 3, 4]
if 3 in l: # gives True
    pass

if 6 in l: # gives False
    pass
```
---

Removing an item **by value**.
Will give an error if item doesn't exist.
```py
l = [1, 2, 3, 4]
l.remove(2) # l = [1, 3, 4]

# good practice to check if the item is in the list first
if 2 in l:
    l.remove(2)
```

Removing an item **by index**.
Will give an error if index is > list length.
```py
l = [1, 2, 3, 4]
l.pop(2) # l = [1, 2, 4]

# good practice to check the length first
if len(l) > 2:
    l.pop(2)
```
---

Slicing a list to get a sub-list.
Returns a new list, the original list stays the same.
```py
l = [1, 2, 3, 4, 5, 6, 7, 8, 9]

start_idx = 2
end_idx = 6
l[start_idx:end_idx] # returns [3, 4, 5, 6]

l[:3] # returns [1, 2, 3]
l[4:] # returns [5, 6, 7, 8, 9]
```

Intuition for the result of the slice:
- Count `end_idx - start_idx` items from the `start_idx`, that is the new list.

---

Merging two lists.
This will **change** the original list.
```py
l = [1, 2, 3]
l.extend([4, 5, 6]) # l is now [1, 2, 3, 4, 5, 6]
```

This will **create** a new list.
```py
a = [1, 2, 3]
b = [4, 5, 6]
l = a + b # l is now [1, 2, 3, 4, 5, 6]
```

---

Sorting a list.
This will **change** the original list.
```py
l = [4, 3, 2, 1]
l.sort() # l is now [1, 2, 3, 4]
```

This will **create** a new list.
```py
l = [4, 3, 2, 1]
sorted(l) # returns [1, 2, 3, 4]
```

Sort and sorted takes an extra parameter, which is a comparison function to determine the order of sorting.
```py
# sort by length
l = ["one", "two", "three", "four"]
l.sort(l, len) # l is now ["one", "two", "four", "three"]
```

## Bad Practices

- Not doing a check for the length or index before `pop` or `remove`.
- Mixing different types of data in a list, having `int`, `string`, etc in one list.