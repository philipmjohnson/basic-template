---
title: "Asymptotic analysis of basic data structures"
published: true
morea_id: experience-asymptotic-basic-data-structures
morea_type: experience
morea_summary: "Practice analysis of basic data structures with respect to their limiting behavior"
morea_sort_order: 1
morea_labels:
 - In class
---
## Basic Data Structures

####  5 points

**1\. (4 pts)** For each of the four types of lists in the following table, what is the _asymptotic worst-case running time_ for each dynamic set operation listed, given a list of length _n_? 

  * Assume that __k_ is the key_, _d_ the data associated with the key, and __p_ a position_ in the data structure.
  * As explained in class, positions abstract and provide encapsulated access to elements of a data structure. We don't have to search for the item if we have a position p for it.
  * Sorted lists are sorted in _ascending order_.
  * Predecessor, successor, minimum, and maximum are _with respect to ordering of keys in the set under "<"_, not necessarily ordering of the list data structure.
  * The cells filled in are from the quiz.

<table width="100%" border="1">
  <caption>
    Worst Case Linked List Operations
  </caption>
  <tbody><tr>
    <th scope="col">&nbsp;</th>
    <th scope="col">Unsorted, Singly Linked (no tail pointer)</th>
    <th scope="col">Sorted, Singly Linked (no tail ponter)</th>
    <th scope="col">Unsorted, Doubly Linked with Sentinel and Tail pointer</th>
    <th scope="col">Sorted, Doubly Linked with Sentinel and Tail pointer</th>
  </tr>
  <tr>
    <th scope="row">insert(k, d)</th>
    <td>&nbsp;</td>
    <td>&nbsp;</td>
    <td>&#920;(1)</td>
    <td>&#920;(n)</td>
  </tr>
  <tr>
    <th scope="row">search(k)</th>
    <td>&nbsp;</td>
    <td>&nbsp;</td>
    <td>&#920;(n)</td>
    <td>&#920;(n)</td>
  </tr>
  <tr>
    <th scope="row">delete(p)</th>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
  </tr>
  <tr>
    <th scope="row">successor(p)</th>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
  </tr>
  <tr>
    <th scope="row">minimum()</th>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
  </tr>
</tbody></table>
  

**2\. (1 pt)** Write a Θ(_n_)-time recursive procedure that, _given an _n_-node binary tree, prints out the key of each node of the tree_ in any order you wish. Assume that trees consist of vertices of class `TreeNode` with instance variables `parent`, `left`, `right`, and `key`. Your recursive procedure takes a `TreeNode` as its argument (the root of the tree or subtree being considered by the recursive call).
    
    
    **
    printTreeNodes(TreeNode root)
        if (root != null) {
    
    
    **


