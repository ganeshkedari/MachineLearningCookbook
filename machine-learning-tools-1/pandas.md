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
* Exctracting Data from Pandas
  1. Get Single Column
  2. Get Range of rows in Single Column
  3. Get Single value in Column
  4. Get Multiple Columns
* Sort Data Frame
* Count Values in Column
* Plot a Data Frame
* Replace values in Column 
    df[<Column Name>].replace(<Value to Serch>,<Value to Replace>,inplace=True)
* Printing Column in Pandas
    print(df[<Column Name>]) 
* Rename Columns in Pandas 
    df.columns = ['Column Name', 'Column Name', 'Column Name', 'Column Name']      
* Unique Values In A Column     
    print(df.<Column Name>.unique())
 * Append a column in Dataframe
    df[<Column Name>]=<Value to be appended>
 * Insert a column 
    DataFrameName.insert(loc, column, value, allow_duplicates = False)
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
- Adding Lables to Plot lines 
````
	df.plot(label="AGE")
````



- Convert column to Date time format

  ```
  df['Month'] = pd.to_datetime(df['Month'],infer_datetime_format=True)
  ```
