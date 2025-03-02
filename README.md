# nosql-challenge

# Eat Safe, Love

The NoSQL_setup.ipynb sets up and updates the database. The NoSQL_analysis.ipynb queries relevant information for analyses and converts results into Pandas DataFrame. The data provided in the establishments.json file was imported using Terminal with mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json.

# Set Up and Update Database

Insert the new halal restaurant opened in Greenwich to the Database.

establishments.insert_one(new_restaurant)
Update the new restauarant with the correct BusineesTypeID.

# Exploratory Analysis

Which establishments have a hygiene score equal to 20?

There are 41 establishments with a hygiene score of 20 from the uk_food dataset.

Which establishments in London have a RatingValue greater than or equal to 4?

There are 34 establishments in London that have a RatingValue greater than or equal to 4 from the uk_food dataset.

What are the top 5 establishments with a RatingValue rating value of '5', sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?

The top 5 establishments with a RatingValue of '5' sorted by lowest hygiene score nearest to "Penang Flavours" are: "Volunteer", "Plumstead Manor Nursery", "Atlantic Fish Bar", "Iceland", and "Howe and Co Fish and Chips - Van 17".

How many establishments in each Local Authority area have a hygiene score of 0?

There are 55 rows in the DataFrame. This is the preview of the first 10 rows:

_id	count
Thanet	1130
Greenwich	882
Maidstone	713
Newham	711
Swale	686
Chelmsford	680
Medway	672
Bexley	607
Southend-On-Sea	586
Tendring	542

# Instructions

The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. You've been contracted by the editors of a food magazine, Eat Safe, Love, to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.
Part 1: Database and Jupyter Notebook Set Up

Use NoSQL_setup_starter.ipynb for this section of the challenge.
Import the data provided in the establishments.json file from your Terminal. Name the database uk_food and the collection establishments. Copy the text you used to import your data from your Terminal to a markdown cell in your notebook.
Within your notebook, import the libraries you need: PyMongo and Pretty Print (pprint).
Create an instance of the Mongo Client.
Confirm that you created the database and loaded the data properly:
List the databases you have in MongoDB. Confirm that uk_food is listed.
List the collection(s) in the database to ensure that establishments is there.
Find and display one document in the establishments collection using find_one and display with pprint.
Assign the establishments collection to a variable to prepare the collection for use.
Part 2: Update the Database

