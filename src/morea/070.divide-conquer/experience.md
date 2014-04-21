---
title: "Understanding substitution and induction"
published: true
morea_id: experience-substitution
morea_type: experience
morea_summary: "Learn about substitution and induction."
morea_sort_order: 1
morea_labels:
 - In class
---

## Solving _T_(_n_) = _T_(_n_ − 1) + _n_ with Substitution

### 5 points

Using substitution and induction, show that the solution of _T_(_n_) = _T_(_n_
− 1) + _n_ is O(_n_2). In the terminology of CLRS, this is our "guess" at the
solution to the recurrence relation.

**a.**   Convert the "guess" to an equivalent algebraic inequality according to the definition of Big-O (removing the Big-O and adding the implied constant _c_): 

> _T_(_n_) =

Make the inductive assumption that what you wrote in (a) holds for all _m_ <
_n_.

Now you need to use induction and substitution to show that the definition
_T_(_n_) = _T_(_n_ − 1) + _n_ implies the inequality that you wrote in (a). In
the process you will determine the constraints on _c_. We'll do the base case
last for your chosen _c_.

**b.**   Write out the definition of T(_n_), and operating _ only_ on the right hand side, substitute in the inductive assumption where appropriate and simplify to isolate the expression (from a) to be proven from the lower order terms:

> _T_(_n_) =

**c.** Use ≤ to get rid of the lower order terms (effectively claiming that what you had above is ≤ _c__n_2), and determine the values of _c_ and _n_ for which the inequality is true:  

> The above is true for all _c_ ≥ ____ and _n_ ≥ ____ because ...

**d.** For the base case, assuming that _T_(0) = 0, show that _T_(1) = _c__n_2 for your choice of _c_:  

> _T_(1) =

### If you finish early:###

Try T(_n_) = 4T(_n_/3) + _n_
    
