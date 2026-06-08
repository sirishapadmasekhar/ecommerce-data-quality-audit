# ecommerce-data-quality-audit

Welcome to the **Data Quality Report for Company X**, where we delve into the complexities of e-commerce data to 

identify and address potential data quality issues.

## Data Description

**conversions Table:**

Contains information about conversions, including conv_id, user_id, conv_date, market, and revenue.
Primary key: (conv_id, user_id, conv_date).

**conversions_backend Table:**

Similar to the conversions table, stores data about conversions.
Primary key: (conv_id, user_id, conv_date).

**api_adwords_costs Table:**

Records information about costs related to AdWords campaigns.
Includes fields such as event_date, campaign_id, cost, and clicks.
Primary key: (event_date, campaign_id).

**session_sources Table:**

Captures details about user sessions, including session_id, user_id, event_date, event_time, channel_name, campaign_name, campaign_id, market, and cpc.
Primary key: (session_id, user_id, event_date).

**attribution_customer_journey Table:**

Represents the attribution data with columns conv_id, session_id, and ihc.
Primary key: (conv_id, session_id).


## Key Questions Explored

**1. Backend Discrepancies**

  - Cross-referenced 'conversions' with 'conversions_backend' to identify and resolve any discrepancies.
     
**2. Conversion Stability Over Time**

  - Examined the stability of conversions over different time periods. Identified patterns or trends that could have implications for business decisions.

**3. Attribution Consistency**

  - Validated the consistency of attribution results across conversions. Investigated conversions with 'ihc' values that deviate from expected patterns.

**4. Cost Coverage Analysis**

  - Investigated whether costs in 'api_adwords_costs' are fully covered in the 'session_sources' table. Identified campaigns with     potential coverage issues.

**5. Channel Stability Over Time**

  - Assessed the stability of the number of sessions per channel over different time periods. Explored insights into potential issues 
    related to channeling.

**6. Additional Data Quality Issues**

  - Investigated the consistency in conversion identifiers across tables for robust data alignment
  - Examined the consistency of campaign_ID across tables
  - Optimized temporal data consistency for comprehensive analysis
  - Conducted market label consistency analysis 
  - Investigated and addressed issues related to incomplete attribution customer journey entries in 'attribution_customer_journey_df'


## Key Findings

**Inconsistency in Conversions:**

- Identified discrepancies between the primary 'conversions' table and the reference 'conversions_backend' table.

**Fluctuating Conversion Values:**

- Observed a general trend of fluctuating conversion values over the specified time period, indicating potential variations.

**Attribution Data Issues:**

- Noted inconsistencies and incorrect data in the 'ihc' column of the conversion table, raising concerns about attribution accuracy.

**Completeness and Accuracy Concerns:**

- Missing campaigns in the 'api_adwords_costs' table raise concerns about the completeness and accuracy of the 'session_sources' table.

**Channeling Issues:**

- Identified issues such as inconsistent channel labeling, data inconsistency, and outliers in the 'session_sources' table across various channels over a period of time.


## Instructions for Running the Code
 
 - To install Python 3.x, preferably version 3.11.1, please visit the [official Python website](https://www.python.org/) 
 
 and follow the provided instructions to download Python on your system.

 - Ensure that the required Python libraries are installed.
 
      - Open a command prompt or terminal.

          - For windows:

             > pip install pandas matplotlib seaborn

          - For MacOS/Linux:
       
             > pip3 install pandas matplotlib seaborn
             
 - Unzip the "challenge.zip" file to access the database file challenge.db

 - Run the main.ipynb file, open it in a Jupyter notebook environment and 
 
 execute each cell sequentially to observe the analysis and results.

## Project Deliverables

 - Data Quality Analysis Report (Notebook)
 - Visualizations and Charts
 - Recommendations for Data Quality Improvement
 - Readme.md summarizing the project and its deliverables










