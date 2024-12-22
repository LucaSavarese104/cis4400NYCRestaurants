# **cis4400NYCRestaurants**

---

## **Table of Contents**
1. [Business Problem](https://github.com/LucaSavarese104/cis4400NYCRestaurants?tab=readme-ov-file#1-business-problem)
2. [Business Impact](https://github.com/LucaSavarese104/cis4400NYCRestaurants?tab=readme-ov-file#2-business-impact)
3. [Business Personas](https://github.com/LucaSavarese104/cis4400NYCRestaurants?tab=readme-ov-file#3-business-personas)
4. [Data Sources and Methods](https://github.com/LucaSavarese104/cis4400NYCRestaurants?tab=readme-ov-file#4-data-sources-and-methods)
5. [Data Tools](https://github.com/LucaSavarese104/cis4400NYCRestaurants?tab=readme-ov-file#5-data-tools)
6. [Interface](https://github.com/LucaSavarese104/cis4400NYCRestaurants?tab=readme-ov-file#6-interface)
7. [Supporting Files](https://github.com/LucaSavarese104/cis4400NYCRestaurants?tab=readme-ov-file#7-supporting-files)
8. [PowerPoint Presentation](https://github.com/LucaSavarese104/cis4400NYCRestaurants?tab=readme-ov-file#8-powerpoint-presentation)
9. [Conclusion and Insights](https://github.com/LucaSavarese104/cis4400NYCRestaurants?tab=readme-ov-file#9-conclusion-and-insights)



## **1. Business Problem**

### Description
This project analyzes NYC restaurant health violations and their correlation with Yelp ratings. The primary objective is to uncover borough-level trends and provide actionable insights to improve compliance, customer satisfaction, and health outcomes.

### Key Objectives
- Investigate correlations between health violations and Yelp ratings.
- Provide borough-specific insights into compliance and public health trends.
- Offer actionable recommendations for restaurant owners, health inspectors, and policymakers.



## **2. Business Impact**

### Benefits
- **Restaurant Owners**: Identify compliance gaps to improve customer satisfaction.
- **Health Inspectors**: Detect boroughs and ZIP codes with recurring violations.
- **Policymakers**: Leverage insights to develop borough-level public health policies.

### **Risks**
- **Data Challenges**:
  - Missing or inconsistent attributes in inspection and Yelp datasets.
  - Duplicate records and format mismatches during integration.
- **Scalability**:
  - Processing and analyzing large datasets without optimized storage or compute resources.
- **API Rate Limits**:
  - Yelp Fusion API restrictions could limit data retrieval for restaurants across all boroughs.
- **Integration Complexity**:
  - Aligning inspection records with Yelp data requires fuzzy matching techniques, which may not be 100% accurate.

### **Costs**
- **Tools**:
  - **Microsoft Azure**: For cloud-based data storage and processing.
  - **Tableau**: For creating interactive dashboards and visualizations.
- **Development**:
  - Time and resources required for data cleaning, ETL processes, and API integration.
- **API Costs**:
  - Limited API calls with Yelp Fusion API (300–500 calls per account tier) may require workarounds like caching.




## **3. Business Personas**

### Key Stakeholders
- **Restaurant Owners**: Utilize insights to address compliance issues.
- **Health Inspectors**: Focus inspections based on borough-specific trends.
- **Policymakers**: Use data to refine public health regulations.

### System Users
- **Data Engineers**: Build ETL pipelines.
- **Data Analysts**: Analyze and visualize trends.
- **Visualization Experts**: Create dashboards for stakeholder insights.


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
  - Data transformation and upload: [`Transform_Open_Restaurant_Data_Group_2.ipynb`](Scripts/Transform_Open_Restaurant_Data_Group_2.ipynb)
  - Yelp API integration: [`Yelp_API_scraping_and_upload.ipynb`](Scripts/Yelp_API_scraping_and_upload.ipynb)
- **Visualization**: Tableau dashboards created from processed data.



## **5. Data Tools**

### Tools Used
- **Storage**:
  - MongoDB for raw data storage.
  - Microsoft Azure for structured data storage.
- **Processing**:
  - Python with libraries like Pandas and NumPy for data cleaning.
- **Visualization**:
  - Tableau for creating interactive dashboards.



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



## **7. Supporting Files**

1. **Model & Architecture**:
   - [Information Architecture](Model%20&%20Architecture/information_architecture.png)
   - [Data Architecture](Model%20&%20Architecture/Data%20Architecture.png)
   - [Dimensional Model](Model%20&%20Architecture/Dimensional%20Model%20Restaurant%20Analysis.png)

2. **Scripts**:
   - [`cleaning_and_merging_borough.ipynb`](Scripts/cleaning_and_merging_borough.ipynb)
   - [`Transform_Open_Restaurant_Data_Group_2.ipynb`](Scripts/Transform_Open_Restaurant_Data_Group_2.ipynb)
   - [`Yelp_API_scraping_and_upload.ipynb`](Scripts/Yelp_API_scraping_and_upload.ipynb)

3. **Presentation**:
   - Final presentation: [`CIS4400 Group 2 Presentation.pptx`](Presentation/CIS4400%20Group%202%20Presentation.pptx)



## **8. PowerPoint Presentation**

The PowerPoint presentation provides a summary of the project's findings, visualizations, and actionable insights. It includes:
1. **Key Findings**: Trends and correlations between Yelp ratings and health violations.
2. **Visualization Snapshots**: Key insights from Tableau dashboards.
3. **Recommendations**: Suggestions for restaurant owners, health inspectors, and policymakers.



## **9. Conclusion and Insights**

### **Conclusion**
This project provided a look into the correlation between health inspection violations and Yelp ratings for restaurants across NYC boroughs. By analyzing borough-specific trends and critical violations, we gained a deeper understanding of the impact of public health compliance on customer satisfaction and restaurant reputation. The integration of NYC Open Data and Yelp API data allowed us to create actionable recommendations for stakeholders, including restaurant owners, health inspectors, and policymakers.

---

### **Insights**
1. **Correlation Between Violations and Ratings**:
   - Restaurants with higher counts of critical violations tend to have lower Yelp ratings, highlighting the strong influence of public health compliance on customer perceptions.

2. **Borough-Specific Trends**:
   - **Manhattan and Brooklyn** show the highest density of critical violations, indicating the need for targeted health inspection efforts.
   - **Bronx** and **Staten Island** generally have fewer violations but also lower average Yelp ratings, suggesting opportunities for improvement in customer satisfaction.

3. **ZIP Code Hotspots**:
   - ZIP codes in lower Manhattan and northern Brooklyn consistently display high counts of critical violations, making them priority areas for health compliance efforts.

4. **Yelp Rating Categories**:
   - Restaurants rated 4.0 or above on Yelp tend to have significantly fewer critical violations compared to lower-rated establishments.

5. **Temporal Trends**:
   - Monthly trends reveal seasonal variations in health violations, with some boroughs experiencing spikes in violations during specific times of the year. This information can be used to schedule targeted inspections.

---

### **Recommendations**
1. **For Restaurant Owners**:
   - Focus on reducing critical violations to improve Yelp ratings and attract more customers.
   - Leverage borough-specific trends to prioritize compliance efforts.

2. **For Health Inspectors**:
   - Target inspections in high-risk ZIP codes, particularly in Manhattan and Brooklyn.
   - Use seasonal data to anticipate periods of increased violations and allocate resources accordingly.

3. **For Policymakers**:
   - Develop borough-specific public health initiatives to address recurring issues in high-violation areas.
   - Create incentive programs for restaurants to maintain health compliance and improve customer satisfaction.

---
