## Pandas Assignment

Q1. How do you load a CSV file into a Pandas DataFrame?
```
Using read_csv()

import pandas as pd
df = pd.read_csv('data.csv')
print(df)
```

Q2. How do you check the data type of a column in a Pandas DataFrame?
```
df.dtypes => For all columns
df['col_name'].dtype => For a particular column

import pandas as pd
data = {'Products': ['AAA','BBB','CCC','DDD','EEE'],
          'Prices': [200,700,400,1200,900]
        }
df = pd.DataFrame(data)
print (df['Prices'].dtypes)
```

Q3. How do you select rows from a Pandas DataFrame based on a condition?
```
import pandas as pd  
record = {
  
 'Name': ['Ankit', 'Amit', 'Aishwarya', 'Priyanka', 'Priya', 'Shaurya' ],
 'Age': [21, 19, 20, 18, 17, 21],
 'Stream': ['Math', 'Commerce', 'Science', 'Math', 'Math', 'Science'],
 'Percentage': [88, 92, 95, 70, 65, 78] }
  
dataframe = pd.DataFrame(record, columns = ['Name', 'Age', 'Stream', 'Percentage'])
print("Given Dataframe :\n", dataframe) 
rslt_df = dataframe[dataframe['Percentage'] > 80]
  
print('\nResult dataframe :\n', rslt_df)
```

Q4. How do you rename columns in a Pandas DataFrame?
```
import pandas as pd
rankings = {'test': ['India', 'South Africa', 'England',
							'New Zealand', 'Australia'],
			'odi': ['England', 'India', 'New Zealand',
							'South Africa', 'Pakistan'],
			't20': ['Pakistan', 'India', 'Australia',
							'England', 'New Zealand']}
rankings_pd = pd.DataFrame(rankings)
print(rankings_pd)

rankings_pd.rename(columns = {'test':'TEST'}, inplace = True)
#OR
#rankings_pd.columns = ['TEST', 'ODI', 'T-20']
#OR
#rankings_pd.set_axis(['A', 'B', 'C'], axis='columns', inplace=True)
#OR
#rankings_pd.columns = rankings_pd.columns.str.replace('odi', 'Col_ODI')
print("\nAfter modifying first column:\n", rankings_pd.columns)
```

Q5. How do you drop columns in a Pandas DataFrame?
```
The drop() method removes the specified row or column.
By specifying the column axis (axis='columns'), the drop() method removes the specified column.
By specifying the row axis (axis='index'), the drop() method removes the specified row.

import pandas as pd
data = {
  "name": ["Sally", "Mary", "John"],
  "age": [50, 40, 30],
  "qualified": [True, False, False]
}
df = pd.DataFrame(data)
newdf = df.drop("age", axis='columns')
print(newdf)
```

Q6. How do you find the unique values in a column of a Pandas DataFrame?
```
import pandas as pd
data = {
    'A':['A1', 'A2', 'A3', 'A4', 'A5'], 
    'B':['B1', 'B2', 'B3', 'B4', 'B4'], 
    'C':['C1', 'C2', 'C3', 'C3', 'C3'], 
    'D':['D1', 'D2', 'D2', 'D2', 'D2'], 
    'E':['E1', 'E1', 'E1', 'E1', 'E1'] }
  
df = pd.DataFrame(data)  
# Get the unique values of 'B' column
df.B.unique()
# Get the unique values of 'E' column
df.E.unique()
```

Q7. How do you find the number of missing values in each column of a Pandas DataFrame?
```
import pandas as pd
import numpy as np
data = {'first_set': [1,2,3,4,5,np.nan,6,7,np.nan,np.nan],
        'second_set': ['a','b',np.nan,np.nan,'c','d','e',np.nan,np.nan,'f'],
        'third_set':['aa',np.nan,'bb','cc',np.nan,np.nan,'dd',np.nan,np.nan,'ee']
        }
df = pd.DataFrame(data,columns=['first_set','second_set','third_set'])

print (df.isna().sum())
```

Q8. How do you fill missing values in a Pandas DataFrame with a specific value?
```
print (df['col_name'].isna().sum())
```

Q9. How do you concatenate two Pandas DataFrames?
```
import pandas as pd
import numpy as np
df1 = pd.DataFrame(np.random.randint(25, size=(4, 4)),
				index=["1", "2", "3", "4"],
				columns=["A", "B", "C", "D"])
df2 = pd.DataFrame(np.random.randint(25, size=(6, 4)),
				index=["5", "6", "7", "8", "9", "10"],
				columns=["A", "B", "C", "D"])
df3 = pd.DataFrame(np.random.randint(25, size=(4, 4)),
				columns=["A", "B", "C", "D"])
df4 = pd.DataFrame(np.random.randint(25, size=(4, 4)),
				columns=["E", "F", "G", "H"])
display(df1, df2, df3, df4)

# concatenating df1 and df2 along rows
vertical_concat = pd.concat([df1, df2], axis=0)
# concatenating df3 and df4 along columns
horizontal_concat = pd.concat([df3, df4], axis=1)
 
display(vertical_concat, horizontal_concat)
```

