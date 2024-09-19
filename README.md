# Projects
Overview of the past projects.

**Descriptive Analysis**

<ins>Project Description:</ins>    

Descriptive Analysis of Council Voting Records.

<ins>Project Title:</ins>    

Understanding Council Voting Patterns in Vancouver (2023-2024).

<ins>Objective:</ins>    

The primary goal of this project is to conduct a descriptive analysis of council voting records to summarize key characteristics of voting behaviors, member participation, and voting outcomes. Through this analysis, we aim to identify trends in voting patterns, including unanimous votes and individual member tendencies, to provide insights for future decision-making.

<ins>Dataset:</ins>    

The dataset includes council voting data for the years 2023 and 2024, with the following key features:  
	•	Vote Number: Unique identifier for each vote.  
	•	Council Member: Name of the council member casting the vote.  
	•	Vote Date: Date and time when the vote was cast.  
	•	Meeting Type: Type of council meeting (e.g., Public Hearing, Regular Meeting).  
	•	Vote Outcome: The result of the vote (e.g., In Favor, Opposed, Absent).  
	•	Decision: Final outcome of the vote (e.g., Carried Unanimously, Not Carried).  

<ins>Additional details include: </ins>    
•	Agenda Description: Summary of the topic or issue being voted on during the meeting.  

<ins>Methodology:</ins>    

Identified metrics to be observed in the process

<img width="452" alt="image" src="https://github.com/user-attachments/assets/75aad636-4574-46ee-8b02-2d9d8f698a77">  

1.	Data Collection and Preparation:  
	•	Load council voting records from 2023 and 2024 into AWS S3 for centralized storage and query the data using AWS Athena.  
	•	Use AWS DataBrew to clean the dataset by addressing missing values, standardizing date formats, and removing redundant records.

DataBrew Projects Created  
<img width="452" alt="image" src="https://github.com/user-attachments/assets/3b96a314-63fc-4618-9aba-f0c9f2ac197c">  

DataBrew Project Completion  
<img width="454" alt="image" src="https://github.com/user-attachments/assets/9224f92d-b1c0-4112-bac2-5808e755860a">  

•	AWS CloudTrail Integration:  
Track and log all interactions with the dataset, including API calls, access, and modifications, ensuring that every action is auditable.  
	•	IAM User Permissions Configuration:  
	•	Data Availability Practices:  
	•	S3 Versioning: Enable versioning on the S3 bucket storing the voting data to maintain multiple versions of the dataset, preventing accidental deletions or overwrites.  
 
S3 bucket structure  
<img width="452" alt="image" src="https://github.com/user-attachments/assets/0bec91c2-adc7-499b-9f90-4297b6a2064c">  
•	Cross-Region Replication: Enable cross-region replication to ensure that the voting data is available even if a regional failure occurs. This ensures continued access to the data for reporting and analysis.  
•	Data Integrity Practices:  
•	S3 Bucket Encryption: Enable Server-Side Encryption (SSE) using AWS KMS (Key Management Service) to ensure that data remains encrypted at rest, protecting sensitive council voting records.  

KMS key  
<img width="468" alt="image" src="https://github.com/user-attachments/assets/3c68b1d3-a75e-4107-8d43-8d48accaaf03">  
Encryption  
<img width="468" alt="image" src="https://github.com/user-attachments/assets/1d26067c-1bc4-46b2-8411-574c262b1a2b">  




2.	Descriptive Statistics:  
•	Calculated key statistics using AWS Athena, such as:

Athena Database  
<img width="452" alt="image" src="https://github.com/user-attachments/assets/604ef786-91ed-4086-b911-08272397ce67">  

 
•	Total number of votes cast by each council member.  
•	Percentage of “In Favour” votes by council members.  
•	Frequency of unanimous decisions across meetings.  
•	Aggregated data by meeting type (e.g., Public Hearing, Regular Meeting).  
•	CloudTrail Logs:  
Verified that all descriptive statistics were generated using securely accessed and unaltered datasets, as recorded by CloudTrail.  
	3.	Data Visualization:  
 
 Data Visualization in web server  
 <img width="452" alt="image" src="https://github.com/user-attachments/assets/5dbfd064-f077-4ef3-9714-c2251c58af4f">  
 
 Data Sharing  
 <img width="452" alt="image" src="https://github.com/user-attachments/assets/e1e7dc35-7fc3-4852-a818-cb13af3aef67">  
 


