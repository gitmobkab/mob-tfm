# email()

## A TFM generator that returns a random email

## This Generator use two optional arguments (*safe* and *domain*)

- safe: Boolean (True by default)
    
    - This parameter stop faker from generating real domain name
    - with **safe=False** you may get `mobsy-not-real-please-tfm-make-faker@gmail.com` which might be the real email of someone.
    - don't bother this one is false
    - On the countrary with **safe=True** (default) you may get `ecox@example.com`,`ecox@example.org`,... 

- domain: string 
    - This parameter define the string to put after the @ in the email
    - **Note: Providing a value to domain will always resort in an override of the *safe* parameter**

## USE CASE FOR EACH POSSIBILITIES
- [First Use case with all default parameters](#use-case-one-default "Jump to the associated example")

- [Second Use case with safe=False](#use-case-two-safefalse "Jump to the associated example")

- [Third use case with safe=True and domain='tfm.make'](#use-case-three-safetruedomaintfmmake "Jump to the associated example")

- [Fourth use case with safe=False and domain='tfm.make'](#use-case-four-safefalsedomaintfmmake "Jump to the associated example")


### use case one default

```
#: IN
$ tfm generate ":email()"
    # ":email() ==> ":email(safe=True)

#: OUT
::INFO::  Detected empty column Preview only mode enabled.

┏━━━━━┳━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃ row ┃                         ┃
┡━━━━━╇━━━━━━━━━━━━━━━━━━━━━━━━━┩
│ 1   │ ecox@example.com        │
├─────┼─────────────────────────┤
│ 2   │ lucasjimmy@example.org  │
├─────┼─────────────────────────┤
│ 3   │ xjohnson@example.org    │
├─────┼─────────────────────────┤
│ 4   │ pricemeagan@example.com │
├─────┼─────────────────────────┤
│ 5   │ deanbrandon@example.com │
└─────┴─────────────────────────┘
   The World is a cruel thing    
```

### use case two safe=False
```
#: IN
$ tfm generate ":email(safe=False)"

#: OUT
::INFO::  Detected empty column Preview only mode enabled.

┏━━━━━┳━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃ row ┃                              ┃
┡━━━━━╇━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┩
│ 1   │ reginald18@davis-leonard.org │
├─────┼──────────────────────────────┤
│ 2   │ edwardstanton@yahoo.com      │
├─────┼──────────────────────────────┤
│ 3   │ stephen91@webb.info          │
├─────┼──────────────────────────────┤
│ 4   │ davidgutierrez@hotmail.com   │
├─────┼──────────────────────────────┤
│ 5   │ anthony39@gmail.com          │
└─────┴──────────────────────────────┘
       The World is a cruel thing
```


### use case three safe=True,domain='tfm.make'
```
#: IN
$ tfm generate ":email(domain='tfm.make')"
    # ":email(domain='tfm.make')" ==> ":email(safe=True,domain='tfm.make')

#: OUT
::INFO::  Detected empty column Preview only mode enabled.

┏━━━━━┳━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃ row ┃                          ┃
┡━━━━━╇━━━━━━━━━━━━━━━━━━━━━━━━━━┩
│ 1   │ michellehuffman@tfm.make │
├─────┼──────────────────────────┤
│ 2   │ scampbell@tfm.make       │
├─────┼──────────────────────────┤
│ 3   │ natalie42@tfm.make       │
├─────┼──────────────────────────┤
│ 4   │ richardschwartz@tfm.make │
├─────┼──────────────────────────┤
│ 5   │ laura06@tfm.make         │
└─────┴──────────────────────────┘
    The World is a cruel thing   
```

### use case four safe=False,domain='tfm.make'
```
#: IN
$ tfm generate ":email(safe=False,domain='tfm.make')

#: OUT
::INFO::  Detected empty column Preview only mode enabled.

┏━━━━━┳━━━━━━━━━━━━━━━━━━━━━━━━┓
┃ row ┃                        ┃
┡━━━━━╇━━━━━━━━━━━━━━━━━━━━━━━━┩
│ 1   │ heatherfox@tfm.make    │
├─────┼────────────────────────┤
│ 2   │ richardburton@tfm.make │
├─────┼────────────────────────┤
│ 3   │ fperez@tfm.make        │
├─────┼────────────────────────┤
│ 4   │ ihampton@tfm.make      │
├─────┼────────────────────────┤
│ 5   │ hillwilliam@tfm.make   │
└─────┴────────────────────────┘
   The World is a cruel thing   
```

