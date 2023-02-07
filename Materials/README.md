

# **FASCIA**

# Introduction

## Background



### induced graph

Induced subgraph of a graph is another graph, formed from a subset of the vertices of the graph and all of the edges (from the original graph) connecting pairs of vertices in that subset.





## Color-coding Algorithm

1.

Template has **k** nodes

Set **k** colors for nodes

-> **k^k** kinds of color status of templates

-> **k!** kinds of possible **colorful template** **embedding**

=> **P(Template is colorful)  = k! / k^k**

2.

Color each node of graph randomly by these k colors

Then count the number of colorful template embeddings -> **CNT_colorful**



-> Now we could estimate total templates embeddings by:

**CNT_estimate = CNT_colorful / P**

<img src="https://user-images.githubusercontent.com/41974269/216795869-d173509f-2bbe-4da1-964b-da258ad96311.png" alt="image" style="zoom:50%;" />


## Contributions

optimizations for approximation algorithms based on color-coding

* shared-memory and distributed-memory parallelization
* reduce overhead in the inner loops of the algorithm
* simple template partitioning method for subgraph counting.
* data structure to reduce communication and memory costs  in distributed environment



# Implementations for color-coding



##  Subgraph counting with FASCIA

1. template partitioning
2. random coloring
3. dynamic programming count 



### Template Partitioning

**Cut** input template recursively to **sub templates**.

Each cut would produce two childs.



A **partitioning tree** would be formed in this process.

This tree can be traced from the bottom up to the original template   

=> **Dynamic Programming** phase of the color coding algorithm.



### Randomly Colored

K colors

**Trade off:** 

higher K, 

then	  decrease the required iterations

but		increases memory requirements



### Dynamic Programming Count

subtemplate: **S_i**		size = **h**

**color set** is mapping: h unique color -> each vertex in S_i

<img src="https://user-images.githubusercontent.com/41974269/217124889-584fc9b6-6428-49a5-9301-710dd707eb07.png" alt="image" style="zoom:50%;" />

all possible color sets C

split C into Ca and Cp (Ca and Cp have totally different colors)

Each possibility of combination of Ca and Cp has **table[a_i] [v] [C_a] * table[p_i] [u] [C_p]** counts of colorful templates



## Color-coding Optimization

combinatorial index system

careful memory management

partitioning the input template



### Combinatorial indexing system









### Memory utilization optimizations



### Template partitioning



## Shared-memory parallelism

OpenMP

two modes -> depended on size of graph and template size

if size large:



if size small:







## Distributed memory parallelism

