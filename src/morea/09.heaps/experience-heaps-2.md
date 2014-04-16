---
title: "Applying your understanding of heaps (again)"
published: true
morea_id: experience-heaps-2
morea_type: experience
morea_summary: "Learn about heaps (at home)."
morea_sort_order: 1
morea_labels:
 - Homework
---


#### 1\. Peer Credit Assignment

Please list the names of the other members of your peer group for this week
and the number of extra credit points you think they deserve for their
participation in group work on Tuesday and Thursday combined.

  * If all three members besides yourself were present at some time, you have a total of 3 points to allocate.
  * If only two members besides yourself were present, you have a total of 4 points to allocate.
  * If only one other member was present, you have a total of 6 points to allocate.
  * You need not allocate all the points available to you. Points allocated to yourself will not be recorded.

* * *

### Heaps

#### 8 points

**2\. ** Illustrate `Build-Max-Heap` on this data in a 1-based indexing array:
    
    
     A = [1, 6, 2, 8, 3, 9, 4, 7, 5],
    

Rewrite the array as it exists after each execution of line 3 (the call to
`Max-Heapify`). A template is provided below. Please use a plain text editor
with fixed width font and replace each underscore character "_" with the
correct value.

    
    
      index        1  2  3  4  5  6  7  8  9
      Start:  A = [1, 6, 2, 8, 3, 9, 4, 7, 5]
    
      i = 4:  A = [_, _, _, _, _, _, _, _, _]
    
      i = 3:  A = [_, _, _, _, _, _, _, _, _]
    
      i = 2:  A = [_, _, _, _, _, _, _, _, _]
    
      i = 1:  A = [_, _, _, _, _, _, _, _, _]
    

You may want to draw the heap in tree form and do the operations on the tree.
You are encouraged to include these trees in your response to help Robert
"debug" any problems, but grading will initially be done on the above
template.

**3\. ** Illustrate `Heap-Extract-Max` on the heap you constructed above. Show the array representation:

**(a)** After line 5 has finished executing
    
    
      A = [_, _, _, _, _, _, _, _, _]
    

**(b)** After line 6 has finished executing
    
    
      A = [_, _, _, _, _, _, _, _, _]
    

**4\. ** Consider now min-heaps rather than max-heaps. Write pseudocode for `Min-Heapify` and `Heap-Decrease-Key`, by copying the textbook's code for the max versions and changing only what you need to change. To make grading easier, please highlight, boldface or circle your changes.
    
    
      MAX-HEAPIFY (A, i) // Change to **MIN**-HEAPIFY 
      1   l = LEFT(i)
      2   r = RIGHT(i)
      3   if l <= A.heap-size and A[l] > A[i]
      4       largest = l
      5   else largest = i
      6   if r <= A.heap-size and A[r] > A[largest]
      7       largest = r
      8   if largest != i
      9       exchange A[i] with A[largest]
      10      MAX-HEAPIFY (A, largest)
    
      HEAP-INCREASE-KEY (A, i, key) // Change to HEAP-**DECREASE**-KEY
      1  if key < A[i]
      2      error "new key is smaller than current key"
      3  A[i] = key
      4  while i > 1 and A[PARENT(i)] < A[i]
      5      exchange A[i] with A[PARENT(i)]
      6      i = PARENT(i)
    


