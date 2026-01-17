---
layout: page
title: Search Algorithms
description: Comparing Dijkstra’s and A* algorithms for solving the sliding tile puzzle (N-puzzle)
img: assets/img/1.jpg
importance: 1
category: Software
---

## Overview

This project explores and compares two classic **graph search algorithms**—**Dijkstra’s (Uniform-Cost Search)** and **A\***—as applied to the **sliding tile puzzle (N-puzzle)**. Both algorithms search the puzzle’s state space to find a sequence of moves that transforms an initial configuration into the goal state.

The page below presents a side-by-side comparison highlighting how each algorithm operates, their strengths, and their performance characteristics.

---

<div class="row">

  <!-- Left column: Dijkstra -->
  <div class="col-md-6 mt-3">
    <h3>Dijkstra’s Algorithm (Uniform-Cost Search)</h3>

    <p>
      Dijkstra’s algorithm treats each puzzle configuration as a node in a graph
      and expands states in order of increasing path cost. Since all moves have
      equal cost, this approach is equivalent to a breadth-first search implemented
      with a priority queue.
    </p>

    <ul>
      <li>Search type: Uninformed</li>
      <li>Cost function: Path length (g)</li>
      <li>Guarantees shortest solution: Yes</li>
      <li>Data structure: Min-heap / priority queue</li>
    </ul>

    <p>
      While reliable and optimal, Dijkstra’s algorithm can be slow for larger
      puzzles because it explores many unnecessary states before reaching the goal.
    </p>
  </div>

  <!-- Right column: A* -->
  <div class="col-md-6 mt-3">
    <h3>A* Search Algorithm</h3>

    <p>
      A* improves upon uniform-cost search by incorporating a heuristic to guide
      exploration. In this project, the heuristic is the <strong>Manhattan distance</strong>,
      which estimates how far each tile is from its goal position.
    </p>

    <ul>
      <li>Search type: Informed</li>
      <li>Cost function: f = g + h</li>
      <li>Heuristic: Manhattan distance</li>
      <li>Guarantees shortest solution: Yes (with admissible heuristic)</li>
    </ul>

    <p>
      By prioritizing states that appear closer to the goal, A* typically explores
      far fewer nodes than Dijkstra’s algorithm, resulting in faster solutions.
    </p>
  </div>

</div>

---

## Key Takeaways

- Both algorithms perform **state-space search** on the N-puzzle
- Dijkstra’s algorithm is simple and optimal but explores more states
- A* is both optimal and more efficient due to heuristic guidance
- Heuristic quality directly impacts A* performance

This comparison highlights the practical advantages of informed search algorithms
for combinatorial problems like the sliding tile puzzle.
