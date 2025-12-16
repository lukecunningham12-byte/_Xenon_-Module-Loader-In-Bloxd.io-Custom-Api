# _Xenon_-Module-Loader-in-Bloxd.io (Custom API)

This project is a **world-code module loader** for Bloxd.io that lets you write modular logic inside **code blocks placed in the world**.

Instead of one callback overwriting another (normal world code behavior), this system **collects callbacks additively** and runs all of them when events occur.

Think of this as a **plugin system** built entirely in world code.

---

## What this system does

- Reads code from blocks at specific coordinates
- Compiles allowed callbacks from block text
- Allows unlimited modules and unlimited callbacks
- Prevents callbacks from overwriting each other
- Adds a full timer API (`setTimeout`, `setInterval`, etc.)
- Handles unloaded chunks safely
- Reports syntax and runtime errors in-game

---

## How modules are stored

Modules live in **code blocks** at fixed coordinates.

Edit this list in world code:

```js
mods.moduleCoords = [
  [0, 0, 0],
  // [x, y, z] add more module blocks here
];
