# Smartdesk Hardware Interface Spec

This document describes how computing hardware is to be integrated into smartdesk furniture. For clarity it uses specific key words such as SHOULD, MAY etc to describe its specifications, their meanings are given [key_word_definitions.md](here).

## Overview

This document describes a loose methodology for mounting small pieces of computing hardware such as Arduinos or Raspberry Pis into furniture to aid interoperability. It MUST NOT be relied on to provide any level of assurance as to the safety or advisability of any particular implementation. If you are mounting electronics into furniture you MUST ensure that your installation is safe and complies with any legislation that applies in your country. 

## Mounting Space Requirements

Any piece of smartdesk furniture MUST provide a clear flat surface for electronics to be mounted on. 
This surface MAY be in any orientation. 
This surface MAY be hidden or exposed.
This surface MUST be large enough to accommodate an enclosure 120mm x 80mm x 40mm mounted with one of its largest faces flush to the surface. This will allow for the mounting of Auduino Uno and Mega boards, all Raspberry Pis, Seeed boards etc.
This surface SHOULD be located to allow for easy access by furniture owners.
Sufficient ventilation MUST be provided for the electronics being mounted.
Consideration MUST be given to how wires will be run to the hardware used, and adequate space allowed for this around the mounting surface.
Four mounting holes MUST be provided on the surface, their centres at the corners of a 100mm x 60mm rectangle centered on the surface as shown in the diagramme below. The holes MUST be either circular drilled holes 6mm in diameter and at lest 10mm deep to accommodate 6mm dowels or M4 threaded inserts. These centres have been chosen for compatibility with the [OpenStructures](http://openstructures.net/) grid.

## Intermediate Mounts

Electronics MUST NOT be mounted directed to the surface of the furniture, an intermediate mount of some kind MUST be used that is attached to the furniture which MUST use the mounting holes described above.
Intermediate mounts MAY be of any size or dimensions but can only rely on furniture providing the space described above.
Intermediate mounts MUST be designed to safely house their electronics, with consideration given to fire risk, heat dissipation and all other safety requirements.
Intermediate mounts SHOULD be designed for ease of access to their components.