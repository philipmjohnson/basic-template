---
title: "Greedy algorithms sample problem: activity scheduling"
published: true
morea_id: experience-greedy-algorithms
morea_type: experience
morea_summary: "Apply the greedy strategy to activity scheduling"
morea_sort_order: 1
morea_labels:
 - In class
---

### Activity Scheduling

The activity scheduling problem is to _**find the largest possible set **_
(maximum _number_, not duration) _**of activities that do not overlap with
each other**_, given their start and finish times.

CLRS show that this problem has the _**greedy choice property**_: a globally
optimal solution can be assembled from locally optimal choices. They show it
by example with this _greedy strategy_: Always select the remaining compatible
activity that ends first, and then solve the subproblem of scheduling the
activities that start after this activity. The local optimization is to select
the activity that finishes first, and the global optimization is scheduling
the maximum number of activities possible.

There are other greedy strategies, but some work and some don't.

#### Alternative Greedy Strategies

In the following three problems you determine whether alternative locally
greedy strategies lead to globally optimal solutions. For each strategy below,

  * either show that the strategy leads to an optimal solution by outlining the algorithm or approach,
  

  * or give a counterexample: write down a set of activities (defined by their start and finish times) that the strategy fails on, and show what goes wrong.

**1.** _Greedy strategy_: Always select the remaining compatible activity that has the **least duration**. _Rationale:_ Leave the most time remaining for other activities. 

**2.** _Greedy strategy_: Always select the remaining compatible activity that has the **latest start time**. _Rationale:_ Leave the most time remaining at the beginning for other activities.

**3.** _Greedy strategy_: Always select the remaining compatible activity that **overlaps with the fewest number of remaining activities**. _Rationale:_ Eliminate the fewest number of remaining activities from consideration.

####  Value Optimization

**4.** Suppose now that different activities earn different amounts of revenue. In addition to their start and finish times _s__i_ and _f__i_, each activity _a__i_ has _revenue_ _r__i_, and our objective is now to maximize the total revenue Σ_a__i_∈_A_ _r__i_. 

  * Does this problem exhibit the greedy choice property?
  * If so, do any of the above strategies apply, or another greedy strategy you can think of?
  * If not, why not, and what alternative problem solving strategy would work on this problem? 


