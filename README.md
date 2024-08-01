# Zomato_Data_Analysis

Overview
This project involves analyzing Zomato data to understand various trends and preferences among customers. The analysis covers aspects such as online delivery, types of restaurants, and preferred price ranges. The project utilizes Python and its libraries, including Pandas, Numpy, Matplotlib, and Seaborn, for data analysis and visualization.

Libraries Used
Pandas: For data manipulation and analysis.
Numpy: For numerical computations.
Matplotlib: For creating static, animated, and interactive visualizations.
Seaborn: For statistical data visualization.
Key Questions Addressed
Online vs. Offline Delivery: Do a greater number of restaurants provide online delivery as opposed to offline services?
Popular Restaurant Types: Which types of restaurants are most favored by the general public?
Preferred Price Range: What price range is preferred by couples for dinner at restaurants?
Getting Started
Prerequisites
Ensure you have the following libraries installed:

Pandas
Numpy
Matplotlib
Seaborn
You can install them using pip:

bash
pip install pandas numpy matplotlib seaborn
Data
The data used for this analysis is sourced from Zomato and is saved in a CSV file named Zomato_data.csv.

Loading the Data

import pandas as pd

# Load the data
dataframe = pd.read_csv("Zomato_data.csv")
print(dataframe.head())
Data Cleaning
We cleaned the data by:

Converting the "rate" column to a float and removing the denominator.
Checking for null values and handling them appropriately.

def handleRate(value):
    value = str(value).split('/')
    value = value[0]
    return float(value)
 
dataframe['rate'] = dataframe['rate'].apply(handleRate)
print(dataframe.head())

# Check for null values
dataframe.info()
Analysis
The analysis includes:

Comparing the number of restaurants offering online delivery versus offline services.
Identifying the most popular types of restaurants.
Determining the price range preferred by couples for dinner.
Visualization
The project uses various plots like histograms, heatmaps, and box plots to visualize the data trends.

Conclusion
The analysis provides insights into customer preferences in the restaurant industry, including the preference for online delivery and popular restaurant types. It also highlights the price range that couples prefer for dining out.

Authors
Bhushan Surendra Sangle
License
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgments
Zomato for the data
Google Colab and Jupyter Notebook for providing an interactive environment for data analysis.
