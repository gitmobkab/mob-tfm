# float()

## A TFM generator that returns a random float with a fixed precision

### This Generator use two optional arguments (*min* and *max*)


**float()** is somewhat a handy guy because of it's versatility

With **float()** you don't have to give the precision of the generated floats

He does it for you with the **max** parameter

- **min**: INT | FLOAT (0.0 by default)
    - the **min** parameter can reveive an int or a float
    
    - if an int is passed it will be converted to a float with one 
    number precision (min=10 ==> min=10.0)

- **max**: INT | FLOAT (1.0 by default)
    - the **max** parameter can reveive an int or a float

    - if an int is passed it will be converted to a float with one 
    number precision (max=10 ==> max=10.0)
    
    - as mentioned above **float** determines the precision of the floats to generate with the **max** parameter, the precision is the one from the float passed to **max**
    
    - Note: if an int is passed then the precision will be of 1

### USE CASES

- [Use case one all values to default](#use-case-one-all-default "Jump to the related section")

- [Use case two min=1,max=50](#use-case-two-min1max50 "Jump to the related section")

- [Use case three min=10.0,max=500.25](#use-case-three-min100max50025-or-min1000max50025 "Jump to the related section")

- [Use case four min=10.456,max=1500.25](#use-case-four-min40456max150025 "Jump to the related section")

### use case one all default

```
#: IN
$ tfm generate ":float()"

#: OUT 
::INFO::  Detected empty column Preview only mode enabled.
   
┏━━━━━┳━━━━━┓
┃ row ┃     ┃
┡━━━━━╇━━━━━┩
│ 1   │ 1.0 │
├─────┼─────┤
│ 2   │ 1.0 │
├─────┼─────┤
│ 3   │ 0.9 │
├─────┼─────┤
│ 4   │ 0.0 │
├─────┼─────┤
│ 5   │ 0.4 │
└─────┴─────┘
The World is 
a cruel thing
```

### use case two min=1,max=50
```
$ tfm generate ":float(min=1,max=50)"

#: OUT 
::INFO::  Detected empty column Preview only mode enabled.

┏━━━━━┳━━━━━━┓
┃ row ┃      ┃
┡━━━━━╇━━━━━━┩
│ 1   │ 26.6 │
├─────┼──────┤
│ 2   │ 9.1  │
├─────┼──────┤
│ 3   │ 13.5 │
├─────┼──────┤
│ 4   │ 35.0 │
├─────┼──────┤
│ 5   │ 40.0 │
└─────┴──────┘
The World is a
 cruel thing  
```

### use case three min=10.0,max=500.25 or min=10.00,max=500.25
```
$ tfm generate ":float(min=10.0,max=500.25)"

#: OUT 
::INFO::  Detected empty column Preview only mode enabled.

┏━━━━━┳━━━━━━━━┓
┃ row ┃        ┃
┡━━━━━╇━━━━━━━━┩
│ 1   │ 417.71 │
├─────┼────────┤
│ 2   │ 133.71 │
├─────┼────────┤
│ 3   │ 450.22 │
├─────┼────────┤
│ 4   │ 16.31  │
├─────┼────────┤
│ 5   │ 359.15 │
└─────┴────────┘
```

### use case four min=40.456,max=1500.25
```
$ tfm generate ":float(min=10.456,max=1500.25)"

#: OUT 
::INFO::  Detected empty column Preview only mode enabled.

┏━━━━━┳━━━━━━━━━┓
┃ row ┃         ┃
┡━━━━━╇━━━━━━━━━┩
│ 1   │ 579.2   │
├─────┼─────────┤
│ 2   │ 203.15  │
├─────┼─────────┤
│ 3   │ 994.16  │
├─────┼─────────┤
│ 4   │ 1282.04 │
├─────┼─────────┤
│ 5   │ 580.72  │
└─────┴─────────┘
 The World is a  
   cruel thing  
```