# garimas_unmessenger_datacleaning
Using different data cleaning methods and technologies to understand the data better and make the data set more suitable for analysis, reporting, and decision-making. I used the .isnull().sum() method to find the number of null values in the column. 

For the empty value in the 'Name' column, I tried to derive the name from the 'Email' column. By retrieving the first and last names from the Email column and storing them in the 'Name' column. Then for the rows where the 'Name' and 'Email' column was empty, I removed them from the dataset.

For the empty values in the 'Age' column, I filled it with the mean value of the entire 'Age' column. But I would have preferred to fill the empty 'Age' value with the median of the column, as for continuous values, the median gets less affected by the outliers than the mean value.

For the 'Phone' column, I standardize the column format into (91-xxxxxxxx). So I used the .split('-') method on the 'Phone' column to get the code and number parts of the phone number. Then made sure that the number part only had eight digits. Then the code and number were separated by '-.'

For the rows with empty 'Email' values and no 'Name' value, I removed them from the dataset as we couldn't get the person's name out of it. Whereas for the rows with no 'Email' value but had 'Name' value, fill it with support@dataisgood.com.

For the 'Department' column, make the data properly with the valuable functions and rename the wrong-spelled words in the department column. First, I standardized the text format of the column by removing extra space and keeping all in lower. Here the 'sles' is an obvious spelling error so we change it to 'sales'. 'operaryion' is an obvious spelling error so we change it to 'operations', 'it department' and 'it devlopement' can be referred to as 'IT'. Now we have seven unique values for the 'Department 'column.

For the 'Address' column, replace the null values with 'Address not Available.'

In the end, I made a few extra changes where I changed the type of the 'Salary' column to float the 'Age' column to int, for 'Gender 'and 'Department' datatype to category. We can see that column Id has only unique values, which will not help us in prediction, so I removed this column.
