# Amazon Vine Analysis Overview

The purpose of this project is to analyze Amazon reveiws written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive the reviews for thier products. Companies like SellBy pay a small fee to Amazon and provide products to Amaxon Vine members, who are then required to publsih a review. In this project the reviews of luggages on Amazon is analyzed. PySpark is used to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. PySpark is used again in a google colab notebook to determine if there is any bias toward favorable reviews from Vine members. 


## Resources
* [Luggage Reviews](https://github.com/Kwas45/Amazon_Vine_Analysis/tree/main/Resources)

## Amazon Vine Analysis Results
In this project, the main dataframe was filtered equal to or greater than 20 to pick reviews likely to be helpful and to avoid having divison by zero errors.

![image](https://user-images.githubusercontent.com/102786356/182001914-0c8ac2a4-a9d5-4820-86e0-0328296aeed0.png)


The filtered dataframe was then filtered again via the division of helpful_votes by total_votes

![image](https://user-images.githubusercontent.com/102786356/182001987-81aae842-355a-444b-9a50-1219522e14e0.png)


1. Total Number of Vine and Non-Vine reviews
Vine Reviews

![image](https://user-images.githubusercontent.com/102786356/182002012-25a75ceb-fe59-42f3-b688-64f70d307b6f.png)

Non_Vine Reviews

![image](https://user-images.githubusercontent.com/102786356/182002039-09a58a7a-ee42-42b3-bab4-f241648c5018.png)

From the tables above, the total number Reviews are **6,711**, of which **21** (0.3%) are Vine reviews and **6,690** (99.7%) are Non-Vine reviews per filtered data. 

2. Number of 5-star Vine and Non-Vine reviews

![image](https://user-images.githubusercontent.com/102786356/182002399-cec9d3ff-ac41-46c2-baac-bb272267b2e0.png)
![image](https://user-images.githubusercontent.com/102786356/182002414-6e3eb736-6f8f-4fef-b512-8da18c408a94.png)

The above chart highliths there were **472** 5-star Vine reviews and **216,023** 5-star Non-Vine reviews.

3. Percentage of 5-star Vine and Non-Vine reviews

![image](https://user-images.githubusercontent.com/102786356/182002399-cec9d3ff-ac41-46c2-baac-bb272267b2e0.png)




