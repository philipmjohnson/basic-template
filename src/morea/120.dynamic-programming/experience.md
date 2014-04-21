---
title: "Dynamic programming sample problem: longest simple path"
published: true
morea_id: experience-dynamic-programming
morea_type: experience
morea_summary: "Apply dynamic programming principles to a sample problem"
morea_sort_order: 1
morea_labels:
 - In class
---

# Longest Simple Path in a Directed Acylic Graph

Given a directed weighted acyclic graph G=(V,E) with real valued edge weights
representing the length of each edge and two vertices s (start) and t
(target), develop a dynamic programming approach for finding a longest
weighted simple path from s to t.

Definitions:

  * directed: it has arrows on the edges and you only go in the direction of the arrows 

  * acyclic: one can never get back to where one started

  * path: a sequence of vertices connected by edges, e.g., ⟨u, v, w⟩ when (u,v) and (v,w) are in E. 

  * simple path: a path that does not repeat vertices. 

Note: in a DAG without self loops (v, v) all paths are simple. Well assume no
self loops.

  

Notations:

  * Write |V| for number of vertices and |E| for number of edges. 

  * (u, v) \- the directed edge from vertex to vertex v. 

  * w(u, v) \- the weight on the edge (u, v), here interpreted as length.

  * G.V \- a list of vertices in G. 

  * G.Adj[u] \- a list of edges in G that begin on u (e.g., (u,v), (u,w), (u,x) ). 

Also, lets assume that vertices are named by integers {1, 2,  |V|} so we can
use vertices as indices into arrays. And draw pictures! After all, these are
graphs!

  

Follow these steps:

  

1. Characterize the Structure of an Optimal Solution

  

Since we need to reason about subpaths, well start at u (which can be s or
any other vertex). Let p be a longest path from u to t. If u =  t then p is
simply ⟨u⟩ and has zero weight. Consider when u ≠ t. Then p has at least two
vertices and looks like:

  

p = ⟨u, v  t⟩   (it is possible that v = t).

  

Let p = ⟨v  t⟩ and prove that p must be a longest simple path from v to t.

  
  

2\. Recursively define the value of an optimal solution:

  

Let dist[u] be the distance of a longest path from u to t.  Fill out the
definition to reflect the above structure: (You will need mathematical
notation that is easier to write on paper. Do it on paper first and figure out
Google equations only if you have time):

  

dist[u] =

  

3\. Compute the value of an optimal solution (simple recursive version):

  

Write a recursive procedure that computes the value of an optimal solution as
defined by the above recursive definition. Do not memoize yet; thats the next
step.

  

Longest-Path-Value-Recursive (G, u, t)

  
  

4\. Compute the value of an optimal solution (dynamic programming version):

  

Now memoize your procedure above by passing the array dist[1..|V|] that
records longest path distances dist[u] from each vertex u to t so you dont
have to repeat computations. We will assume that the caller has initialized
all entries of dist to -∞.

  

Longest-Path-Value-Memoized (G, u, t, dist)

  
  

5\. Analyze the runtime of your solution in #4 in terms of |V| and |E|.

  

Include the runtime (a) to initialize dist and (b) of Longest-Path-Value-
Memoized.

  
  

6\. Extra Credit: Recover a Solution

  

Rewrite Longest-Path-Value-Memoized to Longest-Path-Memoized that takes an
additional parameter next[1..|V|], and records the next vertex in the path
from any given vertex u in next[u]. Assume that all entries of next are
initialized to -1 by the caller.

  

Longest-Path-Memoized (G, u, t, dist, next)

  

Once that is done, you can easily write a procedure that recovers (e.g.,
prints) the path from s to t by tracing through next (but you dont need to do
it here).

  

7\. To Think About

  

How would you analyze the runtime of procedure Longest-Path-Recursive in terms
of |V| and |E|? How does it compare to that of Longest-Path-Memoized?



