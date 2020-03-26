---
layout: docpage
---

# Logical Operators: `and`/`or`


`and` and `or` are _logical operators_ generally used to test wether _all_ or _any_ of a given number of conditions are met.    

The boxes can be added any number of [optional inputs](box-inputs#optional-inputs), which be evaluated left-to-right until a decision can be made:    

- `and` will stop (and return NIL) as soon as one of its inputs evaluates to NIL. Otherwise it will return the result of the last input evaluation.

- `or` will return the result of the first non-NIL encountered result, or NIL if there is no such result.

> _Contrary to most boxes in OM# and functions in Lisp, only the necessary inputs will be evaluated._

The `and` and `or` _logical operators_ boxes can be combined and used as tests for a [contitional / `if`](if) statement, or by themselves as means to control evaluation flow in visual programs.

