---
title: "Applying your understanding of quicksort (again)"
published: true
morea_id: experience-quicksort-2
morea_type: experience
morea_summary: "Learn about quicksort (at home)."
morea_sort_order: 2
morea_labels:
 - Homework
---

### Quicksort

#### 12 points

Show the operation of Partition (not randomized) on this 1-based array:

    
    
     A = [1, 6, 2, 8, 3, 9, 4, 7, 5], p=1, q=9 
    

and the two sub-partitions that result as directed below. In other words, you
will trace the three calls to Partition that are highest in the recursion
tree. (They are _not_ the first three calls: #1 is the first call and #2 is
the second call, but the call marked as #3 below takes place after all the
recursive calls breaking down #2.)

In order to make the desired response format clear and to make it easy for the
TA to grade, I am providing a template for your response. You are to fill in
wherever the underscore character "_" appears. Use a plain text editor with
_fixed-width font_. Be sure to fill in all fields marked with underscore: use
search to make sure you get them all. I start you off with the first few
lines: continue in the same pattern.

    
    
     
    **(#1) Call to Partition (A, 1, 9) made in Line 2 of the initial call to Quicksort:**
    
      Initially: 
      A = [1, 6, 2, 8, 3, 9, 4, 7, 5], i=0, j=1, pivot = A[r] = A[9] = 5 
    
      Trace at the conclusion of each pass through the loop lines 3-6
      A = [1, 6, 2, 8, 3, 9, 4, 7, 5], i=1, j=1, exchanged A[1] with A[1]
      A = [1, 6, 2, 8, 3, 9, 4, 7, 5], i=1, j=2, no exchange 
    
      ... you fill in the rest until the loop exits ... 
    
      A = [_, _, _, _, _, _, _, _, _], i=_, j=3, ___________
      A = [_, _, _, _, _, _, _, _, _], i=_, j=4, ___________
      A = [_, _, _, _, _, _, _, _, _], i=_, j=5, ___________
      A = [_, _, _, _, _, _, _, _, _], i=_, j=6, ___________
      A = [_, _, _, _, _, _, _, _, _], i=_, j=7, ___________
      A = [_, _, _, _, _, _, _, _, _], i=_, j=8, ___________
    
      After the swap in line 7: 
      A = [_, _, _, _, _, _, _, _, _], i=_, j=_, exchanged A[_] with A[_] 
    
    What does Partition(A, 1, 9) return? __
    
    Continuing execution of the top level call to Quicksort, identify the two
    partitions that will be handled by the recursive calls to Quicksort at
    this level: 
    (#2) On what subarray will Quicksort in line 3 be called? A[_, _]
    (#3) On what subarray will Quicksort in line 4 be called? A[_, _]
    
    Now trace these two calls in a manner similar to above. 
    
    **(#2) Call to Partition(A, _, _) handled in the first call to Quicksort line 3: **
    
      Initially: 
      A = [_, _, _, _, _, _, _, _, _], i=_, j=_, pivot = A[r] = A[_] = _
    
      Trace at the conclusion of each pass through the loop lines 3-6
      A = [_, _, _, _, _, _, _, _, _], i=_, j=_, ___________
      A = [_, _, _, _, _, _, _, _, _], i=_, j=_, ___________
      A = [_, _, _, _, _, _, _, _, _], i=_, j=_, ___________
    
      After the swap in line 7: 
      A = [_, _, _, _, _, _, _, _, _], i=_, j=_, exchanged A[_] with A[_] 
    
    What does this second call to Partition return? __
    
    **(#3) Call to Partition(A, _, _) handled in the first call to Quicksort line 4:**
    
      Initially: 
      A = [_, _, _, _, _, _, _, _, _], i=_, j=_, pivot = A[r] = A[_] = _
    
      Trace at the conclusion of each pass through the loop lines 3-6
      A = [_, _, _, _, _, _, _, _, _], i=_, j=_, ___________
      A = [_, _, _, _, _, _, _, _, _], i=_, j=_, ___________
      A = [_, _, _, _, _, _, _, _, _], i=_, j=_, ___________
    
      After the swap in line 7: 
      A = [_, _, _, _, _, _, _, _, _], i=_, j=_, exchanged A[_] with A[_] 
    
    What does this third call to Partition return? __
    

Not graded, but you might think about:

  * What pattern do you see in the second call to Partition? Will this pattern continue in the subsequent calls to Partition in that half of the array? 
  * What pattern do you see in the third call to Partition? Will this pattern continue in the subsequent calls to Partition in that half of the array? 
  * What do these observations tell us about the runtime of Quicksort on data organized as in these partitions? 

* * *

Dan Suthers Last modified: Wed Mar 19 23:22:39 HST 2014

