
# Iris Flower Classification

*Author*: Adarsh Mishra  
*Batch*: May A53  
*Domain*: Data Science

# Aim
This project aims to create a model that classifies iris flowers into different species based on their sepal and petal measurements.

# Libraries Used
The following libraries were utilized in this project:
- numpy
- pandas
- sklearn.cluster.KMeans
- matplotlib.pyplot
- seaborn

# Dataset
The iris dataset was loaded using seaborn's load_dataset function. It includes details about iris flowers such as sepal length, sepal width, petal length, petal width, and species.

# Data Exploration and Preprocessing
- The dataset was imported as a DataFrame using seaborn's load_dataset function, and its first 5 rows were displayed with df.head().
- The 'species' column was encoded to numerical values using pd.factorize (df['species']).
- Descriptive statistics were presented using df.describe().
- Missing values were checked using df.isna().sum().

# Data Visualization
- 3D scatter plots were created to illustrate the relationships between species, petal length, and petal width, as well as species, sepal length, and sepal width, using matplotlib.pyplot and mpl_toolkits.mplot3d.Axes3D.
- 2D scatter plots were generated to visualize the relationship between species and sepal length, as well as species and sepal width, using seaborn.scatterplot.
- The cluster labels were predicted for each data point in the dataset using km.fit_predict(df[['petal_length','petal_width']]).

# Accuracy Measure
The confusion matrix was calculated to evaluate the accuracy of the KMeans clustering.
The confusion matrix was plotted using matplotlib.pyplot.imshow and plt.text to visualize the true and predicted labels.

# Applying Elbow Technique for K-Means Clustering
- The Elbow Technique was used to determine the optimal number of clusters (K) by examining the sum of squared errors (SSE).
- The KMeans algorithm was initialized with various K values (1 to 10), and SSE was calculated for each.
- A plot of K values against SSE was generated using matplotlib.pyplot to pinpoint the "elbow point," indicating the optimal number of clusters.

# Applying K-Means Algorithm
- The KMeans algorithm was applied to the dataset using the optimal number of clusters (K=3), as determined by the Elbow Technique.