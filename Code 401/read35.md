# Graphs
## Graphs
* A graph is a non-linear data structure that can be looked at as a collection of vertices (or nodes) potentially connected by line segments named edges.
### common terminology used when working with Graphs:
1. Vertex - A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.

2. Edge - An edge is a connection between two nodes.

3. Neighbor - The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.

4. Degree - The degree of a vertex is the number of edges connected to that vertex.

### Directed vs Undirected
* Undirected Graphs
>An Undirected Graph is a graph where each edge is undirected or bi-directional. This means that the undirected graph does not move in any direction.

* Directed Graphs (Digraph)
>A Directed Graph also called a Digraph is a graph where every edge is directed.

### Complete vs Connected vs Disconnected:
1. There are many different types of graphs. This depends on how connected the graphs are to other node/vertices.

2. The three different types are completed, connected, and disconnected.

#### Complete Graphs
A complete graph is when all nodes are connected to all other nodes.

#### Connected
A connected graph is graph that has all of vertices/nodes have at least one edge.

#### Disconnected
A disconnected graph is a graph where some vertices may not have edges.

* It is complelty possible to have standalone nodes or edges (also known as islands) in a graph data structure.
### Acyclic vs Cyclic:
In addition to undirected and directed graphs, we also have acyclic and cyclic graphs.

#### Acyclic Graph
* An acyclic graph is a directed graph without cycles.

* A cycle is when a node can be traversed through and potentially end up back at itself.

* A directed acyclic graph is also called a DAG. This can also be represented as what we know as a tree.

#### Cyclic Graphs
* A Cyclic graph is a graph that has cycles.

* A cycle is defined as a path of a positive length that starts and ends at the same vertex.

### Graph Representation
We represent graphs through:

* Adjacency Matrix
An Adjacency matrix is represented through a 2-dimensional array. If there are n vertices, then we are looking at an n x n Boolean matrix

Each Row and column represents each vertex of the data structure. The elements of both the column and the row must add up to 1 if there is an edge that connects the two, or zero if there isn’t a connection.

* a sparse graph is when there are very few connections. a dense graph is when there are many connections

* Within an adjacency matrix, an undirected graph will always be symmetric. This is not the case for a directed graph.

* **Adjacency List**
* An adjacency list is the most common way to represent graphs.

* An adjacency list is a collection of linked lists or array that lists all of the other vertices that are connected.

* Adjacency lists make it easy to view if one vertices connects to another.

### Weighted Graphs
* A weighted graph is a graph with numbers assigned to its edges. These numbers are called weights.
* When representing a weighted graph in a matrix, you set the element in the 2D array to represent the actual weight between the two paths. If there is not a connection between the two vertices, you can put a 0, although it is known for some people to put the infinity sign instead.

* Within adjacency lists, you must include both the weight and the name of the adjacent vertex.



### Real World Uses of Graphs
* Graphs are extremely popular when it comes to it’s uses. Here are just a few examples of graphs in use:
* GPS and Mapping
* Driving Directions
* Social Networks
* Airline Traffic
* Netflix uses graphs for suggestions of products