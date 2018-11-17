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

### `Variables and Collections`
```yml
testVar = 2;
testVar 
```

Accessing a variable before assigning => Error
```yml
try somerandomVar

=> ERROR: undefVarError: somerandomVar not defined
```

Building Arrays and matrices
```yml
x = Int64[]

=> Array{Int64,1}

y = Array{Int64}(undef, 2, 2)

=> 2×2 Array{Int64,2}:
 140126799036160  140126799036288
 140126799036224  140126799036160

y[1]

=> : 140126799036160

z = [1 2; 4 5; 7 8]

=> 3×2 Array{Int64,2}:
 1  2
 4  5
 7  8

```
 
Basic array manipulations

```yml

z = [1 2]
push!(z, 3)

=> 3-element Array{Int64,1}:
 1
 2
 3
pop!(z)

=> 3

z

=> 2-element Array{Int64,1}:
 1
 2
 
a = [4, 5, 7]
append!(z, a)

=> 5-element Array{Int64,1}:
 1
 2
 4
 5
 7
 
 in(5, a)
 => true
 
 a[1:2]
 => 2-element Array{Int64,1}:
 4
 5
 
 ```
 
 Dictionaries for mappings 
 ```yml
 
 newemptyDict = Dict()
 =>Dict{Any,Any} with 0 entries
 
 fillnewDict = Dict("key1" => 3, "key2" => 4)
 => Dict{String,Int64} with 2 entries:
  "key2" => 4
  "key1" => 3
  
  keys(fillnewDict)
  => Base.KeySet for a Dict{String,Int64} with 2 entries. Keys:
  "key2"
  "key1"
  
  values(fillnewDict)
  => Base.ValueIterator for a Dict{String,Int64} with 2 entries. Values:
  4
  3
  
  a = [1:5]
  b = ["a", "b", "c", "d", "e"]
  c = zip(a, b)
  => Base.Iterators.Zip2{UnitRange{Int64},Array{String,1}}(1:5, ["e", "d", "b", "c", "a"])
  
  length(c)
  => 5
  
  first(c)
  => (1, "e")
  ```
