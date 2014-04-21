---
title: "Minimum spanning trees"
published: true
morea_id: experience-minimum-spanning-tree
morea_type: experience
morea_summary: "Basics of minimum spanning trees"
morea_sort_order: 1
morea_labels:
 - In class
---

## Basics of minimum spanning trees

Below is pseudocode for three different algorithms. Each one takes a connected
graph _G_ = (_V_,_E_) and a weight function _w_ as input and returns a set of
edges _T_.

#### Is it an MST algorithm?

For each algorithm, either prove that the set of edges _T_ produced by the
algorithm is always a minimum spanning tree, or find a counter-example where
_T_ is not a minimum spanning tree

**1\. `Maybe-MST-A`**
    
    
    Maybe-MST-A (G, w)
    1  sort the edges into nonincreasing order of edge weights w
    2  T = E
    3  for each edge e, taken in sorted order
    4      if T − {e} is a connected graph
    5          T = T − {e}
    6  return T
    

**2\. `Maybe-MST-B`**
    
    
    Maybe-MST-B (G, w)
    1  T = {} // empty set
    2  for each edge e ∈ E, taken in arbitrary order
    3      if T ∪ {e} has no cycles
    4          T = T ∪ {e}
    5  return T
    

**3\. `Maybe-MST-C`**
    
    
    Maybe-MST-C (G, w)
    1  T = {}
    2  for each edge e ∈ E, taken in arbitrary order
    3      T = T ∪ {e}
    4      if T has a cycle _c_
    5          let e' be a maximum weight edge on c
    6          T = T − {e'}
    7  return T
    

#### Efficient Implementation

**4.** Once you are done, pick on of the above algorithms that you think computes a MST. Then describe an efficient implementation of that algorithm. Each algorithm above uses utility methods such as sorting, testing connectivity, detecting cycles, and finding the maximum weight edge on a cycle. Your response should focus on efficient implementations of these utility methods. 


