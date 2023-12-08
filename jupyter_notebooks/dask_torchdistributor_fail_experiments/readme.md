### Failed Experiments

These three notebooks showcase efforts to use the HuBert acoustic model to extract features directly from the waveform. 
The acoustic model consists in a CNN feature extractor and a Transformer block with masked input features. The goal is to
predict K-means on MFCC features. It was thought that by mounting fully connected layers on top of the acoustic model
accents could be predicted with high accuracy.

The initial plan was to use torch distributor in databricks to run this model. However, because of the time restriction
a simpler model was selected.

While pursuing the simpler model it was found that pyspark is not compatible with numpy data types. There was a way to overcome this challenge
using UDFs, however, this 'trick' could be used only once (there might be another way to go around this limitation, but this author did not
find this alternative approach). An idea was to use Dask instead of PySpark because it is written in python, and according to them compatible
with numpy. This approach did not work and another attempt was tried in PySpark. finalProject2.ipynb showcases attempts made with Dask.
