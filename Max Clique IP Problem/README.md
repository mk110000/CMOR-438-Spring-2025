# Maximum Clique Integer Program

This algorithm formulates the maximum clique problem as an integer program. Each node in the graph is associated with a binary variable indicating whether it is included in the clique. Constraints ensure that only mutually connected (adjacent) nodes can be selected together. The objective is to maximize the number of selected nodes (the size of the clique).

## Key Concepts

- **Clique:** A group of nodes where every node is connected to every other node in the group.  
- **Maximum Clique:** The biggest possible clique in the graph.  
- **Integer Programming:** A type of optimization that uses variables limited to whole numbers—here, just 0 or 1 (binary).

## Goal

To find the largest set of mutually connected nodes (a maximum clique) in a randomly generated graph using linear programming (specifically, binary integer programming with PuLP), and to visualize this clique within the graph using a different color.