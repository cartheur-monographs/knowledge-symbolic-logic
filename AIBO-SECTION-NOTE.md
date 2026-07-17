## AIBO Section Note

Section 4 of the Berkeley-Heiserman paper is stronger now, but the AIBO contribution still needs more intermediate examples in the companion AIBO code paper.

Current concern:

The jump from `Move` to `Football` is probably too large for a first-time reader. `Move` shows monitored action and recovery clearly, but `Football` arrives with a much richer mode structure, more variables, more transitions, and a more complex embodied control pattern. For a reader who is just learning how to see these scripts behaviorally, that leap may feel abrupt.

What to do next in the AIBO code paper:

- Add one or two intermediate examples between `Move` and `Football`.
- `Maze` is the strongest current candidate because it introduces environment-dependent branching and local comparison without yet requiring the reader to absorb the full mode complexity of `Football`.
- Another useful bridge may be a script that shows repeated sensing and reorientation without the full multi-mode pursuit structure.

Why this matters:

The paper's method depends on helping the reader learn a graded behavioral vocabulary. If the examples rise too quickly in complexity, the method looks asserted rather than taught. More intermediate cases would make the ladder from activation, to monitored action, to decision loops, to mode-based embodied control easier to follow.
