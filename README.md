# movies-etl
Using ETL, and database management to create a database about movies.

# Group Members:
- Isabelle DeMartin
- Chia Sun
- Patrice Woida
- Charlie Loveall

# Our data is from:
https://www.kaggle.com/unanimad/the-oscar-award
https://www.kaggle.com/stefanoleone992/imdb-extensive-dataset
https://www.kaggle.com/unanimad/golden-globe-awards

# Each person will have the following duties:
`Charlie Loveall-extracting, github repo manager
Patrice Woida- loading into sql
Chia Sun- data cleaning, extracting
Isabelle DeMartin- transforming data

The purpose of this database is to take a movie and be able to look at awards it has won along with other metrics like box office figures and reviews.

# The Data:
Our dataset contains information for the movies beginning from 1927, but for our purposes we decided to cut the data to only the most recent 50 years.

# Instructions:
1. Use MongoDB in order to store the database
2. Then use Jupyter Notebook and Pandas to extract and transform file. 

# Summary:

Initially, after cleaning the data, we tried to use the merge function to combine the Oscar, Golden Globe, and IMDB CSV's. We were trying to merge two together, and then add in the third file but were continuing to get errors even after further cleaning the data.  

We then trying to use the concatenate function but it was too difficult to sort in a way that concatenate would allow it to work. So we decided it would be simpler to merge the two documents. We tried dropping any data with N/A's, which resulted in dropping all of our data because each row had an N/A value somewhere. 

Ultimately, we decided to use groupby and filtering in order to make the format friendly to MongoDB.  We loaded golden globes and oscars csv's and did GroupBy title. We then had to filter this dataframe and add it to a dictionary so it could be loaded into MongoDB. 

# If we had more time...

If we had more time, we would have done the groupby Actors/Actresses as well. We would also add in more information based on the IMDB Database. 

We would have preferred to use the cleaned data titles for each column in order to distinguish between Golden Globes, Oscars, and IMDB. 