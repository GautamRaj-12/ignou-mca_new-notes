# Fundamentals of Data warehouse

## Data Warehouse
Centralized repo, storing; consolidating; managing large volumes of data from various sources, designed to support Business Intelligence(BI), efficient analysis and decision making.

## Evolution of Data Warehouse
- RDBMS (Early 1980s)
  - Improved access to valuabe info.
  - Transactional databases not always optimized for reporting or analytical needs.
- Genesis of Data Warehousing (1980s)
  - 'Business Data warehouse' by IBM
- **Bill Inmon's Contribution**
  - *Approach*
    - Centralized repo modeled to 3NF
    - Top-Down
  - *Definition*
    - A warehouse is *subject-oriented*, *integrated*, *time-variant* and *non-volatile* data collection for management decision making.
- **Ralph Kimball's contributions**
  - *Approach*
    - Star scema modeling
    - easy to understand for end users
  - *Definiton*'
    - A warehouse is the conglomerate of all data marts within the enterprise, with information stored in the dimensional model.

## Need for data warehouse
- **Enhancing the turnaround time for analysis and reporting** (data from single source)
- **Imrpoved BI** (decision based on reliable facts)
- **Benefit of historical data** (time-period analysis, trend analysis)
- **Standardization of data** (data from heterozenous sources - single format)
- **Immense ROI (Return on Invenstment)** (Additional revenues/reduced expenses)

## Benefits of Data Warehouse
- Faster and accurate data analysis
- Increase Revenue and Returns
- Better Efficiency
- Access to Historical Insights
- Improved Data Security
- Scalability
- Works on premises and on cloud

## Data Warehousing and design approaches
1. **Top Down Approach (Bill Inmon)**

