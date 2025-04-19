# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

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
REG NO:212224040345
NAME:B R SWETHA NIVASINI
```
```
import seaborn as sns
import matplotlib.pyplot as plt
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
```

![Screenshot 2025-04-19 111412](https://github.com/user-attachments/assets/1420918e-a676-472d-8646-265fc78ea588)

```
df=sns.load_dataset("tips")
df
```

![Screenshot 2025-04-19 111542](https://github.com/user-attachments/assets/baa3d11b-c02c-4926-859a-e429e9d0df89)

```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='solid',legend="auto")
```
![Screenshot 2025-04-19 111629](https://github.com/user-attachments/assets/790bc1a3-2ee6-4b3b-b3ff-1182e6f0956c)

```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel('Y Label')
```

![Screenshot 2025-04-19 111717](https://github.com/user-attachments/assets/f9895470-a839-471c-b232-1dc52f027460)

```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total_Bill')
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```

![Screenshot 2025-04-19 112210](https://github.com/user-attachments/assets/6fd7a5fb-ff75-435c-9e81-ce3482bd0ed3)

```
avg_total_bill=tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time')['tip'].mean()
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Toatl Bill',width=0.4)
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip',width=0.4)
plt.xlabel('Time of Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Time of Day')
plt.legend()
```

![Screenshot 2025-04-19 112322](https://github.com/user-attachments/assets/77095702-7929-4c76-904d-8c436c7ce37a)

```
years = range(2000, 2012) 
apples = [0.895, 0.91, 0.919, 0.926, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939, 0] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```


![Screenshot 2025-04-19 112402](https://github.com/user-attachments/assets/50e976ad-a6e2-49d4-956a-538658e93f51)




```
import seaborn as sns
dt=sns.load_dataset('tips')
sns.barplot(x='day',y='total_bill',hue='sex',data=dt,palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
```


![Screenshot 2025-04-19 112505](https://github.com/user-attachments/assets/03493a71-4eaa-456c-b3b5-3a7f3df61ad2)

```
import pandas as pd
tit=pd.read_csv("/content/titanic_dataset (2).csv")
tit
```


![Screenshot 2025-04-19 112631](https://github.com/user-attachments/assets/48e9d3f2-4e63-4841-b24f-d442a3faff5f)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=tit,palette='rainbow')
plt.title("Fare of Passenger by Embarked Town")
```


![Screenshot 2025-04-19 112758](https://github.com/user-attachments/assets/dd8dd179-fb88-4181-b6e5-c282e675f065)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```


![Screenshot 2025-04-19 112908](https://github.com/user-attachments/assets/07373933-d69f-4c02-9442-97df94c44df4)

```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```

![Screenshot 2025-04-19 112945](https://github.com/user-attachments/assets/07344135-840a-4ad2-bfb7-0d5a289d2365)

```
import seaborn as sns
import numpy as np
import pandas as pd
np.random.seed(1)
num_var=np.random.randn(1000)
num_var=pd.Series(num_var,name='Numerical variable')
num_var
```

![Screenshot 2025-04-19 113104](https://github.com/user-attachments/assets/b9cbd8b2-9992-445e-a91b-025202315b6f)


```
sns.histplot(data=num_var,kde=True)
```


![Screenshot 2025-04-19 113145](https://github.com/user-attachments/assets/6f99d486-95a2-46d0-9fca-2039dd9c6d0f)

```
df=pd.read_csv("/content/titanic_dataset (2).csv")
df
```


![Screenshot 2025-04-19 113221](https://github.com/user-attachments/assets/706816d6-90b2-4ce8-bec4-29bb68f8bc2f)

```
sns.histplot(data=df,x='Pclass',hue="Survived",kde=True)
```


![Screenshot 2025-04-19 113301](https://github.com/user-attachments/assets/7603230f-1467-48ec-99be-2b4092821048)

```
import seaborn as sns
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
np.random.seed(0)
marks=np.random.normal(loc=70,scale=10,size=100)
marks
```


![Screenshot 2025-04-19 113401](https://github.com/user-attachments/assets/5a5f1992-7982-4c3b-8a0b-3390b5ade0c0)

```
sns.histplot(data=marks, bins=10, kde=True, stat='count', cumulative=False, multiple='stack', element='bars', palette='Set1')
plt.xlabel('Marks')
plt.ylabel('Density')
plt.title('Histrogram of students Marks')
```


![Screenshot 2025-04-19 113445](https://github.com/user-attachments/assets/4ec63df0-bfe4-43b0-9666-262d53392961)

```
import seaborn as sns
import pandas as pd
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'],y=tips['total_bill'],hue=tips['sex'])
```


![Screenshot 2025-04-19 113517](https://github.com/user-attachments/assets/833ca779-2570-44ca-8cfc-af85458736cf)

```
sns.boxplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,boxprops={"facecolor":"lightblue","edgecolor":"darkblue"},
 whiskerprops={"color":"black","linestyle":"--","linewidth":1.5},capprops={"color":"black","linestyle":"--","linewidth":1.5} )
```


![Screenshot 2025-04-19 113557](https://github.com/user-attachments/assets/fd905e9e-eac1-4c40-8621-efed7b42a518)

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age by Passenger Class ,Titanic")
```


![Screenshot 2025-04-19 113722](https://github.com/user-attachments/assets/c87330c1-f1af-4f58-9988-7116e8a095b3)

```
sns.violinplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,
 palette="Set3",inner="quartile"              )
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("violin  Plot of Total Bill by Day and Smoker Status")
```

![Screenshot 2025-04-19 113810](https://github.com/user-attachments/assets/55c8a25b-a412-4288-b90a-c99991f5d592)

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set2',alpha=0.8)
```


![Screenshot 2025-04-19 113922](https://github.com/user-attachments/assets/76929783-3219-4dc7-b7a5-12c150b1ec3d)

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='layer',linewidth=3,palette='Set2',alpha=0.8)
```

![Screenshot 2025-04-19 114002](https://github.com/user-attachments/assets/1302701c-2d17-4ee6-b073-e58c4d9ad745)

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='stack',linewidth=3,palette='Set2',alpha=0.8)
```


![Screenshot 2025-04-19 114044](https://github.com/user-attachments/assets/f8d91974-34e8-4f14-850f-b27ceed5168e)

```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
mart=pd.read_csv("titanic_dataset.csv")
mart
```


![Screenshot 2025-04-19 114134](https://github.com/user-attachments/assets/ce4937ce-5320-4958-9c6f-793b6ed1625d)

```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```


![Screenshot 2025-04-19 114250](https://github.com/user-attachments/assets/cf984815-f637-411c-b8c7-ad8748c7e4c1)

```
sns.kdeplot(data=mart,x='PassengerId')
```


![Screenshot 2025-04-19 114344](https://github.com/user-attachments/assets/bc05a592-4bc6-4b0e-aa2f-330bf1d842d4)

```
sns.kdeplot(data=mart,x='Age')
```

![Screenshot 2025-04-19 114415](https://github.com/user-attachments/assets/3798da4a-57e3-431c-b6fb-ed7598cee02d)

```
sns.kdeplot(data=mart)
```

![Screenshot 2025-04-19 114447](https://github.com/user-attachments/assets/2aa0464c-8cd6-42c1-b061-64867809cdd8)

```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```


![Screenshot 2025-04-19 114525](https://github.com/user-attachments/assets/5cd3bf09-cc51-4131-80d8-0912b8cac43e)

```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```


![Screenshot 2025-04-19 114555](https://github.com/user-attachments/assets/34199736-0b43-42fc-bb8e-bc64150babab)

```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```


![Screenshot 2025-04-19 114627](https://github.com/user-attachments/assets/39011739-c494-472d-85ff-a021322a2d6d)


```
hm=sns.heatmap(data=data)
```


![Screenshot 2025-04-19 114701](https://github.com/user-attachments/assets/b5ce2fe7-a47a-43d2-8a1a-949883dc1869)

















            







































































































































































































# Result:
 Include your result here