•	Used Excel to create visualizations based on descriptive statistics, including:  
•	Bar Charts: Showcasing the percentage of “In Favour” votes by each council member.  
•	IAM Role Enforcement:  
Restricted access to visualizations and ensured only authorized Data Analysts could generate and view them, using IAM permissions.  
	4.	Voting Segmentation:  
	•	Segmented council members based on their voting behavior, such as frequent voters or those with high percentages of “In Favour” votes.  
	•	Analyzed voting patterns across different meeting types (e.g., Public Hearings vs. Regular Meetings).  
	•	CloudTrail Monitoring:  
Logged all actions during segmentation to ensure only authorized users accessed and modified segmentation criteria.  
	5.	Insights and Findings:  
	•	Generated insights from descriptive analysis, including:  
	•	Identifying council members with consistent voting patterns.  
	•	Observing the prevalence of unanimous votes during certain types of meetings.  
	•	CloudTrail Logs:  
Ensured that all findings were based on secure, validated data as tracked through CloudTrail.  
	•	IAM Permissions:  
Allowed only Admins to review and finalize insights, with access control monitored via IAM policies.  
	6.	Data Availability and Integrity Practices:  
	•	S3 Versioning:    
 
 Bucket Versioning  
 <img width="468" alt="image" src="https://github.com/user-attachments/assets/3eeed0e3-e4e1-4e8b-afc6-807d8aa1125e">  
 

Enabled S3 versioning to ensure that historical versions of the dataset could be retrieved in case of errors or deletions.  
	•	Data Integrity:  
Used AWS KMS for encrypting the dataset in S3 to ensure that voting records were protected at rest and integrity checks were implemented.  

<ins>Tools and Technologies:</ins>    
 
•	AWS S3: For storing raw, curated, and cleaned council voting records.  
•	AWS DataBrew: Used for data cleaning, preparation, and standardization of voting records.  
•	AWS Glue: To implement ETL (Extract, Transform, Load) pipelines for data transformation and aggregation.  

ETL Job  
<img width="452" alt="image" src="https://github.com/user-attachments/assets/ec1ebcc1-4051-4460-ad09-8c6b12681f3a">  

•	Excel: Used for visualizing key metrics and creating bar charts and time series charts for voting behavior analysis.    

<ins>Deliverables:</ins>    
 
•	Detailed Report: A report summarizing the entire process, including data collection, cleaning, and descriptive analysis of council voting patterns.  
•	Data Visualizations: Visualizations such as bar charts and time series plots showcasing council member voting behavior and participation rates, presented using Excel.  
•	Data Pipeline Documentation: Documentation of the AWS Glue ETL pipeline used to process and analyze the voting data.  
•	Data Governance & Security Report: An outline of the data governance strategies applied, including KMS encryption, S3 versioning, and cross-region replication for data protection.  

Bucket Replication  
<img width="468" alt="image" src="https://github.com/user-attachments/assets/308eee91-719b-442f-b4d6-b6a67665d75c">  

PII Detection  
<img width="468" alt="image" src="https://github.com/user-attachments/assets/ce336e85-7986-43e5-a1c2-5bddbe6f87a7">  


**Data Wrangling**

<ins>Dataset:</ins>    
 
The data wrangling process involves working with various datasets, including:  

•	Council Voting Records (2023 and 2024): Contains data on council members, voting dates, vote numbers, and outcomes.  
•	Fields include: Meeting Type, Vote Date, Vote Number, Council Member, Vote Outcome, Decision Outcome.  
•	Council Meeting Agendas: Provides context for what was being voted on during council meetings.  
•	Council Emails: Correspondence and discussions that may have influenced council members’ decisions.  


<ins>Methodology:</ins>    
 

1.	Data Collection:  
•	Collect council voting records from the City of Vancouver’s open data platform, including voting details for the years 2023 and 2024.   
•	Upload raw datasets (voting records, council meeting agendas, and emails) to Amazon S3 for centralized storage and processing.  
2.	Data Assessment:  
•	Perform an initial data quality assessment using AWS DataBrew to identify issues such as:  
•	Missing values in the council member and vote outcome columns.  
•	Inconsistencies in date formats across voting records.  
•	Document the identified issues for further cleaning and standardization.  
3.	Data Cleaning:  
•	Use AWS DataBrew to:  
•	Remove white spaces in the “Council Member” and “Vote” columns.  
•	Standardize date formats (yyyy-mm-dd) for consistency.  
•	Ensure that all records have complete information for key fields such as vote date, council member, and vote outcome.  
4.	Data Transformation:  
•	Create new fields to improve analysis:  
•	Add a “Vote Year” column to distinguish between 2023 and 2024 votes for easier filtering.  
•	Aggregate data to calculate key metrics:  
•	Count of total votes per council member.  
•	Percentage of “In Favour” votes by council members.  
5.	Data Consolidation:  
•	Join the 2023 and 2024 voting records based on common fields such as “Council Member” and “Agenda Description” using AWS Glue.  
•	Store the transformed and consolidated datasets in S3 for further analysis.  
6.	Documentation and Validation:  
•	Document the entire data wrangling process, including the steps taken in AWS DataBrew and Glue for data cleaning, transformation, and aggregation.  
•	Validate the final dataset by querying the cleaned and transformed data in AWS Athena, ensuring completeness and accuracy before proceeding to further analysis.  


