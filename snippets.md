## Counting Item Frequency
```py
def countFreq(l):
    freq = {}
    for x in l:
        freq[x] = freq.get(x, 0) + 1
    return freq

countFreq([1, 2, 3, 1, 1, 1, 2, 3, 1, 1, 1, 2, 3, 1, 1, 2, 3, 3, 3])
# returns {1: 9, 2: 4, 3: 6}
```

## Flip Dictionary
```py
def flipDict(d):
    return dict((v, k) for k, v in d.items())

flipDict({"a": 1, "b": 2, "c": 3})
# returns {1: "a", 2: "b", 3: "c"}
```

## Color Representation Conversion
```py
def hex2rgb(code):
    code = code[int("#" in code):]
    return int(code[:2], 16), int(code[2:4], 16), int(code[4:], 16)

def rgb2hex(r, g, b):
    return f"#{''.join(hex(x).ljust(4, '0')[-2:] for x in (r, g, b))}".upper()

hex2rgb("#00FFC8")
# returns (0, 255, 200)

rgb2hex(0, 255, 200)
# returns "#00FFC8"
```