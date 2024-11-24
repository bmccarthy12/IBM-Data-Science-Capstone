# IBM Data Science Capstone Project: SpaceX Falcon 9 Landing Success Prediction

The **IBM Data Science Capstone Project** is the culminating experience in the IBM Data Science Professional Certificate. This project integrates knowledge of data analysis, machine learning, and visualization tools to predict the success of Falcon 9 first-stage landings for SpaceX. By accurately predicting landing outcomes, this project provides insights into launch costs and reusable rocket technologies.

---

## Project Objectives
1. **Predict Landing Success**: Determine if the Falcon 9 first stage will land successfully using machine learning classification models.
2. **Analyze Factors of Success**: Explore how variables like payload mass, orbit type, and launch site affect landing outcomes.
3. **Cost Implications**: Understand how reusable rockets impact overall space travel affordability.
4. **Model Comparison**: Evaluate various machine learning models to identify the most effective predictive approach.

---

## Methodology

### 1. **Data Collection**
- **SpaceX API**: Extracted rocket launch data using REST API calls.
  - Data included launch site, payload mass, orbit type, and success status.
  - Normalized JSON responses into structured Pandas DataFrames.
- **Web Scraping**: Used Python’s `BeautifulSoup` to scrape additional Falcon 9 launch records from Wikipedia.
  - Parsed HTML tables into Pandas DataFrames for integration with API data.

### 2. **Data Wrangling**
- Cleaned and formatted the data to handle missing values.
- Encoded categorical variables using One-Hot Encoding for machine learning compatibility.
- Combined API and web-scraped data into a unified dataset with 121 launches and relevant features.

### 3. **Exploratory Data Analysis (EDA)**
- Analyzed patterns and relationships between features using **Pandas**, **Matplotlib**, and **Seaborn**.
- Key insights:
  - **Launch Success Over Time**: Success rates improved over years.
  - **Payload Mass**: Higher payload masses correlated with specific orbits and success rates.
  - **Launch Sites**: Sites near the equator and coastlines showed higher success rates.

### 4. **Interactive Visual Analytics**
- **Folium Maps**: Visualized launch site locations, success rates, and proximity to geographic markers like cities and coastlines.
- **Plotly Dash App**: Created an interactive dashboard with:
  - Dropdowns and sliders for user input.
  - Pie charts of success rates by launch site.
  - Scatter plots of payload mass vs. mission outcomes.

### 5. **Machine Learning**
- Prepared data for modeling:
  - Standardized numeric features using `StandardScaler`.
  - Split data into training and test sets.
- Tested models using **GridSearchCV** for hyperparameter tuning:
  - **Logistic Regression**
  - **Support Vector Machine (SVM)**
  - **Decision Tree Classifier**
  - **K-Nearest Neighbors (KNN)**
- Results:
  - Decision Tree Classifier achieved the highest accuracy (94.4%).
  - All models performed comparably on test data, with Decision Tree slightly outperforming others.

---

## Key Insights
- **Launch Site**: KSC LC-39A had the highest success rate, particularly for payloads under 5,500 kg.
- **Orbits**: Orbits such as ES-L1, GEO, and HEO demonstrated a 100% success rate.
- **Geography**: Launch sites near the equator benefit from Earth's rotational speed, reducing fuel costs.
- **Success Trends**: Launch success has consistently improved over time.

---

## Skills and Tools Demonstrated
- **Data Collection**: API usage, web scraping with `BeautifulSoup`.
- **Data Wrangling**: Handling missing data, encoding categorical features.
- **Data Visualization**: Interactive maps with **Folium**, dashboards with **Plotly Dash**.
- **SQL Integration**: Loaded and queried data in Db2 for structured analysis.
- **Machine Learning**: Developed predictive models using Scikit-learn.
- **Evaluation Metrics**: Analyzed confusion matrices, accuracy, and F1 scores.

---

## Conclusion
The project successfully predicted Falcon 9 landing outcomes, highlighting critical factors that influence success rates. These insights contribute to understanding reusable rocket technologies, optimizing costs, and assisting companies in competing with SpaceX.

## Recommendations for Further Research
- Utilize larger datasets for more robust predictive analytics.
- Test advanced models like XGBoost for improved accuracy.
- Conduct principal component analysis (PCA) to identify key predictive features.
