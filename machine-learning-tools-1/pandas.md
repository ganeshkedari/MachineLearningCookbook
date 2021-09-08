# Pandas
# Data Frame
* Importing Pandas Module
    import pandas as pd
    
* Reading CSV File in Pandas
    df = pd.read_csv(<csv File Path>, sep=",")
    
* Showing top Records - head\(\)

* Showing last Records - tail\(\)

* Shape of Data Frame

* Data Frame size \(rows\*columns\)

* Number of Rows in Data Frame - len\(\) 

* Column names in Data Frame 
````python
	# Print All Columns 
	print(df.columns) 
	
	# iterating the columns 
	for col in df.columns: 
    	print(col) 
````
* Exctracting Data from Pandas
  1. Get Single Column
  2. Get Range of rows in Single Column
  3. Get Single value in Column
  4. Get Multiple Columns
  
* Sort Data Frame

* Count Values in Column

* Plot a Data Frame

* Replace values in Column 
  
    ````python
    df[<Column Name>].replace(<Value to Serch>,<Value to Replace>,inplace=True)
    ````
    ```python
    df['Gender'] = df['Gender'].map({'F': 'Female', 'M': 'Male'})
    ```
    
* Printing Column in Pandas
    print(df[<Column Name>]) 
    
* Rename Columns in Pandas 
    df.columns = ['Column Name', 'Column Name', 'Column Name', 'Column Name']     
    

 ```
    df = df.rename(columns={"A": "a", "B": "c"})
 ```

*  
   
* Unique Values In A Column     
    print(df.<Column Name>.unique())
    
 * Append a column in Dataframe
 ````	
 	df[<Column Name>]=<Value to be appended>
 ````

 * Merge Columns in Dataframe
 ````python
 	df['ColumnA'] = df[df.columns[1:]].apply(
    lambda x: ','.join(x.dropna().astype(str)),
    axis=1)
 ````
 * Insert a column 
    DataFrameName.insert(loc, column, value, allow_duplicates = False)
    
 * Remove a column
 ````
 	df = df.drop(columns="Column Name")
 ````
 ## Pandas Plot 
 - Plotting a Dataframe 
   ````python
import pandas as pd
import matplotlib.pyplot as plt
df = pd.DataFrame({
        'name':['john','mary','peter','jeff','bill','lisa','jose'],
        'age':[23,78,22,19,45,33,20]        
    })
df.plot()
plt.show()
   ````
- Showing legends
````python
	plt.legend(loc='best')
````
- Adding Labels to Plot lines 
````
	df.plot(label="AGE")
````



- Convert column to Date time format

  ````
  df['Month'] = pd.to_datetime(df['Month'],infer_datetime_format=True)
  ````

* Keep Most Recent date value in Dataframe

* Convert API Response to Dataframe
````
response = requests.request("POST", URL, headers={'Content-Type': 'application/json'}, data=json_input)
json_output = json.loads(response.text)
df = json_normalize(json_output)
df.to_csv("data\ddf.csv", sep=',', index=False)
````

Merge Dataframes

Slice Dataframe based on Column Value 

