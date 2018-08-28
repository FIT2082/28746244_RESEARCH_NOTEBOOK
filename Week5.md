# Week 5

After looking at branch_relpscost.c and some related files, we now know that the average is stored in the variable's history structure.
This stores a weighted sum of the updated bounds, and also stores the mean and variance

- [X] Look at the files branch_relpscost.c for psuedocost update files

## Goals

Now that we know where the data is updated, we need to output these values every time updatePseudocost is called.

* output variable updates to stdout, so we have a small dataset to work with
* create a struct within SCIP, which is more extensible
* ensure that these values are reasonable
