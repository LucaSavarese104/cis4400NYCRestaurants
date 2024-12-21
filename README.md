# **cis4400NYCRestaurants**

**Exploring the Relationship Between NYC Restaurant Inspections and Yelp Ratings**

---

## **Table of Contents**
1. [Business Problem](#business-problem)
2. [Business Impact](#business-impact)
3. [Business Personas](#business-personas)
4. [Data Sources and Methods](#data-sources-and-methods)
5. [Data Tools](#data-tools)
6. [Interface](#interface)
7. [Supporting Files](#supporting-files)
8. [PowerPoint Presentation](#powerpoint-presentation)

---

## **1. Business Problem**

### Description
This project analyzes NYC restaurant health violations and their correlation with Yelp ratings. The primary objective is to uncover borough-level trends and provide actionable insights to improve compliance, customer satisfaction, and health outcomes.

### Key Objectives
- Investigate correlations between health violations and Yelp ratings.
- Provide borough-specific insights into compliance and public health trends.
- Offer actionable recommendations for restaurant owners, health inspectors, and policymakers.

---

## **2. Business Impact**

### Benefits
- **Restaurant Owners**: Identify compliance gaps to improve customer satisfaction.
- **Health Inspectors**: Detect boroughs and ZIP codes with recurring violations.
- **Policymakers**: Leverage insights to develop borough-level public health policies.

### Costs and Risks
- **Costs**: Microsoft Azure (data storage), Tableau (visualization tools).
- **Risks**: API limitations (e.g., Yelp API call caps), data inconsistency between inspection and Yelp datasets.

---

## **3. Business Personas**

### Key Stakeholders
- **Restaurant Owners**: Utilize insights to address compliance issues.
- **Health Inspectors**: Focus inspections based on borough-specific trends.
- **Policymakers**: Use data to refine public health regulations.

### System Users
- **Data Engineers**: Build ETL pipelines.
- **Data Analysts**: Analyze and visualize trends.
- **Visualization Experts**: Create dashboards for stakeholder insights.

---

## **4. Data Sources and Methods**

### Data Sources
1. **NYC Open Data**:
     - [DOHMH New York City Restaurant Inspection Results](https://data.cityofnewyork.us/Health/DOHMH-New-York-City-Restaurant-Inspection-Results/43nn-pn8j/about_data)
     - [Open Restaurants Inspections](https://data.cityofnewyork.us/Transportation/Open-Restaurants-Inspections/4dx7-axux/about_data)
2. **Yelp API**:
      - [Yelp Dataset](https://www.yelp.com/dataset)
      - [Yelp Fusion API](https://docs.developer.yelp.com/)

### Methods
- **ETL Process**:
  - Scripts for data cleaning: [`cleaning_and_merging_borough.ipynb`](Scripts/cleaning_and_merging_borough.ipynb)
  - Data transformation: [`Transform_Open_Restaurant_Data_Group_2.ipynb`](Scripts/Transform_Open_Restaurant_Data_Group_2.ipynb)
  - Yelp API integration: [`Yelp_API_scraping_and_upload.ipynb`](Scripts/Yelp_API_scraping_and_upload.ipynb)
- **Visualization**: Tableau dashboards created from processed data.

---

## **5. Data Tools**

### Tools Used
- **Storage**:
  - MongoDB for raw data storage.
  - Microsoft Azure for structured data storage.
- **Processing**:
  - Python with libraries like Pandas and NumPy for data cleaning.
- **Visualization**:
  - Tableau for creating interactive dashboards.

---

## **6. Interface**

### Visualization and Insights

1. **Borough vs. Average Yelp Rating by Critical Violations**  
   ![Borough vs. Yelp Rating](Visuals/Borough%20vs.%20Average%20Yelp%20Rating%20by%20Critical%20Violations.png)
      - [Tableau Public](https://public.tableau.com/app/profile/luca.savarese/viz/Boroughvs_AverageYelpRatingbyCriticalViolations/Sheet3)

2. **ZIP Code Analysis for NYC Boroughs**:

    - Manhattan: ![Manhattan Analysis](Visuals/Manhattan%20ZIP%20Code%20Analysis%20Comparing%20Yelp%20Ratings%20and%20Critical%20Health%20Violations.png)
      - [Tableau Public](https://public.tableau.com/app/profile/luca.savarese/viz/ManhattanZIPCodeAnalysis/Sheet83)
   - Brooklyn: ![Brooklyn Analysis](Visuals/Brooklyn%20ZIP%20Code%20Analysis%20Comparing%20Yelp%20Ratings%20and%20Critical%20Health%20Violations.png)
      - [Tableau Public](https://public.tableau.com/app/profile/luca.savarese/viz/BrooklynZIPCodeAnalysis/Sheet84)
   - Bronx: ![Bronx Analysis](Visuals/Bronx%20ZIP%20Code%20Analysis%20Comparing%20Yelp%20Ratings%20and%20Critical%20Health%20Violations.png)
      - [Tableau Public](https://public.tableau.com/app/profile/luca.savarese/viz/BronxZIPCodeAnalysis/Sheet85)
   - Queens: ![Queens Analysis](Visuals/Queens%20ZIP%20Code%20Analysis%20Comparing%20Yelp%20Ratings%20and%20Critical%20Health%20Violations.png)
      - [Tableau Public](https://public.tableau.com/app/profile/luca.savarese/viz/QueensZIPCodeAnalysis/Sheet86)
   - Staten Island: ![Staten Island Analysis](Visuals/Staten%20Island%20ZIP%20Code%20Analysis%20Comparing%20Yelp%20Ratings%20and%20Critical%20Health%20Violations.png)
      - [Tableau Public](https://public.tableau.com/app/profile/luca.savarese/viz/StatenIslandZIPCodeAnalysis/Sheet87)

3. **NYC ZIP Codes: Violation Hotspots**:
   - ![NYC Violation Hotspots](Visuals/NYC%20ZIP%20Codes%20Violation%20Hotspots.png)
      - [Tableau Public](https://public.tableau.com/app/profile/luca.savarese/viz/NYCZIPCodesViolationHotspots/Sheet4)

4. **Yelp Rating Categories and Critical Violations**:
   - ![Yelp Rating Categories](Visuals/Yelp%20Rating%20Categories%20and%20Critical%20Violations.png)
      - [Tableau Public](https://public.tableau.com/app/profile/luca.savarese/viz/YelpRatingCategoriesandCriticalViolations/Sheet2)

5. **Monthly Trends in Critical Flag Health Inspections Across NYC Boroughs**:
   - ![Monthly Trends](Visuals/Monthly%20Trends%20in%20Critical%20Flag%20Health%20Inspections%20Across%20NYC%20Boroughs.png)
      - [Tableau Public](https://public.tableau.com/app/profile/luca.savarese/viz/MonthlyTrends_17348225607490/Sheet15)

---

## **7. Supporting Files**

### File Structure
1. **Model & Architecture**:
   - [Information Architecture](Model%20&%20Architecture/information_architecture.png)
   - [Data Architecture](Model%20&%20Architecture/Data%20Architecture.png)
   - [Dimensional Model](Model%20&%20Architecture/Dimensional%20Model%20Restaurant%20Analysis.png)

2. **Scripts**:
   - [`cleaning_and_merging_borough.ipynb`](Scripts/cleaning_and_merging_borough.ipynb)
   - [`Transform_Open_Restaurant_Data_Group_2.ipynb`](Scripts/Transform_Open_Restaurant_Data_Group_2.ipynb)
   - [`Yelp_API_scraping_and_upload.ipynb`](Scripts/Yelp_API_scraping_and_upload.ipynb)

3. **Visuals**:
   - Borough vs. Yelp Rating: [`Borough_vs_Yelp.png`](Visuals/Borough%20vs.%20Average%20Yelp%20Rating%20by%20Critical%20Violations.png)
   - NYC ZIP Code Hotspots: [`NYC_Hotspots.png`](Visuals/NYC%20ZIP%20Codes%20Violation%20Hotspots.png)

4. **Presentation**:
   - Final presentation: [`CIS4400 Group 2 Presentation.pptx`](Presentation/CIS4400%20Group%202%20Presentation.pptx)

---

## **8. PowerPoint Presentation**

The PowerPoint presentation provides a summary of the project's findings, visualizations, and actionable insights. It includes:
1. **Key Findings**: Trends and correlations between Yelp ratings and health violations.
2. **Visualization Snapshots**: Key insights from Tableau dashboards.
3. **Recommendations**: Suggestions for restaurant owners, health inspectors, and policymakers.

---


