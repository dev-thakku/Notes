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

1. Adjacency Matrix
2. Adjacency List

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
