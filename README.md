# Ex-3-Implement-Depth-First-Search-Traversal-of-a-Graph

**Name:** SOWMIYA G

**Register Number:** 2305002023

### Aim:
To Implement Depth First Search Traversal of a Graph using Python 3.

### Theory:

Depth First Traversal (or DFS) for a graph is like Depth First Traversal of a tree. 
The only catch here is that, unlike trees, graphs may contain cycles (a node may be visited twice). 
Use a Boolean visited array to avoid processing a node more than once. 
A graph can have more than one DFS traversal. Depth-first search is an algorithm for traversing or searching trees or graph data structures. 
The algorithm starts at the root node (selecting some arbitrary node as the root node in the case of a graph) and explores as far as possible along each branch before backtracking. 

### Algorithm:
Construct a Graph with Nodes and Edges
Depth First Search Uses Stack and Recursion
Insert a START node to the STACK
Find its Successors Or neighbors and Check whether the node is visited or not
If Not Visited, add it to the STACK. Else Call The Function Again Until No more nodes needs to be visited.

### Program: 
```
from collections import defaultdict def dfs(graph, start, visited, path):
path.append (start)
visited[start] - True for neighbour in graph[start]: if not visited [neighbour]:
dfs(graph, neighbour, visited, path)
return path
graph = defaultdict(list)
n, e = map(int, input("Enter number of nodes and edges (n e) : ").split())
print ("Enter edges (u v):") for i in range (e):
u, v = input(). split()
graph[u] -append (v)
graph[v] -append (u)
print ("Graph:", dict(graph))
start = 'A'
visited = defaultdict(bool)
path = []
traversed_path = dfs (graph, start, visited, path)
print ("DFS Traversal Path:", traversed_path)

```
### Sample Input:
A B
A C
B D
B E
C E
D E

### Sample Output:

Graph: {'A': ['B', 'C'], 'B': ['A', 'D', 'E'], 'C': ['A', 'E'], 'D': ['B', 'E'], 'E': ['B', 'C', 'D']}
DFS Traversal Path: ['A', 'B', 'D', 'E', 'C']

**###Input:**

<img width="442" height="120" alt="image" src="https://github.com/user-attachments/assets/141b1a68-6410-4ebf-bbd8-9eb5054ecaac" />

### Output:

<img width="759" height="37" alt="image" src="https://github.com/user-attachments/assets/913a0ea1-372d-4ad6-b515-4466d3157b5a" />

**Result:**

Thus, The program as excuted successfully.
