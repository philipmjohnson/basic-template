---
title: "Binary Search"
published: true
morea_id: experience-2
morea_type: experience
morea_summary: "Analyze binary search"
morea_sort_order: 1
morea_labels:
 - In class
---

## In Class: Mixing and Matching with `BinarySearch`

####  5 points

**1\. (1 pt):** The while loop of `InsertionSort` uses a Θ(_n_) linear search to scan backwards through the sorted subarray A[1 .. _j_-1]. Since this subarray is sorted, can we use `BinarySearch` for this search to improve the overall worst case running time of InsertionSort to Θ(_n_ lg _n_)? If yes, argue why the hybrid algorithm would be Θ(_n_ lg _n_). If no, explain why it won't work. 

**2\. (4 pts):** We know from Tuesday's class work that `LinearSearch` is Θ(_n_), so one might think it is always better to use the Θ(lg _n_) `BinarySearch`. However, in order to apply `BinarySearch` we have to sort the data, which (we will soon learn) requires Θ(_n_ lg _n_) time for the best known algorithms (e.g., `MergeSort`). This question explores when it is worth paying this extra cost of sorting the data in order to get fast search.

Suppose you will be **searching a list of _n_ items _m_ times**. When is _m_
big enough relative to _n_ to make it worth sorting and using binary search
rather than just using linear search?

We have two alternatives. Simply using `LinearSearch` _m_ times on _n_ items
has an expected (average) cost of Θ(_mn_). The second alternative is (a)
below, and (b)-(d) explore the tradeoffs.

**a.** What is the expected cost to apply `MergeSort` once to sort _n_ items, and then apply `BinarySearch` _m_ times to _n_ items? 

**b.** Suppose _m_ = 1: which strategy is better, and why? Use the above expressions to justify your answer mathematically. 

**c.** Suppose _n_ = _m_: which strategy is better, and why? Use the above expressions to justify your answer mathematically. 

**d.** What is the cutoff point in terms of _m_ expressed as a function of _n_ between when it is faster to just apply the linear search and when it is faster to apply MergeSort? (Set up an equation and solve for m.) 

(Comment: a more accurate analysis would take into account the different
constants associated with each algorithm: `MergeSort` has a higher constant.
But it can be hard to know the numerical value of the constant to be used in
the analysis. So, if you are really concerned about performance, once the
analysis gives you the ballpark tradeoff, empirical studies can be used to
decide the best cutoff for a given implementation.)


