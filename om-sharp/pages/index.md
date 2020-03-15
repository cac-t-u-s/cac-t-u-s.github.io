---
layout: docpage
---

> **OM#** is a visual programming language dedicated to musical structure generation and processing.    
>
> [&rarr; Back to the main project page](..)

## Environment

OM# does not require setting up and maintaining a **workspace**. All documents can be just be opened, copied and shared independently.   

The state and settings of the working environment are controlled from the "Session" and "Preferences" windows.

- [Session window](session)
- [Preferences](preferences)
- [Document management](doc-management)
- [Listener](listener)
- [Writing / loading Lisp code](lisp)
- [External libraries](libraries)
- [Help](help)


## Visual Programming


A **patch** is a visual program: the graphical equivalent to a Lisp expression (or of a set of Lisp expressions). It contains **boxes** connected together via patch cords (also simply called **connections**).   

Boxes can represent either **Lisp functions**, other **embedded or external visual programs** (sub-patches), **simple values** or **object constructors**.    

A patch can also include inputs and outputs (to receive arguments or return values when it is embedded in another patch), textual comments, and specific _active_ components (e.g. buttons, sliders, etc.) used to set values and arguments for other boxes.


> Use <kbd>Ctrl/⌘</kbd>+<kbd>N</kbd> to open a new patch window. See [Document management](doc-management) for more info on opening/saving/managing patches.



- [Patch editor \| Basics of visual programming](patch)
- [Boxes](box)
  - [Value Box](value-box)
  - [Function Box](function-box)
  - [Objects Box](objects)
- [Box inputs](box-inputs)
- [Connections](connections)
- [Evaluation](eval)
- [Abstractions](abstraction)
  - [Patch Box](patch-box)
  - [Lisp-Function Box](lispfun-box)
  - [Maquette Box](maquette-box)
- [Box State and Evaluation modes](eval-modes)
- [Eval-Once](eval-once)
- [Lambda-functions](lambda) 
- [Control boxes]	
- [Loops]	
- [Recursion]	
- [Reactive processes]
- [Interface boxes]
- [Global variables]
- [Memory] 
- [Comments](comments)
- [Inspect and edit attributes](inspector)

> - [Recap' of basic shortcuts](basic-commands)


## Main objects and editors

- BPF / BPC
- 2D-ARRAY / CLASS-ARRAY
- COLLECTION
- TEXTBUFFER
- DATA-STREAM
- [MIDI-TRACK](midi-track)
- NOTE
- CHORD
- CHORD-SEQ
- VOICE
- MULTI-SEQ / POLY
- N-CERCLE
- SOUND
- SDIFFILE
- 3DC
- [3D-VIEWER](3D-viewer)

## General

- Files
- MIDI
- Audio
- OSC
- SDIF 

## Sequencer

- General presentation

## Other (How-to's)

- [How to write classes and functions](write-code)
- [How to create/adapt an external library](write-library)
- [How to import OpenMusic patches](import-from-om)


