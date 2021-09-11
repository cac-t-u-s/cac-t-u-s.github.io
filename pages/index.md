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
- [Meta-visual programming](meta)


## Player and Time Structures

- [Time-Sequences and Timeline editors](time-sequence)
- [Player](player)

## Sequencer

The **sequencer** is a visual programming tool extending the notion of _patch_ with a temporal dimension.
The geometrical and temporal layout of its contents are programmable and determine a musical form which can be computed, edited, and rendered in time.

- [Sequencer (Box/Document)](sequencer)
- [Sequencer (Editor)](sequencer-editor)
- [Sequencer (Programming)](sequencer-programming)

## Objects and Editors of the Basic Tools Package

- [Break-Point Function – `BPF`](bpf)
- [Break-Point Curve – `BPC`](bpc)
- 3D Curve – `3DC`
- Arrays – `2D-ARRAY` / `CLASS-ARRAY`
- Text Buffer
- `DATA-STREAM`
- [3D objects and `3D-MODEL`](3d-model)

> **&rarr; Explore the "Basic Tools" [package](session#the-packages-library-tab), for instance from the "Function and Classes Reference" (menu "Help"), to discover hundreds of functions dedicated to the processing of lists, and other structured data in this package using arithmetic, combinatorial, and other mathematical or algorithmic methods.**


## Score

OM# provides an extensive set of tools for the manipulation of musical structures, located in the "Score" package.

- Score boxes and editors (general)
- `NOTE`
- `CHORD`
- `CHORD-SEQ`: The classic
- `VOICE` and rhythmic structures
- Polyphonic objects: `MULTI-SEQ` / `POLY`
- Extras: Additional score elements
- `N-CERCLE`: A mathematical tool

## MIDI

MIDI is a standard protocol (and file format) designed for musical software and device to communicate and exchange control data for synthesizers. It includes the high level notions of notes, continuous controllers (volume, pitch bend, panning, etc.)
The MIDI protocol is used in OM# to "play" musical structures: a synthesizer must be connected to receive and render the data into sound.
OM# also provides a set of tools and function to import, process or generate MIDI-encoded data with visual programs.

- MIDI Settings
- [`MIDI-TRACK`](midi-track)
- MIDI tools


## Audio

- Audio Settings
- The `SOUND` box
- Audio tools


## OSC

OSC (Open Sound Control) is a standard format for the communication and data transfer between audio, music, or multimedia devices and applications.

- Sending / Receiving OSC
- OSC data structures

See also the [odot / o.OM external for OM#](https://github.com/cac-t-u-s/o.OM).

## SDIF

- The `SDIFFILE` box
- SDIF tools

## Programming

- [How to write classes and functions](write-code)
- [How to create/adapt an external library](write-library)


