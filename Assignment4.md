**Q1. How do you load a CSV file into a Pandas DataFrame?**

	>> import pandas as pd
	>> df = pd.read_csv("csv_file_path")
	
**Q2. How do you check the data type of a column in a Pandas DataFrame?**

	>> l = [[1,3],[5,7],[9,2],[4,6],[8,0]]
	>> demo_df = pd.DataFrame(l)
	>> print(demo_df.dtypes)
	
**Q3. How do you select rows from a Pandas DataFrame based on a condition?**

	records = {
    'SNo' : [1, 2, 3, 4],
    'Name' : ['vijendra', 'ved', 'raj', 'mahi'],
    'Age' : [25, 23, 26, 26],
    'Project' : ['charm', 'charm', 'procorn', 'docitt'],
	}
	df = pd.DataFrame(records, columns = ['SNo', 'Name', 'Age', 'Project'])
	df_with_condition = df[df['Age'] < 25]
	print(df_with_condition)
	
**Q4. How do you rename columns in a Pandas DataFrame?**

Using rename() function.
	
	user_data = {
		'name': ['vijendra', 'ved', 'raj', 'mahi'],
		'age': [25, 23, 26, 26],
	}
	df = pd.DataFrame(user_data)
	df.rename(columns = { 'name':'Name', 'age':'Age' }, inplace=True)
	print(df)
	
**Q5. How do you drop columns in a Pandas DataFrame?**

There can be multiple ways to drop a column.

Drop a single column using drop() function.
	
	user_data = {
    'name': ['vijendra', 'ved', 'raj', 'mahi'],
    'age': [25, 23, 26, 26],
	}	
	df = pd.DataFrame(user_data)
	df.drop('Age', axis=1)
	
Drop multiple columns using drop() function.

	user_data = {
    'name': ['vijendra', 'ved', 'raj', 'mahi'],
    'age': [25, 23, 26, 26],
	}	
	df = pd.DataFrame(user_data)
	df.drop(['Age', 'Name'], axis=1)
	
Drop columns based on index values.

	user_data = {
    'name': ['vijendra', 'ved', 'raj', 'mahi'],
    'age': [25, 23, 26, 26],
	}	
	df = pd.DataFrame(user_data)
	df.drop(df.columns[[0, 1]], axis=1, inplace=True)
	
**Q6. How do you find the unique values in a column of a Pandas DataFrame?**

	user_data = {
    'name': ['vijendra', 'ved', 'raj', 'mahi'],
    'age': [25, 23, 26, 26],
	}	
	df = pd.DataFrame(user_data)
	df['Age'].unique()
	
**Q7. How do you find the number of missing values in each column of a Pandas DataFrame?**

	import numpy as np
	user_data = {
    'name': ['vijendra', 'ved', 'raj', np.nan],
    'age': [25, np.nan, np.nan, 26],
	}
	df = pd.DataFrame(user_data)
	df.isna().sum()
	
**Q8. How do you fill missing values in a Pandas DataFrame with a specific value?**

	import numpy as np
	user_data = {
    'name': ['vijendra', 'ved', 'raj', np.nan],
    'age': [25, np.nan, np.nan, 26],
	}
	df = pd.DataFrame(user_data)
	df.fillna(0)
	
**Q9. How do you concatenate two Pandas DataFrames?**	

	obj1 = {
    "a": [1, 2, 3],
    "b": [5, 7, 8],
    "c": [3, np.nan, np.nan]
	}
	df1 = pd.DataFrame(obj1)
	df1
	
	obj2 = {
    "a": ["q"],
    "b": ["p"],
    "c": ["a"],
	}
	df2 = pd.DataFrame(obj2)
	df2
	
	frames = [ df1, df2 ]
	result_df = pd.concat(frames)
	result_df
	
**Q10. How do you merge two Pandas DataFrames on a specific column?**

	df1 = pd.DataFrame({
    'Name': ['Vijendra', 'Ved', 'Raj'],
    'Marks': [23, 24, 21],
	})
	df2 = pd.DataFrame({
    'Name': ['Vijendra', 'Ved', 'Mahi'],
    'Age': [24, 22, 34],
    'Address': ['SN', 'AP', 'SN'],	
	})
	df1.merge(df2[['Name', 'Age', 'Address']])
	