<ins>Tools and Technologies:</ins>    

•	AWS DataBrew: Used for data cleaning and preparation, including standardizing date formats and removing inconsistencies in council voting records.  
•	AWS Glue: For automating the ETL (Extract, Transform, Load) process, including transforming and aggregating the voting data from 2023 and 2024.  
•	Excel: For creating visualizations and validating key insights derived from the cleaned data, such as voting percentages.  

<ins>Deliverables:</ins>    
 
•	Cleaned and Transformed Dataset: A fully cleaned and standardized dataset of council voting records for the years 2023 and 2024, stored in a structured format in Amazon S3.  
•	Comprehensive Documentation: A detailed report documenting the data wrangling process, including the steps for cleaning, transforming, and consolidating the data.  
•	Visualizations: Charts and graphs (created in Excel) illustrating key metrics, such as the percentage of “In Favour” votes by council members, generated from the transformed data.  

<ins>Timeline:</ins>    
 
•	Expected Completion Time: 4 weeks, covering the data collection, cleaning, transformation, and final validation phases. This includes 2 weeks for data cleaning and wrangling using AWS DataBrew and AWS Glue, followed by 2 weeks for validation and reporting.  


**Data Quality Control**

<ins>Scope:</ins>    
 
The Data Quality Control initiative for the Council Voting Data Analytic Platform (DAP) will focus on the following key areas:  

•	Data Profiling: Analyzing council voting datasets from 2023 and 2024 to assess their quality, identifying missing values and inconsistencies.  
•	Data Cleansing: Implementing processes to correct errors, standardize data formats, and eliminate duplicates, ensuring accurate council voting records.  
•	Data Validation: Defining and enforcing validation rules to ensure that the data remains consistent and reliable throughout the analytic processes.  
•	Monitoring and Reporting: Establishing dashboards and regular reporting processes using AWS services to track and monitor data quality metrics over time.  
•	Governance and Compliance: Ensuring compliance with data governance regulations, such as PII protection and ensuring data accuracy, using AWS Glue and DataBrew.  

<ins>Methodology:</ins>    


1.	Current State Assessment:  
•	Analyze the council voting datasets stored in S3 to identify quality challenges such as missing values, duplicates, and inconsistent data formats.  
•	Identify critical fields such as council member names, vote outcomes, and meeting dates, which must meet strict quality standards for accurate analysis.  
2.	Data Profiling:  
•	Use AWS DataBrew to perform automated data profiling on the datasets.  
•	Evaluate key data quality indicators, including completeness (e.g., no missing council member names) and consistency across vote records.  
3.	Establish Data Quality Metrics:  
•	Define data quality metrics, including:  
•	Error rates (e.g., missing or incorrect council member information).  
•	Data consistency (e.g., uniform vote outcomes across similar records).  
•	Compliance with formatting rules (e.g., standardized date formats).  
4.	Data Cleansing Processes:  
•	Leverage AWS DataBrew to perform data cleansing tasks, such as:  
•	Removing duplicates in council member names or vote details.  
•	Standardizing inconsistent date formats and vote outcomes across records.  
•	Filling in missing fields where possible (e.g., inferring vote outcomes based on context).  
5.	Validation Rules and Procedures:  
•	Define validation checks within AWS Glue to ensure that future datasets meet quality standards.  
•	Set up rules to prevent errors from being introduced, such as ensuring that all records include valid council member names and dates.  
6.	Monitoring and Reporting:   
•	Implement data quality monitoring using AWS CloudWatch and dashboards for ongoing tracking of quality metrics.  
• Schedule regular reviews of data quality trends, focusing on critical fields such as vote outcomes and council member participation rates.  
7.	Governance and Compliance:  
•	Conduct regular audits of data processing workflows, using AWS Glue and DataBrew, to ensure compliance with legal standards and internal governance protocols.  

<ins>Tools and Technologies:</ins>    
 

•	AWS DataBrew: For automated data profiling, data cleansing, and validation checks on council voting records.  
•	AWS Glue: Used to define data quality metrics and perform validation as part of the ETL process.  
•	AWS CloudWatch: To monitor data quality trends and performance metrics, with alerts for significant deviations in quality.  
•	Excel: For creating visual reports to illustrate data quality metrics and validation results.  


