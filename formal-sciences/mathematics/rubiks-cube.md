# The Rubik's Cube as a mathematical object

## Summary

The Rubik's Cube has 43,252,003,274,489,856,000 reachable positions, about 4.3 x 10^19, and any of them can be solved in at most 20 moves, a result proved in 2010 and published in 2014. The puzzle is a standard example of a permutation group: its moves are permutations of corner and edge pieces, with rules about orientation. People solve it with memorized algorithms and a layered strategy, and not by search, and speedcubing adds finger tricks and look-ahead.

*This note is educational.*

## Prerequisites

No prior notes are needed.

## Core concepts

### Definition

The cube has 8 corner pieces and 12 edge pieces (the centers are fixed relative to each other). A move turns one face by a quarter or half turn. The set of all sequences of moves forms a *group*: moves can be combined, every move can be undone, and the order of combination matters. Rokicki and colleagues (2014) proved that the diameter of this group is 20 (in the half-turn metric): every position can be solved in 20 moves or fewer, and some positions need 20. This number is called *God's number*.

### Counting positions

The count follows from four facts:

| Factor | Reason |
| --- | --- |
| 8! | Corners can be arranged in any order |
| 3^7 | Each corner has 3 orientations, and the last is fixed by the other seven |
| 12! | Edges can be arranged in any order |
| 2^11 | Each edge has 2 orientations, and the last is fixed by the other eleven |
| Divide by 2 | Corner and edge permutations must have the same parity |

### Analogy

Solving the cube is like sorting a deck of cards with only a few allowed shuffles. Each shuffle moves many cards at once, so fixing one card often disturbs others, and the solution is a recipe of shuffles that cancel their side effects. The limit of the analogy is that the pieces also have orientation.

### Solving

```mermaid
flowchart LR
  C[Cross on the first layer] --> F[First two layers]
  F --> O[Orient the last layer]
  O --> P[Permute the last layer]
```

A beginner method works layer by layer. An *algorithm* is a fixed sequence of moves that changes a few pieces and leaves the solved ones in place, for example the sequence that swaps two edges. Speedcubing methods, such as CFOP, use many such algorithms and efficient finger movement. Solvers learn by chunking and automation (see [memory techniques](../../personal-development/skills/soft-skills/cognitive/memory-techniques.md)), a case of the learning stages in [skill acquisition](../../personal-development/skills/skill-acquisition.md).

## Worked example

The code reproduces the count and shows why brute force is not how people solve it.

```python
# Python 3.12. Size of the Rubik's Cube group: 8 corners, 12 edges, with orientation and parity constraints.
from math import factorial

positions = factorial(8) * 3**7 * factorial(12) * 2**11 // 2
print(positions)
print(f"{positions:.3e}")
print("seconds at one position per second, in years:", round(positions / (3600 * 24 * 365.25) / 1e9), "billion")
```

Output:

```text
43252003274489856000
4.325e+19
seconds at one position per second, in years: 1371 billion
```

Visiting every position at one per second would take about 1,371 billion years, so solving relies on structure: reduce the problem layer by layer, and use algorithms whose effects are known.

## Trade offs and when to use it

The cube is a good teaching tool for groups, parity and algorithmic thinking, and for learning how practice builds fast pattern recognition. Optimal solving (finding the shortest solution) is computationally hard, and human methods use a few dozen moves, not 20.

## Common mistakes

- **Taking God's number as the move count of solvers.** It is the worst case of an optimal solution.
- **Believing that the cube needs luck.** It is deterministic.
- **Memorizing without understanding.** Algorithms make sense once the effect on pieces is clear.

## Practice

1. How many corner pieces and edge pieces does the cube have?
2. What is God's number?
3. Why is the count divided by 2?

### Answers

1. 8 corners and 12 edges.
2. 20: every position can be solved in at most 20 moves.
3. The permutations of corners and edges must have the same parity.

## Further reading

- Rokicki, T., Kociemba, H., Davidson, M. et al. (2014). The Diameter of the Rubik's Cube Group Is Twenty. *SIAM Review*, 56(4), 645-670. [DOI](https://doi.org/10.1137/140973499). Proves that any Rubik's Cube can be solved in 20 moves or fewer.
