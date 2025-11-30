# int()

## A TFM generator that returns a random integer

### This Generator use two optional arguments (*min* and *max*)



- **min**: INT | FLOAT (0 by default)
    - the **min** parameter can reveive an int or a float
    
    - if a float is passed it will be converted to an int (min=10.0 ==> min=10)

- **max**: INT | FLOAT (1 by default)
    - the **max** parameter can reveive an int or a float

    - if a float is passed it will be converted to an int (max=10.0 ==> max=10)
    

### USE CASES
- [Use case one all values to default](#use-case-one-all-default "Jump to the related section")

- [Use case two min=1,max=50](#use-case-two-min1max50 "Jump to the related section")

- [Use case three min=10.0,max=500.25](#use-case-three-min100max50025-or-min1000max50025 "Jump to the related section")

- [Use case four min=10.456,max=1500.25](#use-case-four-min40456max150025 "Jump to the related section")

### use case one all default

```
#: IN
$ tfm generate ":int()"

#: OUT 
::INFO::  Detected empty column Preview only mode enabled.
   
┏━━━━━┳━━━┓
┃ row ┃   ┃
┡━━━━━╇━━━┩
│ 1   │ 0 │
├─────┼───┤
│ 2   │ 0 │
├─────┼───┤
│ 3   │ 0 │
├─────┼───┤
│ 4   │ 1 │
├─────┼───┤
│ 5   │ 1 │
└─────┴───┘
 The World 
is a cruel 
   thing   
```

### use case two min=1,max=50
```
#: IN
$ tfm generate ":int(min=1,max=50)"

#: OUT 
::INFO::  Detected empty column Preview only mode enabled.

┏━━━━━┳━━━━┓
┃ row ┃    ┃
┡━━━━━╇━━━━┩
│ 1   │ 12 │
├─────┼────┤
│ 2   │ 21 │
├─────┼────┤
│ 3   │ 41 │
├─────┼────┤
│ 4   │ 17 │
├─────┼────┤
│ 5   │ 9  │
└─────┴────┘
The World is
  a cruel   
   thing 
```

### use case three min=10.0,max=500.25 or min=10.00,max=500.25
```
#: IN
$ tfm generate ":int(min=10.0,max=500.25)"

#: OUT 
::INFO::  Detected empty column Preview only mode enabled.

┏━━━━━┳━━━━━┓
┃ row ┃     ┃
┡━━━━━╇━━━━━┩
│ 1   │ 343 │
├─────┼─────┤
│ 2   │ 314 │
├─────┼─────┤
│ 3   │ 477 │
├─────┼─────┤
│ 4   │ 368 │
├─────┼─────┤
│ 5   │ 113 │
└─────┴─────┘
The World is 
a cruel thing
```

### use case four min=40.456,max=1500.25
```
#: IN
$ tfm generate ":int(min=10.456,max=1500.25)"

#: OUT 
::INFO::  Detected empty column Preview only mode enabled.

┏━━━━━┳━━━━━━┓
┃ row ┃      ┃
┡━━━━━╇━━━━━━┩
│ 1   │ 123  │
├─────┼──────┤
│ 2   │ 123  │
├─────┼──────┤
│ 3   │ 312  │
├─────┼──────┤
│ 4   │ 1360 │
├─────┼──────┤
│ 5   │ 22   │
└─────┴──────┘
The World is a
 cruel thing  
```