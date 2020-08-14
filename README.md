# ETL-grp03

Data Sources: 
https://www.kaggle.com/shivamb/netflix-shows
https://www.kaggle.com/stefanoleone992/imdb-extensive-dataset?select=IMDb+movies.csv

Question: What are the average ratings for movies on Netflix and IMDB?

Extract: Our data sources are from kaggle.com. 
Import the dependencies: Pandas, pymongo, and create_engine from sqlalchemy. 
Read in the 2 CSVs: Netflix and IMDB.
Create 2 dataframes using each of the CSVs.

Transform:
Filter the dataframes to remove any unnecessary columns. 
Check for any duplicate values using 'show id' and 'IMDB title id'.
Merge the 2 dataframes together using a left join on both 'title' and 'release year'.
Drop any movie titles with null average ratings.
Find the mean of the average votes of each movie/show.

Load: 
Load the data to the MongoDB server. We are using a non-relational database because we are working with one table.
Create a collection called 'movies'.