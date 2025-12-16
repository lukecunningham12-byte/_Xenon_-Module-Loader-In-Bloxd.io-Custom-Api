```
/**
 * Get a snapshot list of all active timers (timeouts + intervals).
 *
 * @returns {{ id: number; type: "timeout" | "interval"; ticksLeft: number; intervalTicks: number }[]}
 */
getTimers()

/**
 * Get a snapshot list of all active intervals.
 *
 * @returns {{ id: number; ticksLeft: number; intervalTicks: number }[]}
 */
getIntervals()

js
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
```

