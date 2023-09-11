# nosql-challenge
UNC-CH-DA Module 12- NoSQL Challenge

### **INSTRUCTIONS**
* Clone the repository to your local machine
* cd into the "nosql-challenge' directory.
* The Jupyter Notebooks for the project are 'NoSQL_analysis_setup.ipynb' and 'NoSQL_analysis_solution.ipynb'

### **BACKGROUND**
The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. You've been contracted by the editors of a food magazine, Eat Safe, Love, to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.

### **REQUIREMENTS**

## **PART 1: Database and Jupyter Notebook Set Up (15 Points)**

To recive all points, your Jupyter Notebook setup file must have all of the following:

* Include the mongoimport command text you used to import establishments.json in a markdown cell at the beginning of your Jupyter notebook file (3 points)

* The mongoimport command text correctly drops any existing establishments collection before importing establishments.json into MongoDB (2 points)

* The database is named uk_food and the collection is named establishments (2 points)

* Correctly imports PyMongo and Pretty Print (2 points)

* An instance of the Mongo Client is created (1 point)

* Lists the databases you have in Mongo, which includes uk_food (1 point)

* Lists the collection(s) in the uk_food database, which includes establishments in the output (1 point)

* Uses find_one() and pprint to display one document in the establishments collection (2 points)

* The establishments collection is assigned to a variable (1 point)

## **PART 2: Update the Database (20 Points)**

To recive all points, your Jupyter Notebook setup file must have all of the following:

* The supplied data for the "Penang Flavours" restaurant is correctly inserted into the establishments collection (3 points)

* A query is performed to find the BusinessTypeID for "Restaurant/Cafe/Canteen" and returns only the BusinessTypeID and BusinessType fields (3 points)

* The "Penang Flavours" document is updated with the correct value for BusinessTypeID (3 points)

* A query is correctly performed to delete all the documents in the collection where "Dover Local Authority" is the value for LocalAuthorityName (3 points)

* A count_documents() check is performed before and after the removal of the Dover documents to ensure the documents were removed (4 points)

* An update_many() query is performed to convert the latitude and longitude fields from strings to decimal numbers and RatingValue to integers (4 points)

## **PART 3: exploratory Analysis (55 Points)**

To recive all points, your Jupyter Notebook setup file must have all of the following:

**Question 1: Which establishments have a hygiene score equal to 20? (8 points)**
* A query is correctly performed to find the establishments with a hygiene score of 20 (2 points)

* count_documents() is used to list the correct number of documents (answer: 41) (2 points)

* The first result is printed using pprint (2 points)

* The results are converted to a Pandas DataFrame and displays the first 10 rows (2 points)

**Question 2: Which establishments in London have a RatingValue greater than or equal to 4? (12 points)**
* A query is correctly performed to find the establishments in London with a RatingValue greater than or equal to 4 (4 points)

* The query uses the $regex operator to locate the London establishments (2 points)

* count_documents() is used to list the correct number of documents (answer: 34) (2 points)

* The first result is printed using pprint (2 points)

* The results are converted to a Pandas DataFrame and displays the first 10 rows (2 points)

**Question 3: What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"? (15 points)**
* A query is correctly performed to find the establishments within 0.01 degree of the "Penang Flavours" restaurant (4 points)

* The query also limits the results to establishments with a RatingValue of 5 (2 points)

* The query uses the sort() method in PyMongo to sort in ascending order on the hygiene score (2 points)

* The query uses the limit() method in PyMongo to limit the results to 5 (2 points)

* All five results are printed using pprint (3 points)

* The results are converted to a Pandas DataFrame and displayed (2 points)

**Question 4: How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas. (20 points)**
* An aggregation pipeline is built to include a match query, group, and sort (3 points)

* The match query matches documents with a hygiene score of 0 (2 points)

* The group step of the pipeline is grouped on LocalAuthorityName and counts the number of documents (4 points)

* The sort step of the pipeline sorts the count of the documents in descending order (2 points)

* The aggregation pipeline is correctly sent to the aggregate() method (2 points)

* The results from the aggregation query is cast as a list and then saved to a variable (2 points)

* The first ten results are printed using pprint (3 points)

* The results are converted to a Pandas DataFrame and displays the first 10 rows (2 points)

## **Deployment and Submission (6 points)**
**To receive all points, you must:**
* Submit a link to a GitHub repository that’s cloned to your local machine and contains your files (2 points)

* Use the command line to add your files to the repository (2 points)

* Include appropriate commit messages in your files (2 points)

## **Comments (4 points)**
**To receive all points, you must:**
* Be well commented with concise, relevant notes that other developers can understand (4 points)

### **RESOURCES**
* mongodb query reference: https://www.mongodb.com/docs/v6.0/reference/operator/query-comparison/ 