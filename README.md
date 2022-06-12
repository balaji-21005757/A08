# A08-IMPLEMENT KDE PLOT WITH ANY ONE OF YOUR OWN DATA SET

# PROGRAM:
```
Program developed by : K.Balaji
Regsiter number : 212221230011
```
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

df=pd.read_csv("titanic_dataset.csv")

df

#Create KDE for all the numeric variables in dataframe
sns.kdeplot(data=df)

sns.kdeplot(data=df, x='Pclass')

sns.kdeplot(data=df, x='Age')

sns.kdeplot(data=df, x='Fare')

sns.kdeplot(data=df,x='Survived',hue='Sex')

sns.kdeplot(data=df,x='Fare',hue='Sex')

sns.kdeplot(data=df,x='Survived',hue='Age')

sns.kdeplot(data=df,x='SibSp',hue='Age')

sns.kdeplot(data=df,x='Survived',hue='Pclass')

#Stack KDE on a category using MULTIPLE argument
sns.kdeplot(data=df,x='Survived',hue='Sex',multiple='stack')

sns.kdeplot(data=df,x='Survived',hue='Sex',multiple='stack',linewidth=5,palette='Dark2',alpha=0.5)

sns.kdeplot(data=df,x='Fare',hue='Sex',multiple='stack')

sns.kdeplot(data=df,x='Survived',hue='Pclass',multiple='stack')

sns.kdeplot(data=df,x='Survived',hue='Pclass',multiple='stack',linewidth=5,palette='Dark2',alpha=0.5)

sns.kdeplot(data=df,x='Fare',hue='Pclass',multiple='stack')

#Create a bivariate KDE
sns.kdeplot(data=df, x='Survived',y='SibSp')

sns.kdeplot(data=df, x='Survived',y='Fare')

sns.kdeplot(data=df, x='Age',y='Fare')

sns.kdeplot(data=df, x='Age',y='Pclass')
```
# OUTPUT
## Initial Dataframe:
![output](./1.png)
## KDE for all numeric variables of the Dataframe:
![output](./2.png)
## Basic KDE plot for Pclass column:
![output](./3.png)
## Basic KDE plot for Age column:
![output](./4.png)
## Basic KDE plot for Fare column:
![output](./5.png)
## Basic KDE plot for Survived column:
![output](./6.png)
## Basic KDE plot for SibSp column:
![output](./7.png)
## KDE on a category using MULTIPLE argument:
### Survived Vs Sex:
![output](./8.png)
### Fare Vs Sex:
![output](./9.png)
### Survived Vs Pclass:
![output](./10.png)
## KDE on a category using MULTIPLE argument(Using additional Parameter- stack):
### Survived Vs Sex
![output](./11.png)
### Fare Vs Sex
![output](./12.png)
### Survived Vs Pclass:
![output](./13.png)
### Fare Vs Pclass:
![output](./14.png)
## KDE on a category using MULTIPLE argument(Using additional Parameter- stack,line width):
### Survived Vs Sex:
![output](./15.png)
### Survived Pclass:
![output](./16.png)
## Bivariate KDE:
### Survived Vs SibSp:
![output](./17.png)
### Survived Vs Fare:
![output](./18.png)
### Age Vs Fare:
![output](./19.png)
### Age Vs Pclass:
![output](./20.png)

