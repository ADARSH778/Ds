# Experiment Lab Introduction
### Name : ADARSH CHOWDARY REDDINENI
### Reference Number : 212223040166
### Department : CSE
# Codes of Lab Introduction:
```
1. Write a Python program to select the 'name' and 'score' columns from the following DataFrame.

       Sample DataFrame:

              exam_data = {'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],

               'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],

              'attempts': [1, 3, 4, 3, 5, 3, 6, 1, 7, 1] } 

 

2. For the above dataframe, Write a program to select the data who's attempt is greater than 3.

3. Write python code for indexing rows and columns based on the following conditions:

Assume we have the following dataframe:

data = {'name': ['Alice', 'Bob', 'Charlie', 'Dave'],

        'age': [25, 35, 40, 28],

        'gender': ['F', 'M', 'M', 'M'],

        'salary': [50000, 70000, 60000, 80000]}

df = pd.DataFrame(data)

a. Select rows where age is greater than 30:

b. Select rows where name contains 'e':

c. Select rows where gender is 'M' and salary is greater than 65000:

d. Select columns 'name' and 'age'

ACTIVITY 2:

1. Write python code for indexing rows and columns using iloc or loc method based on the following conditions:

a.  select the rows where clients with primary education have subscribed to a deposit?

b.  select the rows where clients who have not subscribed to a deposit?

c. select the rows where clients who have subscribed to a deposit either have a housing or a personal loan?

d. select the rows where clients with secondary education who have not subscribed to a deposit?

e. select the rows where  clients who have subscribed to a term deposit as an outcome of the successful marketing campaign? 

f. select the rows where unemployed clients who have not subscribed to deposit?

e. Select columns 'name' and 'salary' where age is less than or equal to 30:


```
import pandas as pd
df=pd.DataFrame({"a":[4,5,6],"b":[7,8,9],"c":[10,11,12]},index=[1,2,3])
print(df)

import pandas as pd
data=[1,2,3,4]
df=pd.DataFrame(data)
print(df)

import pandas as pd
data=[["Alex",10],["Bob",20]]
df=pd.DataFrame(data,columns=['Name','Age'])
print(df)

import pandas as pd
data={'cars':['BMW','VOLVO','FORD'],'passings':[3,7,2]}
df=pd.DataFrame(data)
print(df)

import pandas as pd
data=[{"a":1,"b":2},{"a":5,"b":10,"c":20}]
df=pd.DataFrame(data)
df1=pd.DataFrame(data,index=['first','second'],columns=['a','b'])
df1

import pandas as pd
data={'Name':['Jai','Princi','Gaurav','Anuj'],'Height':[5.1,6.2,5.1,5.2],'Qualification':['MSC','MA','MSC','BA']}
df=pd.DataFrame(data)
address=['Chennai','Bangalore','Ooty','Bombay']
df['Address']=address
df

import pandas as pd
data={'Name':['Jai','Princi','Gaurav','Anuj'],'Height':[5.1,6.2,5.1,5.2],'Qualification':['MSC','MA','MSC','BA']}
df=pd.DataFrame(data)
address=['Chennai','Bangalore','Ooty','Bombay']
df['Address']=address
del df['Address']
df

import pandas as pd
data={'Name':['Jai','Princi','Gaurav','Anuj'],'Height':[5.1,6.2,5.1,5.2],'Qualification':['MSC','MA','MSC','BA']}
df=pd.DataFrame(data)
address=['Chennai','Bangalore','Ooty','Bombay']
df['Address']=address
df.drop(['Address'],axis=1,inplace=True)
df

import pandas as pd
data={'Name':['Jai','Princi','Gaurav','Anuj'],'Height':[5.1,6.2,5.1,5.2],'Qualification':['MSC','MA','MSC','BA']}
df=pd.DataFrame(data)
address=['Chennai','Bangalore','Ooty','Bombay']
df['Address']=address
df.drop(['Address'],axis=1,inplace=True)
df.pop('Height')
df

