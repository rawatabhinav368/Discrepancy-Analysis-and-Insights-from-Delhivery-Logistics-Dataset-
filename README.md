# Discrepancy-Analysis-and-Insights-from-Delhivery-Logistics-Dataset-

## Table of Contents

1. [Project Overview](#project-overview)  
2. [Problem Description](#problem-description)  
3. [Data Sources](#data-sources)  
4. [Tools](#tools)  
5. [Data Cleaning & Preparation](#data-cleaning--preparation)  
6. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)  
7. [Data Analysis](#data-analysis)  
8. [Results & Findings](#results--findings)  
9. [Recommendations](#recommendations)  

---

### Project Overview

This project focuses on analyzing discrepancies between estimated and actual delivery metrics in Delhivery's logistics operations. By understanding patterns and factors affecting these deviations, we aim to improve route efficiency, reduce operational costs, and optimize delivery times.

---

### Problem Description

Delhivery, a leading logistics provider, experiences significant discrepancies between estimated and actual delivery metrics, particularly in **time** and **distance**. These deviations result in route inefficiencies, higher operational costs, and delayed deliveries.  

The project analyzes these discrepancies to identify the root causes and provide actionable insights to optimize logistics operations.

---

### Data Sources

**Dataset Source:**  

The primary dataset used for this analysis is the **"delivery_data.csv"** [Download delivery data.csv](https://github.com/rawatabhinav368/Discrepancy-Analysis-and-Insights-from-Delhivery-Logistics-Dataset-/blob/main/Delhivery%20Data.zip) file, which was downloaded from Kaggle's [Delhivery DataSet](https://www.kaggle.com/datasets/santanukundu/delhivery-dataset).  This dataset contains detailed information about Delhivery Logistics Data, including the following features:

**Key Attributes:**  

- **data** – A categorical attribute indicating the type of data (e.g., "training")
- **trip_creation_time** – Timestamp when the trip was created  
- **route_schedule_uuid** – Unique identifier for the route schedule  
- **route_type** – Type of route (e.g., Carting, FTL, LTL)  
- **trip_uuid** – Unique identifier for the trip  
- **source_center** – The source or starting location of the trip  
- **source_name** – Name of the source or origin center
- **destination_center** – The destination center where the trip ends 
- **destination_name** – Name of the destination center  
- **od_start_time** – Timestamp when the trip started  
- **od_end_time** – Timestamp when the trip ended  
- **cutoff_timestamp** – Timestamp when the cutoff occurred for the trip  
- **actual_distance_to_destination** – Actual distance to the destination (in kilometers)
- **actual_time** – Actual time taken for the trip (minutes)  
- **osrm_time** – Estimated time to destination from OSRM (minutes)  
- **osrm_distance** – Estimated distance to destination from OSRM (km)  
- **factor** – Factor affecting time or distance, influencing discrepancies  
- **segment_actual_time** – Actual time taken for each trip segment  
- **segment_osrm_time** – Estimated time for each segment from OSRM  
- **segment_osrm_distance** – Estimated distance for each segment from OSRM  
- **segment_factor** – Factor affecting each segment’s time or distance 

### Tools

1. **Python**: 
    Libraries Used: - Pandas , Numpy, Matplotlib, Seaborn, Plotly, Warnings.

2. **Power Bi**: 
   - Power BI was used for data visualization. It helped in creating an interactive dashboard to analyze Delhivery logistics data, monitor trip efficiency, and identify trends in real-time. This provided key insights into delivery performance by comparing actual and estimated metrics. The dashboard serves as a comprehensive tool for stakeholders to analyze trip discrepancies and make data-driven decisions.


   - ## Delhivery Logistics Discrepency And Efficiency Dashboard 

Click the image below to view the dashboard:

[![Rapido Banglore Service and Demand Anlytics Dashboard](https://github.com/rawatabhinav368/Banglore-RapidoRide-Analytics-Trends-Demand-Forecasting/blob/main/RapidoRide%20Trend%20Bangalore%20Analytics%20And%20Demand%20Forecasting.png)](https://github.com/rawatabhinav368/Banglore-RapidoRide-Analytics-Trends-Demand-Forecasting/blob/main/RapidoRide%20Trend%20Bangalore%20Analytics%20And%20Demand%20Forecasting.png)

### Data Cleaning/Preparation

  In the initital data preparation pharase, we preformed the following tasks:
  
  1. Data Loading and inspection 
  
  2. Checking for missing values -

The missing values in the source_name and destination_name columns have been successfully filled with "Unknown".

* Unique values in source_name after filling missing values: Unique values in source_name after filling missing values:

['Anand_VUNagar_DC (Gujarat)' 'Khambhat_MotvdDPP_D (Gujarat)' 'Bhiwandi_Mankoli_HB (Maharashtra)' ... 'Dwarka_StnRoad_DC (Gujarat)' 'Bengaluru_Nelmngla_L (Karnataka)' 'Kulithalai_AnnaNGR_D (Tamil Nadu)']

* Unique values in destination_name after filling missing values: Unique values in destination_name after filling missing values:

['Khambhat_MotvdDPP_D (Gujarat)' 'Anand_Vaghasi_IP (Gujarat)' 'Pune_Tathawde_H (Maharashtra)' ... 'Chennai_Mylapore (Tamil Nadu)' 'Naraingarh_Ward2DPP_D (Haryana)' 'Mumbai_Ghansoli_DC (Maharashtra)']


  ### Exploratory data analysis (EDA)
 
  EDA involves exploring the delivery logistics data to answer key questions, such as:

  -Which service type (e.g., FTL, Carting, etc.) is most frequently used?

  -What are the peak hours for trip creation or completion?

  -How do trip preferences or efficiency metrics change throughout the day or week?

  -What is the proportion of trips with positive time discrepancies versus negative or no discrepancies?

  -Which source and destination centers have the highest average trip delays?

  -How strongly are features like trip duration, distance, and cutoff factor related to the time and distance discrepancies?

  -Are there specific months or seasons that contribute significantly to a rise in delivery discrepancies?
   

### Data Analysis 

Including some intresting code/features worked with 


## *To summarize our analysis:*

* ### *Data Cleaning and Preparation:*

   * *Filled missing values in source_name and destination_name with "Unknown".*
   * *Converted timestamp columns to datetime format.*

* ### *Exploratory Data Analysis (EDA):*

   * *Visualized the distribution of trip durations and distances.*
   * *Analyzed the relationship between trip duration and distance.*
   * *Examined the impact of route type and cutoff factors on trip duration.*
   * *Compared actual times and distances with OSRM estimated times and distances.*

* ### *Discrepancy Analysis*

   * *Calculated discrepancies between actual and estimated times/distances.*
   * *Performed correlation analysis to identify key factors contributing to discrepancies.*
   * *Built regression models to quantify the impact of these factors on discrepancies.*
 
 ## *Key Findings:* 

   * *The cutoff_factor and start_scan_to_end_scan are significant contributors to the discrepancies between actual and estimated times/distances.*
    
   * *The regression models showed high R-squared values, indicating that the selected features explain a significant portion of the variance in the discrepancies.*
* *These insights can help Delhivery optimize their logistics operations by focusing on improving the factors that contribute to discrepancies, such as refining cutoff times and optimizing the time from start scan to end scan.*
