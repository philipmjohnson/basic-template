---
title: "The accounting method"
published: true
morea_id: experience-amortized-analysis
morea_type: experience
morea_summary: "Working with amortized analysis"
morea_sort_order: 1
morea_labels:
 - In class
---

## Amortized Analysis: Accounting Method

_(This is similar to the problem that was solved using aggregate analysis in
my lecture notes, but the numbers are slightly different: in the lecture, the
table grows at sizes 2i-1; here at 2i; and here you use the accounting method.
Don't do it with aggregate analysis: that won't count! I provide guidance on
approaching the accounting analysis. The problem is relevant to Java hash
tables.)_

Suppose we perform a sequence of _n_ operations on a data structure in which
the _i_th operation costs _i_ if _i_ is an exact power of 2, and 1 otherwise.
_Use the **accounting method** to determine the amortized cost per operation._

**(a)** Choose the (fixed) cost per operation ĉ that you will charge. 

**(b)** Make a table showing 

  * operation number (_i_ = 1, 2, 3, ... up to about 20 to see the pattern), 
  * actual cost of the _i_th operation
  * credit available at the conclusion of the _i_th operation (credit_i_ = credit_i_−1 \+ ĉ − actual cost). 

**(c)** Write an expression for credit at each power of two, 2_i_. Does this credit increase, decrease, or stay the same? 

**(d)** Does credit increase, decrease or stay the same _between_ each power of 2? 

**(e)** Say why this shows that the amortized cost ĉ that you chose in step (a) is an upper bound on the actual cost. 

**(f)** Conclude by giving the big-O upper bound on amortized per-operation cost that (a) and (e) imply. 


