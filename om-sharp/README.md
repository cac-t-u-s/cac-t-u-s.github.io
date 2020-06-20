
**OM#** (om-sharp) is a computer-assisted composition environment derived from [OpenMusic](http://repmus.ircam.fr/openmusic/): a visual programming language dedicated to musical structure generation and processing.     
The visual language is based on [Common Lisp](http://www.gigamonkeys.com/book/introduction-why-lisp.html), and allows to create programs that are interpreted in this language. Visual programs are made by assembling and connecting icons representing Lisp functions and data structures, built-in control structures (e.g. loops), and other program constructs. The visual language can therefore be used for general-purpose programming, and reuse any existing Common Lisp code.  A set of in-built tools and external libraries make it a powerful environment for music composition: various classes implementing musical structures are provided, associated with graphical editors including common music notation, MIDI, OSC, 2D/3D curves, and audio buffers.


------
<img src="./images/icon2.png" height="80px" align="right"> 

### Download

&rarr; OM# is available on [macOS, Windows, and Linux](https://github.com/cac-t-u-s/om-sharp/releases/latest)


------

> ### [Documentation](./pages/index)


------

<img src="./images/lisp.png" width="90pix" margin="10px" align="right">

### Sources

Source repository: <https://github.com/cac-t-u-s/om-sharp/>

-------

### What's new ?

<img src="./images/scores.png" height="180px">
&nbsp;&nbsp;&nbsp;
<img src="./images/mak-tracks.png" height="180px">
&nbsp;&nbsp;&nbsp;
<img src="./images/spat-offline.png" height="180px">


**OM#** includes a brand-new generation of tools and features in your computer-assisted composition environment:

- New [patching interfaces and environment](pages/patch) with easier box inspection / display control / automatic alignment / connections / etc.
- [No workspace](pages/doc-management) to set-up: open your documents and simply organize them in your usual file-system. 
- Interactive visualization of [Lisp code](pages/lisp#getting-the-equivalent-lisp-code-of-a-patch) corresponding to visual programs.
- A native implementation of the [reactive mode](pages/reactive) for visual program execution.
- New [loops](pages/loop). Embed iterative processes in standard patches. Use a collection of new collectors and memory utilities. 
- A new set of [interface components](pages/interface-boxes): list-selection, switch, button, slider, ... / Lock your patch for faster interaction.
- A redesigned [sequencer](pages/maquette) interface including dual program/tracks-based visualization, meta-programming tools, and reactive execution modes.
- Human-readable, easily [editable text format](pages/doc-management#file-format) for patches and other documents. Possibility to read and edit patches as text.
- New **score editors**, BPF/BPC editors, etc. Nicer display. Easier edit. 
- **Collection** : a versatile container handling the storage, visualization and editing of collection of objects.
- A **time-based model** for "executable" objects, including dynamic function execution and data send/transfer possibility.
- Dynamic-memory allocated **audio buffers** (no need to store all your sounds in external files anymore).
- New generation of tools and editors for the representation and manipulation of musical objects (score, sounds, [MIDI tracks](pages/midi-track), temporal data streams, controllers, etc.) 
- A framework for handling **OSC** data and bundles
- ...

&rarr; See also this <a href="https://hal.archives-ouvertes.fr/hal-01567619" target="_blank">ICMC paper</a> (2017) for a quick overview. 

------


### Compatibility

OM# can load patches created in OpenMusic. See the [how to import OpenMusic patches](pages/import-from-om).    
Most OpenMusic external libraries are easily portable (or already ported). See [how to create or adapt a library](pages/write-library).     
Report any problems in porting or converting libraries or patches on the discussion forum (see below).


------


### Help | Bug reports | Community

A [discussion group](https://discussion.forum.ircam.fr/c/om-sharp) is hosted on Ircam Forumnet.     
&rarr; Create an account in order to post questions and replies.    
Subscribe to group notifications using _Watching_ / _Tracking_ and other options.


------

### Externals / Libraries 

External libraries are packages containing additional pieces of code that can be loaded dynamically in an OM# session. A few of them are readily available and listed below, as well as a number of compatible OpenMusic libraries.


> OM# [external libraries](pages/libraries) are structured as a simple folder, called either "libname" or "libname x.y" (where "libname" is the name of the library, and "x.y" is a version number), containing a loader file named **libname.omlib**.

> &rarr; Unzip the external libraries in a common container directory and specify directory in the Preferences/Libraries/


<table>
<tr>
<th>OM# externals</th>
</tr>
<tr>
<td>
<ul>
  <li><a href="https://github.com/cac-t-u-s/csound/releases" target="_blank">csound</a></li>
  <li><a href="https://github.com/cac-t-u-s/o.OM/releases" target="_blank">odot</a></li>
  <li><a href="https://github.com/cac-t-u-s/spat/releases" target="_blank">spat</a></li>
  <li><a href="https://github.com/cac-t-u-s/mathtools/releases" target="_blank">mathtools</a></li>
</ul>
</td>
</tr>
</table>


<table>
<tr>
<th colspan="2" align="center">Compatible OpenMusic libraries</th>
</tr>

<tr>
<td>
<i>"Classic" libraries</i>
</td>
<td>
<i>Connection with external/DSP tools</i>
</td>
</tr>

<tr>
<td>
<ul>
  <li> <a href="https://github.com/openmusic-project/Repmus" target="_blank">Repmus</a></li>
  <li> <a href="https://github.com/openmusic-project/Chaos" target="_blank">Chaos</a></li>
  <li> <a href="https://github.com/openmusic-project/Alea" target="_blank">Alea</a></li>
  <li> <a href="https://github.com/openmusic-project/Esquisse" target="_blank">Esquisse</a></li>
  <li> <a href="https://github.com/openmusic-project/Profile" target="_blank">Profile</a></li>
  <li> <a href="https://github.com/openmusic-project/LZ" target="_blank">LZ</a></li>
  <li> <a href="https://github.com/openmusic-project/Filters" target="_blank">Filters</a></li>
  <li> <a href="https://github.com/openmusic-project/Combine" target="_blank">Combine</a></li>
  <li> <a href="https://github.com/openmusic-project/Patterns" target="_blank">Patterns</a></li>
  <li> <a href="https://github.com/openmusic-project/Morphologie" target="_blank">Morphologie</a></li>
  <li> <a href="https://github.com/openmusic-project/OMTimePack" target="_blank">OMTimePack</a></li>
  <li> <a href="https://github.com/openmusic-project/OMCS" target="_blank">OMCS</a></li>
  <li> <a href="https://github.com/openmusic-project/OMRC" target="_blank">OMRC</a></li>
  <li> <a href="https://github.com/openmusic-project/omchroma" target="_blank">OMChroma</a></li>
  <li> <a href="https://github.com/openmusic-project/omai" target="_blank">OMAI</a></li>
</ul>
</td>

<td>
<ul>
  <li> <a href="https://github.com/openmusic-project/om-supervp" target="_blank">OM-SuperVP</a></li>
  <li> <a href="https://github.com/openmusic-project/om-pm2" target="_blank">OM-pm2</a></li>
  <li> <a href="https://github.com/openmusic-project/om-xmm" target="_blank">OM-XMM</a></li>
  <li> <a href="https://github.com/DYCI2/om-dyci2" target="_blank">OM-Dyci2</a></li>
</ul>
</td>


</tr></table>




------

### Publications

This project has been used as a support for research and production in a number of recent projects.
See related papers below:

  * [OM-AI: A Toolkit to Support AI-Based Computer-Assisted Composition Workflows in OpenMusic](https://hal.archives-ouvertes.fr/hal-02126847). Anders Vinjar, Jean Bresson. Sound and Music Computing conference (SMC'19), Málaga, Spain, 2019.
  * [Musical Gesture Recognition Using Machine Learning and Audio Descriptors](https://hal.archives-ouvertes.fr/hal-01839050). Paul Best, Jean Bresson, Diemo Schwarz. International Conference on Content-Based Multimedia Indexing (CBMI'18), La Rochelle, France, 2018.
  * [From Motion to Musical Gesture: Experiments with Machine Learning in Computer-Aided Composition](https://hal.archives-ouvertes.fr/hal-01815988/document). Jean Bresson, Paul Best, Diemo Schwarz, Alireza Farhang. Workshop on Musical Metacreation (MUME2018), Internationa Conference on Computational Creativity (ICCC’18), Salamanca, Spain, 2018.
  * [Symbolist: An Open Authoring Environment for End-user Symbolic Notation](https://hal.archives-ouvertes.fr/hal-01804933/document). Rama Gottfried, Jean Bresson. International Conference on Technologies for Music Notation and Representation (TENOR'18), Montreal, Canada, 2018. 
  * [Next-generation Computer-aided Composition Environment: A New Implementation of OpenMusic](https://hal.archives-ouvertes.fr/hal-01567619/document). Jean Bresson, Dimitri Bouche, Thibaut Carpentier, Diemo Schwarz, Jérémie Garcia. International Computer Music Conference (ICMC’17), Shanghai, China, 2017.
  * [Landschaften – Visualization, Control and Processing of Sounds in 3D Spaces](https://hal.archives-ouvertes.fr/hal-01567629/document). Savannah Agger, Jean Bresson, Thibaut Carpentier. International Computer Music Conference (ICMC’17), Shanghai, China, 2017.
  * [Timed Sequences: A Framework for Computer-Aided Composition with Temporal Structures](https://hal.archives-ouvertes.fr/hal-01484077/document). Jérémie Garcia, Dimitri Bouche, Jean Bresson. International Conference on Technologies for Music Notation and Representation (TENOR’17), A Coruña, Spain, 2017.
  * [Computer-aided Composition of Musical Processes](https://hal.archives-ouvertes.fr/hal-01370792/document). Dimitri Bouche, Jérôme Nika, Alex Chechile, Jean Bresson. Journal of New Music Research, 46(1), 2017.
  * [Interactive-Compositional Authoring of Sound Spatialization](https://hal.inria.fr/hal-01467080/document). Jérémie Garcia, Thibaut Carpentier, Jean Bresson. Journal of New Music Research, 46(1), 2017.
  * [o.OM: Structured-Functional Communication between Computer Music Systems using OSC and Odot](https://hal.archives-ouvertes.fr/hal-01353794/document). Jean Bresson, John MacCallum, Adrian Freed. ACM SIGPLAN Workshop on Functional Art, Music, Modeling & Design (FARM’16), Nara, Japan, 2016.
  * [Towards Interactive Authoring Tools for Composing Spatialization](https://hal.archives-ouvertes.fr/hal-01108709/document). Jérémie Garcia, Jean Bresson, Thibaut Carpentier. IEEE 10th Symposium on 3D User Interfaces (3DUI), Arles, France, 2015.




