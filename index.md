An industry initiative for standardization of Object-Based Audio (OBA) positioning data in live production ecosystems by implementing the Audio Definition Model (ADM) over Open Sound Control (OSC).

## [Current specification](https://immersive-audio-live.github.io/ADM-OSC/html/adm_spec.html) 
## [0.5 draft specification](https://immersive-audio-live.github.io/ADM-OSC/html/adm_spec_0.5_draft.html) 

## Project Originators
[L-Acoustics](https://www.l-acoustics.com/), [FLUX::SE](https://www.flux.audio/), [Radio-France](https://www.radiofrance.com/innovation-nouveaux-formats)

## Project Contributors
[Adamson](http://www.adamsonsystems.com/), [BBC](https://www.bbc.com/), [d&b Audiotechnik](https://www.dbaudio.com/), [DiGiCo](https://digico.biz/), [Dolby](https://www.dolby.com), [Lawo](https://lawo.com/), [Magix](https://www.magix.com/), [Merging Technologies](https://www.merging.com/), [Meyer Sound](https://meyersound.com/), [Steinberg](https://www.steinberg.net/)

## Currently supported in
- SPAT Revolution (FLUX::SE)
- L-ISA Controller (L-Acoustics)
- Ovation (Merging Technologies)
- Nuendo (Steinberg)
- SpaceMap Go (Meyer Sound)
- QLAB 5 (Figure 53)
- Space Controller (Sound Particles)
- Modulo Kinetic (Modulo Pi)
- Iosono (Barco)
- FletcherMachine (Adamson)

## Context
Immersive audio is gaining ground in different industries, from music streaming to gaming, from live sound to broadcast. [ADM](https://adm.ebu.io/) or Audio Definition Model, is becoming a popular standard metadata model in some of these industries, with serialADM used in broadcast or ADM bwf or xml files used in the studio.

## Motivation & goals
* To facilitate the sharing of audio objects metadata between a live ecosystem and a broadcast or studio ecosystem.
* To define a basic layer of interoperability between Object Editors and Object renderers while not aiming at replacing more complete manufacturer specific protocols or grammars.
* To define a direct translation of the most relevant ADM Object Properties onto a communication protocol widely used in the live industry, [OSC](https://opensoundcontrol.stanford.edu/index.html).
* Keeping the grammar scope aligned with the ADM properties.
* Share this proposal with the EBU so they can become a relay, publish and support this initiative.
* Extend this small grammar to more ADM properties (beds, etc.) in the future.

## Why OSC ?
* Lightweight network protocol
* Easy to implement
* Human readable
* Supports wildcards and bundles
* Specification: [Open Sound Control website](http://opensoundcontrol.org/)
* Available in a plethora of professional audio hardware and software devices

## General principles
* Sender (client)
  * Object Editor sending positioning data to one or more receivers.
  * Position data is always normalized 
* Receiver (server)
  * Handles the (optional) local scaling of normalized data: x, y, z, distance
  * The receiver can be a DAW, an ADM renderer, an object editor, a bridge (ADM-OSC <-> sADM)
  
## [Development & test tools](https://github.com/immersive-audio-live/ADM-OSC/blob/main/docs/dev_and_test.md)

## Current status
The current dictionary covers most Object properties from the Audio Definition model.
A more complete dictionary is being discussed to cover the remaining parts of the Audio Definition model.
OSC Live test tool (talker and listener OSC Live test tool) is now available.

## [Current Discussions](https://github.com/immersive-audio-live/ADM-OSC/issues)