## Week 9

As we move closer to the mid semester break, we aim to make testing each instance easier and further automated.
As such, the majority of this week was spent altering the script so that it does the following:

- Takes any set of data, in the generic format previously described
- Collects all prediction data for all models specified, with all points specified (ALL, Last 10, Last 100, etc)
- Outputs this is into a CSV, storing the SCIP prediction, Actual prediction, and model prediction, all at once

This means that we can rather easily obtain graphs which compare the overall prediction power of any model against SCIP for any instance rather easily.

The next aim to complete over the mid semester break is to continue this automation into an R script which will collate this information into a readable format.
