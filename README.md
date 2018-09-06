# algo-camp
Survey of Algorithms

This contains a survey of algorithms to facilitate quick review.

## BFS - Breadth First Search

### Data structures:
* Queue
* Set

### Looping algorithm

In graph loop: iterate over each node/vertex in the Graph
* if current node not in Visited Set - perform BFS with it
* add node to new Queue
* In Queue loop:
** pull out node from Queue
** add node to Visited Set
** In adjacent node loop:
*** check each of its adjacent nodes against Set of of Visited nodes
*** if node not in Visited Set, add to end of Queue

### Applications: 
* Shortest path : Unweighted graph, Dijkstra, Bellman-Ford
* Minimal spanning tree : Prim

#### Unweighted graph

##### Data structures:
* Queue
* Distance : vector or map
* Previous vertex : vector or map

#### Dijkstra

##### Data structures:
* Priority Queue
* Distance : vector or map
* Previous vertex : vector or map


#### Prim

##### Data structures:
* Priority Queue
* Distance : vector or map
* Previous vertex : vector or map


## DFS - Depth First Search

### Data structures:
Stack

### Recursive algorithm

### Applications:
* Path discovery




