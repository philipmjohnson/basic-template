---
title: "Linear Search"
published: true
morea_id: experience-1
morea_type: experience
morea_summary: "Analyze the linear search algorithm"
morea_sort_order: 1
morea_labels:
 - In class
---

## In Class: Linear Search

#### 5 points

1. Consider the **searching problem**:

Input:

     A sequence of _n_ numbers _A_ = ⟨ _a_1, _a_2, .... _a__n_ ⟩ (in _no particular order_), and a value _v_.

Output:

     An index _i_ such that _v_ = _A_[_i_] or the special value NIL if _v_ does not appear in _A_.

**a. (1 pt):** Write pseudocode for `LinearSearch(A,v)`, an algorithm that scans through sequence _A_ looking for _v_, and provides the desired output (_i_ or NIL). Use Java style 0-based indexing, A[_i_] to access elements, and A.length to get _n_. 

**b. (2 pts):** Let **_p_** be the number of array positions checked. (_p_ will be replaced with a function of _n_. For example, when the element is not present, _p_ = _n_.) Let _c_1 be the cost of executing line 1, _c_2 the cost of executing line 2, etc. As was done in the lecture notes: 

  * Write the expression for the cost to execute each line in terms of _p_ and the _c__i_. 
  * Sum these to get the total cost _T_(_n_). 
  * Then collect the constants and rename them "a" and "b".

**c. (1 pt):** What is _p_ for the _worst case_: precisely how many elements of the input sequence need to be checked? 

  * Rewrite your last expression for this _p_. 
  * In what Θ (Theta) complexity class is this? (Write as Θ(____).) 

**d. (1pt):** What is _p_ for the _average case_: precisely how many elements of the input sequence need to be checked on average, assuming that the element being searched for is present and equally likely to be any element in the array? 

  * Rewrite your expression for this _p_. 
  * In what Θ (Theta) complexity class is this? (Write as Θ (____).) 

Justify all your answers!

