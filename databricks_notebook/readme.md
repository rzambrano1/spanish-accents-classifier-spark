### Databricks Notebook

The databricks notebook is saved as a dbc file, which is not compatible with GitHub. 

In order to view the content of the databricks notebook download either the ipynb, the pdf, or the HTML versions of the file.

**Note:** Commands that were meant to be run only once were commented out after they were run. For example, downloading the zipped file from Common Voice, or (more importantly), the command to unzip the dataset. The goal of commenting them out was to avoid running them again by accidentally selecting 'Run All' instead of running just a single line in the Databricks notebook.

**Note 2:** In the 'Try-Number-2' section of the notebook, the approach to run the model was figured out. As it is described in the paper, to terminate the commands they had to be run in one line. Then predictions and true value columns were saved as csv files to avoid lazy evaluation. When commands were tried in the trainingSummary object, the notebook crashed. The errors thrown when the notebook crashed were left to showcase why lazy evaluation had to be avoided at given milestones. These errors were not coming up when running the same commands on the trainingSummary object in an smaller subset of the common voice data (about 1000 rows).
