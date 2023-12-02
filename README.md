# Home_Sales
Module 22 Challenge - SparkSQL <br>
Contributor: Katy Yelle

### Repository Structure
    -Main Folder
        -.gitignore
        -Home_Sales.ipynb
        -README.md
    
    -Sub Folders
        -images
            -query1.png
            -query2.png
            -query3.png
            -query4.png


## Overview
This file uses SparkSQL to run several queries to answer the following questions on home sales data: (1) What is the average price for a four-bedrooom house sold for each year?, (2)What is the average price of a home for each year it was built that has three bedrooms and three bathrooms?, (3) What is the average price of a home for each year it was built that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2000 square feet?, and (4) What is the view rating for homes costing more than or equal to $350,000? <br>
<br>
The final query was run three times in different settings calculating the runtime  to demonstrate optimizing Spark.  The query without any optimization took .598 seconds.  Performance was optimized by caching the table, improving the run time to .386 seconds. Performance was then further optimized by partitioning the data on the field of 'date_built', improving the run time to .302 seconds.  The improvements are relatively small due to the small size of the data being used for the query, we could expect more dramatic improvements in run time when working with signficantly larger data in Spark. 


## Query Results
What is the average price for a four-bedrooom house sold for each year? <br>
![Query 1 Results](/images/query1.png "Query 1 Results") <br>

What is the average price of a home for each year it was built that has three bedrooms and three bathrooms?<br>
![Query 2 Results](/images/query1.png "Query 2 Results") <br>

What is the average price of a home for each year it was built that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2000 square feet?<br>
![Query 3 Results](/images/query1.png "Query 3 Results") <br>

What is the view rating for homes costing more than or equal to $350,000?<br>
![Query 4 Results](/images/query1.png "Query 4 Results") <br>