![Top Down Approach](https://github.com/GautamRaj-12/ignou-mca_new-notes/assets/64408989/0c3c68d6-6936-48e1-85da-ec14e7597d2e)

2. **Bottom-up Approach (Ralph Kimball)**

![Bottom Up Approach](https://github.com/GautamRaj-12/ignou-mca_new-notes/assets/64408989/082b6b3d-b348-4b07-ba98-60e3427d4d36)

## Characterstics of a data warehouse
- **Subject Oriented:**
  - Provides info about a specific them.
  - Focusses on data demonstration and analysis to make different decisions.
  
  ![subject oriented](https://github.com/GautamRaj-12/ignou-mca_new-notes/assets/64408989/5e51b0d7-64cb-4154-9621-840ace5a21bf)

- **Integrated**
  - A common system to measure all similar data from multiple systems.
  - consistent, readable and coded.
  
  ![Integrated](https://github.com/GautamRaj-12/ignou-mca_new-notes/assets/64408989/b69d2821-9bcf-404d-ad21-5057be687124)

- **Time-variant**
  - Data held in various intervals such as weekly, monthly and yearly
  - history
  - data can't be changed, modified or updated once stored.

  ![time variant](https://github.com/GautamRaj-12/ignou-mca_new-notes/assets/64408989/42263f09-6968-4fea-abf7-18b5fe6ff306)

- **Non-Volatile**
  - Data in DW : Permanent
  - Wehreas in operational DB, we can Select/Insert/Delete/Update

  ![OLTP](https://github.com/GautamRaj-12/ignou-mca_new-notes/assets/64408989/730e3de2-34d8-4dc3-ae04-8fcbef698faf)

  ![Non Valatile](https://github.com/GautamRaj-12/ignou-mca_new-notes/assets/64408989/162884e4-4eb5-4c61-abc7-7d91bf6ddbac)

## How DW works?
- **Components of a DW**
  ![Components of a DW](https://github.com/GautamRaj-12/ignou-mca_new-notes/assets/64408989/9ce0d39e-3004-4fd5-9d66-5062e1eb78b6)

- **Load Manager**
  - Collection of data from various sources
  - Convert data into usable form for the users
  - import/export data from operational systems
  - includes programs for poolig out the data, validation, accuracy, extraction, cleansing etc.
- **Warehouse Manager**
  - Large, physical db that holds vast amount of info.
  - Data is organized such that easy to find and use
- **Query Manager**
  - Provides end-users with access to the stored data warehouse info through various tools.
- **End User Access tools**
  - Reporting Data
  - Query tools
  - Data Dippers
  - Tools for EIS
  - Tools for OLAP

## OLTP and OLAP
- **OLTP**
  - Online Transaction Processing
  - captures and maintains transactions data in a database.
  - Emphasis on fast processing, because OLTP DBs are read, written and updated frequently.
- **OLAP**
  - Online Analytical Processing
  - Applies complex queries to large amounts of historical data, aggregated from OLTP databases.
  - Emphasis on response time to these complex queries

| Characteristic          | OLTP                                        | OLAP                                       |
|-------------------------|---------------------------------------------|--------------------------------------------|
|Characteristics          | Handles a large number of small transactions|Handles large volumes of data with complex queries|
| Query types             | Simple standardized queries                 | Complex queries                            |
| Operations              | Based on INSERT, UPDATE, DELETE commands    | Based on SELECT commands for reporting    |
| Response time           | Milliseconds                                | Seconds, minutes, or hours depending on data|
| Design                  | Industry-specific (e.g., retail, banking)  | Subject-specific (e.g., sales, inventory)  |
| Source                  | Transactions                               | Aggregated data from transactions         |
| Purpose                 | Control and run essential business operations in real time | Plan, solve problems, support decisions, discover hidden insights |
| Data updates            | Short, fast updates initiated by user      | Data periodically refreshed with scheduled batch jobs |
| Space requirements      | Generally small if historical data is archived | Generally large due to aggregating large datasets |
| Backup and recovery     | Regular backups for business continuity and legal/governance requirements | Lost data can be reloaded from OLTP database as needed |
| Productivity            | Increases productivity of end users        | Increases productivity of business managers, data analysts, and executives |
| Data view               | Lists day-to-day business transactions     | Multi-dimensional view of enterprise data   |
| User examples           | Customer-facing personnel, clerks, online shoppers | Knowledge workers such as data analysts, business analysts, and executives |
| Database design         | Normalized databases for efficiency        | Denormalized databases for analysis        |


## Data Granularity
- **Granularity** refers nto the level of detail in data stored in a data warehouse.
- Multiple granular level exist in data warehouses to meet various analytical requirements.
- Operational data : lowest level.
- Fine granularity requires substantually permanent data storage.
- Allow users to navigate from summarized info to finer details.
- Balancing the level of detail with performance requirements is essential.

## Meta Data and Warehousing
- In DW, data is stored using a common schema controlled by a common dictionary.
- Metadata should contain following info:-
  - Data Structure (Programmer's view, Analysts' view)
  - Data sources
  - Data transformation details
  - Model of Data
  - Connection between data model and data warehouse
  - Data extraction history

## Data Warehousing Applications
- **Investment and Insurance** : Analyze customer, market trends
- **Healthcare**: Forecadt treatment's outcomes, research
- **Retail**: Distributing, marketing, pricing policies
- **Social media websites**: Fb, Twitter, Impressions, locations, member
- **Banking**: Spending Patterns, Special Offers, deals
- **Government**: Store and analyze taxes
- **Airlines**: Flight frequency, read probability analyses
- **Public Sector**: Helps govt and agencies manage their data and records

## Types of Data Warehouses
1. **Enterprise**
   - Central repo database
   - Central place when all business info from different sources are made available
2. **Operational**
   - Data refreshed in near real-timee
   - Used for routine commercial activity
3. **Data Mart**
   - Subset of DW
   - Supports specific region, business unit etc.
   - Contains subset of data in DW :- enhancing user experiences by reducing volume of data.

## Popular data warehouse platform
- **Google Big Query:**
  - Cost-effective, built in machine learning capabilities.
  - Can be integrated with *Cloud ML* and *Tensoor Flow*
  - Scalable and Serverless
- **AWS Redshift**
  - Cloud Based
  - Can Process petabytes of data fast.
  - Suitable for high speed data analytics.
- **Snowflake**
  - Make business more data driven.
  - Set up an enterprise-grade cloud DW
  - Dependent on Azure, Amazon Web Services, Google Cloud Services
- **Microsoft Azure Synapse**
  - Robust platform for data management, analytics, integration and more
  - AI, Blockchain etc
