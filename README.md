# Project_1: Analyze MovieLens data
## Project Description
Import csv data about movies and their ratings into HDFS, then create tables from the imported files in Hive. Once imported, create queries to analyze and display data about the movies and their ratings. For e.g.; display first 5 entries from movies table, count number of unique movies, Which movie received the highest number of ratings, top 25 most rated movies etc.

## Technology Stack
* Hive
* HDFS
* Hadoop
* Git + Github

# Getting Started
Github clone URL: https://github.com/AmanSagar009/Revature-Project_1.git

* Install virtualbox vm
* Install hortonworks 2.6.5 vm 
* Open Linux Terminal
* ssh localhost
* maria_dev@sandbox-hdp.hortonworks.com -p 2222
* maria_dev@sandbox-hdp ~
* hdfs dfs -mkdir /user/maria_dev/Deep-Divers-P2
* maria_dev@sandbox-hdp Deep-Divers-P2
* hdfs dfs -put ./p2.py /user/maria_dev/Deep-Divers-P2

* Hadoop - version 2.7.3.2.6.5.0-292
* HDFS - version 2.7.3.2.6.5.0-292
* Hive - version 2.6.5.0-292
* Git -version 2.32.0.windows.1

## Features

List of features ready and TODOs for future development
using this project some query are solved using hiveQL ,following questions are listed below:

 01. first 5 entries from movies table
 02. number of unique movies
 03. summary of ratings data
 04. minimum rating given to a movie
 05. maximum rating given to a movie
 06. is any row null in tags
 07. number of unique tags 
 08. drop null rows from tags and create another table of the resulting rows
 09. filtering to get the list of drama movies
 10. total number of drama movies
 11. filtering to get the list of comedy movies
 12. total no. of comedy movies
 13. search movie id by tag search
 14. displays first 5 data from ratings table
 15. merging two tables movies and ratings into a new table without the "timestamp" column from the ratings table.
 16. display high rated movies (rating > 4)
 17. display low rated movies (rating < 4)
 18. total number of unique movie genres
 19. top 25 most rated movies
 20. slicing out columns to display only title and genres columns from movies table
 21. extract year from title of the movie
 22. count how many times each of genres occur
 23. Which movie received the highest number of ratings?



## Getting Started
   

To start this project user need to install sandbox-Hortonworks in virtual machine.After installing the VM start the VM then put the following command in Git bash then connect to VM using SSH command "ssh maria_dev@sandbox-hdp.hortonworks.com -p 2222" after this you need to put the password the default password for USER maria_dev is "maria_dev"

Performing the above action you are enter to VM CLI then do the following command which are listed below for the project.

* Create a folder in local VM using command "mkdir folder_name"
* In this folder clone the git repository from where we pull the dataset using command "git clone 'git repository link' "
* All dataet are in a zip file we have to unzip it using command "unzip file_name" (N.B: if you are unzip in the current file ) .
* After unzip all the file create a folder in hdfs using command which is little bit difference before we tried while creating folder is "hdfs dfs -mkdir folder_name" (By default this folder created in the path user/maria_dev/ ) and copy all file to the hdfs folder by ""hdfs dfs -put file-name /user/maria_dev/folder_name".
* To open HiveQL terminal we have have to give command "Hive".
* Before performing all the above action try to check whether your Ambari which is management platform for hadoop started all services or not.
* In hive terminal ,check database and if not create one and use the database using following command and after creating database create tables and load data from the folder in hdfs to the respected table and perform analysis using the query which are mention the txt file "Project_1.txt" 

** WAY TO UPLOAD FILES

* clone the git repository using git clone <link> in our local system
* load ""sudo yum install unzip"" - Used to install unzip to unzip the zip files.
* unzip files using "" unzip <file_name.csv.zip> "" - Used to unzip the zip files.
* Make dir in hdfs using hdfs dfs -mkdir </path to hdfs in which dir will be created>
* Move the unzip files (i.e .csv files) inside the dir.
* put files in hdfs "" hdfs dfs -put ./<filename.csv> /user/maria_dev/movie ""
* go to ambari --> hive view --> upload table( /user/maria_dev/<dir_name>/<file_name>)
* gitbash --> hive --> create database demo1; --> use demo1; 

### For creating database  
create database demo1;
(#"demo1" is the database name here)

### For work in the database
use demo1;

I had created the tables directly from the ambari hive view and load all the files in their respective tables.

## Usage

>Using this project any one can perform analysis with the movielens dataset