**Q11. How do you group data in a Pandas DataFrame by a specific column and apply an aggregation function?**

	grp_df = pd.DataFrame({
    'Name': ['a', 'b', 'c', 'a', 'd', 'c'],
    'Roll': [1, 3, 2, 5, 6, 3]
	})
	grp_df.groupby(['Name'])
	grp_df.agg(['sum'])
	
**Q12. How do you pivot a Pandas DataFrame?**

pivot_table takes 3 arguments index which specify rows, columns which specifies columns and values which will be the values based on row and col. 

	import pandas as pd

	df = pd.DataFrame({
    'states': ['Gujarat', 'Rajasthan', 'Panjab', 'Delhi'],
    'Sales': [1000, 4000, 2300, 8900],
    'Amount': [120000, 34000, 67890, 98210]
	})
	df.pivot_table(index='Sales', columns='states', values='Amount')
	
**Q13. How do you change the data type of a column in a Pandas DataFrame?**

For changing the type of column we can use DataFrame.astype().
	
When we have to change all the column type to same type.
	
	d_f = pd.DataFrame({
    'A': [1, 2, 3, 4, 5],
    'B': ['a', 'b', 'c', 'd', 'e'],
    'C': [1.1, '1.0', '1.3', 2, 5]
	})
	d_f = d_f.astype(str)
	print(d_f.dtypes)

when we have to change each column type of different type.

	d_f = pd.DataFrame({
    'A': [1, 2, 3, 4, 5],
    'B': ['a', 'b', 'c', 'd', 'e'],
    'C': [1.1, '1.0', '1.3', 2, 5]})
	types = {'A': int, 'C': float}
	d_f = d_f.astype(types)
	print(d_f.dtypes)
	
**Q14. How do you sort a Pandas DataFrame by a specific column?**	
		
We can sort the DF using DataFrame.sort_values() function(By default sorting is ASC)

	d_f = pd.DataFrame({
    'A': [1, 4, 2, 5, 3],
    'B': ['a', 'b', 'c', 'd', 'e'],
    'C': [1.1, '1.0', '1.3', 2, 5]})
	d_f.sort_values('A')
	
Changing the order of sorting.

	d_f.sort_values(by="A", ascending=False)

Specifying the algorithm type.

	d_f.sort_values(by="A", ascending=False, kind="mergesort")
	
Sorting with multiple columns.

	d_f.sort_values(by=["A", "B"])[["A", "B"]]
	
**Q15. How do you create a copy of a Pandas DataFrame?**

Copies can be created using DataFrame.copy(deep=True).

When deep=True (default), a new object will be created with a copy of the calling object’s data and indices. Modifications to the data or indices of the copy will not be reflected in the original object 

	s = pd.DataFrame({
    'A': [2, 3]
	})
	deep = s.copy()
	deep
	
	shallow = s.copy(deep=False)
	
**Q16. How do you filter rows of a Pandas DataFrame by multiple conditions?**

	df = pd.DataFrame({
    'states': ['Gujarat', 'Rajasthan', 'Panjab', 'Delhi'],
    'Sales': [1000, 4000, 2300, 8900],
    'Amount': [120000, 34000, 67890, 98210]
	})
	df.loc[ (df['Sales']>1000) & (df['Amount']<100000) ]
	
**Q17. How do you calculate the mean of a column in a Pandas DataFrame?**

	df = pd.DataFrame({
    'states': ['Gujarat', 'Rajasthan', 'Panjab', 'Delhi'],
    'Sales': [1000, 4000, 2300, 8900],
    'Amount': [120000, 34000, 67890, 98210]
	})
	df['Sales'].mean()
	
**Q18. How do you calculate the standard deviation of a column in a Pandas DataFrame?**

Standard deviation tells about how the values in the dataset are spread. They also tells how far the values in the dataset are from the arithmetic mean of the columns in the dataset.

	df = pd.DataFrame({
    'states': ['Gujarat', 'Rajasthan', 'Panjab', 'Delhi'],
    'Sales': [1000, 4000, 2300, 8900],
    'Amount': [120000, 34000, 67890, 98210]
	})
	df['Sales'].std()
	
