# cis4400NYCRestaurants
Analysis of NYC restaurant inspections and Yelp ratings, with data sourced from NYC Open Data and Yelp API, to explore the correlation between health violations and customer reviews.

## **Table of Contents**
- [Project Overview](#project-overview)
- [Business Requirements](#business-requirements)
- [Information Architecture](#information-architecture)
- [Data Architecture](#data-architecture)
- [Dimensional Modeling](#dimensional-modeling)
- [Cost, Benefits, Risks](#cost-benefits-risks)


## **Project Overview**
This project analyzes the correlation between NYC restaurant health violations and Yelp ratings. By combining health inspection data from NYC Open Data with Yelp customer reviews, the project provides actionable insights for:
- Restaurant owners to improve compliance and customer satisfaction.
- Health inspectors to identify borough-wide trends and recurring violations.
- Policymakers to create regulations that improve public health and safety.

## **Business Requirements**

### 1. **Key Objectives**
   - **Correlation Analysis**:
      - Determine the relationship between health inspection violations and Yelp ratings.
   - **Violation Trends**:
      - Identify borough-specific patterns in violations and ratings.
   - **Actionable Insights**:
      - Provide recommendations for improving compliance and customer satisfaction.

      ---

### 2. **Functional Requirements**:
   - Use Python for ETL tasks.
   - Use Tableau for visualizing trends and insights.
   - Integrate data from NYC Open Data and Yelp APIs.



## **Information Architecture**
The Information Architecture describes the data flow and tools used in the project pipeline:

### 1. **Data Sources**:
   - NYC Open Data:
     - [DOHMH New York City Restaurant Inspection Results](https://data.cityofnewyork.us/Health/DOHMH-New-York-City-Restaurant-Inspection-Results/43nn-pn8j/about_data)
     - [Open Restaurants Inspections](https://data.cityofnewyork.us/Transportation/Open-Restaurants-Inspections/4dx7-axux/about_data)
   - Yelp Dataset and API:
      - [Yelp Dataset](https://www.yelp.com/dataset)
      - [Yelp Fusion API](https://docs.developer.yelp.com/)
      - Provides restaurant ratings, review counts, and metadata.

      ---

### 2. **Pipeline Stages**:
   - **Data Collection**: Collect data from NYC Open Data and Yelp APIs.
   - **Cleaning**: Handle missing values, duplicates, and align data formats.
   - **Transformation**: Reformat data into a star schema for analysis.
   - **Storage**: Store intermediate data in MongoDB and processed data in Azure.
   - **Visualization**: Create dashboards in Tableau to present insights.

---

### 3. **Key Tools**:
   - Data collection via APIs.
   - MongoDB for raw data storage.
   - Google Colab and Microsoft Azure for data processing and storage.
   - Tableau for visualization.

   ---

(image here)
## **Data Architecture**

## **Dimensional Modeling**

## **Cost, Benefits and Risks**
This section outlines the anticipated costs, potential benefits, and associated risks of the project, providing a balanced view of its overall impact.

### 1. **Costs**
- **Tools**:
  - **Microsoft Azure**: Cloud storage and processing for structured data.
  - **Tableau**: Visualization software for building dashboards.
- **Development**:
  - Time and effort for ETL pipeline development, data cleaning, and integration.
- **API Limitations**:
  - Yelp API: Limited to 300-500 calls depending on account tier.

---

### 2. **Benefits**
- **Restaurant Owners**:
   - Insights into compliance gaps and customer satisfaction drivers.
   - Strategies for improving health inspection scores and Yelp ratings.

- **Consumers**:
   - Empowered decision-making with access to high-compliance restaurants.

---

### 3. **Risks**
- **Data Challenges**:
  - Incomplete or inconsistent data from APIs or missing attributes in inspection records.
- **Scalability Issues**:
  - Handling large datasets from NYC Open Data and Yelp without optimized storage.
- **Technical Limitations**:
  - API rate limits for Yelp may restrict the amount of data retrieved.
- **Data Integration Complexity**:
  - Merging disparate datasets (e.g., inspection data and Yelp reviews) with inconsistent identifiers.

---

This section balances the project’s value with its potential challenges, ensuring transparency and demonstrating proactive planning.