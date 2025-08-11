# Human Resources Data Analysis

## Table of Contents
1.  [Project Overview](#project-overview)
2.  [Dataset](#dataset)
3.  [Tools & Technologies](#tools--technologies)
4.  [Data Cleaning & Preprocessing Methodology](#data-cleaning--preprocessing-methodology)
5.  [Key Insights](#key-insights)
6.  [Setup & Usage](#setup--usage)
7.  [Project Structure](#project-structure)
8.  [Contact](#contact)

## Project Overview

This project focuses on analyzing Human Resources data to gain insights into employee demographics, hiring patterns, location, and departmental distribution. The analysis involves data cleaning, and preprocessing to prepare the dataset for further HR analytics and decision-making in Tableau.


## Dataset
-   **Source File**: `HumanResources.csv` (Downloaded from [Data world] (https://data.world/markbradbourne/rwfd-real-world-fake-data/workspace/file?filename=Human+Resources.csv))
-   **Total Records**: 37,408 initial entries (22,214 valid employee records after cleaning)
-   **Total Features**: 13 columns
-   **Key Fields**:
    *   **id**: Unique employee identifier
    *   **Demographics**: `first_name`, `last_name`, `birthdate`, `gender`, `race`
    *   **Employment Details**: `department`, `jobtitle`, `location`, `hire_date`, `termdate`
    *   **Location Information**: `location_city`, `location_state`
    *   **Employment Status**: Active employees (termdate = null) vs. Former employees (termdate populated)

## Tools & Technologies
The entire data cleaning and preparation process was conducted within a Python environment, leveraging the following tools:

-   **Data Manipulation & Cleaning**: Python 3.12
-   **Development Environment**: Jupyter Notebook
-   **Data Analysis**: Pandas for data processing and temporal analysis

![Python Logo](https://img.icons8.com/color/120/python--v1.png)![Jupyter Logo](https://img.icons8.com/?size=100&id=J0SgMWzAxqFj&format=png&color=000000) ![Pandas Logo](https://img.icons8.com/?size=100&id=xSkewUSqtErH&format=png&color=000000)

## Data Cleaning & Preprocessing Methodology
The raw dataset underwent systematic cleaning to ensure data quality and analytical readiness:

1.  **Initial Data Assessment**
    *   Loaded the dataset and performed comprehensive data profiling using `df.info()`, `df.head()`, and `df.isnull().sum()`
    *   Identified significant data quality issues: 15,194 rows (40.6%) had missing employee IDs

2.  **Handling Missing Values and Data Integrity**
    *   **Critical ID Management**: Removed 15,194 rows with missing employee IDs as these records lacked primary identifiers essential for HR analysis
    *   **Data Validation**: Verified no completely duplicate records existed in the dataset
    *   **Termination Date Handling**: Preserved 18,285 null values in `termdate` column as these represent currently active employees

3.  **Data Type Handling**
    *   **Date Conversion**: Transformed `hire_date` and `termdate` columns from object to datetime format with UTC localization
    *   **Error Handling**: Used `errors='coerce'` parameter to handle any unparseable date formats

## Screenshots
![Alt text](<Screenshot 2025-08-10 at 6.50.52 PM.png>)

![Alt text](<Screenshot 2025-07-20 at 2.22.23 PM.jpg>)

## Key Insights

### 📊 Organizational Overview
- **Total Workforce**: 22,214 employees with 3,929 terminated employees
- **Overall Retention Rate**: 85.0%
- **Departmental Diversity**: 13 distinct departments across the organization

### 🌍 Geographic Distribution & Work Arrangements
- **Headquarters Dominance**: 75.25% of employees work from headquarters
- **Remote Workforce**: 24.75% work remotely, indicating flexible work policies
- **Multi-State Presence**: Operations span across Ohio, Michigan, Pennsylvania, Indiana, and Wisconsin
- **Cleveland Concentration**: Primary hub located in Ohio

### 👥 Workforce Demographics

#### Gender Composition
- **Male Majority**: 51% male employees
- **Female Representation**: 46% female employees  
- **Inclusive Policies**: 3% non-conforming employees, demonstrating commitment to diversity

### 📈 Hiring & Employment Trends

#### Age Distribution Insights
- **Mature Workforce**: Heaviest concentration in 35-44 age range

#### Temporal Patterns
- **Steady Monthly Hiring**: Consistent hiring pattern ranging from 70-110 employees per month

### 🏢 Departmental Analysis

#### Top Departments by Size
1. **Engineering**: Largest department (~6,000 employees)

#### Department-Specific Observations
- **Engineering Dominance**: Suggests technology/manufacturing focus
- **Low Termination Rates**: Most departments show minimal terminated employees
- **Balanced Growth**: Proportional hiring across departments

### 🎯 Tenure & Retention Excellence

#### Tenure Distribution
- **Long-term Employees**: 21.7% with 20+ years tenure
- **Experienced Workforce**: 24.2% with 15-19 years tenure  

### 🔍 Strategic HR Implications

#### Strengths
- **Exceptional Retention**: 85% retention rate indicates strong employee satisfaction
- **Demographic Balance**: Good gender and racial diversity
- **Geographic Flexibility**: Successful remote work integration
- **Career Longevity**: High tenure rates suggest strong company culture

#### Areas for Consideration
- **Remote Work Expansion**: 24.75% remote rate suggests room for growth in flexible arrangements
- **Young Talent Pipeline**: Continued focus on attracting <25 age group for future leadership

## Setup & Usage
To replicate the data cleaning process on your local machine, please follow these steps:

1.  **Clone the Repository**
    ```bash
    git clone https://github.com/shrististha/HumanResourcesAnalysis.git
    cd HumanResourcesAnalysis
    ```

2.  **Set Up a Python Virtual Environment**
    ```bash
    # For macOS/Linux
    python3 -m venv venv
    source venv/bin/activate

    # For Windows
    python -m venv venv
    .\venv\Scripts\activate
    ```

3.  **Install Required Dependencies**
    ```bash
    pip install pandas jupyter
    ```

4.  **Run the Analysis Notebook**
    ```bash
    jupyter notebook HumanResources.ipynb
    ```
    Open and execute the cells in the notebook. This will process the raw `HumanResources.csv` file and generate the cleaned `HumanResourcesCleanDataset.csv` file.

5.  **Access Cleaned Data**
    The cleaned dataset will be saved as `HumanResourcesCleanDataset.csv` and is ready for further HR analytics, dashboard creation, or machine learning applications.

6. **Connect `HumanResourcesCleanDataset.csv` by opening `HumanResources_Dashboard.twbx` dashboard.**
7. The online version of this dashboard can be accessed from this [link]([https://public.tableau.com/app/profile/shristi.shrestha2022/viz/CustomerChurnAnalysisDashboard_17530394841520/OverviewDashboard](https://public.tableau.com/app/profile/shristi.shrestha2022/viz/HumanResourcesDashboard_17530387295710/HRDashboard?publish=yes&showOnboarding=true)).

## Project Structure
```
HumanResourcesAnalysis/
│
├── HumanResources.ipynb                # Jupyter Notebook with Python cleaning code
├── HumanResources.csv                  # Original raw HR dataset
├── HumanResourcesCleanDataset.csv      # Final cleaned dataset (output)
├── HumanResources_Dashboard.twbx      # Tableau Interactive Dashboard
└── README.md                          # This project documentation file
```

## Contact
*([Shristi Shrestha])* - [GitHub](https://github.com/shrististha) | [LinkedIn](https://linkedin.com/in/shristi-stha)

