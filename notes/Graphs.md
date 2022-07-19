# 1. Definition:
A graph G is a set V of vertices and a set E of edges that connect vertices.
$$G = (V, E)$$

# 2. Types
* Directed
* Undirected

`Digraph`: 有向图。from vertex v to some other vertex w. $e = (v, w)$.

`Undirected`: 无向图。e is an unordered pair.
$(v, w) = (w,v)$.

`Self-edge`: $(v, v)$

`Path`: sequence of vertices with each adjacent pair connected by an edge.If graph is directed, edges must be aligned with direction of path. 

`Length of path`: number of edges in path. <4,5,6,3>: path of length 3. <2>: path of length zero.

`Strongly connected`: There's a path from any vertex to any other vertex (called connected in undirected graph).
任意两个节点都有连接。

`degree`: number of edges incident on vertex ( self-edges count as one) 度

`digraphs`: 入度与出度

* indegree: number of edges directed toward vertex. 

* outdegree: number directed away.

# Graph Representations:
## Adjacency matrix: |v|-by-|v| array of booleans.
两个节点间的连接。

## Adjacency lists:
Each vertex v has a lined list of edges out.

## HashTable
If vertices have names, use hash table to map Strings(or any object).


Adjecency list is more space and time-efficient for a sparse graph, but less efficient for a complete graph.

# Graph traversals
Visits each vertex once.

Each vertex has boolean "visited" filed that tells us if we're visited it before.
## Depth-first search (DFS)
## Breadth-first search (BFS)




