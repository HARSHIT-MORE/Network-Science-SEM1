# Dijkstra Shortest Path Algorithm (Python)

## 📌 Overview
This project implements **Dijkstra’s Shortest Path Algorithm** in Python for an **undirected weighted graph**.  
The program allows users to input graph details (nodes, edges, and weights) and then computes the shortest path distances from a chosen source node to all other nodes.

## 📘 Features
- Uses **adjacency list** representation for the graph.
- Implements Dijkstra using a **min-heap priority queue** (`heapq`).
- Supports **undirected weighted graphs**.
- Fully interactive, user-input driven.
- Outputs shortest distance from the source to every node.

## 🧠 How It Works

### 1️⃣ Graph Construction
The program stores the graph using Python’s `defaultdict(list)`:
node → [(neighbor, weight), ...]

### 2️⃣ Distance Initialization
- A `distances` array is created with all values set to `∞`.
- The distance of the **source node** is set to `0`.

### 3️⃣ Priority Queue (Min-Heap)
The algorithm uses:
(priority_queue) = [(distance, node)]
`heapq` ensures the node with minimum current distance is always extracted first.

### 4️⃣ Relaxation Process
For every neighbor of the current node:
new_distance = current_dist + weight
if new_distance < distances[neighbor]:
update distances[neighbor]
push (new_distance, neighbor) into heap

### 5️⃣ Output
After processing all nodes, the program prints:
Node i: shortest_distance

---

## 📦 Required Libraries
This program uses only **built-in Python libraries**, so no installations are needed.

Imported modules:
- `collections` (for defaultdict)
- `heapq` (for priority queue)

---

## ▶️ Usage

### **Run the program**
```bash
python filename.py
User Input Format:
1)Total number of nodes
2)Total number of edges
3)List of edges in the form:

u v w
u, v = nodes
w = weight
4) Source node

Enter total number of nodes: 5
Enter total number of edges: 6

Enter edges as: node node weight
0 1 4
0 2 1
2 1 2
1 3 1
2 3 5
3 4 3

Enter the source node: 0

Shortest path distances from node 0 :
Node 0: 0
Node 1: 3
Node 2: 1
Node 3: 4
Node 4: 7

