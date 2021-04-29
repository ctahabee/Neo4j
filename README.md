# Neo4j
This repository includes files containing in-class projects I've done using graph databases on Neo4j.

In the .ipynb file included, the graph database was imported from the 'companies.csv' file. 
The 'companyName', 'employees', 'founded', and 'annualRevenue' columns in the csv file were each imported as properties under 
the 'Company' node label using the CREATE clause and converted to appropriate data types. The 'city', 'state' and 'country' columns
were each imported under their own corresponding node labels with the values mapped to their 'name' property using the MERGE clause.

#### 1. Node label:

Companies

#### Properties:

i. name (imported from 'companyName' column in csv file) (string)
ii. employees (imported from 'employees' column in csv file) (int)
iii. year (imported from 'founded' column in csv file) (int)
iv. revnue (imported from 'annualRevenue column in csv file) (float)

#### 2. Node label:

City

#### Properties:

name (imported from the city column in csv file) (string)

#### 3. Node label:

State

#### Properties:

name (imported from the state column in csv file) (string)

#### 4. Node label:

Country

#### Properties:
name (imported from the country column in csv file) (string)


3 relationships were generated using the CREATE clause, as well as the '-' and '->' operators to specify the direction of the relationship:
1. HEADQUARTERED_IN - the one-way relationship between companies and city (i.e. companies are headquartered in a city)
2. LOCATED_IN - the one-way relationship between city and state (i.e. cities are located in a state)
3. PART_OF - the one-way relationship between state and country (i.e. states are part of a country)

#### The resulting graph database has 27 nodes.

![alt text](https://github.com/ctahabee/Neo4j/blob/main/Tahabee_APAN5400_Graph_DB.png?raw=true)
