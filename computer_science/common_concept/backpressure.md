# What is Backpressure

## Definition

`Resistance or force opposing the desired flow of data through software`

Sometimes it could also be used to describe something has the `ability to control backpressure` in case backpressure is inevitable.

## Examples and Solutions

- I/O read is faster than I/O write, making operation that require read then write to clutter in writing.
I/O libraries usually support synchronizing I/O read/write speeds.
- Server A sends requests faster to B than it can process. If possible, slow A down, if not, use buffer. Using buffer will eventually hit the limits but this method can stop other service from being unable to use B (cascading Denial of Service).
- Data comes in faster than it can be rendered. Render multiple data at the same time with rate.

## Approaches

1. Control and adjust the rate (best option)
1. Buffer (limited solution)
1. Drop (last resort)

When selecting which approach to take, use User Experience (UX) as guidance.

## References

- [Backpressure explained — the resisted flow of data through software](https://medium.com/@jayphelps/backpressure-explained-the-flow-of-data-through-software-2350b3e77ce7)
