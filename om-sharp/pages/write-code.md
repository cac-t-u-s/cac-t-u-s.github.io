
# Writing classes and functions

Any Lisp function or class can be used in OM# graphical programs. However, a specific syntax allows to specify some specific behaviours.

> OM# inherits from [OpenMusic](https://openmusic-project.github.io/openmusic/dev/codeforom) the syntax of function and class definitions that follow, so that any code written for OpenMusic can also be loaded and used in OM#.

The macros `defclass!` and `defmethod!` allow for your defined classes and methods:
- To be attached and displayed in [external libraries](write-library)
- To display some specific help and graphical attributes 

The [OpenMusic developer resources](https://openmusic-project.github.io/openmusic/dev/codeforom) give the following examples:

```cl
(defclass! my-chord (om::chord) 
   ((tonality :initform '(C Major) :initarg :tonality :accessor tonality))
  (:icon :tonal-chord))
```

```cl
(defmethod! is-major? ((self my-chord)) 
   :doc "tells if the associated tonality of the note is major" 
   :icon 193 
   (eq (second (tonality self)) 'Major))
```

```cl
(defmethod! compare ((c1 my-chord) (c2 my-chord) lowest) 
   :icon 180 
   :initvals (list nil nil T) 
   :indoc '("a note" "a note" "mode-menu") 
   :doc "compares the pitch of 2 notes, and yields the lowest (or the highest) one" 
   :menuins '( (2 ( ("lowest" T) ("highest" NIL)))) 
   (if lowest 
     (if (<= (om::list-min (om::lmidic c1) (om::list-min (om::lmidic c2))) c1 c2) 
    (if (>= (om::list-max (om::lmidic c1) (om::list-max (om::lmidic c2))) c1 c2)
   )
 )
```


The `defmethod!`-specific attributes in these definitions are:


- `:icon` defines an icon Id for the function (the icon must be in the "icon" folder of OM#, or of the external library)
- `:initvals` a list with a default value for each input.
- `:indoc` a list with a documentation string for each input.
- `:numouts` tells how many outputs the function has
- `:doc` documentation of the function
- `:menuins` defines a pop-up menu definition list attached to some given input number(s)






