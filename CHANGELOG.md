# CHANGELOG

## 2.0.0

**Breaking change:** the `Time` field has been dropped (it was an optional field according to the [mozlog specification](https://wiki.mozilla.org/Firefox/Services/Logging) anyway).

**Breaking change:** the `Timestamp` field now receives the value of the `time` field of a `pino` log. Before, `pino-mozlog` was "converting" `time` from milliseconds to nanoseconds (`time * 1000000`). Now, `pino` logs MUST have `time` values in nanoseconds.
