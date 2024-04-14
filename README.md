# US_Salary_Analysis_Dashboard
**Problem Statement**

The client seeks to determine the average salary by state and job type in the United States. This information will aid in making informed decisions about career planning or salary negotiations.

This task involves diagnostic analysis.

The steps are as follows:

- Load and explore the given dataset (EDA).
- Clean the data.
- Remove unnecessary attributes.
- Conduct clustering.
- Visualize the data.

In conclusion, the analysis aims to answer the following questions:

1. What are the average salaries for different job titles in the United States?
2. How have average salaries changed over time for different job titles?
3. Which industries in the United States offer the highest and lowest salaries?
4. What are the average salaries for different job titles in various states?
5. What factors influence average salaries?

**Project Report**
Purpose:
The client wants to find out the average salary by state and job type in the United States. This data can be used to make informed decisions about career planning or salary negotiations.

Approach:
A diagnostic analysis project to explore and visualize average salaries by state and job type in the United States.

Project Goals:
1.Analyze data provided in the data set (EDA)
2.Build dashboards that can help to understand the result of analysis better.

Project Outline:

Loading and Exploring Data
Cleaning Data
Dropping Unnecessary Attributes
Clustering
Visualization

Step 1:  Load, explore and clean the data
 
Python Code:
Python
import json

# Load the JSON data into a data frame
df = pd.read_json('glassdoor_jobs.json')

# Explore the data
print(df.head())

Step 2:Dropping Unnecessary Attributes and Clustering 
Python Code:
# Drop unnecessary attributes
df = df.drop(['Company Name', 'Company Location', 'Headquarters Size', 'Founded', 'Type of Ownership', 'Industry Sector'], axis=1)

# Cluster the data using k-means clustering
kmeans = KMeans(n_clusters=6)
kmeans.fit(df)

# Assign each job title to a cluster
df['cluster'] = kmeans.labels_

Step 3: Build a Visualization

Conclusion:
This project will provide users with a powerful tool to explore and understand average salaries by state and job type in the United States. The data can be used to make informed decisions about career planning, salary negotiations, and other financial matters.



