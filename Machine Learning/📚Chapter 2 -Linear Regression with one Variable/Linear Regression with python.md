# Simple Linear Regression with Python - Andrew

In the first part of exercise 1, we're tasked with implementing simple linear regression to predict profits for a food truck. Suppose you are the CEO of a restaurant franchise and are considering different cities for opening a new outlet. The chain already has trucks in various cities and you have data for profits and populations from the cities. You'd like to figure out what the expected profit of a new food truck might be given only the population of the city that it would be placed in.

## Examining the Data

Let's start by examining the data which is in a file called "ex1data1.txt" in the "data" directory of my repository above. First, we need to import a few libraries.

### Import Libraries

```python
import os
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
%matplotlib inline

from google.colab import drive
drive.mount('/content/drive')

import pandas as pd 
data = pd.read_csv('/content/drive/MyDrive/Datasets/Andrew ML/ex1data1.txt', header=None, names=['Population', 'Profit'])
data.head()

data.describe()

data.plot(kind='scatter', x='Population', y='Profit', figsize=(12,8))