Q10. How do you merge two Pandas DataFrames on a specific column?
```
import pandas as pd
df1 = pd.DataFrame({'Name':['Raju', 'Rani', 'Geeta', 'Sita', 'Sohit'],
					'Marks':[80, 90, 75, 88, 59]})
df2 = pd.DataFrame({'Name':['Raju', 'Divya', 'Geeta', 'Sita'],
					'Grade':['A', 'A', 'B', 'A'],
					'Rank':[3, 1, 4, 2 ],
					'Gender':['Male', 'Female', 'Female', 'Female']})
display(df1)
display(df2)
# applying merge with more parameters
df1.merge(df2[['Grade', 'Name']], on = 'Name', how = 'left')
```

Q11. How do you group data in a Pandas DataFrame by a specific column and apply an aggregation function?
```
import pandas as pd
df = pd.read_csv("nba.csv")

df.aggregate({"Number":['sum', 'min'],
			"Age":['max', 'min'],
			"Weight":['min', 'sum'],
			"Salary":['sum']})

```

Q12. How do you pivot a Pandas DataFrame?
```
The pivot() function is used to reshaped a given DataFrame organized by given index / column values. This function does not support data aggregation, multiple values will result in a MultiIndex in the columns.

import numpy as np
import pandas as pd
df = pd.DataFrame({'fff': ['one', 'one', 'one', 'two', 'two',
                           'two'],
                   'bbb': ['P', 'Q', 'R', 'P', 'Q', 'R'],
                   'baa': [2, 3, 4, 5, 6, 7],
                   'zzz': ['h', 'i', 'j', 'k', 'l', 'm']})
df.pivot(index='fff', columns='bbb', values='baa')

O/P:-
bbb	P	Q	R
fff			
one	2	3	4
two	5	6	7
```

Q13. How do you change the data type of a column in a Pandas DataFrame?
```
import pandas as pd
df = pd.DataFrame({
	'A': [1, 2, 3, 4, 5],
	'B': ['a', 'b', 'c', 'd', 'e'],
	'C': [1.1, '1.0', '1.3', 2, 5]})

# converting all columns to string type
df = df.astype(str)

# using dictionary to convert specific columns
convert_dict = {'A': int,
                'C': float
                }
df = df.astype(convert_dict)

print(df.dtypes)

```

Q14. How do you sort a Pandas DataFrame by a specific column?
```
import pandas as pd
students = [('Ankit', 22, 'Up', 'Geu'),
		('Ankita', 31, 'Delhi', 'Gehu'),
		('Rahul', 16, 'Tokyo', 'Abes'),
		('Simran', 41, 'Delhi', 'Gehu'),
		('Shaurya', 33, 'Delhi', 'Geu'),
		('Harshita', 35, 'Mumbai', 'Bhu' ),
		('Swapnil', 35, 'Mp', 'Geu'),
		('Priya', 35, 'Uk', 'Geu'),
		('Jeet', 35, 'Guj', 'Gehu'),
		('Ananya', 35, 'Up', 'Bhu')
			]

# Create a DataFrame object from list of tuples with columns and indices.
details = pd.DataFrame(students, columns =['Name', 'Age', 'Place', 'College'],
				index =[ 'b', 'c', 'a', 'e', 'f', 'g', 'i', 'j', 'k', 'd'])

# Sort the rows of dataframe by 'Name' column
rslt_df = details.sort_values(by = 'Name')
rslt_df
```

Q15. How do you create a copy of a Pandas DataFrame?
```
The copy() method returns a copy of the DataFrame.
By default, the copy is a "deep copy" meaning that any changes made in the original DataFrame will NOT be reflected in the copy.
import pandas as pd
data = {
  "name": ["Sally", "Mary", "John"],
  "qualified": [True, False, False]
}
df = pd.DataFrame(data)
newdf = df.copy()

print(newdf)
```

Q16. How do you filter rows of a Pandas DataFrame by multiple conditions?
```
import pandas as pd
dataFrame = pd.DataFrame({'Name': [' RACHEL ', ' MONICA ', ' PHOEBE ', ' ROSS ', 'CHANDLER', ' JOEY '],
						'Age': [30, 35, 37, 33, 34, 30],
						'Salary': [100000, 93000, 88000, 120000, 94000, 95000],
						'JOB': ['DESIGNER', 'CHEF', 'MASUS', 'PALENTOLOGY', 'IT', 'ARTIST']})
# filter dataframe
display(dataFrame.loc[(dataFrame['Salary']>=100000) & (dataFrame['Age']< 40) & (dataFrame['JOB'].str.startswith('D')),
					['Name','JOB']])

```

Q17. How do you calculate the mean of a column in a Pandas DataFrame?
```
import pandas as pd
df = pd.DataFrame({"A":[12, 4, 5, 44, 1],
				"B":[5, 2, 54, 3, 2],
				"C":[20, 16, 7, 3, 8],
				"D":[14, 3, 17, 2, 6]})

df['A'].mean(axis = 0)
```

