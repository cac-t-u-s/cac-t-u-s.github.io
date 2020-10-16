---
layout: docpage
---

# Abstractions

> Abstraction is a fundamental concept in computer programming, which can have different meanings and facets. In our case, making an abstraction consists in using parts of visual programs as functions (or _procedures_, _sub-routines_, etc.) in order to single out a specific behaviour or sequence of operations, which can be labeled with a name and eventually used/re-used in a larger-scale program. 
There can be arbitrary numbers of levels of abstraction and encapsulation of patches within one another.     
Abstraction allows to structure a program by establishing levels of complexity, reuse components, and focus on certain levels of details when programming.
It quickly becomes an essential part of writing consistent programs in any language.

**In OM# (and similar visual programming languages), abstractions are generally [patches](patch-box) embedded inside other higher-level patches.**
They also include [sequencers](sequencer-box), or [Lisp functions](lispfun-box) boxes.

Abstractions can be either **[global](#global-abstraction)** or **[internal](#internal-abstraction)**.

> ### See Also...
> - [Patch Box](patch-box)
> - [Lisp-Function Box](lispfun-box)
> - [Sequencer Box](sequencer-box)


------

## Global Abstraction

**A "global abstraction" is included in apatch, but exists as a self-standing document on the disk.**

To create a new (global) abstraction, first create a file with the main _File/New..._ menu items (or the <kbd>Ctrl/⌘</kbd> + <kbd>S</kbd> shortcut for a patch), or find an existing one to include in the patch.

To include an existing abstraction in a patch, you can use one of the following options:

1. Drag the corresponding file (**.opat**, **.olsp**, **.omaq**) from your system Desktop manager.
2. Use the menu "Box/Add Box/External abstraction", click somewhere in the container patch and select a .opat file from the file-chooser dialog. 
3. Type <kbd>P</kbd> and enter the name or full pathname of the file.

<img src="./images/create-abs-patch-box.png"> 

In (3) either the name of the file or its _pathname_ (i.e. file location, with folders separated by a "/") can be specified. The search locations are:

- The folder where the current container patch is located.
- The "search path" specified in the "File and folders" [preferences](preferences).

<img src="./images/preferences-search-path.png"> 

### Finding / changing the location of an abstraction

> Global abstractions are convenient as they allow a same file to be reused at several places. They are the true way of dealing with modularity in a program, since they are really independant of their caller environment and context.
>
> The drawback is that they need to be always reachable and found, and the relative-pathname link and be easily broken by simply moving or renaming the patch file.

The full reference pathname of an abstraction box can be read in the [inspector panel](inspector).

<img src="./images/abs-pathname.png"> 

This pathname can be changed or edited: if it is changed to another existing file, the patch box will now make reference to this new abstaction.

A patch box with lost abstraction will display in red, as well as the pathname field in the inspector panel. Use this field to edit and restore the abstraction pathname.

<img src="./images/abs-lost.png"> 

> In order to avoid loosing tracks of abstractions, patches and dependencies should either be moved and transfered jointly in a same folder, or placed in the search path specified in the "File" [Preferences](preferences).


### Copies and multiple references

A global abstraction points to a unique function defined by the referenced document.    
As a consequence, **all the instances and copies of a global abstraction point to the same reference**.

### Save

Save modifications in an abstraction editor using the standard command <kbd>Ctrl/⌘</kbd> + <kbd>S</kbd> in its editor window.   
&rarr; Saved changes will apply to all the abstraction boxes referring to it.

> If a patch abstraction contains other global abstractions, **saving it will _not_ save changes in the documents pointed by these abstraction boxes**.

### Internalize

**Convert a global abstraction to a local abstraction using the menu "Boxes/Interanlize abstraction(s)" or the keyborad shortcut** <kbd>A</kbd>.

> Internalizing a global abtraction box makes a local copy and attaches it to the box.    
_The link to the original reference is then broken._



------

## Internal Abstraction

**An internal abstraction is defined and embedded _inside_ a patch**: it is stored in it, and not as a standalone document. 

To create an internal patch in another patch, you can use one of the following options:

1. Type "patch", or "p" in the same text field you would use to type a function or class name (displayed with double-click or using the <kbd>N</kbd> keyboard shortcut).     
<img src="images/new-internal-patch.png"> 
2. Use the menu "Box/Add Box/Internal patch", then click somewhere in the container patch to create the new patch box.
3. (_for patches only_) [Encapsulate](patch-box#encapsulation) some boxes that are already in the container patch, using <kbd>shift</kbd> + <kbd>E</kbd> (see paragraph below).
     


### Renaming an internal abstraction

Internal abstractions are not bound to any external reference and therefore can be renamed at anytime without any consequence on the execution.    
There are two ways of changing the name of an internal abstraction:
1. Double-click on the name text-field on the box.     
<img src="images/patch-box-rename.png"> 
2. Use the "Name" property in the [inspector panel](inspector).     
<img src="images/patch-box-name.png">

### Copies and multiple references

An internal abstraction refers to a function that is defined locally.   
As a consequence, **each copy of an internal abstraction box points to a new copy of the reference**. 
Copies do _not_ maintain any link (except if they contain common [global abstractions](#global-abstraction)!)

### Save

Changes to an internal abstraction can not be saved locally, as they do not correspond to a file on the disk.    
&rarr; **The "Save" command <kbd>Ctrl/⌘</kbd> + <kbd>S</kbd> in the respective editor window will apply to the container document.** 

> If the patch is encapsulated in multiple successive abstractions, the "Save" command applies to the first global patch/document in the stack of containers. 

### Externalize / Save internal abstractions as new file

The "File / Externalize" menu or the <kbd>Ctrl/⌘</kbd> + <kbd>shift</kbd> + <kbd>S</kbd> shortcut (similar to "Save as...") allow you to create a new file on the disk corresponding to the edited internal abstraction, and attach the corresponding box to the newly created file.   
&rarr; **The box becomes a _global_ abstraction.**


------

## Evaluation

Abstraction boxes display the inputs and outputs of the abstraction, to be connected to other boxes in the container program. 
They are internally compiled and [evaluate](eval) just like [functions](function-box). 

> !! If the abstraction has several outputs, each output evaluation might trigger to a new evaluation of the whole patch. 
&rarr; See how to handle this in OM# **[eval-once mechanisms](eval-once)**.





