# 🔍 Lab 37 — BFS/DFS Implementation

This lab introduces two fundamental graph traversal algorithms: **Breadth-First Search (BFS)** and **Depth-First Search (DFS)**.

You will represent a graph using adjacency lists, implement both traversal algorithms, and compare their traversal strategies and use cases.

---

## 🎯 Objective

By completing this lab, you will:

- Understand graph data structures.
- Represent a graph using adjacency lists.
- Understand Breadth-First Search.
- Implement BFS in Python.
- Understand Depth-First Search.
- Implement DFS in Python.
- Compare BFS and DFS traversal strategies.
- Identify common use cases for both algorithms.

---

## 📚 Prerequisites

- Basic understanding of graph theory.
- Familiarity with Python functions.
- Familiarity with loops.
- Understanding of lists and dictionaries.
- Basic knowledge of data structures.

---

## 🧠 Introduction

Graph traversal algorithms are used to systematically explore nodes and connections within a graph.

Two important traversal strategies are:

- Breadth-First Search (BFS)
- Depth-First Search (DFS)

Both algorithms can explore the same graph but use different strategies.

---

# 🕸️ Task 1 — Graph Representation

Represent a graph using a dictionary of adjacency lists.

```python
graph = {
    'A': ['B', 'C'],
    'B': ['D', 'E'],
    'C': ['F'],
    'D': [],
    'E': ['F'],
    'F': []
}
```

Each key represents a node.

The corresponding list contains the nodes directly connected to it.

---

## 🧠 Key Concept — Adjacency List

An adjacency list is a collection of lists used to represent a graph.

Each node has a list containing its neighboring nodes.

This provides a practical representation for many graph problems.

---

# 🌊 Task 2 — Implement Breadth-First Search

BFS explores nodes based on their distance from the starting node.

It uses a queue.

Import `deque`:

```python
from collections import deque
```

Create the BFS function:

```python
def bfs(start_node, graph):
    visited = set()
    queue = deque([start_node])

    while queue:
        node = queue.popleft()

        if node not in visited:
            print(node, end=' ')
            visited.add(node)

            queue.extend(
                [n for n in graph[node] if n not in visited]
            )
```

---

## 🧠 BFS Key Concept — Queue

BFS uses a queue so that nodes are explored in the order they were discovered.

The general process is:

1. Add the starting node to the queue.
2. Remove a node from the queue.
3. Mark it as visited.
4. Add its unvisited neighbors.
5. Continue until the queue is empty.

---

# 🧭 Task 3 — Implement Depth-First Search

DFS explores one branch as deeply as possible before backtracking.

The supplied implementation uses recursion.

```python
def dfs(node, graph, visited=None):
    if visited is None:
        visited = set()

    if node not in visited:
        print(node, end=' ')
        visited.add(node)

        for neighbor in graph[node]:
            dfs(neighbor, graph, visited)
```

---

## 🧠 DFS Key Concept — Recursion

DFS can use recursion to continue exploring neighboring nodes before returning to previous levels.

The recursive process continues until there are no more unvisited nodes along the current path.

---

# 🧪 Task 4 — Compare BFS and DFS

### Visiting Order

BFS explores nodes based on their distance from the starting point.

DFS explores as far as possible along a branch before backtracking.

### Use Cases

BFS can be useful for:

- Finding shortest paths in unweighted graphs.
- Level-by-level exploration.
- Maze-style shortest-path problems.

DFS can be useful for:

- Exhaustive searches.
- Cycle-related problems.
- Backtracking.
- Exploring connected components.

---

## 📊 BFS vs DFS

| Feature | BFS | DFS |
|---|---|---|
| Main structure | Queue | Recursion/Stack |
| Exploration | Level by level | Deep before backtracking |
| Shortest path in unweighted graph | Suitable | Not generally preferred |
| Backtracking | Less direct | Natural |
| Typical implementation | Iterative | Recursive or iterative |

---

## 🔬 Complete Example

```python
from collections import deque


graph = {
    'A': ['B', 'C'],
    'B': ['D', 'E'],
    'C': ['F'],
    'D': [],
    'E': ['F'],
    'F': []
}


def bfs(start_node, graph):
    visited = set()
    queue = deque([start_node])

    while queue:
        node = queue.popleft()

        if node not in visited:
            print(node, end=' ')
            visited.add(node)
            queue.extend(
                [n for n in graph[node] if n not in visited]
            )


def dfs(node, graph, visited=None):
    if visited is None:
        visited = set()

    if node not in visited:
        print(node, end=' ')
        visited.add(node)

        for neighbor in graph[node]:
            dfs(neighbor, graph, visited)


print("BFS:", end=' ')
bfs('A', graph)

print("\nDFS:", end=' ')
dfs('A', graph)
```

---

## 🛡️ Cybersecurity Perspective

Graphs are useful for representing relationships between entities.

Potential cybersecurity applications include:

- Network topology analysis.
- Asset relationships.
- Dependency analysis.
- Attack-path modeling.
- Connected-component analysis.

For example, a network can be represented as nodes and connections, allowing graph algorithms to explore relationships between systems.

---

## 📸 Evidence / Screenshots

Capture:

- Graph representation in the source code.
- BFS implementation.
- DFS implementation.
- Terminal output showing traversal.
- Comparison between BFS and DFS.

Suggested structure:

```text
37-bfs-dfs-implementation/
├── README.md
└── screenshots/
    ├── graph-code.png
    └── bfs-dfs-output.png
```

---

## ⚠️ Best Practices

- Track visited nodes to avoid unnecessary repeated traversal.
- Understand the graph representation before implementing the algorithm.
- Choose BFS or DFS based on the problem requirements.
- Test algorithms using graphs of different structures.

---

## 🧠 Self-Check

1. What is a graph?
2. What is an adjacency list?
3. What data structure does BFS use?
4. What data structure or technique does DFS commonly use?
5. Why does BFS use a queue?
6. Why does DFS often use recursion?
7. Which algorithm is generally useful for shortest paths in unweighted graphs?
8. Give one practical use case for BFS.
9. Give one practical use case for DFS.

---

## ✅ Completion Checklist

- [ ] Created an adjacency-list graph.
- [ ] Imported `deque`.
- [ ] Implemented BFS.
- [ ] Implemented DFS.
- [ ] Tested both algorithms.
- [ ] Compared traversal strategies.
- [ ] Reviewed cybersecurity applications.
- [ ] Captured useful evidence.

---

## 🏁 Conclusion

In this lab, you learned how to represent graphs using adjacency lists and implemented both BFS and DFS traversal algorithms.

You also compared their traversal strategies and common use cases.

---

## ➡️ Next Lab

**Lab 38 — Parameter Passing & Unpacking**
