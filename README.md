# Snowflake cricket analytics


This repository contains the code and documentation for an end-to-end data engineering project focused on cricket analytics. The project includes the ingestion of data from JSON files, processing it through various layers, and building a consumption layer for analytics. The analytics results can be visualized in a dashboard using Snowsight.

## Project Structure

The project is organized into several layers:

1. **Land Layer**: The initial landing layer where raw data in JSON format is stored.
- Used **Json Cracker** tool to visualize our deeply nested Jsons to understand their structure.
- Created internal Stage and Json File Format to store our Json files in Snowflake.

2. **RAW Layer**: The raw layer stores the ingested data without any transformation. It includes tasks to load data from JSON files into Snowflake tables.

- ingested our data in a Raw Format to MATCH_RAW_TABLE Table
<img width="980" alt="Screenshot 2024-10-08 at 11 36 24 AM" src="https://github.com/user-attachments/assets/a751152f-c870-48fb-b581-d2e1477fa69a">

3. **Clean Layer**: The clean layer is responsible for cleaning and transforming the raw data. It includes tasks to create clean tables that are more suitable for analysis.
- Created Three Tables in Clean Schema (Layer): Concerning Player , Match_detail , Delivery Table.
<img width="981" alt="Screenshot 2024-10-08 at 11 37 30 AM" src="https://github.com/user-attachments/assets/d943228f-82a1-4a0d-87a6-d3d113cc34a1">

4. **Consumption Layer**: The consumption layer is designed for analytics and reporting. It includes the final tables and views that are used for creating dashboards.
- Use Data Modeling to build our Datawarehouse Facts and dimensions.
 <img width="782" alt="Screenshot 2024-10-08 at 11 39 08 AM" src="https://github.com/user-attachments/assets/9fb009a5-0474-4346-8d8e-ee5f0317633a">



5. **Dashboard**: The dashboard layer utilizes Snowsight to visualize the analytics results. It can be accessed for insightful data analysis and reporting.
<img width="880" alt="Screenshot 2024-10-08 at 11 39 37 AM" src="https://github.com/user-attachments/assets/fa460add-ab0e-40fd-b71b-8487b780b584">




5. **Automate Continuous Data Flow**: automating continuous data flow, specifically by creating automated tasks to listen to change data capture (CDC) and update data in all tables.

