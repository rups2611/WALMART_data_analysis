# WALMART_data_analysis
1. Set Up Kaggle API:
API Setup: Obtain your Kaggle API token from Kaggle by navigating to your profile settings and downloading the JSON file.
Configure Kaggle:
Place the downloaded kaggle.json file in your local .kaggle folder.
Use the command kaggle datasets download to pull datasets directly into your project.

2. Install Required Libraries and Load Data:
Loading Data: Read the data into a Pandas DataFrame for initial analysis and transformations.

3. Explore the Data:
Goal: Conduct an initial data exploration to understand data distribution, check column names, types, and identify potential issues.
Analysis: Use functions like .info(), .describe(), and .head() to get a quick overview of the data structure and statistics.

4. Data Cleaning:
Remove Duplicates: Identify and remove duplicate entries to avoid skewed results.
Handle Missing Values: Drop rows or columns with missing values if they are insignificant; fill values where essential.
Fix Data Types: Ensure all columns have consistent data types (e.g., dates as datetime, prices as float).
Currency Formatting: Use .replace() to handle and format currency values for analysis.

5. Create New Column:
Calculate the Total Amount for each transaction by multiplying unit_price by quantity and adding this as a new column.

6. Connect to PostgreSQL and Load Data:
Now, we'll connect to a PostgreSQL database and insert the cleaned and transformed data.
1. Connect to PostgreSQL: Use psycopg2 to connect to your database.
2. Insert Data into PostgreSQL: Loop through the DataFrame and insert each record into the movies table.
