# algo-camp
Survey of Algorithms

This contains a survey of algorithms to facilitate quick review.

## BFS - Breadth First Search

### Data structures:
* Queue
* Set

### Looping algorithm

Build **adjacency set** or **queue** for each node.

In **graph loop:** Iterate over each node/vertex in the Graph
* if current **node** not in **Visited Set** - perform BFS with it
* add **node** to new **Queue**
* In **Queue loop**:
  * pull out **node** from **Queue**
  * Process: print, etc
  * add **node** to **Visited Set**
  * In **adjacent node loop**:
    * check each of its adjacent nodes against **Set of Visited** nodes
    * if **adj-node** not in **Visited Set**, add to end of **Queue**
    
### Applications: 
* Shortest path : Unweighted graph, Dijkstra, Bellman-Ford
* Minimal spanning tree : Prim

---
### Unweighted graph - Shortest Path

#### Data structures:
* Queue
* Distance : vector or map - this is similar to the Visited Set for BFS
* Previous vertex : vector or map

#### Looping algorithm

Given vertex/node to find Shortest Path for
* add **node** to **Distance map**: {key=**node**, value=**0**}
* add **node** to **Queue**
* In **Queue loop**:
  * pull out **node** from **Queue**
  * Process: print, etc
  * In **adjacent node loop**:
    * if **adj-node** not in **Distance map**
      * add **adj-node** to **Distance map**: {key=**adj-node**, value=**(1 + Distance.get(node)**}
      * add **adj-node** to **Queue**
      * set **Previous map**: {key=**adj-node**, **node**}
    
---
### Dijkstra - Shortest Path in Weighted graph

#### Data structures:
* Priority Queue
* Distance : vector or map
* Previous vertex : vector or map

#### Looping algorithm

Given a map of **edge weights**.
Given node/vertex to find shortest path from.
* add the **node** to the **PriorityQueue** with value 0
* **Distance map** is set to 0 for the node
* In **PriorityQueue loop**
  * remove **min node** from the **PriorityQueue**
  * In **adjacency loop**
    * calculate **distance** = **Distance.get(node)** + **weight(node, adj-node)**
    * if not **Distance.get(adj-node)**
      * put **adj-node** into the **PriorityQueue** with **weight=distance**
      * update: **Distance.set(adj-node, distance)**
      * update: **Previous.set(adj-node, node)** : { key=**adj-node**, value=**node** }
    * else if **Distance.get(adj-node)** > **distance**
      * found lighter weight path so update **PriorityQueue** for **adj-node** with **weight=distance**
      * update: **Distance.set(adj-node, distance)**
      * reset: **PreviousMap.set(adj-node, node)**

---
### Prim - Minimal Spanning Tree

The Minimal Spanning Tree is a sub-graph of a Graph that contains all the vertices in an undirected Graph.

This algorithm very similar to Dijkstra.

#### Data structures:
* Priority Queue
* Distance : vector or map
* Previous vertex : vector or map

#### Looping algorithm

Given a map of **edge weights**.

Loop through all nodes/vertices in the Graph
  * if **node** not in **Distance map**, add it with weight=0
  * add it to **PriorityQueue** with weight = 0
  * Loop through the **adjacency nodes** 
    * calculate **distance** = **Distance.get(node)** + **weight(node, adj-node)**
    * if not **Distance.get(adj-node)**
      * put **adj-node** into **PriorityQueue**: **PriorityQueue.put(adj-node, distance)**
      * update: **Distance.put(adj-node, weight(node, adj-node))**
      * update: **Previous.put(adj-node, node)**
    * else if **Distance.get(adj-node)** > **distance**
      * update **PriorityQueue** with **adj-node** and **distance**
      * update: **Distance.put(adj-node, weight(node, adj-node))**
      * update: **Previous.put(adj-node, node)**

---
### Kruskal - Minimal Spanning Tree

TODO

---
## DFS - Depth First Search

### Data structures:
Stack

### Recursive algorithm

### Applications:
* Path discovery

---
## Bipartite Graph



