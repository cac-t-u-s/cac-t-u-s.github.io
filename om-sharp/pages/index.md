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

> **[How to import OpenMusic patches](import-from-om)**


## Visual Programming


A **patch** is a visual program: the graphical equivalent to a Lisp expression (or of a set of Lisp expressions). It contains **boxes** connected together via patch cords (also simply called **connections**).   

Boxes can represent either **Lisp functions**, other **embedded or external visual programs** (sub-patches), **simple values** or **object constructors**.    

A patch can also include inputs and outputs (to receive arguments or return values when it is embedded in another patch), textual comments, and specific _active_ components (e.g. buttons, sliders, etc.) used to set values and arguments for other boxes.


> Use <kbd>Ctrl/⌘</kbd>+<kbd>N</kbd> to open a new patch window. See **[Document management](doc-management)** for more info on opening/saving/managing patches.

> **[Recap' of basic shortcuts](basic-commands)**


- [Patch Editor \| Basics of Visual Programming](patch)
- [Inspect and Edit Attributes](inspector)
- [Boxes](box)
  - [Value Box](value-box)
  - [Function Box](function-box)
  - [Object Box](objects)
  - [Interface Boxes](interface-boxes)
- [Box Inputs](box-inputs)
- [Connections](connections)
- [Comments](comments)
- [Evaluation](eval)
  - [Box State and Evaluation Modes](eval-modes)
  - [Eval-Once](eval-once)
- [Control Boxes](control)
  - [Sequencing Operations: `seq`](seq)
  - [Basic Iteration: `repeat-n`](repeat-n)
  - [Logical Operators: `and`/`or`](logic)
  - [Conditional: `if`](if)
  - [Multiple Connections: `hub`](hub)
  - [Splitting List Contents: `split`](split)
- [Abstractions](abstraction)
  - [Patch Box](patch-box)
  - [Lisp-Function Box](lispfun-box)
- [Lambda-Functions](lambda)
- [Store and Collect](store-collect)
- [Memory](memory)
- [Global Variables](global-variable)
- [Slot Accessors](slots)
- [Loop](loop)
- [Recursion](recursion)
- [Reactive Processes](reactive)
- [Reading/Writing Files](file-io)


## Objects and Editors from the Basic Package

- BPF / BPC
- 2D-ARRAY / CLASS-ARRAY
- TEXTBUFFER
- DATA-STREAM
- 3DC
- [3D-VIEWER](3D-viewer)

## MIDI

- [MIDI-TRACK](midi-track)

## OSC 

## Score

- NOTE
- CHORD
- CHORD-SEQ
- VOICE
- MULTI-SEQ / POLY
- N-CERCLE

## Audio

- SOUND

## SDIF

- SDIFFILE

## Sequencer

- General presentation
- Maquette Box
- Meta-programming

## Programming

- [How to write classes and functions](write-code)
- [How to create/adapt an external library](write-library)


