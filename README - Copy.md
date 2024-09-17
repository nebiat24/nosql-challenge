# module12-Challenge -NoSQL-Databases
Data Analytics Boot Camp - Module 12 NoSQL Databases

NoSqL Challenge

## Results
The NoSQL subfolder contains the following files:

1. NoSQL_setup.ipynb
2. NoSQL_analysis.ipynb

## Implementation notes

Part 1: Database and Jupyter Notebook Set Up

Used the mongoimport utility to import the data provided in establishments.json

The command-line text used to perform the import is included at the top of NoSQL_setup.ipynb

Part 2: Update the Database

Added the restaurant "Penang Flavours" to the database, by inserting a new document using using the supplied details.
Queried the BusinessTypeID corresponding to BusinessType "Restaurant/Cafe/Canteen", and updated the new restaurant 
record with that ID value.

Confirmed the new Restaurant entry was added to the database, and its BusinessTypeID value was updated accordingly, by utilising the ObjectId saved from the insert step.

Removed documents with 'LocalAuthorityName' of Dover.

Converted Latitude/Longitude values and Rating values to appropriate numeric data type.

Part 3: Exploratory Analysis

Queried for various field values using PyMongo comparison operators (documentation reference below).

Pattern matching in strings via $regex evaluation operator (article and documentation references below), to find the full name of the London local authority (City of London Corporation).

PyMongo standard search implementation pattern using 'find':

collection.find(query).sort(sort).limit(limit)
PyMongo aggregation pipeline implementation pattern:

pipeline = [match_query, group_query, sort_query]
collection.aggregate(pipeline)


## Resources used for building SQL project include:

Multiple sources such as: I referenced official Bootcamp course material and documentation; instructor teaching (classes & shared resources), aid from fellow students, Google Search, StackOverflow, W3C Schools, content as well as support and guidance from the Xpert Learning Assistant and ChatGPT. In particular I spent the primary amount of my time reviewing the official MongoDB documentation located on its site here: https://www.mongodb.com/docs/drivers/pymongo/ especially around the areas of aggregation documentation as required by this exercise.

