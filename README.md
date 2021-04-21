SPARKIFY PROJECT:

Sprakify the music streaming app wants to analyze their user data with a focus on songs that the user is listening to.
To extract this information they need the information to be retrieved from log JSON files at user end and song JSON files to combine and provide appropriate information.


To achieve the goal a Star schema is implemented with the songplay table as fact table and 4 dimension tables as users, songs, artists, and time.

The project consists of the following files:

sql_queries.py: consist of all the queries that need to be executed to create table and schema and drop tables if already exist. NO NEED to run this file as this will be exported to or  imported by the Create_tables.py file



create_tables.py :
- Creates database connection 
- imports queries for dropping tables , creation of tables from sql_queries.
-  consist of 4 functions: 
    - create_database : creates databse 
    - drop_tables: drop tables if already exists
    - creat_tables: creates all the tables.
    - main function:  calls the other three funcions 
    
etl. ipynb:Break down of code into easy steps for undeerstaning.

etl.py: 
 - Also consists of 4 functions.
 - Import query for inserting data in tables from sql_queries.
 - Extract the json file iterativel to continously update tha tables to create data base.
     - process_song_file : extracts information from sing and artists JSON files and laod data into 
     - process_log_file : on basis of songid and artist id extract information from log JSON files transform the data and  laod timetamp and other information in          songplay table
     - process_data:Acess all the files from folder and iteratively calls them to prcoess.
     
test.ipynb : Juptier notebook to validate databas is bieng updated and enteries are there.

     
     
 Flow of execution: 
  - Execute create_tables.py file first for data base creation and tables . to excute run python<space>create_tables.py
  - Execute etl.py to excute run python<space>etl.py
     
    data: folder with song an duser json files from where data comes
 



