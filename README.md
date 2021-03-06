# Data 612 week_1 assignment

1.	Open GitHub account and give it’s URL:

[Hari's GitHub repository](https://github.com/harikosaraju9)

2. Hari's repository link:

[Repository link](https://github.com/harikosaraju9/Data_612_assignments)

# Data_612 week_2 assignment

1. Folder ‘week_2_HW_Hari Kosaraju’ contains dataset with new columns 'date_dt' & ‘months’ added

2. COLAB notebook link:

[Hari's COLAB notebook link](https://colab.research.google.com/drive/1RYu_6Ecaxa4bcLCo-kVMaTbuQgRRoVmV?usp=sharing) 

# Data 612 Week_3 homework

1. Selected two datasets. The datasets are under week_3 data folder.

   df = State_Drug_Utilization_Data_2010_Hari.csv - with 5% of original data
   df_E_Col = State_Drug.csv - dataset created as part of homework week_2. has two extra columns 'date_dt' and 'months'
   
2. Split dataframe df into three dataframes df1, df2, and df3 by specifying different random states.

3. Concatenated df1, df2, and df3 into row_concat dataframe.

4. Selected 21% of  data from State_Drug.csv to equal row_contact dataframe. Now both dataframes have same number of rows.

5. Merged both dataframes.

6. Two extra columns in State_Drug.csv added to dataframe. 

7. New dataframe has missing values in row data of added columns.

8. Used fillna, interpolate to fill missing values.

[Week_3 'COLAB' link](https://colab.research.google.com/drive/1LY5DOZD0z_DEkekfYWMuDsrPndBueWvH?usp=sharing)

# Data 612 Week_4 homework

Action Items:
  • Convert data

1. Work on your selected data set and covert a column of non-categorical type into a categorical type.
2. Convert another column into a string type.
3. Post your work on GitHub
4. Add a README file

[hari's week_4 HW 'COLAB' link](https://colab.research.google.com/drive/1TCLz-PHllgawWuL4bZ5V7dERQyrt0pLP?usp=sharing) 

# Data_612 Week_5 homework

Action Items:
• Working with strings.

    Clean a column on your data set using regular expression methods.

    Store the cleaned column into another column of your data set and call it “your_col_name_cleaned”.

*Another data set will be provided if your data set is not appropriate to apply regular expression methods.

1) Used 'State_Drug_Utilization_Data_2010_Hari.csv' as input file. 
2) Cleaned 'Product name' column and added it as 'Cleaned_col' to output dataset. Cleaned column using regex commands.
   a) Product names were starting with numerical values. Cleaned data, so that product name starts with alphabet.
3) Output dataset is 'State_Drug_Utilization_Data_2010_week_5.csv'. This has cleaned column attached to it.

• Use of .apply()

    Create a function that returns the mean, sum, mode, median, and range (separately)
    Run the function into your chosen data set using the .apply() method.
    Post your work on GitHub
    
    1) Input file is cleaned of str type columns. The file name is 'Week_5_data.csv'.
    2) apply() method is applied on dataframe for aggregate functions.
    
[Week_5 COLAB link](https://colab.research.google.com/drive/1YoiEC-yp7mQSnPy62RQqaZfhcHJZMGoq?usp=sharing)


# Data_612 Week_6 homework

The function 'get_data_table' takes 4 parameters, df, date_col, group_col, type_x.

      The 'df' represents the dataframe.
      The 'date_col' represents the date column.
      The group_col represents the column to groupby and
      The 'type_x' represents the column with a specific value/category == 'type_x'.


def get_data_table(df, date_col, group_col, type_x):
    df_gross = (df.loc[(df.type == type_x) &
                                      df.category.isin(['category_x', 'category_xy', 'category_xyz'])
                                     ]
                         .groupby([group_col, date_col]).sum()
                         .unstack(date_col)['amount'].fillna(0)
                         .resample('M', axis=1).sum()
                        )

    df_recovered = (df.loc[(df.type == type_x) &
                                  df.category.isin(['category_01', 'category_05', 'category_07'])
                                 ]
                    .groupby([group_col, date_col]).sum()
                    .unstack(date_col)['amount'].fillna(0)
                    .resample('M', axis=1).sum()
                    )

    return df_gross.add(df_recovered * -1, fill_value=0)
    
  [Week_6_COLAB_LINK](https://colab.research.google.com/drive/13KaMLAdtAlDoSGR7ntYSLsrN7aUImrx7?usp=sharing)
  
  
  # Data_612 Week_7 homework - Vizualizations
  
  Create three different charts using Seaborn package.

    1) Create three different meaningful charts using Seaborn package on your selected data set.
    2) Explain when it is best to use
    3) Post your work in GitHub
    4) Add a README file
    
   [Week_7_HW_COLAB_Link](https://colab.research.google.com/drive/1GyFDeCH3ImN1RVu5NwC7iG2WiF-nY4Y4?usp=sharing)
   
   [Week_7_HW_COLAB_Link_2](https://colab.research.google.com/drive/1MQMWLqIpqz6Gx7TXSr5q6y730ac7dCsQ?usp=sharing)
   
  
   # Data_612 Week_8 homework - Final project preprations
   
   1) Open an account on Drivendata.org
   2) Sign up for competition: Pump it up data mining for Water table
   
   [Week_8_HW_COLAB_LINK](https://colab.research.google.com/drive/1PkDE8UpJsiJ9vQebsjlbIsJ7yIpnBT7l?usp=sharing)
   
   # Data_612 Final project - work
    
   Submitted internally
    
   
  
  
