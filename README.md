# algo-camp
Survey of Algorithms

This contains a survey of algorithms to facilitate quick review.

## BFS - Breadth First Search

### Data structures:
* Queue
* Set

### Looping algorithm

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

---
### Prim

#### Data structures:
* Priority Queue
* Distance : vector or map
* Previous vertex : vector or map


## DFS - Depth First Search

### Data structures:
Stack

### Recursive algorithm

### Applications:
* Path discovery




