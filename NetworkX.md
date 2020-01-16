# Introduction
NetworkX, as the name suggests, is essentially a Python package which helps you create, manipulate, and analyze complex networks.  

From the official documentation - NetworkX provides the following:
- tools for the study of the structure and dynamics of social, biological, and infrastructure networks;
- a standard programming interface and graph implementation that is suitable for many applications;
- a rapid development environment for collaborative, multidisciplinary projects;
- an interface to existing numerical algorithms and code written in C, C++, and FORTRAN; and
- the ability to painlessly work with large nonstandard data sets.

### Simple steps to start off with NetworkX:

Creating an empty graph:  
```
import networkx as nx
G = nx.Graph()
```

Add Nodes: ``` G.add_node(1) ```

Add Edges: ``` G.add_edge(1,2) ```

Creating Directed Graphs: ``` G.DiGraph() ``` 

Creating Multi Graphs: ``` G.MutliGraph() ```