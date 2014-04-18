---
title: "Computing Transpose"
published: true
morea_id: experience-graph-transpose
morea_type: experience
morea_summary: "Apply transpose under different representations"
morea_sort_order: 1
morea_labels:
 - In class
---

### Computing Transpose Under Different Representations

The **transpose** of a directed graph _G_ = (_V_, _E_) is the graph _G__T_ =
(_V_, _E__T_), where _E__T_ = {(_v_, _u_) such that (_u_, _v_) ∈ _E_}. In
other words, _G__T_ is the graph _G_ with all of its edges reversed.

Algorithms for computing transpose by copying to a new graph are trivial to
write under matrix and adjacency list representations. However, we will be
working with very large graphs and want to avoid copies. Can we transpose a
graph "in place" without making a copy, and minimizing the amount of extra
space needed? What is the time and space cost to do so?

(In the following, you are writing algorithms that work "inside" the ADT: you
are allowed to access the matrix and list representations directly.)

**1.** Describe an efficient algorithm for computing _G__T_ from _G_, _in place_ (don't make a copy), for the _adjacency-matrix_ representation of _G_. Do this by actually _modifying the matrix_. Analyze the space and time requirements of your algorithm. 

**2.** Now describe a way to compute _G__T_ from _G_ under the _adjacency-matrix_ representation _without modifying the matrix_, and by _using only one bit_ of extra storage! Analyze space and time requirements. (_Hint:_ You need only make it _appear_ to the client to be transposed.)

**3.** Describe an efficient algorithm for computing _G__T_ from _G_ using the _adjacency-list_ representation of _G_, using _as little space as possible_. Can you do it "in place"? Analyze the space and time requirements of your algorithm. 

**4.** Now suppose you have an _edge-list_ representation of _G_. What algorithm would efficiently compute _G__T_ with the edge-list, and with what space and time requirements? 


