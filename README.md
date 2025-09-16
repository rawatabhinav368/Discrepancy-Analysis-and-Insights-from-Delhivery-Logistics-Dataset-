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

The primary dataset used for this analysis is the **"rides_data.csv"** [Download rides_data.csv](https://github.com/rawatabhinav368/Hospital-Supply-Chain-Inventory-Optimization/blob/main/inventory_data.csv) file, which was downloaded from Kaggle's [Bangalore Rapido Ride Services Dataset](https://www.kaggle.com/datasets/vishaldeoprasad/bangalore-rapido-ride-services-dataset?select=rides_data.csv).  This dataset contains detailed information about Bangalore Rapido Ride Services, including the following features:

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

### Data Cleaning/Preparation

  In the initital data preparation pharase, we preformed the following tasks:
  
  1. Data Loading and inspection 
  
  2. Checking for missing values -

* There was 5036 null values in our data set, for all cancelled ride (ride_charge	misc_charge	total_fare	payment_method) it shows NaN. 
  A canceled ride does not incur any charges, so filling 0.
* No transaction occurred, "Not Applicable" is a meaningful label for payment method.
* Created canceled column : 1 for canceled rides, 0 for all other rides.

  ### Exploratory data analysis (EDA)
 
  EDA involves exploring the ride data to answer key questions, such as:

  - Which service type (e.g., Bike, Auto, Cab) is most preferred by users?
  - What are the peak demand hours for each service type?
  - How do service preferences change throughout the day or week?
  - What proportion of rides are completed versus canceled?
  - Which payment methods are most popular among users?
  - How strongly are features like distance, duration, and fare related?
  - Are there specific periods that contribute significantly to revenue spikes?
  - 

### Data Analysis 

Including some intresting code/features worked with 


### Results/Findings

The analysis results are summarized as follows:
* High demand for bike services during early mornings, auto and cab demand peaks in the afternoon and evening.
* Ride counts fluctuate over time, with consistent peaks during specific periods.
* Paytm and GPay are the most popular payment methods, possibly influenced by promotions.
* Bike services are the most preferred, offering consistent ride durations, while auto and cab services show more variability.
*  ARIMA and SARIMAX models suggest growing demand with daily fluctuations.

  ## Recommendations
* Increase bike availability during morning hours and prioritize auto/cab services in the evening.
* Promote bike services as a cost-effective, quick option for short-distance travel.
* For auto and cab services, focus on improving ride consistency by reducing variability in ride durations (e.g., through better route optimization or partnerships with local authorities to reduce traffic bottlenecks).
*  Capitalize on Paytm and GPay’s popularity by offering time-limited discounts to further drive engagement.
*  Promote premium cab services during evenings for social outings or corporate travel to attract higher-paying customers.
