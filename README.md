It may be defined as the normalization technique that modifies the dataset values in a way that in each row the sum of the squares will always be up to 1. It is also called least squares.

Example
In this example, we use L2 Normalization technique to normalize the data of Pima Indians Diabetes dataset which we used earlier. First, the CSV data will be loaded (as done in previous chapters) and then with the help of Normalizer class it will be normalized.

The first few lines of following script are same as we have written in previous chapters while loading CSV data.

from pandas import read_csv
from numpy import set_printoptions
from sklearn.preprocessing import Normalizer
path = r'C:\pima-indians-diabetes.csv'
names = ['preg', 'plas', 'pres', 'skin', 'test',…
 Now, we can use Normalizer class with L1 to normalize the data.

Data_normalizer = Normalizer(norm='l2').fit(array)
Data_normalized = Data_normalizer.transform(array)
We can also summarize the data for output as per our choice. Here, we are setting the precision to 2 and showing the first 3 rows in the output.

set_printoptions(precision=2)
print ("\nNormalized data:\n", Data_normalized [0:3])
Output
Normalized data:
[[0.03 0.83 0.4 0.2 0. 0.19 0. 0.28 0.01]
[0.01 0.72 0.56 0.24 0. 0.22 0. 0.26 0. ]
[0.04 0.92 0.32 0. 0. 0.12 0. 0.16 0.01]]
