# Data-Engineering-Prj.

# Tools used are:
  1. Pyspark 2. python 3. mysql 4. Shell Scripting

 # Introduction:
    
   This is a data engineering problem which is usually encountered in today's data world. It broadly      
   includes three challenges:
   
    1. Script that takes  URL as a shell parameter and combines all of the Storm Event Details
       into a single CSV. 

    2. Perform data analysis on the consolidated Storm data and Consumer-Complaint-database
       data gathered after 1st step

    3. Generating a bar chart of characters  frequency in a random text document stripping out punctuation
       and whitespace.

# Elaboration of Steps:

# Task 1(Extracting the FTP Links):
   URL: https://catalog.data.gov/dataset/consumer-complaint-database 

 This above URL contains FTP links to around more than 200 compressed csv files along with links to other irrelevant  
 content.
 So the challenge here was to extract only certain FTP links which are 230 in number and save the data files to their 
 respective locations.
 
 See below screenshot:
 
![FTP-Files-Sample](https://user-images.githubusercontent.com/23733029/30528057-183c0434-9be4-11e7-9737-7b55716be085.png)


Three types of file are being pulled:

Event Details File
Storm Data Location
Storm Data Fatality 
            and
Consumer-Complaint-Database 

   # Tools used:
      Python-Web-Scraping library(Beautiful soup) 
       Shell command
 
1. Python Script(BeautifulSoup) to web scrape the below shown URL to get the FTP links to 230 files
    and save those links to a textfile.
    
 --Link to Python Script:  https://github.com/abhishekparmanand/Data-Engineering-Prj./blob/master/Python-BS4-Script.txt



# Step 2:(Download the files ,uncompressing and merging and consolidation)

   1. Unix shell comes handy in downloading and merging similar schema files into one.
     
  --Link to Shell Script: https://github.com/abhishekparmanand/Data-Engineering-Prj./blob/master/ShellScript

# Task 2:
Generate the insights out of the storm data which could further used as precautionary measure before 
 building house by minimizing the damage caused through storm:
   
# Datasets 

# First Dataset(Storm Data):   
   Event Details File: Contains the details of the storm
   Storm Data Location: Contains the geographic location details
   Storm Data Fatality Files: Contains the fatality caused by storms 
 
 --Link to Metadata file: https://github.com/abhishekparmanand/Data-Engineering-Prj./blob/master/Storm-Data-Export-Format.docx


# Insights and Analysis(Storm Data)
  1. summarizing the property damage, by state, by year, into another csv or table.
--Link to Script: https://github.com/abhishekparmanand/Data-Engineering-Prj./blob/master/Storm-Pyspark-Script
 
# Tools used:

# Pyspark: Used to mine data perform aggregation, manipulations and data analysis
# Sqoop: To export the analysed data to mysql database
# Mysql  Database: To store the final result for future reporting and visualizations.
# Script that summarizes the property damage, by state, by year, into table and JSON




 # Second Dataset(consumer-complaint-database)

   #  Tools Used: Pyspark(mainly)
   
   # Data Set: Consumer-Complaint-Database (Metadata Link: https://cfpb.github.io/api/ccdb//fields.html )
     
  # Analysis performed are:
    1. Put all non-conformant postal codes into a file paired with their `complaint_ID
    2. Filters by complaints reported in or after 2016.
    3. Records grouped by their zip (for example: Number of Complaints By Zip, By Zip, etc).
    --Link to scripts: https://github.com/abhishekparmanand/Data-Engineering-Prj./blob/master/Complaints_Pyspark
  
# Task 3:
# Generating a bar chart of character's frequency in a random text document stripping out punctuation and whitespace

# Tools Used:
   Pyspark
   Python(Matplotlib)

--Link to Script: https://github.com/abhishekparmanand/Data-Engineering-Prj./blob/master/Character-Bar-Chart.txt


# Bar Chart:
![bar-chart](https://user-images.githubusercontent.com/23733029/30528491-5e308204-9be8-11e7-9828-8dccf6634c41.png)






   
