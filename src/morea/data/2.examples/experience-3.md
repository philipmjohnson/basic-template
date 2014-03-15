---
title: "More on linear and binary search"
published: true
morea_id: experience-3
morea_type: experience
morea_summary: "Analyze linear and binary search (homework)"
morea_sort_order: 3
morea_labels:
 - Homework
---


## #1. Peer Credit Assignment

### 1 Point Extra Credit for replying

Please list the names of the other members of your peer group for this week
and the number of extra credit points you think they deserve for their
participation in group work on Tuesday and Thursday combined.

  * If three members besides yourself were present at some time, you have a total of 3 points to allocate.
  * If only two members besides yourself were present, you have a total of 4 points to allocate.
  * If only one other member was present, you have a total of 6 points to allocate.
  * You need not allocate all the points available to you. Points allocated to yourself will not be recorded.

## #2. Correctness of `LinearSearch`

### 5 points

**(a)** Show the pseudocode for `LinearSearch` that you will be analyzing. It should be code that you understand and believe is correct, so you may revise your group's solution if you wish. Give each line a number for reference in your analysis.

**(b)** Using a loop invariant, prove that your algorithm is correct. Make sure that your loop invariant fulfills the three necessary properties (page 19).

_(This will be a little tricky because the loop can exit for two reasons.
Rather than complicate your invariant trying to cover the two cases, you might
write a simpler one that gets part of the work done, and reason about the two
exit conditions when you show how the invariant _helps_ to prove
correctness.)_

## #3. Runtime of `BinarySearch`

### 5 points

This problem steps you through a recursion tree analysis of BinarySearch (the
algorithm for searching a sorted array that was reviewed in class) to show
that it is Θ(lg _n_) in the worst case (that is, O(lg _n_) in general). Θ and
"big-O" are concepts introduced in Topic 3: if they are not familiar to you,
just think of this as meaning the longest possible execution on input of size
_n_ will take time proportional to lg _n_.

**(a)** Write the recurrence relation for `BinarySearch`, using the formula T(_n_) = _a_T(_n_/_b_) + D(_n_) + C(_n_). (We'll assume T(1) = some constant _c_, and you can use _c_ to represent other constants as well, since we can choose _c_ to be large enough to work as an upper bound everywhere it is used.)

**(b)** Draw the recursion tree for `BinarySearch`, in the style shown in podcast 2E and in Figure 2.5. (Don't just copy the example for `MergeSort`: it will be incorrect. Make use of the recurrence relation you just wrote!)

**(c)** Using a format similar to the counting argument in Figure 2.5 of the text or of podcast 2E, use the tree to show that `BinarySearch` is Θ(lg _n_) in the worst case. Specifically,

  1. show what the row totals are,
  2. write an expression for the tree height (justifying it), and
  3. use this information to determine the total computation represented by the tree.

Since this problem involves mathematical expressions and diagrams, you may
want to do your work on paper and digitize it (please compress images) and
submit as jpg or pdf. Alternatively, use a drawing program.



