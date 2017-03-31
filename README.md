

## Provider recommender Medicare
Build a recommender system for selecting a provider using Medicare payment data.

## Business Understanding
Cost of similar medical conditions can vary widely between providers and between regions. The goal is to generate a provider recommender system considering location, medical condition, cost, and provider rating.  The model will be used by the individual customer to identify an optimal provider in term of affordability and rating. In addition data will allow comparative analysis at regional or national levels, conditions to identify outliers (ex: fraudulent claims by provider). 
Data Understanding
Data is in CSV format and consist of multiple files. Data is unstructured, but the files can be connected using various codes for providers, procedures, etc. The general assumptions are provider submitted Medicare claims are proportional with provider regular insurance claims and Medicare payments are proportional with insurance payments. 

## Data Preparation
https://www.cms.gov/Research-Statistics-Data-and-Systems/Statistics-Trends-and-Reports/Medicare-Provider-Charge-Data/Physician-and-Other-Supplier2014.html

If we use only the Provider Charge Data database for 2014, data is relatively clean and doesn’t need extended preparation. However more data can be added to include previous years. Depending of project details, data can be expanded to include details for each procedure, actual procedure cost instead of average cost, location data, etc. Provider total rating is calculated by aggregating individual patient ratings using data located here:

https://www.cms.gov/Medicare/Quality-Initiatives-Patient-Assessment-Instruments/PQRS/index.html

Data from various files will be summarized in a file that containing provider identification data, medical condition data, payment details, rating details.

## Modeling
Use Random Forest and other algorithms to validate the model. Use Isolation Forest to identify the outliers. Review the outliers and rate them.

## Evaluation
Select data for a limited numbers of providers and run the model to generate results. 
Build a model with limited complexity, considering fewer features and test it.  Find the optimal model features, parameters and generalize the result for the entire data set. Evaluate if there are relative discrepancies between prices for similar conditions, identify most expensive procedures, build indicators to identify the best providers.

Backup data: https://data.cms.gov/Medicare/Inpatient-Prospective-Payment-System-IPPS-Provider/97k6-zzx3

## Deployment
The initial deployment will be in a Github repository and presented in a powerpoint format. 
