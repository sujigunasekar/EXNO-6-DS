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
![328149364-49d9b1ca-f56c-4a3c-9f69-2fd60595a9bd](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/af87f220-794b-4b87-8972-efcaa108722e)
```
df=sns.load_dataset('tips')
df
```
![328149572-fd6d7841-8c38-4994-9fbf-85db4897edf7](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/c85900b6-7adb-4369-bf74-f4ed0f0da0cc)
```
sns.lineplot(x='total_bill',y='tip',data=df,hue='sex',linestyle='solid',legend='auto')
```
![328149708-9f5e55e3-a87f-4db0-b679-c7f2f6299e9e](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/524c1e7e-c1d5-4d13-81f0-323a25e6e3ab)
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
![328149872-be2634bf-e69f-4bd7-80c2-961e8e985caa](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/7b3e563b-7e22-4cb3-bd9e-21433880ed64)
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
![328150023-d6e12d89-00ee-4020-9052-95353c75ddfc](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/6cdba5f6-4d65-4cbb-ac91-047a1ad07fe8)
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
![328150259-8b6cf167-f1b1-4125-a1bf-893d015466d2](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/d78095b9-3f84-45be-a0b7-121bac260372)
```
import seaborn as sns
dt= sns.load_dataset('tips')
# Bar plot with hue parameter
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
```
![328150790-552ea7af-f178-4ee3-a995-3cea86a3d517](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/f9814cf5-63e9-4fdf-b80a-0e05ff025ebc)
```
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![328151022-85bbe2e0-26d9-48f4-a525-dba9676dec9e](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/e00bb5f2-87d3-47e7-946f-ce8e4293a728)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```
![328217626-04aef0b1-40bc-4ed1-8712-39b11bc5c8de](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/4eed8b41-c066-4a64-bd03-84c367674c93)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![328151511-3abb21a9-8a8f-4e3f-869c-817cd65f372f](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/f1f5e5b6-bb30-413b-a056-ff227aac3ae1)
```
import seaborn as sns
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![328151702-69a6d3bd-7a4c-4f22-9ec0-0a395db5bfe5](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/e6f44550-a09e-4b7e-8174-9ef39adc7751)
```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![328152700-9afb2c33-4183-424b-9f6f-a759713f8dff](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/090a5ddc-7117-4733-af73-be0dee31b047)
```
sns.histplot(data = num_var, kde = True)
```
![328152857-23c94a65-4311-4ee7-9b6e-7a363ebab670](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/b83f5d86-e855-4d02-8235-297a77f5e294)
```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![328153012-d13a9418-892a-453d-b72f-30ac8e87bcbd](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/60792e90-95d3-40a3-8a3e-b7a5256b5625)
```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![328153140-e20337b2-2b14-495f-a52f-0af4cf6c1caa](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/7a6ff59c-dc70-4cfe-bd74-86c4dba8bd1d)
```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![328153315-5beeead7-5e71-44b9-9f4d-1757c08b717e](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/c3bb1141-ef64-4422-8b99-0fc897d59cf0)
```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6,
palette="Set3", inner="quartile")
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![328153527-60486938-8a31-476b-9a03-82f02e229ce1](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/aa7ee9ef-a616-496f-8b60-881d3ef8d488)
```
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![328153665-8fde639d-a3b9-4768-b4d7-fe7ccc6318fb](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/e7fcbb56-284f-444f-a001-0922fc0bb591)
```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```
![328218294-047ec4fb-77ef-4904-9336-4c36470af5ca](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/f3e6e584-bb0b-48b5-b672-9f3655a20cdf)
```
sns.kdeplot(data=mart,x='PassengerId')
```
![328218502-f5e857ca-4b90-4797-9921-009d3801bd42](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/8123a60c-6d42-49d0-bb04-22f67f14fa7b)
```
sns.kdeplot(data=mart,x='Age')
```
![328218740-08ccbb17-85df-44f2-af62-231d19053113](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/4b91c28f-5564-4fdb-b784-e1ab89d9f6aa)
```
sns.kdeplot(data=mart)
```
![328219012-a3a4a863-dafb-4267-be4f-89f875c8594a](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/35cd854f-7c22-46f2-94d3-243f8922b7ea)
```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![328219264-3464c54e-9040-42dd-8bdc-4e8307ea657c](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/d2c7cc1a-647c-4018-b6da-161f363399e2)
```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![328219748-af4205be-34da-4900-968d-dcd16a430976](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/4d61767d-8e22-4fbe-8716-e05192940db0)
```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![328219751-39c01876-fb2e-41e1-8e58-49e786960738](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/03f9c11c-c7aa-41dd-9b09-28420b71dad1)
```
hm=sns.heatmap(data=data)
```
![328219832-01ef62a5-40a0-4c78-aaac-d2183ea2609b](https://github.com/sujigunasekar/EXNO-6-DS/assets/119559822/578598d0-db27-4321-9e06-3109f88f836d)

# Result:
Thus, all the data visualization techniques of seaborn has been implemented.
