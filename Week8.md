# Week 8

Over the weekend I noticed that sometimes we were getting two training points which describe the same expansion.
After meeting with Pierre, Edward and Tim, it seems that SCIP sometimes "collapses" nodes which are infeasible in strong branching, see the illustration below:
![week 8 explanation][logo]

[logo]:https://github.com/FIT2082/28746244_RESEARCH_NOTEBOOK/blob/master/week8.png?raw=true

So we need to spend a small amount of time altering the script such that this works.

## Goals
- Incorporate more models into the script
- Create an R script which models the prediction difference over time
- Begin Poster design for Pierre and Edward to give thoughts on
- Add depth to the output, begin getting some large datasets for testing
