# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY
## Name: Prajin S
## Reference Number: 212223230151
## Department: Artificial Intelligence And Data Science
## Date:
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
import seaborn as sns
import matplotlib.pyplot as plt
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
```
![image](https://github.com/user-attachments/assets/d2e8ba0f-f6e6-42fa-ad7c-336b80d08e59)

```
df=sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/6a64e3e9-c2cd-42bd-b458-90724185591b)

```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle="solid",legend="auto")
```
![image-2](https://github.com/user-attachments/assets/bf3a0b75-c6b9-48b3-b64a-92048d898685)

```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title("Multi-Line Plot")
plt.xlabel("X Label")
plt.ylabel("Y Label")
```
![image-3](https://github.com/user-attachments/assets/8aa38ace-87fe-427c-8fb1-9edc08174fd8)

```
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill')
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![image-4](https://github.com/user-attachments/assets/c3b302f4-a4a3-4f91-ab22-bef126a799fb)

```
avg_total_bill=tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time')['tip'].mean()
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill',width=0.4)
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip',width=0.4)
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![image-5](https://github.com/user-attachments/assets/48f95dd1-0a8b-4830-81e8-d3b6f1e36c8c)

```
years=range(2000,2012)
apples=[0.895,0.91,0.919,0.926,0.929,0.931,0.934,0.936,0.937,0.9375,0.9372,0.939]
oranges=[0.962,0.941,0.930,0.923,0.918,0.908,0.907,0.904,0.901,0.898,0.9,0.896]
plt.bar(years,apples)
plt.bar(years,oranges,bottom=apples)
```
![image-6](https://github.com/user-attachments/assets/664326db-faf5-4229-8940-4a4cc58e7382)

```
dt=sns.load_dataset('tips')
sns.barplot(x='day',y='total_bill',hue='sex',data=dt,palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
```
![image-7](https://github.com/user-attachments/assets/aad55fa1-3896-4782-8b26-0b88a1995f52)

```
import pandas as pd
df=pd.read_csv("titanic_dataset (1).csv")
df
```
![image-8](https://github.com/user-attachments/assets/21600ccb-c098-4b92-9e71-95684282aead)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title('Fare of Passenger by Embarked Town')
```
![image-9](https://github.com/user-attachments/assets/496474d1-463f-4560-946d-f2a32f963469)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow',hue='Pclass')
plt.title('Fare of Passengers by Embarked Town,Divided by Class')
```
![image-10](https://github.com/user-attachments/assets/b944864a-e402-4b3d-acf9-c5a623a8cad7)

```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs Tip Amount')
```
![image-11](https://github.com/user-attachments/assets/816214a0-28a7-41c0-8f4e-73cb97fc08d0)

```
import seaborn as sns
import numpy as np
import pandas as pd
np.random.seed(1)
num_var=np.random.randn(1000)
num_var=pd.Series(num_var,name="Numerical variable")
num_var
```
![image-12](https://github.com/user-attachments/assets/56737cf0-384a-44b1-b667-617e1b69b77b)


```
sns.histplot(data=num_var,kde=True)
```
![image-13](https://github.com/user-attachments/assets/f0c50998-4db9-4f97-87bd-7d896d8b44ac)

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![image-14](https://github.com/user-attachments/assets/13aed84c-bbff-45fa-9679-c463266094eb)

```
np.random.seed(0)
marks=np.random.normal(loc=70,scale=10,size=100)
marks
```
![image-15](https://github.com/user-attachments/assets/2bc05f25-82d6-4163-adc0-87e8b2e29a6d)

```
sns.histplot(data=marks,bins=10,kde=True,stat='count',cumulative=False,multiple='stack',element='bars',palette='Set1',shrink=0.7)
plt.xlabel('Marks')
plt.ylabel('Density')
plt.title('Histogram of Students Marks')
```
![image-16](https://github.com/user-attachments/assets/ed4f4c7b-5634-43dd-83c5-c270c883b192)

```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'],y=tips['total_bill'],hue=tips['sex'])
```
![image-17](https://github.com/user-attachments/assets/0c91f747-2fd9-4fe3-b92f-e3e8be5c85df)

```
sns.boxplot(x='day',y='total_bill',hue='smoker',data=tips,linewidth=2,width=0.6,boxprops={'facecolor':'lightblue','edgecolor':'darkblue'},whiskerprops={'color':'black','linestyle':"--",'linewidth':1.5},capprops={"color":"black","linestyle":"--","linewidth":1.5})
```
![image-18](https://github.com/user-attachments/assets/2428a343-427f-4af3-8d24-5f19bc8b2c3f)

```
sns.boxplot(x="Pclass",y='Age',data=df,palette='rainbow')
plt.title("Age by Passenger Class, TITANIC")
```
![image-19](https://github.com/user-attachments/assets/c34e69e2-62ce-408a-9e0f-6ad38a81d41a)

```
sns.violinplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,palette="Set3",inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot Of Total Bill by Day and Smoker Status")
```
![image-20](https://github.com/user-attachments/assets/236ba18b-31f3-40c2-8e40-85fbb2cfa56c)

```
sns.set(style='whitegrid')
tip=sns.load_dataset('tips')
sns.violinplot(x='day',y='tip',data=tip)
```
![image](https://github.com/user-attachments/assets/7196a172-97e8-4076-b64b-7b20cd78c71e)

```
sns.set(style='whitegrid')
tip=sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"])
```
![image](https://github.com/user-attachments/assets/dc22d8d9-17a6-4201-9b46-5b6b8c03ac73)

```
sns.set(style='whitegrid')
tips=sns.load_dataset('tips')
sns.violinplot(x='tip',y='day',data=tip)
```
![image](https://github.com/user-attachments/assets/0a9af8cd-d2ac-4220-a7de-cc558b72e354)

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set2',alpha=0.8)
```
![image-24](https://github.com/user-attachments/assets/2b16decb-6fca-486b-b7ce-1126d24f9467)

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='stack',linewidth=3,palette="Set2",alpha=0.8)
```
![image-25](https://github.com/user-attachments/assets/eee95b62-b927-4f94-85ad-0d104423385d)

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='layer',linewidth=3,palette="Set2",alpha=0.8)
```
![image-26](https://github.com/user-attachments/assets/6a8b18ef-3471-4d93-88a6-65fefc20272b)

```
mart=pd.read_csv("supermarket.csv")
mart
```
![image-27](https://github.com/user-attachments/assets/9d51eb53-eb1f-4b6d-bbd2-41822a2710fb)

```
mart=mart[['Gender','Payment','Unit price','Quantity','Total','gross income']]
mart.head(10)
```
![image-28](https://github.com/user-attachments/assets/57fe82fa-fd2b-4d64-9dcd-b3943ca80981)

```
sns.kdeplot(data=mart,x='Total')
```
![image-29](https://github.com/user-attachments/assets/b69a9f13-2dcf-492e-851f-625b45a33dd9)

```
sns.kdeplot(data=mart,x='Unit price')
```
![image-30](https://github.com/user-attachments/assets/e09c180e-c01c-43e1-b89f-9b3d90d2265a)

```
sns.kdeplot(data=mart)
```
![image-31](https://github.com/user-attachments/assets/42fb9521-b2c0-4ac7-a806-0a2901c0376b)

```
sns.kdeplot(data=mart,x='Total',hue='Payment',multiple='stack')
```
![image-32](https://github.com/user-attachments/assets/8bb69041-6ded-4b7e-883c-3612987f1bbe)

```
sns.kdeplot(data=mart,x='Total',hue='Payment',multiple='stack',linewidth=5,palette='Dark2',alpha=0.5)
```
![image-33](https://github.com/user-attachments/assets/0bd9a2cc-d68f-41e7-9369-f022103894a4)

```
sns.kdeplot(data=mart,x='Unit price',y='gross income')
```
![image-34](https://github.com/user-attachments/assets/6ff1d357-2453-4e38-b4b0-0a436bce42f3)

```
data=np.random.randint(low=1,high=100,size=(10,10))
print("The data to be plotted:\n")
print(data)
```
![image-35](https://github.com/user-attachments/assets/65f5c6d7-4674-4ae6-8147-cff07de7da9a)

```
sns.heatmap(data=data,annot=True)
```
![image-36](https://github.com/user-attachments/assets/7c9e88fc-04e7-4f83-ac7f-f5241aaaccd2)

```
sns.heatmap(data=data)
```
![image-37](https://github.com/user-attachments/assets/86b37a34-4280-4226-8913-95414508f312)

```
tips=sns.load_dataset('tips')
numeric_cols=tips.select_dtypes(include=np.number).columns
corr=tips[numeric_cols].corr()
sns.heatmap(corr,annot=True,cmap='plasma',linewidth=0.5)
```
![image-38](https://github.com/user-attachments/assets/3ad92895-b650-40a4-84a9-f0ddbadb758c)

# Result:
Hence, DATA VISUALIZATION USING SEABORN LIBRARY is executed successfully
