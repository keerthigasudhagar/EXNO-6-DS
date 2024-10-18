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
import seaborn as sns
import matplotlib.pyplot as plt
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
```
![328403702-5ebc90bd-e2c7-44f7-bea0-aaa3a79e73fe](https://github.com/user-attachments/assets/dd29add1-4faa-4257-bbd5-f601da2f705f)
```
df=sns.load_dataset('tips')
df
```
![328403854-72459e98-f5ea-4bb4-a7a2-a6a44c9f763d](https://github.com/user-attachments/assets/f3ada332-9ba7-473a-b297-84e301b69fdc)
```
sns.lineplot(x='total_bill',y='tip',data=df,hue='sex',linestyle='solid',legend='auto')
```
![328404015-0df857a5-6fd8-4cd7-8cc4-4afac12569d4](https://github.com/user-attachments/assets/2e20da6d-16b5-41f9-befc-60e1cb48f9be)
```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi-Line Plot')
plt.xlabel('X Label')
plt.ylabel('Y Lbel')
```
![328404202-878a2de5-5e0e-48a2-a86b-30641c9106e4](https://github.com/user-attachments/assets/d5e76906-128c-40f9-a1da-409523d0372b)
```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill')
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title("Average Total Bill and Tip by Day")
plt.legend()
```
![328404393-1259f51f-5be7-4cbb-963b-e22417e22bbc](https://github.com/user-attachments/assets/245bc601-31f5-48cd-840e-63e6bf755123)
```
avg_total_bill=tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time')['tip'].mean()
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill',width=0.4)
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip',width=0.4)
plt.xlabel('Time of Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Time of Day')
plt.legend()
```
![328404601-25e619ff-5674-463c-83ef-6db4bcf71b4c](https://github.com/user-attachments/assets/c5163b1f-ffab-471d-8f2e-ceb8fc71c25b)
```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![328404770-a7821d08-b812-4d0a-a31b-d2d8d2c4348e](https://github.com/user-attachments/assets/143986bb-c1ef-4b32-8965-d9ea9cc844dc)
```
import seaborn as sns
dt= sns.load_dataset('tips')
# Bar plot with hue parameter
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
```
![328404948-d420004b-4947-4982-8822-8e091d4c2556](https://github.com/user-attachments/assets/6076ad44-8263-42c6-ba9f-33d54a7af34c)
```
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![328405125-6af33110-1f33-4ee0-9ad8-067c8c344995](https://github.com/user-attachments/assets/86fe29d1-934a-4e57-8521-849659f619d8)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```
![328405327-72e604dd-914f-4d4e-a8be-d2cc6572b28d](https://github.com/user-attachments/assets/5bcab762-186d-4985-9f19-96ef30214805)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![328405492-8b942432-e331-4f8c-bae7-74b18939e108](https://github.com/user-attachments/assets/38b80761-8d7b-4153-8f9d-b8d6c6ca44e3)
```
import seaborn as sns
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![328405640-e264d020-9594-48e3-b154-6f49edc043dc](https://github.com/user-attachments/assets/935c6197-645c-48b0-9cb4-9586c895a067)
```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![328405774-18efe9cb-616e-446c-9c58-5cdd72a4be21](https://github.com/user-attachments/assets/9fcdd1a4-b8a4-4b63-9763-582421b0aca4)
```
sns.histplot(data = num_var, kde = True)
```
![328405940-8c280caa-0672-49c4-86d4-0987726ad754](https://github.com/user-attachments/assets/7bccbe52-884b-4ebd-9c1d-c64afac5899e)
```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![328406105-dda607c5-9719-4277-b152-38fbd0f9ce47](https://github.com/user-attachments/assets/4a750dad-8fe5-477c-be76-1f62c3486117)
```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![328406323-e199b39b-099c-4ae5-92fd-670f3ea6339a](https://github.com/user-attachments/assets/af844aaf-7b29-4d20-baf3-58c7cb96e918)
```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![328406523-aca2c18f-b186-4cb5-bd46-83bbb4736c98](https://github.com/user-attachments/assets/2e5f41c2-4be8-4b8f-9b4a-35bd534a9d29)
```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6,
palette="Set3", inner="quartile")
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![328406688-876ce9b6-03d2-4ce8-ba2a-4e81fd87a53f](https://github.com/user-attachments/assets/706e8bdf-03f6-4181-ab37-9bf138eda3a5)
```
mart=pd.read_csv("titanic_dataset.csv")
mart
```
```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```
![328407027-bb4d692b-8293-48d4-b634-20ab0e01921c](https://github.com/user-attachments/assets/8e907254-369d-43dc-9b89-f66202b5e067)
```
sns.kdeplot(data=mart,x='PassengerId')
```
![328407161-ec85ccb3-2f33-4f55-9289-580309acb24f](https://github.com/user-attachments/assets/e518e393-e4df-4678-b8db-0fef933c526e)
```
sns.kdeplot(data=mart,x='Age')
```
![328407305-7e7b1cea-ee95-44e7-a9a9-882368562b43](https://github.com/user-attachments/assets/beff4c54-2453-442b-b197-913c4fce8d0f)
```
sns.kdeplot(data=mart)
```
![328407448-d4e4842c-e5d4-4db6-8c64-1aa72e29ba39](https://github.com/user-attachments/assets/4f547506-ab80-43f2-8399-d1b754c21020)
```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![328407620-05b28957-4959-41a7-b222-ecf9cbd39141](https://github.com/user-attachments/assets/21050a74-c1df-431b-8cdf-850c26e62d0d)
```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![328407757-805b0432-424f-4f07-9c53-250059b27be4](https://github.com/user-attachments/assets/26b027ba-4c52-4be4-9ff0-e99edf03e0c8)
```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![328407902-9fb6c87b-fe9c-4c73-b7f8-6758b9f5c37f](https://github.com/user-attachments/assets/7402c572-fc70-40db-9f52-81ca9ec11f4f)
```
hm=sns.heatmap(data=data)
```
![328408044-12f0265a-2d04-4087-adcb-1778588da21e](https://github.com/user-attachments/assets/fea3cf93-36c8-4a7f-b537-2bc642d35349)

# Result:
Thus, all the data visualization techniques of seaborn has been implemented.
