###Description

The data was generated using Neha’s python scripted program for extracting scalable Wisconsin Benchmark data.  The program converted the three sets of data, the 1K and two 10K, into csv files. Furthermore, they were moved into the “script” folder under the PostgreSQL folder. 

The process of loading the csv files into the pgAdmin database required the following commands. 

1. Create the Wisconsin Benchmark Table with its 16 attributes
	CREATE TABLE TENKTUP1
 ( 
    unique1 integer NOT NULL,
    unique2 integer NOT NULL PRIMARY KEY,
    two integer NOT NULL,
    four integer NOT NULL,
    ten integer NOT NULL,
    twenty integer NOT NULL,
    hundred integer NOT NULL,
    thousand integer NOT NULL,
    twothous integer NOT NULL,
    fivethous integer NOT NULL,
    tenthous integer NOT NULL,
    odd100 integer NOT NULL,
    even100 integer NOT NULL,
    stringu1 char(52) NOT NULL,
    stringu2 char(52) NOT NULL,
    string4 char(52) NOT NULL
)

2. Write a SQL statement to load the csv files into the table
    COPY public. "tenktup1" FROM 'C:\Program Files\PostgreSQL\13\scripts\Tenktup1.csv' csv HEADER;

3. The table should be created and confirmed with the view data icon in the PostgreSQL. 

###Project Contributors:
   Yan Li & Minjin Enkhjargal

