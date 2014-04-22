---
title: "Remember asymptotic concepts"
published: true
morea_id: assessment-asymptotic-concepts
morea_type: assessment
morea_sort_order: 1
morea_labels:
 - "Bloom: Remember"
---

Assessed ability to remember asymptotic concepts through an in-class multiple choice exam:

<link rel="stylesheet" href="http://cdn.oesmith.co.uk/morris-0.4.3.min.css">
<script src="//cdnjs.cloudflare.com/ajax/libs/raphael/2.1.0/raphael-min.js"></script>
<script src="http://cdn.oesmith.co.uk/morris-0.4.3.min.js"></script>

<div class="well">
  <div id="assessment" style="height: 250px;"></div>
</div>

<script>
Morris.Bar({
  element: 'assessment',
  hideHover: false,
  data: [
        { y: 'Very satisfactory', num: 15 },
        { y: 'Satisfactory', num: 37 },
        { y: 'Unsatisfactory', num: 8 },
        { y: 'Absent', num: 3 },
        ],
  xkey: 'y',
  ykeys: ['num'],
  resize: true,
  labels: ['Students']
});
</script>