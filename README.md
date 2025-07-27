# NetflixDataProject

This project follows the below steps,
1. First pulls data from github and loads it to azure data lake using azure data factory.
2. Stores the data under raw container in ADLS
3. Using the newly created metastore, I have attached the databricks access connector which has access to my ADLS, have imported the data to databricks
4. In dbx, I have used autoloader to read the data from adls(have created external locations for respective containers in ADLS) and directly loaded back to bronze layer in ADLS from raw
5. Then again read from bronze and did some transformations and loaded to silver layer in ADLS
6. In gold layer, used DLT to read data from silver and stored the tables in gold layer


Skills and Technologies used: Pyspark,Databricks,ADF,ADLS



Concepts: Activities in ADF, Linked Services,Datasets in ADF,Transformations,DLT,Unity catalog,metastore creation.
