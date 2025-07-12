#COMPANY: CODTECH IT SOLUTIONS

NAME:Kumkum C. Bhanarkar

INTERN ID: CT08DN279

DOMAIN: BIG DATA

DURATION: 8 WEEKS

MENTOR: NEELA SANTOSH
In this task, I focused on performing data analysis on a large dataset using Apache Spark with PySpark, specifically targeting operations like filtering, grouping, and aggregations. The goal was to extract meaningful insights from the data using Spark’s distributed computing capabilities. These operations are essential when working with big data, as they help summarize, segment, and understand trends hidden in large volumes of information.

To begin, I set up the environment in Google Colab by installing the PySpark library using the command !pip install pyspark. After installation, I imported the necessary modules, especially functions like col, count, avg, sum, max, and min from pyspark.sql.functions, which are commonly used for aggregation and data transformations.

I then created a SparkSession named “SparkDataAnalysis”, which serves as the main entry point for interacting with Spark’s DataFrame API. After setting up the session, I loaded the dataset (originally in Excel format and converted to CSV) using the read.csv() method. I enabled the header=True and inferSchema=True options to allow PySpark to automatically recognize column headers and infer the appropriate data types.

After successfully loading the dataset, I previewed the top records using the show() method to get an idea of the structure and contents of the dataset. This step is always important to verify if the data was read correctly and to plan the transformations accordingly.

The first major operation was filtering. I applied a basic filter to select only the records where the "Votes" column had values greater than 100. This was done using the filter() method combined with the col() function. Filtering allows us to focus on high-quality or high-activity data, eliminating noise or irrelevant rows from the analysis.

Next, I performed grouping and aggregation. I started by grouping the dataset by the "City" column using the groupBy() method, followed by a basic count using the count() function to see how many entries existed per city. This gives a quick snapshot of how the data is distributed across different locations.

To go deeper, I applied multiple aggregations on the "Votes" column grouped by "City". I used avg(), sum(), and max() to calculate:

The average number of votes per city

The total votes each city received

The highest vote count observed in any single entry per city

This part of the task showed how PySpark can perform multiple complex aggregations efficiently, even on large-scale datasets. The results were displayed using the show() function and then saved to a CSV file using the write.csv() method. I used coalesce(1) to ensure the output was written to a single file rather than being split across multiple partitions, which is a common behavior in distributed environments.

Overall, this task taught me how to use PySpark for practical data analysis, including filtering large datasets, grouping records, and applying multiple aggregations efficiently. Unlike traditional Python tools, Spark's distributed nature makes it suitable for handling big data operations quickly and at scale. It was also a great exercise in understanding how to derive high-level summaries and insights from raw data in a clean and structured way.
#Output 
