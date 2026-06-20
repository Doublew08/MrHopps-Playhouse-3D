# Mr. Hopp's Playhouse 3D

<p align="center">
  <b>A 3D mechanical translation of the 2D indie horror game Mr. Hopp's Playhouse.</b><br/>
  <i>Adapts 2D stealth mechanics into a 3D finite state machine for enemy AI.</i>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Unity-2022.3%2B-black?logo=unity" alt="Unity Version">
  <img src="https://img.shields.io/badge/C%23-10.0-blue?logo=c-sharp" alt="C# Version">
</p>

---

*Mr. Hopp's Playhouse 3D* is a fan-made, three-dimensional reimagining of the original 2D side-scrolling stealth horror game. Transitioning from 2D to 3D requires fundamentally redesigning the stealth AI and level geometry. Instead of simple line-of-sight on a 2D plane, this project utilizes custom raycast-based vision cones, baked static lighting, and vertical puzzle design to preserve the tension of the original game in a fully navigable 3D space.

## Architecture

The core of the stealth experience relies on a custom Finite State Machine (FSM) governing the enemy AI.

1. **Vision System**: Enemy entities use sweeping 3D raycasts to detect the player, factoring in occlusion from environmental props and lighting conditions.
2. **State Machine**: The AI transitions between Patrol, Investigate, Chase, and Attack states based on audio and visual stimuli.
3. **Lighting & Optimization**: To maintain high framerates in a horror environment, static geometry lighting is baked, while real-time lights are aggressively culled using Unity's occlusion culling.

---

## Status

- [x] Level design and 3D modeling
- [x] Core player controller (movement, crouch, hide)
- [x] Basic FSM AI architecture
- [x] Raycast vision cones and occlusion
- [x] Audio engine integration (footsteps, ambient, jump scares)

---

## Build

Clone the repository and open the project using Unity Hub.

``bash
git clone https://github.com/Doublew08/MrHopps-Playhouse-3D.git
``

Requires **Unity 2022.3 LTS** or newer. Ensure all packages in the Package Manager are restored before entering Play Mode.

---

## References

- Moonbit Studios. *Mr. Hopp's Playhouse*. 
- Unity Documentation: *Finite State Machines in C#*.

License: MIT.