Formula 1 Data Engineering Project
Project Overview
This project demonstrates a comprehensive data engineering pipeline built for analyzing Formula 1 racing data using various Azure services including Azure Databricks, Azure Data Lake Storage, and Azure Data Factory. The goal of the project is to ingest, process, and transform raw race data into meaningful insights and visualizations using Power BI, simulating a real-world data engineering workflow.

Architecture
The project architecture is designed to handle data ingestion, processing, transformation, and visualization in a scalable and automated manner:

Azure Data Lake Storage (ADLS): Used for storing raw, processed, and presentation layers of the data.
Azure Databricks: Employed for data processing and transformation using Python and PySpark, including schema enforcement, data cleansing, and aggregation.
Azure Data Factory (ADF): Orchestrates the entire data pipeline, ensuring automated data ingestion and transformation on a scheduled basis.
Power BI: For creating dynamic and interactive visualizations to analyze race results, driver standings, and team performances.
Data Pipeline Workflow
Ingestion Layer:

Raw data is ingested from the Ergast API into the raw container in ADLS.
Multiple datasets including circuits, races, constructors, drivers, and race results are processed.
Data is then transformed and loaded into the processed container.
Transformation Layer:

Processed data is further refined and stored in the presentation layer.
Various tables are created to analyze and visualize race results, driver standings, and team performances.
Automation:

ADF pipelines are configured to run on a weekly schedule using tumbling window triggers.
The pipeline checks for new data and processes it without failure, even if no new data is available.
Visualization:

Power BI is connected to the presentation layer in ADLS to generate dashboards.
Visualizations include insights into race performance, driver rankings, and constructor standings.
Key Features
Incremental Data Load: Efficient handling of new data by only loading changes while retaining historical data.
Error Handling: Integrated checks ensure the pipeline continues to run smoothly even if new data files are not available.
Automation: Fully automated data pipeline using ADF with minimal manual intervention.
Scalability: Designed to handle large volumes of data and scale as new races are added over time.
Getting Started
Prerequisites
Azure Subscription: Required to deploy and use Azure Databricks, ADLS, and ADF.
Ergast Developer API: Source for Formula 1 race data.
Setup Instructions
Clone the Repository:

bash
Copy code
git clone https://github.com/your-username/formula1-data-engineering.git
cd formula1-data-engineering
Provision Azure Resources:

Create an ADLS account and configure containers for raw, processed, and presentation layers.
Set up Azure Databricks and create necessary notebooks for data processing.
Configure ADF pipelines and set up triggers for automation.
Run the Pipeline:

Manually trigger the ADF pipeline or wait for the scheduled run.
Verify the data processing in Databricks and monitor outputs in ADLS.
Visualize the Data:

Connect Power BI to the presentation layer in ADLS.
Customize and publish the dashboards for race analysis.
Repository Structure
/notebooks: Contains Databricks notebooks used for data ingestion, processing, and transformation.
/adf-pipelines: Exported JSON definitions of ADF pipelines and triggers.
/docs: Documentation and images related to the project.
README.md: This file.
Screenshots
![image](https://github.com/user-attachments/assets/3fd0be70-dfca-4090-a805-e39afb7a3b8e)
![image](https://github.com/user-attachments/assets/f2cd2c0c-0314-4b36-89a6-23d1ca24b759)
![image](https://github.com/user-attachments/assets/9d08a728-b350-43c8-a848-dba5ed547516)
![image](https://github.com/user-attachments/assets/aaba6023-346a-430c-8010-b55bfeb8884c)
![image](https://github.com/user-attachments/assets/58192229-e5a8-438e-bc98-b7ac3be088db)
<img width="708" alt="image" src="https://github.com/user-attachments/assets/fd4a6e55-4dc3-460d-ba60-022a4d57caec">






Contributing
Feel free to open issues or submit pull requests if you have suggestions or improvements.

License
This project is licensed under the MIT License - see the LICENSE file for details.

