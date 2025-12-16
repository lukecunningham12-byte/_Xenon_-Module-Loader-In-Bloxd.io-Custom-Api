# Custom API Reference

This document lists APIs added by the Xenon Module Loader.  
These APIs behave like native Bloxd APIs and are available inside module code.

All timers are **tick-based** and execute during `tick`.

---

## Timers

```js
/**
 * Schedule a function to run once after a delay.
 *
 * @param {Function} callback
 * @param {number} delay
 * @param {"ms" | "s"} [unit] - Optional time unit (defaults to ticks)
 * @returns {number}
 */
setTimeout(callback, delay, unit)

/**
 * Cancel a timeout created with setTimeout.
 *
 * @param {number} timerId
 * @returns {void}
 */
clearTimeout(timerId)

/**
 * Schedule a function to run repeatedly.
 *
 * @param {Function} callback
 * @param {number} delay
 * @param {"ms" | "s"} [unit] - Optional time unit (defaults to ticks)
 * @returns {number}
 */
setInterval(callback, delay, unit)

/**
 * Cancel an interval created with setInterval.
 *
 * @param {number} timerId
 * @returns {void}
 */
clearInterval(timerId)
