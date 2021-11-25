# Graphs
- non-linear data structure (node or vertices  ) connected by line segments named edges.

## important to know

- Vertex :node
- Edge :a connection between two nodes.
- Neighbor : adjacent nodes
- Degree : the number of edges connected
- sparse graph is when there are very few connections
- dense graph is when there are many connections
- A cycle is when a node can be traversed through and potentially end up back at itself.

# type of Graphs
- Directed vs Undirected:

Undirected:does not move in any direction,
Directed move at another node with a specific requirement of what node should be referenced next.

- Complete vs Connected vs Disconnected

Complete all nodes are connected to all other nodes,Connected all of vertices have at least one edge,  some vertices may not have edges.

- Acyclic vs Cyclic
Acyclic graph without cycles,Cyclic has Cyclic

- Weighted Graphs

Graph Representation

- Adjacency Matrix: matrix is represented through a 2-dimensional array with n vertices we use   n x n Boolean matrix in array if the node have edge take 1
if no take 0
- Adjacency List: list is a collection of linked lists or array that lists all of the other vertices have connectin


## Weighted Graphs
a graph with numbers assigned to its edges.

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/weightGraph.PNG)

- weight matrix
![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/weightMatrix.PNG)
we but weight btween two connection vertices

- Adjacency List
![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/weightList.PNG)
her 
we put all of the other vertices have connectin with its weight


## what the algorithm breadth first traversal looks like:

Enqueue the declared start node into the Queue. Create a loop that will run while the node still has nodes present.
Dequeue the first node from the queue
if the Dequeue‘d node has unvisited child nodes, add the unvisited children to visited set and insert them into the queue.
```
ALGORITHM BreadthFirst(vertex)
    DECLARE nodes <-- new List()
    DECLARE breadth <-- new Queue()
    DECLARE visited <-- new Set()
    breadth.Enqueue(vertex)
    visited.Add(vertex)
    while (breadth is not empty)
        DECLARE front <-- breadth.Dequeue()
        nodes.Add(front)
        for each child in front.Children
            if(child is not visited)
                visited.Add(child)
                breadth.Enqueue(child)   

    return nodes;

```
## The algorithm for a depth first traversal

Push the root node into the stack
Start a while loop while the stack is not empty
Peek at the top node in the stack
If the top node has unvisited children, mark the top node as visited, and then Push any unvisited children back into the stack.
If the top node does not have any unvisited children, Pop that node off the stack
repeat until the stack is empty
Real World Uses of Graphs

1. GPS and Mapping
2. Driving Directions
3. Social Networks
4. Airline Traffic
5. products