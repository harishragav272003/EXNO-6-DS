# EX:6 DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import pandas as pd
df=pd.read_csv("/content/titanic_dataset.csv")
df.head()
import seaborn as sns
import matplotlib.pyplot as plt
```
![image](https://github.com/chandrumathiyazhagan/EXNO-6-DS/assets/119393023/f83d445f-47d6-4030-b1ac-349061d8446f)


### 1.Line Plot
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
![image](https://github.com/chandrumathiyazhagan/EXNO-6-DS/assets/119393023/ff29a7a6-f9c5-48e2-aadf-a5df5adcf617)


### 2.Multi Line Plot
```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
![image](https://github.com/chandrumathiyazhagan/EXNO-6-DS/assets/119393023/fce23053-5339-4aa1-b2e2-6b149cf3f90a)

## TO VISUALIZE RELATIONSHIPS
### 1.Bar Chart
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
![image](https://github.com/chandrumathiyazhagan/EXNO-6-DS/assets/119393023/554517c7-0025-40c9-91dd-1cc251d7d769)


### 2.Scatter Plot
```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
![image](https://github.com/chandrumathiyazhagan/EXNO-6-DS/assets/119393023/5cb1073f-df00-4730-8b0d-c9b3ad5a91e5)


### 3.Bubble Chart
```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
![image](https://github.com/chandrumathiyazhagan/EXNO-6-DS/assets/119393023/8d9a4978-7b71-4d03-9c2e-1cc8e84a8c42)


## TO CAPTURE DISTRIBUTIONS
### 1.Histogram
```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![image](https://github.com/chandrumathiyazhagan/EXNO-6-DS/assets/119393023/f9e5f588-347b-414d-adcf-c4e97327cfc8)


### 2.Box Plot
```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
![image](https://github.com/chandrumathiyazhagan/EXNO-6-DS/assets/119393023/ddadf567-47bb-40e7-9cea-28cc4eec3c18)


### 3.Violin Plot
```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
![image](https://github.com/chandrumathiyazhagan/EXNO-6-DS/assets/119393023/e4e84071-4cfd-411e-9ef4-c87f1ba820bb)


### 4.Density Plot
```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
![image](https://github.com/chandrumathiyazhagan/EXNO-6-DS/assets/119393023/80cfb121-4f96-442b-ab9e-43559a91c92e)

### 5.Heatmap
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
![image](https://github.com/chandrumathiyazhagan/EXNO-6-DS/assets/119393023/bea2b9f0-618d-42cf-a46b-5a44b7e46292)

# Result:
  Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