**Q19. How do you calculate the correlation between two columns in a Pandas DataFrame?**

Correlation is used to summarize the strength and direction of the linear association between two quantitative variables. It is denoted by r and values between -1 and +1. A positive value for r indicates a positive association, and a negative value for r indicates a negative association.

	df = pd.DataFrame({
    'states': ['Gujarat', 'Rajasthan', 'Panjab', 'Delhi'],
    'Sales': [1000, 4000, 2300, 8900],
    'Amount': [120000, 34000, 67890, 98210]
	})
	df['Sales'].corr(df['Amount'])
	
**Q20. How do you select specific columns in a DataFrame using their labels?**

	df = pd.DataFrame({
    'states': ['Gujarat', 'Rajasthan', 'Panjab', 'Delhi'],
    'Sales': [1000, 4000, 2300, 8900],
    'Amount': [120000, 34000, 67890, 98210]
	})
	print(df['Sales'])
	
**Q21. How do you select specific rows in a DataFrame using their indexes?**

We can get a specific row using DataFrame.iloc[row_index].

	df = pd.DataFrame({
    'states': ['Gujarat', 'Rajasthan', 'Panjab', 'Delhi'],
    'Sales': [1000, 4000, 2300, 8900],
    'Amount': [120000, 34000, 67890, 98210]
	})
	df.iloc[0]
	
**Q22. How do you sort a DataFrame by a specific column?**

We can sort the DF using DataFrame.sort_values() function(By default sorting is ASC)

	d_f = pd.DataFrame({
    'A': [1, 4, 2, 5, 3],
    'B': ['a', 'b', 'c', 'd', 'e'],
    'C': [1.1, '1.0', '1.3', 2, 5]})
	d_f.sort_values('A')
	
Changing the order of sorting.

	d_f.sort_values(by="A", ascending=False)

Specifying the algorithm type.

	d_f.sort_values(by="A", ascending=False, kind="mergesort")
	
Sorting with multiple columns.

	d_f.sort_values(by=["A", "B"])[["A", "B"]]
	
**Q23. How do you create a new column in a DataFrame based on the values of another column?**

	df = pd.DataFrame({
    'states': ['Gujarat', 'Rajasthan', 'Panjab', 'Delhi'],
    'Sales': [1000, 4000, 2300, 8900],
    'Amount': [120000, 34000, 67890, 98210]
	})
	df['new_col'] = df['Sales'] + df['Amount']
	
**Q24. How do you remove duplicates from a DataFrame?**

When the complete row is duplicated.

	df = pd.DataFrame({
    'states': ['Gujarat', 'Rajasthan', 'Panjab', 'Gujarat'],
    'Sales': [1000, 4000, 1000, 1000],
    'Amount': [120000, 34000, 67890, 120000]
	})
	df.drop_duplicates()
	
To remove duplicates present in specific column.

	df = pd.DataFrame({
    'states': ['Gujarat', 'Rajasthan', 'Panjab', 'Gujarat'],
    'Sales': [1000, 4000, 1000, 1050],
    'Amount': [120000, 34000, 67890, 13450]
	})
	df.drop_duplicates(subset='states', keep=False, inplace=True)
	df
	
**Q25. What is the difference between .loc and .iloc in Pandas?**

loc() and iloc() are used in slicing data from the Pandas DataFrame.

The loc() function is label based data selecting method which means that we have to pass the name of the row or column which we want to select. This method includes the last element of the range passed in it, unlike iloc(). loc() can accept the boolean data unlike iloc().

**Ex 1.** Selecting data according to some conditions.
**display(df.loc[condition])**

**Ex 2.** Selecting a range of rows from the DataFrame.
**display(df.loc[2: 5])**

**Ex 3.** Updating the value of any column.
**df.loc[ (condition), ['Col_name']] = value**

The iloc() function is an indexed-based selecting method which means that we have to pass an integer index in the method to select a specific row/column. This method does not include the last element of the range passed in it unlike loc(). iloc() does not accept the boolean data unlike loc().

**Ex 1.** Selecting rows using integer indices.
**display(df.iloc[[0, 2, 4, 7]])**

**Ex 2.** Selecting a range of columns and rows simultaneously
**display(df.iloc[1: 5, 2: 5])**

	
	
	
