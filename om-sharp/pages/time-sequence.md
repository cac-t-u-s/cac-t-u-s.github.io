---
layout: docpage
---

# Time Sequences


Most "playable" objects in OM# implement the notion of "time sequence": they can be considered as a sequence of "timed item" (i.e., anything that has a position in time, and evenutally a duration).

Example of "time sequences" are: [`BPF`](bpf), [`BPC`](bpc), [`3DC`](3DC) (all representing a sequence of timed-points), but also [`DATA-STREAM`](data-stream), and its subclasses: [`MIDI-TRACK`](midi-track), [`CHORD-SEQ`](chord-seq), [`VOICE`](voice)...   

Some of them can be edited thanks to a "timeline editor" included in their main editor window.

## Timeline editor

The timeline editor is a simple view representing the timed items as circles on a horizontal line representing time.

<img src="time-sequence_img/timeline.png">


The timeline editor has a horizontal time ruler allowing to scroll and zoom in and out in the time sequence. 

Timed items can be translated in time using mouse drag operations, or using the <kbd>&larr;</kbd> / <kbd>&rarr;</kbd> keys.

<img src="time-sequence_img/timeline-move-point.png">

_The order of the timed items can not be changed_, and translation will always be blocked at the immediate proximity of surrounding timed items.

The timeline editor also allows to add timed-items (whatever they are!) using <kbd>Ctrl/⌘</kbd> + click, to remove them using the <kbd>backspace</kbd> key.

## Timing

The timeline editor supports [player interactions](player), by setting the cursor position (with a double click) and play intervals (by a dragging of the cursor).

<img src="time-sequence_img/timeline-interval.png">

### Un-timed items

Not all the items in a time sequence need to have a fixed time (this is particularly relevant for time sequences like the [`BPC`](bpc) object).     
When an item has no time, its actual timing is calculated by interpolation between the two closest timed items.

Un-timed items are represented by an empty circle. They get a time as soon as they are manually edited from the timeline editor.

<img src="time-sequence_img/timeline-untimed-items.png">


### "Master" timed items

Some items in a time sequence can be set to a status of "master" items, and displayed with an additional circle in the timeline editor.

<img src="time-sequence_img/timeline-master-points.png">

Use the <kbd>M</kbd> key ti set/unset this status.

Moving a _master_ point (using mouse drag operations, or using the <kbd>&larr;</kbd> / <kbd>&rarr;</kbd> keys) stretches/compresses all the timed items situated between this point and its neighbouring master points.

> **Note:** The first and last items of a sequence are always considered as "master" points.

