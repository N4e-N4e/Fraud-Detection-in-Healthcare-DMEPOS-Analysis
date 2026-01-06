# Case Study Team Repository

Welcome to DSA case study team project.

Healthcare fraud, waste, and abuse (FWA) drain billions of taxpayer dollars each year and undermine the integrity of federally funded programs, posing a persistent challenge to the U.S. healthcare system. In fact, FY2024 estimates indicate that improper payments totaled $31.7 billion in Medicare Fee-for-Service and $31.1 billion in Medicaid (CMS, Fiscal Year 2024 Improper Payments Fact Sheet). One particularly vulnerable area involves Durable Medical Equipment, Prosthetics, Orthotics, and Supplies (DMEPOS), which includes items such as wheelchairs, knee braces, and other medical supplies. According to the Office of Inspector General (OIG), Medicare payments for DMEPOS exceed $7 billion annually, and this category remains “a major concern” for FWA in federal programs (OIG, Durable Medical Equipment Fraud and Safeguards in Medicare). 

The U.S. legal and enforcement landscape has increasingly prioritized combating FWA, establishing it as a strategic focus of federal healthcare oversight. For example, on June 30, 2025, the U.S. Department of Justice announced the largest healthcare fraud takedown in U.S. history, charging 324 defendants in schemes amounting to $14.6 billion (United States Department of Justice, National Health Care Fraud Takedown). Although there has been a revitalized focus, FWA investigations rely heavily on public hotline referrals, interagency recommendations, manual audits, and retrospective reviews, which are often slow, resource-intensive, and reactive rather preventive.  Our project will explore how data-driven and predictive approaches can identify providers whose billing and financial behaviors deviate from expected norms. Using a machine-learning framework to analyze provider-level claims data and socioeconomic data to predict potential DME-related fraud, we will be positioning the integrity and anti-fraud agencies to stay ahead of emerging AI driven schemes. 

## SpIn Artifact Descriptions

Scripts are ordered by how they must run. Run all scripts folder by folder, in SpIn order. 
Turn this into markdown renderable text:

**SpIn_1_Artifacts**
Data Loading and Cleaning
1.	medicare_enrollment_clean.ipynb - Cleaning the Medicare Enrollment Monthly Data
2.	CMS_General_Payments_Data_Dict.json – Data Dictionary for General Payments
3.	ownership_payment_clean.ipynb - Cleaning the CMS Ownership data
4.	By_ZCTA.ipynb - Using the Census API to get location and poverty indicators by ZCTA
5.	By_County.ipynb - using the Census API to get location and poverty indicators by County
6.	Phase_2A_DMEPOS_rfrhpr.ipynb - Cleans the DMEPOSby Referring Provider and Service datasets
7.	Phase_2A_DMEPOS_rfrr.ipynb - Cleans the DMEPOS by Referring Provider dataset (no services)
8.	cms_general_payments_clean.ipynb – Cleans the CMS General Payments
9.	oig_leie_clean.ipynb – Cleans the LEIE list

**SpIn_2_Artifacts**
Data Carpentry and Feature Engineering
1.	DMEPOS-Supplier_Service_Datacarpentary.ipynb –Prepared and cleaned DMEPOS by Supplier and Service datasets 
2.	DMEPOS-Supplier_Datacarpentary.ipynb – Prepared and Cleaned DMEPOS by Supplier datasets 
3.	'DMEPOS - BENE_DEMO.ipynb' – Derived beneficiary demographics from DMEPOS by Supplier datasets 
4.	Provider_and_Supplier.ipynb – Prepared, feature-engineered and cleaned DMEPOS by Referral Provider and Service datasets and conducted EDA 
5.	Provider_Amount_Metrics.ipynb – Derived amount related-variable metrics from cleaned DMEPOS by Referral provider and Service dataset
6.	DMEPOS_Amount_stats_explore.ipynb- Builds on Provider_Amount_Metrics.ipynb work by engineering new summary features with HCPCS code counts per NPI by program year.
7.	'Creating Specialties Table.ipynb' - Creates a one row per NPI with the most recent specialty information from our data.
8.	Unique_services.ipynb - Creates a dataset containing every unique combination of HCPCS code and description.
9.	RBCS_Grouping.ipynb - Creates a dataset containing every unique combination of RBCS levels, ID and description, and HCPCS code and description.
10.	'Unifying Datasets.ipynb' – Merges General Payments, Ownership Payments, LEIE, Specialties, and 
11.	'NLP Feature Topic Modeling.ipynb' – Applies NLP to product names from Open Payments.
12.	rfrhpr_validation.ipynb – Analyzing dataset structure, identifying candidate key and investigating dependencies for efficient storage 
13.	rfrr_validation.ipynb - Analyzing dataset structure, identifying candidate key and investigating dependencies for efficient storage

**SpIn_3_Artifacts** 
Database Setup
1.	B_TEMP_SETUP_I1.ipynb – temporary script for database modeling
2.	DB_PostgreSQL.ipynb -  Initial Setup of database structure

**SpIn_4_Artifacts**
EDA
1.	cms_general_payments_eda.ipynb - EDA vizes and summary stats for the General Payments Dataset
2.	oig_leie_eda.ipynb – Basic map created on OIG LEIE counts and vizes on the entity types.
3.	rfrhpr_eda.ipynb - EDA for the DMEPOS by Referring Provider and Service
4.	rfrr_eda.ipynb - EDA for the DMEPOS by Referring Provider (No Service)
5.	'Time Series.ipynb' - time-based visuals and modeling on the payment_date within the general_payments_record_id_level_clean.csv.
6.	DMEPOS-by_supplier_EDA.ipynb – Initial testing; simple cleaning and performing EDA on data (only for 2023 dataset)
7.	DMEPOS-by_supplier___service_EDA.ipynb - Initial testing; simple cleaning and performing EDA on data (only for 2023 dataset)
8.	Providers_and_Supplier_v02.ipynb – Builds on Provider_and_Supplier.ipynb work, visualizes excluded NPIs and Top HCPCS codes via choropleth map and bar chart
9.	DMEPOS_Amount_stats_eda.ipynb – Performs EDA on DMEPOS_Amount_Stats_labeled.csv dataset
10.	EDA_Census_AND_Exclusion-.ipynb - Explores the relationship between healthcare provider exclusions and socioeconomic characteristics at the ZIP code level.
11.	EDA_Ownership_Payment.ipynb - Explores the relationship between healthcare provider exclusions and socioeconomic characteristics at the ZIP code level.
12.	Radar Chart.ipynb – Single test radar chart and a quadrant of four radar charts by specified LEIE excluded NPIs.
13.	Specialty_boxplots.ipynb – Boxplots and analysis on provider specialties. 

**SpIn_5_Artifacts**
Machine Learning and Feature Selection
1.	'K Means.ipynb' - Uses the unified_dataset.csv and run a K-means clustering algorithm on it.
2.	'Local Outlier Factor.ipynb'  - Uses the unified_dataset.csv and the fraud_flag to perform local outlier factor analysis.
3.	feature_selection.ipynb - Uses the unified_dataset.csv to perform XGBClassifier as a means of feature selection based on the class labels.

**SpIn_6_Artifacts**
Final Visuals and Models
-	empty for now, work in progress
