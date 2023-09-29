# Sales-Analysis-Project

Created this Data Analytics Project using Python, and also used some advanced Data Analytics concepts to analyze better. Libraries used in this project are: Pandas, Matplotlib, OS, Itertools, Collections.

# The Question used to solve this dataset are:
1. What was the best month for sales? How much was earned that month?
2. Which City had the highest number of sales?
3. At what time should we display advertisements to maximize the sales of our products?
4. What products are sold together most often?
5. What product sold the most? And Why was it sold?

# To perform the analysis I've used Jupyter Notebook.
First all the files are present in the Sales_Data folder, to use those files I converted them into a single file using the pre-built functions in pandas such as: "pd.DataFrame" to create a dataframe, "pd.concat" to merge all files into one file, and ".to_csv" function to convert that single file into a '.CSV' format file.
After completing that step I used a dataframe called "all_data" to store all the values of the CSV file into that for further calculations.

## Data Cleaning
The dataset I used was too messy to work with, so I tried my best to clean the data. First I deleted all the NaN values present inside the data then I cleaned the data to remove 'Or' values which were present inside the data.

## Converting columns to their respective datatypes.
In this dataset all the colummns had 'Object' type datatype: I used 'pd.to_numeric' function for columns with numeric data and I used 'pd.to_datetime' function for converting the column which had datetime data.

## Adding columns
I created columns for the data analysis on based on the questions I'll be solving, Using '.astype('int32')' function created 'Month' Column. For 'Sales' column I multiplied the 'Quantity Ordered' column to 'Price Each' column. Adding 'City' column was the hardest because to extract the city from the data I had to use '.apply' function with 'def' and 'lambda' function respectivelyy to extract the values of the city from 'Purchase Address' column. After that I created few more columns such as 'Hour', 'Minute', 'Grouped' respectively. After completing the cleaning and creating columns then I worked on to solve the question on this data.

# Solving the questions:

### Question 1. What was the best month for sales? How much was earned that month?
  To sovle the first question I used '.groupby', '.sum()', '.loc[:,[columns to show]]' respectively to calculate the sales earned per month. Using bar plot to create a chart to represnt the findings.
  
### Question 2. Which City had the highest number of sales?
  To solve this question I used the same functions as the first question, and also used 'for' loop to filter the data.

### Question 3. At what time should we display advertisements to maximize the sales of our products?
  To solve this question I used 'for' loop and 'line' chart to represent the findings.
  
### Question 4. What products are sold together most often?
  To solve this question I used 'combinations' and 'Counter' function to count the values which was ordered by the customer togeter.
  
### Question 5. What product sold the most? And Why was it sold?
  To solve this question I used 'for' loop and 'box' plot with 'line' chart to represent the findings. And I also used the help of stack-overflow to create the second chart which was quite hard to create.
