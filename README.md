# nosql-challenge
The UK Food Standards Agency evaluates various establishments across the United Kingdom and gives them a food hygiene rating.

## Database and Jupyter Notebook Set Up
In the NoSQL_setup.ipynb Jupyter Notebook, there is code to import the JSON data in the Resources folder into MongoDB using Command Prompt/Terminal. It can also be uploaded through MongoDB Compass. The database is called `uk_food` and the collection is called `establishments`.

The file checks that data was uploaded correctly and can be accessed through Jupyter Notebook. It adds a new restaurant, Penang Flavours, to the database with pymongo and updates the field 'BusinessType' with the code for 'Restaurant/Cafe/Canteen' that is categorized in this dataset. All documents related to the Dover Local Authority are removed from the database. The values for latitude and longitude in the database are updated to doubles instead of strings.

## Exploratory Analysis
In the NoSQL_analysis.ipynb Jupyter Notebook, pymongo queries and aggregation pipelines are used to answer the following questions:
<ol>
  <li>Which establishments have a hygiene score equal to 20? </li>
  <li>Which establishments in London have a RatingValue greater than or equal to 4?</li>
  <li>What are the top 5 establishments with a RatingValue of '5', sorted by lowest hygiene score, nearest to the new restaurant added, Penang Flavours?</li>
  <li>How many establishments in each Local Authority area have a hygiene score of 0? </li>
</ol>

## Data Source
<a href=https://www.food.gov.uk/>UK Food Standards Agency</a> (2022). UK food hygiene rating data API. https://ratings.food.gov.uk/open-data/en-GB. Contains public sector information licensed under the <a href=https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/>Open Government Licence v3.0</a>.
Accessed Sept 9, 2022 and Sept 12, 2022 with the establishment settings as follows: longitude=51.5072, latitude=-0.1276, maxdistancelimit=4567, pagesize=10000, sortoptionkey=distance, pagenumber=(1,2,3,4,5,6,7,8).