Q18. How do you calculate the standard deviation of a column in a Pandas DataFrame?
```
import pandas as pd
my_data = {'Name':pd.Series(['Tom','Jane','Vin','Eve','Will']),'Age':pd.Series([45, 67, 89, 12, 23]),'value':pd.Series([8.79,23.24,31.98,78.56,90.20])}
print("The dataframe is :")
my_df = pd.DataFrame(my_data)
print(my_df)
print("The standard deviation of column 'Age' is :")
print(my_df['Age'].std())
print("The standard deviation of column 'value' is :")
print(my_df['value'].std())
```
Q19. How do you calculate the correlation between two columns in a Pandas DataFrame?
```
import pandas as pd
data = pd.DataFrame({
	"column1": [12, 23, 45, 67],
	"column2": [67, 54, 32, 1],
	"column3": [34, 23, 56, 23]
}
)
print(data)

# correlation between column 1 and column2
print(data['column1'].corr(data['column2']))

# correlation between column 2 and column3
print(data['column2'].corr(data['column3']))

# correlation between column 1 and column3
print(data['column1'].corr(data['column3']))

```

Q20. How do you select specific columns in a DataFrame using their labels?
```
import pandas as pd
technologies = {
    'Courses':["Spark","PySpark"],
    'Fee' :[20000,25000],
    'Duration':['30days','40days'],
    'Discount':[1000,2300]
              }
df = pd.DataFrame(technologies)
print(df)

df2 = df[["Courses","Fee","Duration"]]
#or
# df.loc[,start:stop:step]
df2 = df.loc[:, ["Courses","Fee","Discount"]]
```

Q21. How do you select specific rows in a DataFrame using their indexes?
```
print(df.iloc[[2,3,6]])
```

Q22. How do you sort a DataFrame by a specific column?
```
import pandas as pd
students = [('Ankit', 22, 'Up', 'Geu'),
		('Ankita', 31, 'Delhi', 'Gehu'),
		('Rahul', 16, 'Tokyo', 'Abes'),
		('Simran', 41, 'Delhi', 'Gehu'),
		('Shaurya', 33, 'Delhi', 'Geu'),
		('Harshita', 35, 'Mumbai', 'Bhu' ),
		('Swapnil', 35, 'Mp', 'Geu'),
		('Priya', 35, 'Uk', 'Geu'),
		('Jeet', 35, 'Guj', 'Gehu'),
		('Ananya', 35, 'Up', 'Bhu')
			]

# Create a DataFrame object from list of tuples with columns and indices.
details = pd.DataFrame(students, columns =['Name', 'Age', 'Place', 'College'],
				index =[ 'b', 'c', 'a', 'e', 'f', 'g', 'i', 'j', 'k', 'd'])

# Sort the rows of dataframe by 'Name' column
rslt_df = details.sort_values(by = 'Name')
rslt_df

```

Q23. How do you create a new column in a DataFrame based on the values of another column?
```
We can add/append a new column to the DataFrame based on the values of another column using df.assign(), df.apply(), and, np.where() functions and return a new Dataframe after adding a new column.


import pandas as pd
import numpy as np
technologies= {
    'Courses':["Spark","PySpark","Hadoop","Python","Pandas"],
    'Fee' :[22000,25000,23000,24000,26000],
    'Discount':[1000,2300,1000,1200,2500]
          }

df = pd.DataFrame(technologies)
print(df)

# Add column using arithmetic operation based on existing columns 
df["Final_Fee"] = df["Fee"] - df["Discount"]
print(df)

# Add New Column from Existing Column
df = pd.DataFrame(technologies)
df1 = df.assign(Discount_Percent=lambda x: x.Fee * x.Discount / 100)
print(df1)

# Add column using np.where()
df['Discount_rating'] = np.where(df['Discount'] > 2000, 'Good', 'Bad')
print(df)

# Add column using apply()
df['Final_fee'] = df.apply(lambda x: x['Fee'] - x['Discount'], axis=1)
print(df)

```

Q24. How do you remove duplicates from a DataFrame?
```
import pandas as pd
data = {
  "name": ["Sally", "Mary", "John", "Mary"],
  "age": [50, 40, 30, 40],
  "qualified": [True, False, False, False]
}
df = pd.DataFrame(data)

newdf = df.drop_duplicates()
```

Q25. What is the difference between .loc and .iloc in Pandas?
```
The main difference between pandas loc[] vs iloc[] is loc gets DataFrame rows & columns by labels/names and iloc[] gets by integer Index/position.
For loc[], if the label is not present it gives a key error. For iloc[], if the position is not present it gives an index error. 
In this article, I will cover the difference and similarities between loc[] and iloc[] in Pandas DataFrame by exploring with examples.
```
<img width="707" alt="Screenshot 2023-01-22 at 2 10 06 AM" src="https://user-images.githubusercontent.com/118146044/213886329-902a6fbb-0b8f-4316-aa53-3dd167f3585f.png">
