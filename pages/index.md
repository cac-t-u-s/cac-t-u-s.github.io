---
layout: docpage
---

> **OM#** is a visual programming language dedicated to musical structure generation and processing.
>
> [&rarr; Back to the main project page](..)

## Environment

The main state and settings of the working environment in OM# are controlled from the "Session" and "Preferences" windows.

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


## Player and Temporal Structures

- [Time-sequences and Timeline Editor](time-sequence)
- [Player and Playable Objects](player)
- [`DATA-TRACK`](data-track)

## Sequencer

The **sequencer** is a visual programming tool extending the notion of _patch_ with a temporal dimension.
The geometrical and temporal layout of its contents are programmable and determine a musical form which can be computed, edited, and rendered in time.

- [Sequencer (Box/Document)](sequencer)
- [Sequencer (Editor)](sequencer-editor)
- [Sequencer (Programming)](sequencer-programming)

## Objects and Editors of the Basic Tools Package

- [Break-Point Function – `BPF`](bpf)
- [Break-Point Curve – `BPC`](bpc)
- Arrays: [`2D-ARRAY`](2d-array) – [`CLASS-ARRAY`](class-array)
- [Text - `TEXTBUFFER`](textbuffer)

> &rarr; Explore the "Basic Tools" [package](session#the-packages-library-tab), for instance from the "Function and Classes Reference" (menu "Help"), to discover hundreds of functions dedicated to the processing of lists, and other structured data in this package using arithmetic, combinatorial, and other mathematical or algorithmic methods.

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

> &rarr; See [MIDI Settings](midi-settings) for how to play (and hear!) score objects in OM#.

## MIDI

[MIDI (Musical Instrument Digital Interface)](https://www.midi.org/) is a standard protocol and file format designed for musical software and device to communicate and exchange control data.
The MIDI protocol is used in OM# to "play" musical structures: a synthesizer must be connected to receive and render scores and other musical data.
OM# also provides a set of tools and function to import, process or generate MIDI data.

- [MIDI Settings](midi-settings)
- [Important MIDI Concepts](midi-basics)
- [Sending MIDI](midi-out)
- [MIDI Events](midi-events)
- [`MIDI-TRACK`](midi-track)
- [Continuous Controllers](midi-cc)
- [MIDI Mix Console](midi-mix-console)
- [Receiving and Recording MIDI](midi-in)
- [Saving as MIDI](midi-save)

## Audio

Audio programming in Common Lisp is fun, and can even perform pretty well. OM# provides a library of tools which allow manipulating audio files and audio buffers in visual programs. These tools can be combined to implement digital sound processing or associated with other external tools for audio synthesis or analysis.

- [`SOUND` Object](sound)
- [Sound Editor](sound-editor)
- [Audio Settings](audio-settings)
- [Sound Processing](sound-processing)
- [Analysis/Synthesis Libraries](sound-libs)


## Space / 3D

The tools in the 3D package extend the basic tools with data structures, editors and other utilities dediacted to the representation and processing of spatial structures (e.g. trajectories for sound spatialization, or positioning and movements of other objects).

- [3D Curve – `3DC`](3dc)
- [Background elements (BPF/BPC/3DC)](background-element)
- [3D objects and `3D-MODEL`](3d-model)


## OSC

[OSC (OpenSoundControl)](http://opensoundcontrol.org/) is a common data transport specification (or encoding) for realtime message communication among audio, music, or multimedia applications and hardware.

- [OSC Messages and Bundles](osc)
- [Sending OSC](osc-send) 
- [Receiving OSC](osc-receive)

See also the [odot external for OM#](https://github.com/cac-t-u-s/o.OM).

## SDIF

[SDIF (Sound Description Interchange Format)](http://sdif.sourceforge.net/) is a standard for the representation, storage and interchange of a variety of sound descriptions including time-domain, spectral, or sinusoidal models. SDIF consists of a basic data format framework and an extensible set of standard sound descriptions.

- The `SDIFFILE` box
- SDIF tools

## Programming

- [How to write classes and functions](write-code)
- [How to create/adapt an external library](write-library)
