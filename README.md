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
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
<img width="1032" height="178" alt="image" src="https://github.com/user-attachments/assets/dcd20cea-0acd-424d-9be7-33d4ee28f59e" />
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
<img width="659" height="533" alt="image" src="https://github.com/user-attachments/assets/57847684-d1be-4dc2-ba17-9bfbeb8e97d8" />
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
<img width="664" height="536" alt="image" src="https://github.com/user-attachments/assets/2394c2dd-e6fd-4f03-b0e7-9b75e38d740f" />
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
<img width="846" height="579" alt="image" src="https://github.com/user-attachments/assets/8f3e9f3d-c56b-44a5-9728-b579cd1007f6" />
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
<img width="703" height="549" alt="image" src="https://github.com/user-attachments/assets/0077d544-32ab-416f-87e7-670cc1badcf4" />
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
<img width="706" height="551" alt="image" src="https://github.com/user-attachments/assets/c2826262-9b4b-4107-a128-83b48efee60f" />
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
<img width="571" height="432" alt="image" src="https://github.com/user-attachments/assets/a9af838b-b62e-4b1e-9369-a6dc33316532" />
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
<img width="684" height="550" alt="image" src="https://github.com/user-attachments/assets/3c192977-6711-4027-968b-02887a9d323a" />
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
<img width="571" height="453" alt="image" src="https://github.com/user-attachments/assets/87b239e1-0ccd-44da-88dd-a8fd1ace47dc" />
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
<img width="723" height="551" alt="image" src="https://github.com/user-attachments/assets/72eedd8a-6318-46c6-b507-08be4af98e5f" />
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
<img width="730" height="614" alt="image" src="https://github.com/user-attachments/assets/93c32702-8c77-4eb1-86e7-0537869510db" />

# Result:
Thus,the Data Visualization using seaborn python data is implemented successfully