import pandas as pd
data={'Name':['Jai','Princi','Gaurav','Anuj'],'Age':[27,24,56,45],'Address':['Chennai','Bangalore','Ooty','Bombay'],'Qualification':['MSC','MA','MSC','BA']}
df=pd.DataFrame(data)
df
df.rename(columns={'Address':'place'},inplace=True)
df

import pandas as pd
df=pd.DataFrame([[1,2],[3,4]],columns=['a','b'])
df2=pd.DataFrame([[5,6],[7,8]],columns=['a','b'])
df=pd.concat([df,df2])
df

data={'Name':['Jai','Princi','Gaurav','Anuj'],'Age':[27,24,56,45],'Address':['Chennai','Bangalore','Ooty','Bombay'],'Qualification':['MSC','MA','MSC','BA']}
df=pd.DataFrame(data)
df.drop(2,axis=0,inplace=True)
df

data={'Name':['Jai','Princi','Gaurav','Anuj'],'Age':[27,24,56,45],'Address':['Chennai','Bangalore','Ooty','Bombay'],'Qualification':['MSC','MA','MSC','BA']}
df=pd.DataFrame(data)
df=df['Name']
df

data={'Name':['Jai','Princi','Gaurav','Anuj'],'Age':[27,24,56,45],'Address':['Chennai','Bangalore','Ooty','Bombay'],'Qualification':['MSC','MA','MSC','BA']}
df=pd.DataFrame(data)
print(df[['Name','Qualification']])

data={'Name':['Jai','Ajey','Gaurav','Anuj'],'Age':[27,24,56,45],'Address':['Chennai','Bangalore','Ooty','Bombay'],'Qualification':['MSC','MA','MSC','BA']}
df=pd.DataFrame(data)
df.filter(items=['Name','Age'])
df.filter(like='ame')
df.filter(regex='a|e',axis=1)

data={'Name':['Jai','Ajey','Gaurav','Anuj'],'Age':[27,24,27,45],'Address':['Chennai','Bangalore','Ooty','Bombay'],'Qualification':['MSC','MA','MSC','BA']}
df=pd.DataFrame(data)
df=df.drop_duplicates(subset=(['Age']))
df

data={'Name':['Jai','Ajey','Jai','Anuj'],'Age':[27,24,27,45],'Address':['Chennai','Bangalore','Ooty','Bombay'],'Qualification':['MSC','MA','MSC','BA']}
df=pd.DataFrame(data)
df=df.drop_duplicates(subset=(['Name','Age']),keep='last')
df

data={'Name':['Jai','Ajey','Gaurav','Anuj'],'Age':[27,24,27,45],'Address':['Chennai','Bangalore','Ooty','Bombay'],'Qualification':['MSC','MA','MSC','BA']}
df=pd.DataFrame(data)
dfs=df.sample(n=2)
dfs

data={'Name':['Jai','Ajey','Gaurav','Anuj'],'Age':[27,24,27,45],'Address':['Chennai','Bangalore','Ooty','Bombay'],'Qualification':['MSC','MA','MSC','BA']}
df=pd.DataFrame(data)
df_sample=df.sample(frac=0.5)
df_sample

import pandas as pd
data={'name':['Alice','Bob','Charlie','David'],'age':[25,30,35,40],'salary':[20000,45000,23000,67000],'gender':['F','M','F','M']}
df=pd.DataFrame(data)
top=df.nlargest(1,columns='salary') #(nsmallest) for smaller salary
print(top)

a=df.query('age>30')
print(a)

a=df.query('name.str.contains("a") and salary>40000')
print(a)

a=df.query(' gender == ["F","M"] and age>30')
a

a=df.loc[:,'age']
a

b=df.iloc[:,0]
b

a=df.loc[:,['name','age']]
a

a=df[df['age']>30]
a

a=df[(df['gender']== 'F') & (df['age']>30)]
a

a=df[df['name'].str.startswith(('A','C'))]
a

print(df.tail(2)) #head for first to last

print(df.head(2))

df.info()

df.describe()

# Result:
Hence the lab activity are completed successfully
