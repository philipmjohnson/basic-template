---
title: "Understanding master method and substitution"
published: true
morea_id: experience-master-method
morea_type: experience
morea_summary: "Apply your knowledge of the master method and substitution."
morea_sort_order: 1
morea_labels:
 - Homework
---
    
### Peer Credit Assignment

**1.** Please list the names of the other members of your peer group for this week and the number of extra credit points you think they deserve for their participation in group work on Tuesday and Thursday combined.

  * If all three members besides yourself were present at some time, you have a total of 3 points to allocate.
  * If only two members besides yourself were present, you have a total of 4 points to allocate.
  * If only one other member was present, you have a total of 6 points to allocate.
  * You need not allocate all the points available to you. Points allocated to yourself will not be recorded.

### Master Method Practice

**2\. ** (6 pts) Use the Master Method to give tight Θ bounds for the following recurrence relations. Show _a_, _b_, and _f_(_n_). Then explain why it fits one of the cases, if any. If it fits a case, write and _ simplify _ the final Θ result 

**a.**   _T_(_n_) = 2_T_(_n_/4) + √_n_  

**b.**   _T_(_n_) = 2_T_(_n_/4) + _n_  

**c.**   _T_(_n_) = 4_T_(_n_/3) + _n_



### Substitution Method

**3.** (7 pts) Use substitution _as directed below_ to solve 

> _T_(_n_) = 4_T_(_n_/3) + _n_

It is strongly recommended that you read page 85-86 "Subtleties" before trying
this!

**a.**   First, use the result from the Master Method in 2c as your "guess" and inductive assumption. We will do this without Θ and _c_: just use the algebraic portion. Take the proof up to where it fails and say where and why it fails. (See steps below.) 

**b.**   Redo the proof, but subtracting _d__n_ from the guess to construct a new guess. This time it should succeed. 

As a reminder, to do a proof by substitution you:

  1. Write the definition _T_(_n_) = 4_T_(_n_/3) + _n_
  2. Replace the _T_(_n_/3) with your "guess" instantiated for _n_/3 (you can do that by the inductive hypothesis because it's smaller than _n_). 
  3. Operating _only_ on the right hand side of the equation, transform that side into the _exact_ form of your "guess".
  4. Determine any constraints on the constants involved. 
  5. Show the base case holds. 


