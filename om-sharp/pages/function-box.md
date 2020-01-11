---
layout: docpage
---

# Function Box

_Function Boxes_ are the main type of boxes in OM# visual programs. 
Any Lisp function, in-built or defined in the environment, can be used as a function box in an OM#.

<img src="./images/box-lisp-fun.png" align="right">

- Common Lisp functions appear without a specific icon with inputs corresponding to the function arguments, and an output corresponding to the returned value.

<img src="./images/box-om-fun.png" align="right">

- OM#-specific functions are also Lisp functions, defined with special macros `defmethod*` / `defmethod!` (see [Writing code for OM#](write-code)). They present additional features such as icons, documentation, etc. 

### Inputs

The function ["lambda-lists"](http://www.lispworks.com/documentation/HyperSpec/Body/03_da.htm) determines the different inputs of a function boxes, and **the type of data that it accepted for each input**.

> In Common Lisp / OM# a data **type** can be either a basic type defined in the language (e.g. integer, string, symbol, ...) or determined by a class definition (e.g. BPF, CHORD, ...). Connecting wrong types to the function inputs yields an runtime-excecution error, that is generally handled and displayed by OM# as follows:      
>
> <img src="./images/type-error.png">

> See [Box Inputs](box-inputs) for details on the different kinds of inputs.



### Outputs

Most functions have one single output; some OM# functions can have more. 

Ordinarily the result of calling a Lisp function is a single Lisp object/value. Sometimes, however, it is convenient for a function to compute and return several objects. Common Lisp provides a mechanism for handling multiple values directly. For an OM box and in standard evaluation mode, the multiple outputs generally trigger several evaluations of the box.

> See [Evaluation modes](eval-modes) for advanced handling of multiple-evaluations of function boxes.

