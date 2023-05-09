AirBNB Data Optimization Repository

Introduction
This repository focuses on optimizing the performance and structure of the AirBNB listings data using MongoDB, Docker, and Studio 3T. The current state of the data, which is all collected in a single document, has resulted in slow query performance and other issues. My goal is to address these issues by applying appropriate data model patterns, implementing indexing strategies, and fixing data collection errors.

Technologies
MongoDB: A powerful and flexible NoSQL database management system, which will be used to store and manage the AirBNB listings data.
Docker: A platform that simplifies the deployment and management of applications in containers, ensuring consistency and reducing overhead.
Studio 3T: A popular GUI for MongoDB, which will help us in visualizing, querying, and managing the data more efficiently.
Key Challenges
Query Performance: The current data model has led to slow query performance. We will explore hybridization of data models to improve query response times.

Lack of Patterns: The previous team did not apply any data model patterns, which is a significant factor in the suboptimal performance. We will investigate and apply suitable patterns to enhance the data model.

Missing Indexes: The current data model does not make use of indexes, which can greatly improve query performance. We will identify key fields for indexing and implement appropriate index structures.

Growing Review Data: With the rapid growth of AirBNB application usage, the number of reviews has increased substantially. Instead of overwriting reviews, we will store all of them to facilitate the business intelligence department's analysis over time.

Data Collection Errors: There are known issues with the data collection process, such as duplicate data entries and incorrect timestamps for transactions. We will develop strategies to address these problems and ensure data integrity.
