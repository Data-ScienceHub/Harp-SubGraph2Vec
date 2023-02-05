



# Background



### induced graph

Induced subgraph of a graph is another graph, formed from a subset of the vertices of the graph and all of the edges (from the original graph) connecting pairs of vertices in that subset.





# Color-coding Algorithm

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







