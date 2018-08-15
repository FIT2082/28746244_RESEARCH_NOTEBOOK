# Week 2

This was the first week me and Time had the chance to meet Pierre - our supervisor for this project.
We were able to discuss the meat of the project, as well as goals for next week and the end of the project.

## What are we doing?

To give a brief overview (A more detailed explanation can no doubt be found in the upcoming project specification), Linear constraint solving is rather easy, and solvable in polynomial time.
What becomes problematic is when we enforce that some of the variables on these constraints must be integers, that things run amuck.

This isn't a totally contrived problem either, as many solutions in real world problems don't assume a continuous amount of supply can be given - When you go to the supermarket it isn't exactly easy to buy exactly 3.45 cans of beans, its 3 or 4.

It turns out the solving this problem in particular is NP-Hard, and as such currently has no known polynomial solution.
In order to give a good estimate of the best integer solution, the open source state of the art program SCIP does the following:

* Solve the problem in the continuous case
* For this continuous solution, if there is some non-integer solution which should be an integer, then consider the two regions either side of the point, where we enforce this.
(For example, $x = (2, 3.4, 5)$ becomes the two regions $x_2 \leq 3, x_2 \geq 4$)
* Consider the continuous solutions in each of these regions,  and split accordingly until the subset you are looking at is completely small

There are 2 main problems that arrive at the moment:

1. How do we decide which variable to split on?
2. Every time the amount of areas we have to search doubles. Doesn't this mean this algorithm will be extremely slow?

The answers to which are:

1. We calculate the upper bound of solutions in that area by solving the continuous version of the problem, and then choose those which give the "most distinct" split in bounds (The details of which are outside the scope of this project)
2. While this is a problem, if we can reliably take away branches of a problem, then this wouldn't be a problem. Let's say we found an integer solution with value 5 at some branch of the problem - then every branch which had a maximum score of 5 or less can be discarded and thus not search!

Normally, to get these upper bounds per area, the continuous problem is solved (In polynomial time), although once enough branches are made, the execution of this code adds up, and the current state of the art solution to this is to predict the next upper bounds on some variable split $x_k$ by looking at all previous splits on $x_k$ and their upper bounds.
The current estimation method is a simple average over all previous cases, although Pierre thinks we can do better with a very lightweight machine learning algorithm.

As such, this research project will include testing different lightweight machine leraning methods to be trained on the fly in order to increase the prediciton power of such upper bounds, leading to a hopeful increase in efficiency of the algorithm.

## Goals for next week

Me and Tim aim to have the following done by next week's gathering:

* Have SCIP downloaded, as well as an introduction to C
* A working linux environment, knowledge of Make and general linux commands
* A git repo, where we can edit SCIP files for testing
