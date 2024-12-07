# Redfin Analytics: Python ETL Pipeline with Apache Airflow

![Redfin Analytics ETL Pipeline](./Redfin%20Pipeline%20Structure.png)

## Project Overview
This project demonstrates a fully automated ETL (Extract, Transform, Load) pipeline developed for **Redfin Analytics**, utilizing **Python**, **Apache Airflow**, **AWS**, and **Snowflake**. The pipeline is designed to extract real estate data from Redfin, process and transform it, and then load it into **Snowflake** for real-time analysis and visualization.

## Pipeline Architecture
1. **Data Extraction (Python):**
   - The pipeline initiates with Python scripts extracting real estate data from Redfin’s API. The raw data is stored in **Amazon S3** for further processing.

2. **Data Transformation (Python):**
   - Using Python, the raw data undergoes a series of transformation processes, such as cleaning, reshaping, and filtering, to ensure it is optimized for analytics. The transformed data is then stored in a separate S3 bucket.

3. **Orchestration (Apache Airflow):**
   - **Apache Airflow**, deployed on an **AWS EC2 instance**, orchestrates the entire workflow. Airflow schedules and triggers each step of the pipeline, ensuring tasks are executed in the correct order and are fault-tolerant.

4. **Data Loading (SnowPipe):**
   - Once transformed, the data is automatically loaded into **Snowflake** using **SnowPipe** for real-time ingestion. SnowPipe allows continuous loading of new data into Snowflake for efficient querying.

5. **Visualization:**
   - With the data now available in Snowflake, it can be leveraged for analytics and visualized using various BI tools to uncover real estate trends and insights.

## Technologies Used
- **Python**: For data extraction and transformation.
- **Amazon S3**: As a storage solution for raw and transformed data.
- **Apache Airflow**: For orchestrating and automating the ETL workflow.
- **AWS EC2**: For hosting the Airflow instance.
- **Snowflake**: For data warehousing and real-time analytics.
- **SnowPipe**: For automated data loading into Snowflake.

## How to Run the Project
To run this project on your local machine or cloud environment, follow these steps:
1. Clone the repository.
2. Set up the environment with necessary dependencies listed in `requirements.txt`.
3. Configure Apache Airflow on an AWS EC2 instance.
4. Adjust the configuration to point to your **Amazon S3** buckets and **Snowflake** account.
5. Trigger the Airflow DAG to initiate the pipeline.

## Mentions
I’d like to thank **Saylani Mass IT Training Program** and especially **Sir Qasim Hassan** for his invaluable guidance throughout my learning journey. The support and mentorship by sir Qasim have equipped me with the skills necessary to implement this project successfully.
