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
* Unique Values In A Column     
    print(df.<Column Name>.unique())
 * Append a column in Dataframe
    df[<Column Name>]=<Value to be appended>
