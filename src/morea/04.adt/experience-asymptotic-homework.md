---
title: "Asymptotic analysis: Homework"
published: true
morea_id: experience-asymptotic-homework
morea_type: experience
morea_summary: "Practice asymptotic analysis."
morea_sort_order: 2
morea_labels:
 - Homework
---

## Homework Problems

_There are 6 problems for a total of 20 points. Most of them are easier than
they look at first._

_Please consider:_ The homework is really "worth" a lot more than 20 points
because exams have similar problems. If you have not practiced with the
homeworks, you'll do worse on the exams. So, if you think these problems are
not worth the time for the points, think again.

### #1. Peer Credit Assignment

#### 1 Point Extra Credit for replying

Please list the names of the other members of your peer group for this week
and the number of extra credit points you think they deserve for their
participation in group work on Tuesday and Thursday combined.

  * If three members besides yourself were present at some time, you have a total of 3 points to allocate.
  * If only two members besides yourself were present, you have a total of 4 points to allocate.
  * If only one other member was present, you have a total of 6 points to allocate.
  * You need not allocate all the points available to you. Points allocated to yourself will not be recorded.

* * *

### #2. Proving asymptotic complexity

#### 4 points

Using the truth-condition definition of big-O, prove that 3_n_2 \+ 9 =
O(_n_2).

> The definition is the one that starts with "_f_(_n_) = O(_g_(_n_)) iff ...".
You will have to choose suitable _c_ and _n_0, plug them into the definition
in "...", and argue that the condition is met.  
The 4 points are: (1) identification of _c_ and _n_0 that work; (1) writing
out the definition, and (2) demonstrating that it is satsified as _n_ grows
beyond _n_0 (not just for _n_ = _n_0).

* * *

### #3. Relative growth rates of functions

#### 3 points

Continuing in the style of Tuesday's class exercise, fill in the table for
these pairs of functions with "Yes" or "No" in each empty box. Then, for each
row, justify your choice, preferably by showing mathematical relationships
(e.g., transforming one expression into another, or into expressions that are
more easily compared).

<table width="100%" border="1">
  <caption>
    Asymptotic Relations
  </caption>
  <tbody><tr>
    <th scope="col">&nbsp;</th>
    <th scope="col">f(n)</th>
    <th scope="col">g(n)</th>
    <th scope="col">O?</th>
    <th scope="col">o?</th>
    <th scope="col">&#937;?</th>
    <th scope="col">&#969;?</th>
    <th scope="col">&#920;?</th>
  </tr>
  <tr>
    <th scope="row">e.</th>
    <td>4<i>n</i><sup>2</sup></td>
    <td>4<sup>lg <i>n</i></sup></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
  </tr>
  <tr>
    <th scope="row">f.</th>
    <td>2<sup>lg <i>n</i></sup></td>
    <td>lg<sup>2</sup><i>n</i></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
  </tr>
  <tr>
    <th scope="row">g.</th>
    <td>&#8730;<i>n</i></td>
    <td>n<sup>sin <i>n</i></sup></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
  </tr>
</tbody></table>

### #4. Complexity of Dynamic Set Operations in List Implementations

#### 2 points

For each of the four types of lists in the following table, what is the
asymptotic worst-case running time for `predecessor` and `maximum`?

Assume that _k_ is the key, _d_ the data associated with the key, and _p_ a
position in the data structure. This version of the ADT is similar to the
book's, but abstracts list elements _x_ to positions (returned by search).
`predecessor` and `maximum` are with respect to ordering of keys in the set
under "<", NOT ordering of the data structure. Sorted lists are sorted in
ascending order. This continues your in-class work, which you may want to
review for correctness first.

<table width="100%" border="1">
  <caption>
    Worst Case Linked List Operations
  (continued)
  </caption>
  <tbody><tr>
    <th scope="col">&nbsp;</th>
    <th scope="col">Unsorted, Singly Linked (no tail pointer)</th>
    <th scope="col">Sorted, Singly Linked (no tail ponter)</th>
    <th scope="col">Unsorted, Doubly Linked with Sentinel and Tail pointer</th>
    <th scope="col">Sorted, Doubly Linked with Sentinel and Tail pointer</th>
  </tr>
  <tr>
    <th colspan="5" scope="row"><i>... others done in class here ... </i></th>
  </tr>
  <tr>
    <th scope="row">predecessor(p)</th>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
  </tr>
  <tr>
    <th scope="row">maximum()</th>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
  </tr>
</tbody></table>



### #5. Tree Traversals

#### 4 points

