---
title: Julia
category: Julia
layout: 2017/sheet
keywords:
  -Variables and Collections
  -Primitive Data Types and Operators
  -Types
  -Multiple Dispatch
  -Control Flow
  -Functions
  -Scoping
  -I/O Streams 
  -Profiling
---

Getting Started
---------------

### 'Variables and Collecions' 
```
testVar = 2;
testVar 
```

Accessing a variable before assigning => Error
```
try 
	somerandomVar

=> ERROR: undefVarError: somerandomVar not defined
```

Building Arrays and matrices
```
x = Int64[]

=> Array{Int64,1}

y = Array{Int64}(undef, 2, 2)

=> 2×2 Array{Int64,2}:
 140126799036160  140126799036288
 140126799036224  140126799036160

y[1]

=> 140126799036160

z = [1 2; 4 5; 7 8]

=> 3×2 Array{Int64,2}:
 1  2
 4  5
 7  8

```
 