---
title: "Asymptotic concepts"
published: true
morea_id: experience-asymptotic-concepts
morea_type: experience
morea_summary: "Practice analysis of functions with respect to their limiting behavior"
morea_sort_order: 1
morea_labels:
 - In class
---

## Asymptotic Concepts

#### 5 points

**1\. (1 pt)** We can extend asymptotic notation to the case of two parameters n and m that can go to infinity independently at different rates. For example, we denote by O(g(n,m)) the set of functions:

> O(_g_(_n_,_m_)) = {_f_(_n_,_m_) : there exists positive constants _c_, _n_0
and _m_0 such that 0 ≤ _f_(_n_,_m_) ≤ _c__g_(_n_,_m_) for all _n_ ≥ _ _n0 or
_m_ ≥ _m_0}

Give a corresponding definition for Θ(_g_(_n_,_m_)).

**2\. (4 pts)** Indicate, for each pair of expressions (_f_(_n_), _g_(_n_)) in the table below, whether _f_(_n_) = ___(_g_(_n_)), where the ___ may be O, o, Ω, ω or Θ. Assume that k ≥ 1, _c_ > 1, and d > 0 are constants and we are analyzing growth rates in terms of the variable _n_. To respond, write "Yes" or "No" in each box. Grading will be based on these entries first, but if you give your justifications below we can give better feedback and possibly partial credit in case of wrong answers. 


<table width="100%" border="1">
  <caption>
    Asymptotic Relations
  </caption>
  <tbody><tr>
    <th scope="col">&nbsp;</th>
    <th scope="col"><i>f</i>(<i>n</i>)</th>
    <th scope="col"><i>g</i>(<i>n</i>)</th>
    <th scope="col">O?</th>
    <th scope="col">o?</th>
    <th scope="col">&#937;?</th>
    <th scope="col">&#969;?</th>
    <th scope="col">&#920;?</th>
  </tr>
  <tr>
    <th scope="row">a.</th>
    <td>n<sup>lg <i>c</i></sup></td>
    <td>c<sup>lg <i>n</i></sup></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
  </tr>
  <tr>
    <th scope="row">b.</th>
    <td>lg<sup><i>k</i></sup><i>n</i></td>
    <td>n<sup><i>d</i></sup></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
  </tr>
  <tr>
    <th scope="row">c.</th>
    <td>2<sup><i>n</i></sup></td>
    <td>2<sup><i>n</i>/2</sup></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
  </tr>
  <tr>
    <th scope="row">d.</th>
    <td>lg(<i>n</i>!)</td>
    <td>lg(<i>n</i><sup><i>n</i></sup>)</td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
    <td><strong>&nbsp;</strong></td>
  </tr>
</tbody></table>


