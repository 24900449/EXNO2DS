# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT

```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
dt = pd.read_csv("/content/titanic_dataset.csv")
dt
```

<img width="1243" height="999" alt="image" src="https://github.com/user-attachments/assets/0d2d3bf2-137a-4ec9-9d16-dfa6a8bd53d5" />

```
dt.info()
```
<img width="1251" height="842" alt="image" src="https://github.com/user-attachments/assets/8af4b39c-3862-4389-a0fe-f5bf5d92a21f" />

```
dt.shape
```

<img width="1241" height="557" alt="image" src="https://github.com/user-attachments/assets/417a0a52-ff14-4c72-be34-3b33801338ce" />

```
dt.set_index("PassengerId", inplace=True)
dt.describe()
```

<img width="1242" height="662" alt="image" src="https://github.com/user-attachments/assets/37b80024-1619-4940-b6bd-06e8ae0a7a6c" />

```
dt.nunique()
```

<img width="1257" height="910" alt="image" src="https://github.com/user-attachments/assets/3d0e71d4-8154-4e14-8fd3-bf96ce823408" />

```
dt["Survived"].value_counts()
```
<img width="1265" height="565" alt="image" src="https://github.com/user-attachments/assets/b1bb41b6-f092-4397-be5e-927723652ea1" />

```
per = (dt["Survived"].value_counts() / dt.shape[0] * 100).round(2)
per
```
<img width="1248" height="554" alt="image" src="https://github.com/user-attachments/assets/8052da7c-d63e-42ad-b952-ae27960b6b3c" />

```
sns.countplot(data=dt, x="Survived")
```

<img width="1254" height="1064" alt="image" src="https://github.com/user-attachments/assets/e2c93759-4535-4d94-9ebd-a61a7c220a07" />

```
dt.Pclass.unique()
```

<img width="1250" height="675" alt="image" src="https://github.com/user-attachments/assets/10491cb4-b3a3-4eb6-87a2-f91a581f7a2a" />


```
sns.pairplot(dt)
```

<img width="1234" height="1130" alt="image" src="https://github.com/user-attachments/assets/be3e2ce1-3686-4eb7-8e71-02645eb78b0f" />

# RESULT
        <<INCLUDE YOUR RESULT HERE>>
