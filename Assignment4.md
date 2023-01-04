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
