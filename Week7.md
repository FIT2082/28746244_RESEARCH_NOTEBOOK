# Week 7

Now that we have a script to run and data to test with, we can begin to see results. Using only 1 Linear Regression Model, and only the solvaldelta as input, the model gave the following result for a small dataset:
Average error in models:
- SCIP Estimate:  0.17014952173913042
- All Training Points:  0.2169457017225378
- 50 Temporaly Close Training Points:  0.18822731405178839

As such we intend to try similar things with larger datasets and more features, in an attempt to maximise our prediction efficiency.

## Goals

- Investigate Depth within SCIP, possibly a second feature
- Expand to include more models, and more training points selection criteria (5, 10, 20, 50, 100, 500)
- Investigate methods for model comparison
