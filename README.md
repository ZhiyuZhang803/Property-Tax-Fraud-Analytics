## Property-Tax-Fraud-Analytics

Notice: For security purpose, all files are stored under master branch.

### Project Goal:

This project explores a real dataset of 1,000,000 properties in New York City (provided by offical website https://data.cityofnewyork.us/Housing-Development/Property-Valuation-and-Assessment-Data/rgy2-tti8), and builds two unsupervised machine learning models based on the basic information of properties to help government find and explore potential tax fraud.

### Project Overview:

This project broke up model building into six steps, strictly following the steps of data engineering and machine learning. The details are shown as follows:

- Data exploration: I examined the dataset through identifying each variable, calculating minimum, maximum, percentage of null values for the numeric variables & calculating the number of unique values and the most common field value for the categorical variables. After the data examination, I wrote a Data Quality Report (DQR) for the dataset.

- Data cleaning: To better prepare the data for model building, I cleaned and organized the data. The first focus was on dropping the government owned properties. I also dealt with missing values in different fields with different methods.

- Variable creation and feature selection: Before the model building, I created as many variables as possible to better capture all possible variables that can be used to build a good predictive model to detect the fraud properties in the future. To achieve this, I did basic calculation of original fields and used PCA to reduce the dimension to only 7 fields (which contain over 90% of information in the original dataset).

- Model building: I built 2 unsupervised machine learning models- z scaling model and auto-encoder model- to score the records according to its ranking. Then, the average value was calculated and properties with high average values were selected. Those properties have high probabilities conducting fraud.

- Results: After filtering top records, I explored top100 properties and gathered more information through google map, official website and reviews. After ensuring those target properties, I iterated the whole process and improved the algorithm.

### Folder Explaination:

This project is divided into 3 folders. All implementation codes can be found under folders.

(1) Data Exploration Part: (Folder)

- Practice of “Data Exploration” part listed above.
- Csv zip file is the original dataset.
- Ipynb file is the code used in this step.
- Word file is the results of this step.

(2) Data Cleaning and Create New Variables: (Folder)

- Practice of “Data Cleaning” and "Variable Creation" parts listed above.
- Csv zip file is the original dataset.
- Ipynb file is the code used in this step.
- Xlsx file is the results of this step. (Description of the variables created)

(3) Fit Models & Property Detection Report: (Folder)

- Practice of “Freature Selection”, "Model Building" and "Result" parts listed above.
- Csv zip file used in this step can be acquired from previous step. (not provide here because of the size limitation, you can get this file by executing the previous step)
- Ipynb file is the code used in this step.
- Xlsx file is the result of this step. (properties srted by average fraud score)
- Word file includes details of top 5 suspicious properties measured by our algorithms.

