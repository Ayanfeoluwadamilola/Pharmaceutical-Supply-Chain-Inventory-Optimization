# Pharmaceutical Supply Chain Inventory Optimization

PharmaCorp faces significant challenges in optimizing its pharmaceutical supply chain inventory. This project delves into the issues surrounding overproduction, shelf-life management, market trends, and competitive pressures, and aims to provide a data-driven solution to address these problems.

## Table of Contents
1. [Business Problem](#business-problem)
2. [Rationale for the Project](#rationale-for-the-project)
3. [Project Aim](#project-aim)
4. [Tech Stack](#tech-stack)
5. [Project Scope](#project-scope)
6. [Data Collection](#data-collection)
7. [Data Preprocessing](#data-preprocessing)
8. [Exploratory Data Analysis](#exploratory-data-analysis)
9. [Feature Engineering](#feature-engineering)
10. [Model Building & Evaluation](#model-building--evaluation)

## Business Problem

PharmaCorp faces significant challenges in the following areas:

- **Overproduction and Losses**: Overproduction leads to financial losses from unsold products due to expired shelf life.
- **Shelf Life Management**: Managing varying shelf lives of pharmaceutical products is complex, leading to further losses if products expire.
- **Market Trends**: Aligning production schedules with constantly evolving market trends and demand patterns is difficult.
- **Competitive Pressures**: Efficient inventory management is crucial to maintaining a competitive edge.

## Rationale for the Project

Supply Chain Inventory Optimization is critical in the pharmaceutical industry due to the perishable nature of drugs and the need for quality control. The main reasons for initiating this project include:

- **Cost Reduction**: Minimize financial losses due to overproduction and inventory mismanagement.
- **Enhanced Profitability**: Reducing waste and improving resource allocation will increase profitability.
- **Competitive Advantage**: Efficient inventory management helps PharmaCorp respond better to market trends and customer demand.
- **Sustainability**: Reducing waste supports PharmaCorp's sustainability efforts.

## Project Aim

The project aims to achieve the following objectives:

1. **Reduce Overproduction**: Implement an inventory optimization strategy to reduce overproduction.
2. **Minimize Losses**: Align inventory with shelf life to minimize financial losses from expired products.
3. **Improve Forecasting**: Enhance forecasting accuracy by incorporating market trends and historical sales data.

## Tech Stack

The project used the following tools and technologies:

- **Python**: Programming language.
- **Libraries**: 
  - Pandas
  - Matplotlib
  - Seaborn
  - Scikit-learn (Sklearn)

## Project Scope

The project followed these steps:

1. **Data Collection**: Gathered product information, sales data, market data, and compliance data.
2. **Data Processing**: Cleaned and preprocessed data, handling missing values and outliers.
3. **Exploratory Data Analysis**: Explored patterns in the data.
4. **Feature Engineering**: Created relevant features for modeling.
5. **Model Building**: Developed machine learning models to forecast sales.
6. **Model Evaluation**: Assessed model performance using various metrics.
7. **Inventory Optimization**: Determined optimal inventory levels.

## Data Collection

The dataset provided by PharmaCorp contained the following fields:

- **Product ID**: Unique identifier for each product.
- **Shelf Life (Days)**: Shelf life of the product in days.
- **Sales 2021 & 2022**: Total sales for the respective years.
- **Market Trend Factor**: Measures factors like market trends and competitor actions.
- **Compliance Status**: Indicates whether a product is compliant or non-compliant with regulations.

## Data Preprocessing

The dataset was processed using the Pandas library, which was used to:

- Handle missing values.
- Get an overview of the data's structure and quality.

## Exploratory Data Analysis

### Univariate Analysis:
- Distribution of categorical variables showed that:
  - Product Category B had the highest frequency.
  - Warehouse A was the most common storage location.
  - More compliant products were found than non-compliant ones.

### Multivariate Analysis:
- Boxplots were used to compare sales across years, but no significant pattern was found with categorical variables.
- Scatterplots showed no significant correlation between market trends, sales, and shelf life.

### Key Insights:
- Product Category C had the highest shelf life range, while Category B had the least.
- Category A showed the highest safety stock range, suggesting careful attention to avoid overproduction or underproduction.

## Feature Engineering

The following features were created:

- A projected sales column for 2023 using market trend factors and sales data from 2022.
- A **Decision Tree Regressor** was trained to forecast sales for 2023, achieving a Mean Absolute Percentage Error (MAPE) of 1.1%.
- Another Decision Tree Regressor was used to project optimal inventory levels, yielding a MAPE of 1.5%.

## Model Building & Evaluation

### Model Building:
- The **Decision Tree Regressor** was chosen to forecast future sales and optimize inventory levels.

### Model Evaluation:
- The models were evaluated using Mean Absolute Percentage Error (MAPE), with the sales forecast model achieving 1.1% error and the inventory optimization model achieving 1.5% error.
