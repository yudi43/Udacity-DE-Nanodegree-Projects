### Purpose of this database:
#### The default storage of data is in the form of Json files scattered in various folders, to query some set of data to analyse some statistics is very hard right now and for that purpose we need a nicely modeled database where all the tables are related to each other and holds relavent data.

### Database schema design and ETL pipeline.
#### I have seperated the fact table and dimension tables to form a start schema. Here all the facts (songplays) are stored in one place and all the relavent data regarding the facts (songplays) is stored in the dimension tables. The fact table contains various foreign keys which are the primary keys for the other dimension tables so we know that they are really related. We can easity query any data using different joins on these tables.
#### And for the ETL pipeline, we have two files called create_tables.py and etl.py respectively. The job of create_tables.py is just to go and check if the database exists and if not then create one. And then add the required tables to the db. The second file does nothing but read data from the respective json files and populates the tables accordingly.

