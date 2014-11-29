<head>
<link type="text/css" rel="stylesheet" href="http://fonts.googleapis.com/css?family=Inconsolata">
</head>
<pre style="margin-left:100px">
<h2>
Schedulers state machine:
------------------------
- RATM
- Problems
- Execution
</h2>
</pre>
<pre style="font-size: 15px; margin-left:120px;">

This document jumps right into scheduler implementation details. If you've never
read scheduler code before, you might benefit from talking to someone on the lab
team to get context first. You can also check out the docstrings in <a href="https://chromium-review.googlesource.com/#/c/174080/">this cl</a>.

<h3>
RATM:
====
</h3>

This segment can also be viewed as a crosssection of db writes in the scheduler,
since anything that runs in the lab records state in mysql. None of what follows
will make much sense if you've never thought about how jobs run in the lab.

</pre>
