# Real-Time Seismic Event Analysis and Risk Prediction

## Project Overview
This project demonstrates an end-to-end data pipeline for real-time seismic event analysis and risk prediction using Microsoft Fabric. The pipeline integrates Data Engineering, Data Factory, and Power BI to analyze real-time earthquake data from the USGS (United States Geological Survey) earthquake API. The data pipeline follows the Medallion Architecture to transform raw earthquake event data into actionable insights. Predictive analytics and real-time data processing capabilities further enhance the value of this project, enabling proactive risk management and disaster response.

---

## Technologies Used
- **Python** and **PySpark** for data processing.
- **Microsoft Fabric** for lakehouse creation and data engineering.
- **Azure Data Factory** for orchestration and automation.
- **Power BI** for data visualization and reporting.
- **Azure Stream Analytics** or **Spark Structured Streaming** for real-time data ingestion and processing.
- **Azure Machine Learning** for predictive analytics.

---

## Key Objectives
1. **Real-Time Data Ingestion:** Ingest real-time earthquake event data from the USGS API.
2. **Data Transformation:** Process raw data incrementally using the Medallion Architecture (Bronze, Silver, and Gold layers).
3. **Predictive Analytics:** Train machine learning models to predict earthquake magnitudes and regions with higher seismic activity.
4. **Visualization:** Create interactive dashboards in Power BI for real-time analysis and insights.
5. **Automation and Scalability:** Automate the pipeline and optimize it for larger datasets.

---

## Medallion Architecture
### Bronze Layer
- Stores raw, unprocessed data fetched from the USGS earthquake API.
- Retains the original JSON structure for future transformations.

### Silver Layer
- Transforms raw data into a cleaner, more structured format.
- Key transformations include:
  - Extracting latitude, longitude, and elevation.
  - Parsing timestamps into human-readable formats.
  - Filtering incomplete or irrelevant data.

### Gold Layer
- Creates business-ready datasets optimized for analysis.
- Aggregates key metrics such as:
  - Earthquake frequency by region or time period.
  - Average magnitude and significance scores.

---

## Pipeline Workflow
### Data Engineering
- **Python Scripts and PySpark Notebooks:**
  - Fetch and preprocess earthquake event data from the API.
  - Transition data through the Bronze, Silver, and Gold layers.

### Real-Time Data Processing
- **Azure Stream Analytics or Spark Structured Streaming:**
  - Enables near real-time ingestion and processing of earthquake events.
  - Provides immediate insights for disaster response.

### Data Orchestration
- **Azure Data Factory:**
  - Automates the pipeline with a daily or real-time schedule.
  - Ensures incremental updates to all layers.

### Predictive Analytics
- **Machine Learning Models:**
  - Use Azure Machine Learning or Spark MLlib to predict:
    - Earthquake magnitudes.
    - Regions with high seismic activity.
    - Potential aftershock events.

### Visualization
- **Power BI Dashboards:**
  - Visualize trends, geographical patterns, and predictions.
  - Include features such as:
    - Interactive heatmaps.
    - Drill-down capabilities by region and time.
    - 3D visualizations for enhanced geographical analysis.

---

## Data Attribute Definitions
| Attribute          | Type    | Description                                                  |
|--------------------|---------|--------------------------------------------------------------|
| `id`               | String  | Unique identifier for each earthquake event.                |
| `latitude`         | Double  | Latitude of the earthquake event.                           |
| `longitude`        | Double  | Longitude of the earthquake event.                          |
| `elevation`        | Double  | Elevation at the event location, in meters.                 |
| `title`            | String  | Title or name of the earthquake event.                      |
| `place_description`| String  | Description of the event location.                          |
| `sig`              | BigInt  | Significance score of the earthquake event.                 |
| `mag`              | Double  | Magnitude of the earthquake.                                |
| `magType`          | String  | Type of magnitude scale used.                               |
| `time`             | Timestamp | Time of the earthquake event.                              |
| `updated`          | Timestamp | Last update time for the event data.                        |

---

## Enhancements and Future Work
1. **Real-Time Data Processing:**
   - Implement near real-time processing using Azure Stream Analytics or Spark Structured Streaming.
   - Provide immediate insights for disaster response teams.

2. **Predictive Analytics:**
   - Train machine learning models to predict seismic events.
   - Perform trend analysis to identify long-term seismic patterns.

3. **Advanced Visualization:**
   - Add interactive heatmaps and 3D visualizations in Power BI.
   - Enable drill-down capabilities for granular analysis.

4. **Geospatial Analysis:**
   - Leverage GIS tools like GeoPandas for spatial analysis.
   - Analyze proximity to fault lines or urban centers.

5. **Data Quality Monitoring:**
   - Implement validation checks to detect anomalies or missing data.
   - Use monitoring tools to track pipeline health and performance.

6. **Scalability:**
   - Integrate additional data sources, such as volcanic activity or weather data.
   - Optimize Spark jobs for larger datasets.

7. **Documentation and CI/CD:**
   - Provide comprehensive documentation for each pipeline component.
   - Set up CI/CD pipelines for seamless deployment of updates.


---

## Link to the API
- **USGS Earthquake API:** [USGS Earthquake API Documentation](https://earthquake.usgs.gov/fdsnws/event/1/)

---

## Summary
The "Real-Time Seismic Event Analysis and Risk Prediction" project showcases how Microsoft Fabric can be used to build a robust, real-time data pipeline for seismic event analysis. With predictive analytics, real-time insights, and advanced visualization capabilities, this project paves the way for better disaster response and proactive risk management.

