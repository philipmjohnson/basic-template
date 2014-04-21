---
title: "Experience all pairs shortest paths"
published: true
morea_id: experience-all-pairs-shortest-paths
morea_type: experience
morea_summary: "Floyd-Warshall and Johnson's algorithm"
morea_sort_order: 1
morea_labels:
 - In class
---

### Floyd-Warshall

**1.** What do the main diagonal entries of the matrix constructed by the Floyd-Warshall algorithm mean? 

**2.** How can we use the diagonal entries to detect negative weight cycles? 

### Johnson's Algorithm

These questions are related to each other. Answering one might help answer the
other.

**3.** We put 0-weighted links from _s_ to every other vertex _v_, so isn't δ(_s_, _v_) always 0? When is it not? 

**4.** Suppose that G=(V,E) has no negative weight edges. What is the relationship between w and ŵ for G, and why? 

**5.** What is the purpose of adding the new vertex _s_ to _V_, to construct _V_'? Why don't we just pick an arbitrary vertex in _V_ to start from? 


