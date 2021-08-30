# Graphs

## Introduction

A Graph is a non-linear data structure consisting of nodes and edges. The nodes are sometimes also referred to as vertices and the edges are lines or arcs that connect any two nodes in the graph.

> A Graph consists of a finite set of vertices(or nodes) and set of Edges which connect a pair of nodes.

<img src="https://www.geeksforgeeks.org/wp-content/uploads/undirectedgraph-300x130.png" alt="Directed Graph"/>

## Types of graphs

### 1. Directed Graphs:

A directed graph is graph, in which all the edges are **directed** from one vertex to another.

Example of a directed graph with three vertices and four directed edges (the double arrow represents an edge in each direction).

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a2/Directed.svg/800px-Directed.svg.png" alt="Directed Graph" width=150 />

### 2. Undirected Graphs:

An undirected graph is graph, in which all the edges are **bidirectional**.

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/bf/Undirected.svg/800px-Undirected.svg.png" alt="Directed Graph" width=150 />

## Representation of Graphs

A graph can be reprecented using

1. [Adjacency Matrix](#adjacency-matrix)
2. [Adjacency List](#adjacency-list)

#### 1. Adjacency Matrix:

An adjacency matrix is a square matrix used to represent a graph. The adjacency matrix is a (0,1)-matrix with zeros on its diagonal.

> The size of the matrix is `VxV` where `V` is the number of vertices in the graph and the value of an entry `A[i][j]` is either 1 or 0 depending on whether there is an edge from vertex `i` to vertex `j`.

| <img src="https://cdn.programiz.com/sites/tutorial2program/files/adjacency-matrix_1.png" alt="Directed Graph"/> |
:---:
| <c> Adjacency List representation </c> |

#### 2. Adjacency List:

An adjacency list represents a graph as an array of linked lists. The index of the array represents a vertex and each element in its linked list represents the other vertices that form an edge with the vertex.

| <img src="https://cdn.programiz.com/sites/tutorial2program/files/adjacency-list.png" alt="Directed Graph"/> |
:---:
| <c> Adjacency List representation </c> |

## Traversal Methods

Mainly there are two types of traversal methods. They are:

- [Breadth First Search (BFS)](#breadth-first-search)
- [Depth First Search (DFC)](#depth-first-search)

### 1. Breadth First Search 

A standard BFS implementation puts each vertex of the graph into one of two categories:

1. Visited
1. Not Visited

The purpose of the algorithm is to mark each vertex as visited while avoiding cycles.

The algorithm works as follows:

1. Start by putting any one of the graph's vertices at the back of a queue.
2. Take the front item of the queue and add it to the visited list.
3. Create a list of that vertex's adjacent nodes. Add the ones which aren't in the visited list to the back of the queue.
4. Keep repeating steps 2 and 3 until the queue is empty.


<table>
  <tr>
    <td rowspan=2>Step 1</td>
    <td><img src="https://cdn.programiz.com/sites/tutorial2program/files/graph-bfs-step-0.png" alt="Step1"></td>
  </tr>
  <tr>
    <td align="center">Undirected graph with 5 vertices</td>
  </tr>
  <tr>
    <td rowspan=2>Step 2</td>
    <td><img src="https://cdn.programiz.com/sites/tutorial2program/files/graph-bfs-step-1.png" alt="Step2"></td>
  </tr>
  <tr>
    <td align="center">Visit start vertex and add its adjacent vertices to queue</td>
  </tr>
  <tr>
    <td rowspan=2>Step 3</td>
    <td><img src="https://cdn.programiz.com/sites/tutorial2program/files/graph-bfs-step-2_2.png" alt="Step3"></td>
  </tr>
  <tr>
    <td align="center">Visit the first neighbour of start node 0, which is 1</td>
  </tr>
  <tr>
    <td rowspan=2>Step 4</td>
    <td><img src="https://cdn.programiz.com/sites/tutorial2program/files/graph-bfs-step-3.png" alt="Step4"></td>
  </tr>
  <tr>
    <td align="center">Visit 2 which was added to queue earlier to add its neighbours</td>
  </tr>
  <tr>
    <td rowspan=2>Step 5</td>
    <td><img src="https://cdn.programiz.com/sites/tutorial2program/files/graph-bfs-step-4.png" alt="Step5"></td>
  </tr>
  <tr>
    <td align="center">4 remains in the queue</td>
  </tr>
  <tr>
    <td rowspan=2 width="85px">Step 6</td>
    <td><img src="https://cdn.programiz.com/sites/tutorial2program/files/graph-bfs-step-5.png" alt="Step6" ></td>
  </tr>
  <tr>
    <td align="center">Visit last remaining item in the stack to check if it has unvisited neighbors</td>
  </tr>
  <tr>
    <td colspan=2 align="center">Since the queue is empty, we have completed the Breadth First Traversal of the graph.</td>
  </tr>
</table>

### 2. Depth First Search

A standard DFS implementation puts each vertex of the graph into one of two categories:

1. Visited
1. Not Visited

The purpose of the algorithm is to mark each vertex as visited while avoiding cycles.

The DFS algorithm works as follows:

1. Start by putting any one of the graph's vertices on top of a stack.
1. Take the top item of the stack and add it to the visited list.
1. Create a list of that vertex's adjacent nodes. Add the ones which aren't in the visited list to the top of the stack.
1. Keep repeating steps 2 and 3 until the stack is empty.


<table>
  <tr>
    <td rowspan=2>Step 1</td>
    <td><img src="https://cdn.programiz.com/sites/tutorial2program/files/graph-dfs-step-0.png" alt="Step1"></td>
  </tr>
  <tr>
    <td align="center">Undirected graph with 5 vertices</td>
  </tr>
  <tr>
    <td rowspan=2>Step 2</td>
    <td><img src="https://cdn.programiz.com/sites/tutorial2program/files/graph-dfs-step-1.png" alt="Step2"></td>
  </tr>
  <tr>
    <td align="center">Visit the element and put it in the visited list</td>
  </tr>
  <tr>
    <td rowspan=2>Step 3</td>
    <td><img src="https://cdn.programiz.com/sites/tutorial2program/files/graph-dfs-step-2.png" alt="Step3"></td>
  </tr>
  <tr>
    <td align="center">Visit the element at the top of stack</td>
  </tr>
  <tr>
    <td rowspan=2>Step 4</td>
    <td><img src="https://cdn.programiz.com/sites/tutorial2program/files/graph-dfs-step-3.png" alt="Step4"></td>
  </tr>
  <tr>
    <td align="center">Vertex 2 has an unvisited adjacent vertex in 4, so we add that to the top of the stack and visit it.</td>
  </tr>
  <tr>
    <td rowspan=2>Step 5</td>
    <td><img src="https://cdn.programiz.com/sites/tutorial2program/files/graph-dfs-step-4.png" alt="Step5"></td>
  </tr>
  <tr>
    <td align="center">Vertex 2 has an unvisited adjacent vertex in 4, so we add that to the top of the stack and visit it.</td>
  </tr>
  <tr>
    <td rowspan=2 width="85px">Step 6</td>
    <td><img src="https://cdn.programiz.com/sites/tutorial2program/files/graph-dfs-step-5.png" alt="Step6" ></td>
  </tr>
  <tr>
    <td align="center">After we visit the last element 3, it doesn't have any unvisited adjacent nodes, so we have completed the Depth First Traversal of the graph.</td>
  </tr>
</table>

# Algorithms

## 1. `makeGraph()`
```c++
template <class T>
void Graph<T>::makeGraph(T )
{
  int i, edges,
}
```


## 2. `BFS(T)`

```c++
template <class T>
void Graph<T>::BFS(T s)
{
  int v;
  for (int i = 0; i <= nodes; i++)
    visited[i] = 0;
  QueueADT<int> q;
  q.enqueue(s);
  visited[s] = 1;
  while (!q.isEmpty()) 
  {
    v = q.dequeue();
    cout << v << "\t";
    for (int i = 0; i <= nodes; i++)
    {
      if (graph[v][i] == 1)
      {
        if (visited[i] == 0)
        {
          q.enqueue(i);
          visited[i] = 1;
        }
      }
    }
  }
}
```

## 3. `DFS(T)`

```c++
template<class T>
void Graph<T>::dfs(int s)
{
   for(i=0; i<nodes; i++)
      visited[i]=0;   
   visit(visited,s); 
}
```
