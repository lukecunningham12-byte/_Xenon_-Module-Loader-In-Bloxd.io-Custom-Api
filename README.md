# _Xenon_-Module-Loader-In-Bloxd.io-Custom-Api


This world code lets you write “modules” inside code blocks placed at specific coordinates.  
The loader reads the block text, compiles allowed callback functions, and runs them when events happen.

## How modules are stored
Edit `mods.moduleCoords` in world code:
```js
mods.moduleCoords = [
  [0, 0, 0],
  // [x, y, z], add more modules here
];

## How to write modules (IMPORTANT CONCEPT)

### Think of this like normal world code — with one key difference

You write module code **the same way you would write world code**:

- You define callbacks like `onPlayerJoin`, `tick`, `onPlayerChat`
- You write normal JavaScript inside them
- You can call `api.*` exactly like usual

**The difference:**  
Callbacks in modules **do NOT overwrite each other**.

Instead:
- Every time a callback name appears in a module, it is **added**
- When the event happens, **all matching callbacks run**

---

## Multiple callbacks are allowed (and expected)

In normal world code, this would break things:

```js
onPlayerJoin = () => { api.broadcastMessage("A"); };
onPlayerJoin = () => { api.broadcastMessage("B"); };
