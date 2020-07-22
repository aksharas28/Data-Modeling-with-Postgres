Purpose of the database:

Data Modeling for a startup called "Sparkify" is performed. The platform is an online music platform. "Sparkify" startup aims in collecting data on songs and user activity on the streaming platform. In this project, Data Modeling is done to empower the analytics team for getting tons of insights from the available data. Currently, they don't have an easy way to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

In order to enable Sparkify to analyze their data, a Relational Database Schema was created, which can be filled with an ETL pipeline.

How to run Python Scripts:

To create the database tables and run the ETL pipeline, you must run the following two files in the order that they are listed below

To create tables: python3 create_tables.py

To fill tables via ETL: python3 etl.py

Datasets:

The two main databases used in this project are "Song Dataset" and "Log Dataset". "Song Dataset" holds complete details and metadata about the song. "Log Dataset" holds the User activity log.

Purpose of Database:

Using a database makes it easier to analyze the data. The data can be searched and summarized quickly and easily by using SQL and star schema, joins and aggregations. By using a relational database, Sparkify can also perform ad hoc analysis of its database.

Database Schema:

The Database Schema used in this project is "Star Schema". "Star Schema" is used to model the dataset by dividing them into facts and dimensions in the structured manner. There are two types of tables used in the Schema which is "Fact Table" and "Dimension Table".

Fact Table:

In this project, songplays table is used as the Fact table. The songplays table contains the metadata of the complete information about each user activity. One fact table is connected to many dimensions tables.

Dimension Tables:

In this project, the dimension tables used are users,songs,artists and time. These tables will be having detailed information about a single row from facts table.

The database schema design and ETL pipeline:

In order to enable Sparkify to analyze their data, a Relational Database Schema was created, which can be filled with an ETL pipeline. Star scheme enables the company to view the user behaviour over several dimensions. The fact table is used to store all user song activities that contain the category "NextSong". Using this table, the company can relate and analyze the dimensions users, songs, artists and time. 
In order to fill the relational database, an ETL pipeline is used, which makes it possible to extract the necessary information from the log files of the user behaviour as well as the corresponding master data of the songs and convert it into the schema.

Fact Table: songplays
Dimension Tables: users, songs, artists and time.
ETL Pipleline:

The data from json log files are collected and ETL pipeline is created in this project and then inserts them into respective tables. In this project, complete pipeline is present int "etl.py" file. 

Files Explained
There are 7 files in this project.

data - This folder contains the log and song datasets.
etl.ipynb - This is a jupyter notebook which I used to create the skeleton for the pipeline. It is kind of a workbook.
test.ipynb - This jupyter notebook checks whether the written scripts for creating tables and inserting data are working fine or not.
create_tables.py - This program contains postgresql queries for creating the database and tables.
etl.py - This script contains the complete ETL pipeline for the project.
Readme.md - Documentation regarding the project.
sql_queries.py - This python script contains the create and insert contains for the database.

Running the project:

To run the project, go to terminal and run create_tables.py script using the command "python create_tables.py" in the terminal. Run etl.py script with the help of the command "python etl.py". This will run the etl pipeline and extract data from the log files and insert them into the facts and dimension tables.