---
title: "Experience maximum flow"
published: true
morea_id: experience-maximum-flow
morea_type: experience
morea_summary: "maximum flow"
morea_sort_order: 1
morea_labels:
 - In class
---

## Flow 

**1.** (2 pts) Suppose that _f_1 and _f_2 are flows in a network _G_ (NOT in the residual graph). Assume that _f_1 and _f_2 individually satisfy the conservation property and capacity constraints, and we computed the augmented flow _f_1↑_f_2. 

**(a)** Does this augmented flow _f_1↑_f_2 necessarily satisfy the conservation property? Show why (proof) or why not (counter-example).

**(b)** Does _f_1↑_f_2 necessarily satisfy the capacity constraint? Show why (proof) or why not (counter-example).

**(c)** How does finding augmented flows in the residual graph _G__f_ prevent the problem you identified in one of the above questions?

**2.** (3 pts) Professor Addams' children, Pugsley and Wednesday, dislike each other intensely. When walking to school (they go to the same school), they refuse to walk down any block that the other child has walked down, though strangely they have no problem crossing the same corner. Professor Addams wants to figure out how to get his children to school. Fortunately both their house and the school are on corners. The professor has a map of his town. Show how to formulate the problem of determining whether both of his children can go to the same school as a maximum flow problem. 

_Note: If you answer with either "yes they can go to school" or "no they
cannot go to school" you will get 0 points for this question, as you cannot
solve the problem without the map. You are showing the Professor how to model
the problem as a flow problem so that he can solve it using his map._

#### If you have more time, discuss this problem:

**3.** Suppose that, in addition to edge capacities, a flow network has **vertex capacities**. We will extend the capacity function _c_ to work on vertices as well as edges: _c_(_v_) gives the amount of flow that can pass through _v_. How would you transform a flow network _G_=(_V_,_E_) with vertex capacities into an equivalent flow network _G_*=(_V*_,_E*_) and a _c*_ that is defined only on edges (without vertex capacities) such that a maximum flow in _G*_ has the same value as a maximum flow in _G_.   


