I worked on data from the famous Tytanic Boat disaster.Below are steps that i undertook and my findings🔔

Data Cleaning and Preparation
1. Data Loading and Missing Value Analysis: The Titanic dataset was loaded, and a heatmap was generated to visualize missing values, revealing gaps in key features like `Age` and `Cabin`. This provided a foundation for targeted cleaning steps.

2. Age Imputation: Missing ages were filled based on the median age within each passenger class, helping retain as many records as possible while introducing reasonable age estimates.

3. Dropping Irrelevant Columns: The `Cabin` column was dropped due to a high percentage of missing data, which reduced noise. Other non-essential columns, such as `Name` and `Ticket`, were also removed to focus on relevant features.

4. Encoding Categorical Variables: Gender and embarkation location were encoded into numerical values, enabling the model to interpret these categorical attributes.

 Exploratory Data Analysis (EDA)
1. Survival Distribution: A count plot showed a higher number of passengers did not survive, establishing a baseline understanding of survival odds.

2. Survival by Gender and Class: Analysis by gender showed that women had a higher survival rate, aligning with historical evacuation practices. Additionally, passengers in 1st class had a higher survival rate compared to lower classes, indicating an influence of socio-economic status.

3. Age and Fare Distributions: Histograms revealed a broad age range among passengers, with potential survival implications for different age groups, and a skewed fare distribution, where most passengers paid lower fares, but a few paid significantly more, likely corresponding to 1st-class tickets.

4. Sibling/Spouse Presence: Analyzing the `SibSp` variable provided insight into travel companionship, potentially influencing survival decisions.

Model Fitting and Evaluation
1. Data Splitting: The data was split into training and test sets (70%/30%) to enable model evaluation.

2. Logistic Regression Model: Logistic regression was chosen for its suitability in binary classification. The model was trained on the training data to predict `Survived`.

3. Model Performance:
   - The model achieved an accuracy of 87.28% on the test data, indicating it correctly predicted the survival outcome in approximately 87% of cases.
   - Precision was high (87%) for both survival classes, meaning the model had a low false-positive rate.
   - The model demonstrated strong recall for non-survivors (93%) but slightly lower recall for survivors (78%), indicating it was slightly better at predicting non-survivors.
   - F1-scores, balancing precision and recall, averaged around 87% for both classes, showing the model’s robustness in predicting both classes fairly well.
