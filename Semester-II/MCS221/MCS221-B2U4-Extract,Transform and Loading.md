# Extract, Transform and Loading

## ETL and its need
Extract, Transform and Load(ETL) is a proecess of *data integration* that encompasses three steps: ***Extraction***, ***Trnasformation***, ***Loading***

- **Extract:** This stage determines *which data sources to use, the refresh rate of each source and the priorities between them.*
- **Transform:** It brings clarity and order
  - Date and times :- combined into a single format
  - String parse down into their underlying meanings.
  - Location data converted to coordinates, zip codes or cities/countries.
  - sums up, rounds and average measures
  - deletes useless data and errors
  - masks personally identifiable info to comply with GDPR, CCPA and other privacy requirements
- **Loading:**
  - determines targets and refresh rates
  - This phase determines whether loading will happen incrementally or it will require updating existing data and inserting new data.

## ETL Process
3 steps:
1. **Data Extraction**
   - 4 Steps
     1. **Identify the data to extract:** From various sources like SQL or NOSQL DB or any other platform - which data you want , which data field is required
     2. **Estimate how large the data extraction is:** make large datasets manageable by dividing or upgrade hardware to handle larger dataset.
     3. **Choose the extraction method:**
        - 3 principles
          1. **Update Notifications:** Preferred method, notification sent that record has changed, update only new info.
          2. **Incremental Extraction:** Identify which records have changed and perform extractio of only those records.
          3. **Full Extraction:** Complete Update, Only feasible to small datasets.
     4. **Assess your SaaS Platform:**
        - formerly in-house warehouse
        - now on site server like Google Analytics, Hubspot, Salesforce etc.
2. **Data Transformation**
   - **Deduplication(Normalizing):** Remove duplicate info
   - **Key Restructuring:** Draws key connections from one table to another
   - **Cleansing:** Delete old, incomplete, duplicate data
   - **Format Revision:** Converts data in diff. format to single consistent format
   - **Derivation:** Subtract/add - deriving data
   - **Aggregation:** Gathers abd searches data - summarized repeat format
   - **Integration:** Reconciles diverse names/values to standard
   - **Filtering:** Selects specific columns,rows and fields
   - **Splitting:** Splits one column into more than one column
   - **Joining:** Links data from two or more sources
   - **Summarization:** Creates different business metrics by calculating
   - **Validation:** Rules to follow in diff. circumstances
3. **Data Loading**
   - Processs of loading the extracted info into the target repository
   - 2 ways
     1. **Full Load**
     2. **Incremental Load:** Extract abd Load infor that has appeared since last load
   - **Types of Incremental Loads**
     1. **Batch Incremental Loads**
