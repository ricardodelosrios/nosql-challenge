# nosql-challenge

## Introduction

The UK Food Standards Agency assesses various establishments across the United Kingdom and assigns them food hygiene ratings. They have been commissioned by the editorial team of the renowned food magazine, Eat Safe, Love, to analyze the ratings data. This analysis will assist the magazine's journalists and food critics in determining the focus areas for their future articles."

## Folders and files

 * It will find **2 Files** in this project:
  
    * [NoSQL_setup_starter.ipynb](https://github.com/ricardodelosrios/nosql-challenge/blob/main/NoSQL_setup_starter.ipynb). In this file, you will find the code to set up the project.
    * [NoSQL_analysis_starter.ipynb](https://github.com/ricardodelosrios/nosql-challenge/blob/main/NoSQL_analysis_starter.ipynb). You will find the code to analyze, which will help you find the places you want to visit and avoid.

* It is going to find a **folder** in this project:
   * The folder called `Resources` will find 1 json file. Listed below are the names of the files you will find:

      * [establishments.json](https://github.com/ricardodelosrios/nosql-challenge/tree/main/Resources)
    
## Import

The following command is used to import the JSON file into the MongoDB database.

```
 mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json

```
To understand it, below is the breakdown of the command:

* `mongoimport`:used to import data into MongoDB from files.
* `--type json`:This option specifies the type of input file to import. For this project, a JSON file will be imported.
* `-d uk_food`:This option specifies the destination database in MongoDB. In this project, the database to be created is "uk_food".
* `-c establishments`: This option specifies the target collection within the database. For this project, a collection called "establishments" will be created.
* `--drop`:This option will avoid that if the "establishments" collection already exists in the database, it is removed before importing or creating it. This ensures that the old data is replaced by the new data from the JSON file.
* `--jsonArray`: This option tells MongoImport that the input file contains JSON documents (rows) instead of a single JSON document (row).
* `establishments.json`: This is the name of the Json file to import.
