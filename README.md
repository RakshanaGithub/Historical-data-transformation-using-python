# Historical-data-transformation-using-python
Objective: Transform current employee data from a columnar format into a historical, row-based versioning format suitable for database storage using Python.

Approach to the assignment:

1. Importing the neccesary data into Python using Pandas function read_csv()
2. Performing Data Transformation: Transforming columnar data related to compensation, engagement, and review separately into a row-based format by using melt from pandas.
3. Droping Redundant rows: Dropping the rows that contains null value in all 3 columns Compensation, Performance Rating, Engagement Score to get rid of redundant columns using dropna.
4. Optimizing Data Types: Checking the datatypes and converting the dates in apropriate format using pandas function to_datetime.
5. Combining data in 3 different columns: Combining 3 columns Pay, Feedback1, Feedback2 into one column Type by defining a function concatenate_columns
6. Deriving effective date: Employing a function that utilizes an if-else statement to determine the effective date
7. Calculating End date: Switching the employee code from its role as the index using reset_index .
   Determining the date prior to the effective date on the next row to calculate the previous date
   Utilizing this particular date to establish the end date involves crafting a function that assesses the employee data to decide whether to utilize the exit date or the previous date.
8. Updating Employee Information: Inherit values from the most recent past record for the same employee using forward filling and altering NAN End dates
9. Adding new columns with data for last compensation and last pay raise:
    Determining the last pay raise and compensation values involves iterating through the data using a for loop.
    Within for loop, we check if the previous compensation and employee code match the current values. If they differ, we fill the columns with the previous values using an if statement and forward filling with the required data.
10. Adding other neccesary columns and reordering the columns using reindex
