#  BUILDING MODEL TO PREDICT HUMAN DEVELOPMENT INDEX AND CLUSTER LIVABLE PROVINCES AND CITIES IN VIETNAM

## Overview

This repository contains a dataset collected by our team from the website of the General Statistics Office of Vietnam [1]. The dataset includes various socio-economic attributes of provinces and cities in Vietnam from the year 2002 to 2022.

## Dataset Description

The dataset encompasses a wide range of features, covering aspects such as healthcare, social security, economy, labor, employment, and per capita income. Each entry in the dataset represents a province or city and includes data for multiple years. 

The dataset consists of 26 attributes (3 text attributes and 20 numerical attributes) and 7955 data entries. Our team collected the data from the website of the General Statistics Office [1], which is a government agency specialized in collecting statistics in Vietnam. The data on the website is considered credible and reliable. Additionally, the data is publicly available and permissible for use.

We used a downloading tool to retrieve the Excel files provided on the website. After filtering, our team managed to collect 55 files corresponding to 55 attributes. Subsequently, we analyzed and synthesized the general structure of the data, then merged the 55 attributes to form a complete dataset in CSV format. 

## Data Collection and Preparation

We collected the data in compliance with the terms and conditions outlined by the General Statistics Office, which allows the use of statistical data for research purposes with proper source citation. The collected data was standardized and aggregated from various sources, ensuring consistency and coherence.

- **Preprocessing for Analysis and Exploration:**
  - Normalizing Unicode for province and region names.
  - Standardizing numerical types for values in attributes.
  - Subattributes can be separated into individual attributes for analysis.
  - Upon exploration, the team discovered that missing data was denoted by "..". These instances were normalized to NaN.
  - Attributes with data inconsistent with the team's initial direction were removed due to incomplete data across the years, within the data range from 2018 to 2022. Attributes with excessively missing data for multiple years were also removed, as they did not yield significant insights. Ultimately, the team obtained a subset dataset comprising 44 attributes.

- **Preprocessing for Training Data:**
  - The team augmented the data by obtaining corresponding data for the target variable (HDI) for each year (2018, 2019, 2020, 2021).
  - Subattributes were separated into individual attributes.
  - Attributes with missing data for more than 2 years were removed.
  - The team selected 0, mean, and mode as the imputation values for missing data, as most quantitative variables had a normal distribution.
  - Finally, the team obtained a dataset for model training comprising 36 attributes and 1 target variable (HDI). This dataset was divided into training and testing sets for model training and evaluation. During model training, the team chose 0, mean, and mode as the imputation methods for missing data, as most quantitative variables had a normal distribution.


## Analysis and Modeling

We performed exploratory data analysis and applied machine learning techniques to analyze the dataset. Specifically, we used regression and clustering algorithms to model and evaluate different aspects of the data.

## Tools and Libraries Used

We utilized popular data processing and visualization libraries such as Pandas, Numpy, Tableau, and Seaborn to manipulate and visualize the dataset effectively.

## Evaluation Metrics

To assess the quality of life and build predictive models for provinces and cities in Vietnam, we proposed four evaluation metrics tailored to the characteristics of the dataset.

| Mô hình           | R2 (Điền giá trị 0) | MSE (Điền giá trị 0) | MAE (Điền giá trị 0) | R2 (Điền giá trị trung bình) | MSE (Điền giá trị trung bình) | MAE (Điền giá trị trung bình) | R2 (Điền giá trị xuất hiện nhiều nhất) | MSE (Điền giá trị xuất hiện nhiều nhất) | MAE (Điền giá trị xuất hiện nhiều nhất) |
|------------------|---------------------|----------------------|----------------------|-------------------------------|--------------------------------|---------------------------------|--------------------------------------|---------------------------------------|---------------------------------------|
| Linear           | 0.7891              | 0.0004               | 0.0161               | 0.7979                        | 0.000                          | 0.0158                          | 0.7979                               | 0.0004                                | 0.0158                                |
| SGD              | 0.3841              | 0.0012               | 0.0272               | 0.6865                        | 0.000                          | 0.0212                          | 0.6865                               | 0.0006                                | 0.0212                                |
| Random Forest    | 0.8881              | 0.0002               | 0.0118               | 0.8843                        | 0.000                          | 0.0123                          | 0.8843                               | 0.0002                                | 0.0123                                |
| GradientBoosting | 0.9132              | 0.0002               | 0.0102               | 0.9143                        | 0.000                          | 0.0103                          | 0.9143                               | 0.0002                                | 0.0103                                |
| LGBM             | 0.9155              | 0.0002               | 0.0102               | 0.9164                        | 0.000                          | 0.0101                          | 0.9164                               | 0.0002                                | 0.0101                                |
| CatBoost         | 0.9359              | 0.0001               | 0.0093               | 0.9337                        | 0.000                          | 0.0096                          | 0.9337                               | 0.0001                                | 0.0096                                |

## Purpose

This dataset and project were developed as part of the Data Visualization course. It serves as a learning resource for students interested in data analysis and machine learning.

## Usage

Feel free to explore, analyze, and utilize the dataset for research and educational purposes. If you use the dataset in your work, please ensure to cite the source properly.

## Contact

For any inquiries or feedback regarding the dataset, you can contact us at [].
Authors:
- Nhi Ngoc-Yen Nguyen: [21521231@gm.uit.edu.vn](mailto:21521231@gm.uit.edu.vn)
- Vo Hoang An: [21520555@gm.uit.edu.vn](mailto:21520555@gm.uit.edu.vn)
- Tran Thai Hoa: [21522082@gm.uit.edu.vn](mailto:21522082@gm.uit.edu.vn)


[1] - [General Statistics Office of Vietnam Website](https://www.gso.gov.vn/)

---

**Disclaimer:** This dataset is provided for educational and research purposes only. While we have taken efforts to ensure the accuracy and reliability of the data, we cannot guarantee its completeness or correctness. Users are encouraged to verify the data independently before making any decisions based on it.