_In class you wrote a recursive procedure for traversal of a binary tree in
O(n) time, printing out the keys of the nodes. Here you write two other tree
traversal procedures. The first is a variation of what you wrote in class; the
second is on a different kind of tree that you read about pages 248-249 and in
my lecture notes and screencast._

**(a)** Write an O(_n_)-time **_non-recursive_** procedure that, given an _n_-node binary tree, prints out the key of each node of the tree in whatever order you wish. Assume that trees consist of vertices of class `TreeNode` with instance variables `parent`, `left`, `right`, and `key`. Your procedure takes a `TreeNode` as its argument (the root of the tree). **_Use a stack as an auxiliary data structure._**

>     printBinaryTreeNodes(TreeNode root) {


**(b)** Write an O(_n_)-time procedure that, given an _n_-node rooted tree with **_arbitrary_** number of children using the **_left-child, right-sibling representation_**, prints out the key of each node of the tree in whatever order you wish. Assume that for economy of code we are re-using our `TreeNode` class. The instance variable `left` points to the left child as before, but now `right` points to the right sibling instead of the right child (which is no longer unique). Your procedure takes a `TreeNode` as its argument (the root of the tree). You may choose to use either the recursive or non-recursive approach.

>     printLCRSTreeNodes(TreeNode root) {


### #6. A Hybrid Merge/Insertion Sort Algorithm

#### 7 points

Although MergeSort runs in Θ(_n_ lg _n_) worst-case time and InsertionSort
runs in Θ(_n_2) worst-case time, the constant factors in insertion sort
(including that fact that it can sort in-place) can make it faster in practice
for small problem sizes on many machines. Thus, it makes sense to
**_coarsen_** the leaves of the MergeSort recursion tree by using
InsertionSort within MergeSort when subproblems become sufficiently small.

Consider a modification to MergeSort in which _n_/_k_ sublists of length _k_
are sorted using InsertionSort and are then merged using the standard merging
mechanism, where _k_ is a value to be determined in this problem. In the first
two parts of the problem, we get expressions for the contributions of
InsertionSort and MergeSort to the total runtime as a function of the input
size _n_ and the cutoff point between the algorithms _k_.

**(a - 1pt)** Show that InsertionSort can sort the _n_/_k_ sublists, each of length _k_, in Θ(_nk_) worst-case time. To do this:

  1. write the cost for sorting _k_ items with InsertionSort,
  2. multiply by how many times you have to do it, and 
  3. show that the expression you get simplifies to Θ(_nk_).

**(b - 3pts)** Show that MergeSort can merge the _n_/_k_ sublists of size _k_ in Θ(_n_ lg (_n_/_k_)) worst-case time. To do this: 

  1. draw the recursion tree for the merge (a modification of figure 2.5), 
  2. determine how many elements are merged at each level, 
  3. determine the height of the recursion tree from the _n_/_k_ lists that InsertionSort had already taken care of up to the single list that results at the end, and 
  4. show how you get the final expression Θ(_n_ lg (_n_/_k_)) from these two values. 

_**Putting it together:**_ The asymptotic runtime of the hybrid algorithm is
the sum of the two expressions above: the cost to sort the _n_/_k_ sublists of
size _k_, and the cost to divide and merge them. You have just shown this to
be

> Θ(_n__k_ \+ _n_ lg (_n_/_k_))

In the second two parts of the question we explore what _k_ can be.

**(c - 2pts)** The bigger we make _k_ the bigger lists InsertionSort has to sort. At some point, its Θ(_n_2) growth will overcome the advantage it has over MergeSort in lower constant overhead. How big can _k_ get before InsertionSort starts slowing things down? Derive a theoretical answer by proving the largest value of _k_ for which the hybrid sort has the same Θ runtime as a standard Θ(_n_ lg _n_) MergeSort. This will be an upper bound on _k_. To do this: 

  1. Looking at the expression for the hybrid algorithm runtime Θ(_n__k_ \+ _n_ lg (_n_/_k_)), identify the upper bound on _k_ expressed as a function of _n_, above which Θ(_n__k_ \+ _n_ lg (_n_/_k_)) would grow faster than Θ(_n_ lg _n_). _Give the _f_ for _k_ = Θ(_f_(_n_)) and argue for why it is correct._
  2. Show that this value for _k_ works by substituting it into Θ(_n__k_ \+ _n_ lg (_n_/_k_)) and showing that the resulting expression simplifies to Θ(_n_ lg _n_). 

**(d - 1pt)** Now suppose we have implementations of InsertionSort and MergeSort. How should we choose the optimal value of _k_ to use for these given implementations in practice? 

