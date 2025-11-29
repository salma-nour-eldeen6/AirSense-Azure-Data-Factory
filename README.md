# AirSense - Global Air Travel Analytics

AirSense is a data engineering project aimed at analyzing how global events impact international air travel. The system collects, processes, and visualizes diverse datasets, providing actionable insights for decision-makers.

---

## Project Overview
Global events—including health crises, sports, political developments, and cultural phenomena—directly influence human mobility and air travel. AirSense builds an end-to-end data pipeline to help understand these effects quickly and accurately.

---

## Methodology
AirSense transforms flight, health, and event data into meaningful insights through a structured process:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/45cc6d48-5abb-48c5-82ac-89fe15ea654c" />

1. **Data Collection**  
   - Flight data: OpenSky Network (2021–2022)  
   - COVID-19 data: Our World in Data  
   - Global events & sports 

2. **Data Ingestion**  
   - Move raw data from local sources to Azure Blob Storage (Landing Zone)  
   - Connect PostgreSQL (local) → Azure Data Factory (ADF) → Blob Storage  
   - Store datasets in Parquet format for optimized processing  

3. **Data Cleaning & Preprocessing**  
   - Standardize formats, handle missing values, remove duplicates  
   - Keep essential fields for Flights, COVID, Sports, and Global Events  

4. **Dimensional Modeling**  
   - Galaxy Schema with conformed dimensions (Date, Location, Aircraft, Global Trends)  
   - Fact tables: Flights, COVID Impact, Sports Events  

5. **Transformation & ELT**  
   - Aggregations: daily/monthly flight volumes  
   - Derived metrics: estimated passenger capacity, event impact  
   - Link facts to dimensions using Azure Data Factory Mapping Data Flows
     <img width="925" height="719" alt="image" src="https://github.com/user-attachments/assets/be14e340-a5bb-4b0a-b0e0-964b898235a7" />


6. **Pipeline Orchestration**  
   - Automated ETL workflows in ADF  
   - Maintain referential integrity and performance using self-hosted integration runtime  

7. **Analysis & Visualization**  
   - Query processed datasets with Azure Synapse Analytics  
   - Visualize trends and impacts in Power BI dashboards
     <img width="1192" height="659" alt="image" src="https://github.com/user-attachments/assets/539ef952-8580-4afa-9e5a-40f3f0d71cf2" />
     <img width="1196" height="658" alt="image" src="https://github.com/user-attachments/assets/eb062f6b-b9d8-40bc-b76b-4310338bd62f" />
     <img width="1171" height="662" alt="image" src="https://github.com/user-attachments/assets/956c1cb7-c939-4e5e-8ef1-69d3ea331d6a" />




---

## Key Technologies
- **Azure Data Factory (ADF)**: ETL/ELT orchestration  
- **Azure Data Lake Storage**: Data storage & curation  
- **Azure Synapse Analytics**: Data analysis  
- **Power BI**: Interactive visualization  
- **PostgreSQL**: Staging and structured storage  
- **Parquet format**: Optimized data storage  

---

## Outcomes
- Cleaned and structured datasets ready for analysis  
- Insights into how global events affect air travel trends  
- Dashboards enable temporal and geographical exploration of flight patterns  

---

## Project Team
- **Salma Nour-Eldeen** – Data Engineer  
- **Hanin Baher**  




