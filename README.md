# Restaurant Recommendation System
## Overview
The Restaurant Recommendation System is a Python-based project that leverages machine learning techniques and data visualization libraries to offer location-based restaurant recommendations. The project uses the Yelp Academic Dataset, focusing specifically on the business.json file, which contains business data including location data, categories, review counts, and ratings.
 
 <img width="1017" alt="recom" src="https://github.com/catplotlib/REstaurantRecommendation/assets/61319491/3ba05ae9-edc9-49eb-a942-237283a0dfcd">

## Libraries Used
- Pandas
- Numpy
- Geopandas
- Matplotlib
- Seaborn
- Plotly
- Sklearn
- Data Loading

The Yelp Academic Dataset is loaded into a pandas dataframe from a json file named 'yelp_academic_dataset_business.json'. This dataset contains information about various businesses including restaurants.

### Data Preprocessing
The dataset is filtered to contain only restaurants by checking the 'categories' column for the presence of the string 'Restaurants'.

### Exploratory Data Analysis (EDA)
Several visualizations are created using matplotlib, seaborn and plotly to understand the distribution of review counts and ratings among the restaurants. The restaurants are also plotted on a map for a geographical understanding.

### Feature Engineering
Restaurants in the state of Pennsylvania are singled out for further analysis. The latitude and longitude data of these restaurants are used as features for clustering.

### Model Training
K-Means clustering is performed on the geographical coordinates of the restaurants. The optimal number of clusters is determined using the Elbow Method. The quality of the clustering is assessed using silhouette analysis.

### Recommendation System
A location-based recommendation function is defined which predicts the cluster for any given coordinates and returns the top restaurants in that cluster. This function can be used to recommend restaurants based on a user's current location or a location of their choice.

### Visualization of Recommendations
The recommended restaurants, along with their respective clusters, are visualized on a map for easy understanding. The location passed to the recommendation function is also plotted to give a spatial context to the recommendations.

## Running the Code
To run the code, you would need to have all the libraries mentioned above installed. You can then clone the repository and run the Python notebook 'RestaurantRecommendationSystem.ipynb'.

## Future Work
The current system can be expanded to include more factors in the recommendation such as user preferences, restaurant cuisine, etc. The model can also be updated to use more advanced clustering techniques for better performance.
