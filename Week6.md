# Week 6

In the week preceeding we found where the variable info is stored, and have since modified SCIP to print these values out.
At the moment we only print training data (IE when we are exploring knew nodes and psuedo costs are updated, not when SCIP is queried for an estimate)
As such I am working on a script to simulate the training and prediction process, and Tim is working on getting the prediction data out as well.

- [X] Output variable updates to stdout, so we have a small dataset to work with

## Goals

- Output variable data for prediction steps
- Create a script which simulates the machine learning process
