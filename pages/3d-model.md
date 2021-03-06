---
layout: docpage
---

# `3D-MODEL`

`3D-MODEL` is an object allowing for the visualization and editing of a set of 3D-objects.


## Construction 

Currently-supported 3D objects are: `3D-LINES`, `3D-CUBE` and `3D-SPHERE`.

- `3D-CUBE` and `3D-SPHERE` can be constructed as "standard" [objects](objects) in OM patches: 

<img src="3d-model_img/3d-model-cubes.png">

- `3D-LINES` shall just be specified as list of values. Their colour is assigned randomly. 

<img src="3d-model_img/3d-model-lines.png">


> **Note:** The `3D-LINES` object will be fully functional in the coming OM# update. In the meantime, it is also possible to create `3D-LINES` from your own Lisp code or functions, in which case the colour, and other aspects of rendering are also accessible. 

The main editing consists in 3D-rotations along different combinations of axes.

> **Note:** For the simple visualization of 3D trajectories, the `[3DC](3dc)` object (eventually in a `[COLLECTION](store-collect#collection)` object) might be easier to use.



<img src="3d-model_img/3d-model.png" width="500" align="right">

## Viewpoint 

Modify the view point by using the mouse "click-and-drag".    
Viewpoint short-cuts:
- <kbd>+</kbd> : Zoom in
- <kbd>-</kbd> : Zoom out
- <kbd>Esc</kbd> : Reinitialize viewpoint
- <kbd>c</kbd> : Change background color

## Rotation

Rotate the data using the slider on the editor GUI, or use the mouse "click-and-drag" + <kbd>shift</kbd> or <kbd>alt</kbd> key pressed.
The editor GUI allow to configure the rotation axes according to the <kbd>shift</kbd> / <kbd>alt</kbd> keys.

Click-drag or double-click on the _center-x_ and _center-y_ frames to set the center of the rotation.

Rotation short-cuts:
- <kbd>&larr;</kbd> <kbd>&rarr;</kbd> <kbd>&uarr;</kbd> <kbd>&darr;</kbd> : move the center of rotation in the x/y plane
- <kbd>O</kbd> : Reinitialize rotations
- <kbd>shift</kbd> + <kbd>O</kbd> : Reinitialize rotation center


## How to use it...

- Use additional inputs of the `3D-MODEL` box to set the rotation values, some scaling factor(s) and/or grid parameters from the OM patch.

- Use the function `get-transformed-data` to output the transformed data out of the viewer in an OM patch. 

- If _filter-off-grid_ is on, the data out of the grid will not be exported in `get-transformed-data`.

> **Note:** Press _Space_ in the editor to activate a [reactive notification](reactive) in the box. 
This will output transformed data out in the patch and update downstream reactive connected boxes.

<center>
<img src="3d-model_img/3d-model-boxes.png" width="400" align="middle">
</center>

