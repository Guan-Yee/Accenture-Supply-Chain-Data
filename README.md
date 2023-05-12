# Accenture-Supply-Chain-Resilience-Data-Challenge


The original datasets are found on Kaggle. However, these datasets have limited access. Nonetheless, the datasets are obtained from the data folder in this repository https://github.com/JNADatathon2022/Datathon.

## Motivation
Late Deliveries cause reputation damage and loss of potential revenue for both the logistics companies and the cilents. Hence, this project seeks to investigate the underlying factors that cause the delivery to be delayed and provide preemptive actions for the stakeholders to reduce future instances of late deliveries.
## Methodology
1. Preprocessing the datasets by performing the necessary encoding on the respective variables.
2. Create 2 datasets Stratified and Adasyn to address the imbalanced nature of the dataset.
3. Perform the splitting into training and testing datasets.
4. Perform Mutual Information, Chi square test on the categorical variables.
5. Perform Mutual Information and the correlation test on the numerical variables.
6. Remove varaibles with low Mutual information and Chi square test.
7. Train them with Random forest, XGBoost and LGBM classifier.

## Evaluation Criterions
* Confusion matrix is used to evaluation the performance on the test dataset
* The ROC score is used to show the overall performance of the classifier as well.
* Shaply plot for each model will be shown as well

## Dataset Description
Transactional historical data of the company supply chain inbound/outbound shipments
#### **orders.csv**
| Column Name | Description |
| --- | --- |
| `order_id`(string) | unique identifier of transactional order from port inbound to final destination. Primary key of data set. |
| `origin_port`(string) | location of port where order imports arrives. |
| `3pl`(string) | Third-party logistic company id used for distribution, warehousing, and fulfillment services. |
| `customs_procedure`(string) | Type of procedure to be used in the imports legal process |
| `logistic_hub`(string) | city name of company logistic hub address. Intermediate step between origin_port and customer |
| `customer`(string) | city name of customer destination address |
| `product_id`(string) | unique identifier of final product |
| `units`(integer) | order size quantity |
| `late_order`(boolean) | target variable, if 1 the order_id have been tagged as a late delivery, 0 is on-time |

#### **product_attributes.csv**
Master data of product unit weight
| Column Name | Description |
| --- | --- |
| `product_id`(string) | unique identifier of final product |
| `weight`(integer) | product weight per 1 unit in grams |
| `material_handling`(integer) | Classification id for product safety risk and risk of damage e.g. fragile, toxic, flammable. |

#### **cities_data.csv**
Geographic coordinates of cities involve in the supply chain.
Including distance between pair of cities
| Column Name | Description |
| --- | --- |
| `city_from_name`(string) | City of location starting point |
| `city_to_name`(string) | City of destination location |
| `city_from_coord`(tuple) | Coordinates in (latitude, longitude) of city_from |
| `city_to_coord`(tuple) | Coordinates in (latitude, longitude) of city_to |
| `distance`(float) | kilometers between the pair cities |




