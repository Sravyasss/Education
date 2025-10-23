# EDUCATION PROJECT

> The purpose of this project is to compare the relationship between the average ACT score and the socioeconomic factors of EdGap data set. This mainly investigates whether school performance, as measured by average ACT score is predicted by socioeconomic factors and school personnel expenditures. The analysis examines data from 7,986 schools across the United States, examining how poverty concentration, unemployment, adult education, family structure and school spending relate to student achievement.

---

## Project Overview

This project analyzes predictors of school achievement using data from 7,986 US schools. Using regression modeling and statistical analysis, the study determines whether socioeconomic factors and school personnel expenditures significantly predict student achievement as measured by average ACT scores. This project integrates three data sets to provide a comprehensive examination of the factors affecting educational outcomes and to address long-standing questions in education policy about resource allocation versus systemic inequality.

1. Do community socioeconomic factors predict school performance?
2. How does school spending, including total and federal-funded salary expenditure, relate to achievement?
3. Which socioeconomic factor is the most influential predictor?
4. Do charter schools and traditional public schools show different relationships between predictors and performance?
5. How much of the variation in ACT scores can be explained by combining socioeconomic and expenditure variables?

- **Objective:** To determine the primary predictors of school achievement and the relative importance of school expenditure versus socioeconomic factors in explaining achievement variation.
- **Domain:** Education
- **Key Techniques:** Exploratory Data Analysis (EDA), Correlation Analysis, Univariate Linear Regression, 
Multiple Regression Modeling, Regression Analysis, Standardization and Model Comparison, Interaction Terms and  Stratification

---

## Project Structure


├── Education/ 
    ├── data/                 # Raw and processed data
        ├──EdGap_data.xlsx    
        ├──ccd_sch_029_1617_w_1a_11212017.csv      
        ├──School expenditures.csv
        ├──education_clean.csv
    ├── code/                 # Jupyter notebooks and Python scripts
        ├──Education.ipynb 
        ├──.ipynb_checkpoints
    ├── reports/              # Generated reports and visualizations
    ├── requirements.txt      # Dependencies
    └── README.md             # Project documentation

---

## Data

- **Source:** 

1. EdGap_data.xlsx is downloaded from github link.

https://github.com/brian-fischer/DATA-5100/blob/main/EdGap_data.xlsx 
 The main origin is from "https://www.edgap.org/#5/37.718/-95.998"

2. ccd_sch_029_1617_w_1a_11212017.csv is loaded from dropbox. 

dropbox.com/scl/fi/fkafjk8902sq8ptxh94r2/ccd_sch_029_1617_w_1a_11212017.csv?rlkey=gucrdz5f6e38bezz2y3yalxbw&dl=0 
The main sources is from "https://nces.ed.gov/ccd/pubschuniv.asp"

3. school expenditure data from the Civil Rights Data Collection (CRDC)

https://ocrdata.ed.gov/data

- **Description:** 

1.The EdGap dataset contains 7986 observations and 7 columns representing socioeconomic indicators with size 436.9+ KB. 
2.The School Information dataset contains 102182 rows with 8 columns including school identifiers, state, district, and with a size of 50.7+ MB.
3.The School Expenditures dataset contains 17604 records and 27 columns with detailed financial information, including total personnel salary expenditures both with and without federal funding 20.1+ MB.

- **License:** https://catalog.data.gov/dataset/civil-rights-data-collection-crdc, https://opendefinition.org/licenses/cc-by/

---

## Analysis

Step 1: Data loading and integration
Load and merge the EdGAP, CCD and CRDC datasets using pandas to create a unified dataset of 7,986 schools with 14 key variables. Handle missing values through listwise deletion and document data quality.

Step 2: Exploratory data analysis and correlation analysis
Compute summary statistics and correlation matrices to explore relationships between predictors and ACT scores. Use regression plots and residual diagnostics to visualize trends and examine linearity and variance patterns.

Step 3: Multiple regression modeling and model comparison
Fit three OLS regression models (baseline, standardized, and interaction) and compare them with root mean square error, and Meam absolute error to find the best fit model. Identify important predictors that affect school performance.

Step 4: Regression and estimate validation
Evaluate the residuals for normality, homoscedasticity and linearity. Identify and analyze outliers to ensure model validity and understand cases that deviate significantly from predicted performance.

Step 5: Stratified analysis and results
Conduct stratified analyzes by charter status using pairwise plots to explore individual predictor effects. Summarize the findings on the relative impact of socioeconomic and expenditure factors and discuss the implications for education policy.

---

## Results

Strong correlations were observed between average household income, parental education, and average ACT scores, confirming that socioeconomic status plays an important role in predicting academic achievement. When comparing school spending to employee salaries with achievement, the relationship was weaker than expected indicating that higher salary spending alone does not guarantee better student outcomes. Non-federal versus federal funding differences were tested and results showed that non-federal funding had a slightly stronger relationship with ACT performance, but not enough to eliminate socioeconomic effects. Regression analysis revealed that socioeconomic variables particularly income and parental education explained most of the variance in performance, with expenditure variables adding limited additional predictive power.

## Authors

Sravya sri Murala - (https://github.com/Sravyasss)

---

## License

This project is licensed under the MIT License - see the [LICENSE] file for details.
https://opendefinition.org/licenses/cc-by/

---

## Acknowledgements

Tools/libraries used: pandas, numpy, scikit-learn, statsmodels, Matplotlib, Seaborn, Jupyter, Patsy.

Tutorials or papers referenced: Canvas lectures, https://www.act.org/content/dam/act/unsecured/documents/R2405-Equity-in-Education-2024-05.pdf, https://www.proquest.com/openview/bff78e66da4b3523be3393b7602550a9/1?pq-origsite=gscholar&cbl=18750&diss=y

Inspiration: Dr. Brian Fischer
