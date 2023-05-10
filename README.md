This repository focuses on optimizing the performance and structure of the Airbnb listings data using MongoDB, Docker, and Studio 3T. The current state of the data, which is all collected in a single document, has resulted in slow query performance and other issues. My goal is to address these issues by applying appropriate data model patterns, implementing indexing strategies, and fixing data collection errors.

Technologies used:


MongoDB: A powerful and flexible NoSQL database management system, which will be used to store and manage the AirBNB listings data.


Docker: A platform that simplifies the deployment and management of applications in containers, ensuring consistency and reducing overhead.


Studio 3T: A popular GUI for MongoDB, which will help us in visualizing, querying, and managing the data more efficiently.


Objectives tackled:


1) The most typical use case for the database is to show information relating to a property listing to a customer. This is done by a query to the database which returns one of the listing documents. Currently a lot of time is spent when a listing is retrieved from the database to show to a customer. Decide what information should be returned in a typical query and optimise the structure for this use case. For example, we typically only want a sample of reviews but not all reviews (although all reviews ), the customer does not need to know past transaction data, etc. Update the document schema for this typical use case. This may involve the creation of new collections and documents.


2) Review the data for any errors (such as transactions that don’t fit the listing) or inappropriate duplication and clean up as appropriate.


4) Once per month we like to reward hosts with recognition. Pick three superhosts who have at least two property listings that can accommodate more than four people?


4) One of employees is thinking of buying a property to rent out. Which bed type is most common in the listings that have waterfront and a dishwasher in New York?


5) We are thinking of identifying someone to hire to write review for us professionally. What is the name of the reviewer who left the longest review in New York?


6) We are thinking of trying to assess the security of different areas based on the security deposit required. What is the biggest and smallest difference between the price and deposit for security per number of visitors staying at the property?


7) We want to identify areas by whether they are typically used for short breaks, like weekend mini breaks, or whether they are more suitable for long trips. We will use this information to target advertising of different customers. It is not expected this information will change much over time so we won’t look to update it we just would like a current view. What is the average duration of stay (in nights) per type of property per city (you can use the maximum_nights to measure length of stays)? For each property type return the city with the highest and lowest average value.


8) We want to have a new webpage for hosts when setting up their account. It will list suggested typical amenities. This data will need to be available every time a host registers a property but is not expected to change very much. The starting point for the list will be all unique amenities currently listed in properties (across all documents). Optimise the database for this use case and show how the data should be queried.


9) We want to start tracking our reviewers better. We want to create a webpage that shows the top 20 reviewers and the count of the number of reviews of each of these reviewers. This webpage should be kept up to date. It should also have a link to return the number of reviews for a given reviewer ID or Name (show how to query for number of reviews by ID or query quickly).


10) For each property we store review scores across different metrics (accuracy, check-in, cleanliness etc). We are thinking we may soon add more metrics, although we don’t know what these will be. We want to be able to easily query the average score across all of these metrics, including any new metrics that might be added without changing the query. Adjust the data model so this can be done and show the query for an example property.


11) We wish to be able to have better access to information about transaction, we wish to develop a search engine that can calculate the average value of transactions in a given period of time quickly for a given property.


12) We wish to have a summary webpage that displays information about our top destinations. This webpage should display for each of the top 10 cities some basic information about our operations in the area (number of properties by type for example, average price by type) but you can choose the metrics. For each of the top 10 cities it should also provide some basic information about the top 3 properties in each city (price, number of review, whatever you think useful) to show an example of the properties available in the area. We would like to keep this webpage up to date as information changes.


Database updates:


Remeber to cosider how to prevent any data you have previously created from becoming stale.


13) Add a new property, this property should have a new host, and should be located in one of the top 10 cities. The host selects the top 10 most common amenities to be listed for the property.


14) Add a new review to this property, the review should be from one of our top 20 reviewers.


15) Add a new review metric called x_factor to the new document and give a score of 10. Show that the average across all metrics is correctly calculated for this listing, with the query you previously developed.


Key Challenges:

Query Performance: The current data model has led to slow query performance. We will explore hybridization of data models to improve query response times.

Lack of Patterns: The previous team did not apply any data model patterns, which is a significant factor in the suboptimal performance. We will investigate and apply suitable patterns to enhance the data model.

Missing Indexes: The current data model does not make use of indexes, which can greatly improve query performance. We will identify key fields for indexing and implement appropriate index structures.

Growing Review Data: With the rapid growth of AirBNB application usage, the number of reviews has increased substantially. Instead of overwriting reviews, we will store all of them to facilitate the business intelligence department's analysis over time.

Data Collection Errors: There are known issues with the data collection process, such as duplicate data entries and incorrect timestamps for transactions. We will develop strategies to address these problems and ensure data integrity.
