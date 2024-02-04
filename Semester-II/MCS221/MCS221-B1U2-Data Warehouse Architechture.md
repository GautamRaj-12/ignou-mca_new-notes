# Data Warehouse Architecture 

## Data Warehouse Architecture and its types
- Data warehouse architecture is a data storage framework’s design of an 
organization. It takes information from raw data sets and stores it in a 
structured and easily digestible format
- Data warehouse architecture defines the arrangement of the data in different 
databases. As the data must be organized and cleansed to be valuable, a 
modern data warehouse structure identifies the most effective technique of 
extracting information from raw data.

### Types of Data Warehouse Architechture

1. Single-tier data warehouse architecture
2. Two-tier data warehouse architecture
3. Three-tier data warehouse architecture

### Single-tier data warehouse architecture
- **Main Goal:** To remove redundacy by minimizing the amount of data stored.
- **Disadvantage:**  It doesn’t have a component that separates analytical 
and transactional processing.
- Not a frequently practiced approach

# ADD IMAGE HERE

### Two-tier data warehouse architecture
- Includes a ***staging area*** for all data sources
- To ensure all data loaded into the warehouse is cleansed and in the appropriate format.

# ADD IMAGE HERE

### Three-tier data warhouse Architecture
- **Bottom-tier:** It is the DB of the warehouse, where the cleansed and transformed data is loaded.
- **Middle-tier:** It is the application layer giving an abstracted view of 
the database.  It arranges the data to make it more suitable for analysis.
- **Top-tier:** It is where the user accesses and interacts with the data. It 
represents the front-end client layer. 

# ADD IMAGE HERE
# ADD IMAGE HERE

### Cloud based data warehouse architecture
- This data warehouse architecture means that the actual data warehouses are accessed through the cloud.
- There are several cloud based data warehouses options, each of which has different architectures
- Cloud-based platforms make it possible to create, share, and store massive data sets with ease, paving the way for more efficient and effective data access and analysis.
- Notable cloud data warehouses in the market include Amazon Redshift, Google BigQuery, Snowflake, and Microsoft Azure SQL Data Warehouse.

### Difference between cloud based vs traditional approach
- **Up-front costs:** Cloud cheaper as components expense not required.
- **Ongoing costs:** Cloud offers, pay as you go model.
- **Speed:** Cloud-based is speedier.
- **Flexibility:** Cloud data warehouses are designed to account for the 
variety of formats and structures found in big data. 
- **Scale:** Cloud more scalable


