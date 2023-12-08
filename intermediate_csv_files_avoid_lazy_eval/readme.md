### Intermediate csv files

This folder showcases intermediate files used while running PySpark on databricks. It seemed that lazy evaluation led to all the steps 
being calculated every time a triggering method was run. When running either the UDF to calculate MFCC features or the logistic regression model
lazy evaluation -from the beginning- made the notebook crash. To avoid this, the dataframe was saved as a csv file and then load to continue
the script. This helped by dividing the lazy evaluation into milestone blocks. Using this strategy, the script ran in its entirety.
