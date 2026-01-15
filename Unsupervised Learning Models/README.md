# Unsupervised Learning Models
The *Unsupervised_[seeds_dataset].ipynb* Colab Notebook consists of Unsupervised Learning Models like K-Means Clustering with two dimensions and with higher dimensions, and Principal Component Analysis (PCA) along with K-Means Clustering.

## Dataset
The dataset used is the "seeds" dataset [https://archive.ics.uci.edu/dataset/236/seeds] from the UCI Machine Learning Repository. It has 7 features and 210 instances of real data type. The data provided is clean and does not have any missing values. The dataset can be used for the tasks of classification and cluster analysis.

The examined group comprised kernels belonging to three different varieties of wheat: Kama, Rosa and Canadian, 70 elements each, randomly selected for the experiment. High quality visualization of the internal kernel structure was detected using a soft X-ray technique. The images were recorded on 13x18 cm X-ray KODAK plates. Studies were conducted using combine harvested wheat grain originating from experimental fields, explored at the Institute of Agrophysics of the Polish Academy of Sciences in Lublin.

## Data Pre-Processing
The *"seeds_dataset.txt"* is in text format, which is separated by any spaces between the values using the Pandas library functions. A DataFrame is created and column names are added to it.

Scatter plots are drawn for every feature against each other, except for "class" which is used to differentiate between the three categories of wheat.

## Models
The value of *k* is set equal to three as there are three classes. For the first model, only two features- "compactness" and "asymmetry" are fit into the model. Scatter plots are drawn for the original DataFrame and the K-Means Clusters that are mapped to the given clusters.

The second model fits all the features except "class", and scatter plots are again drawn for "asymmetry" vs "compactness" where the K-Means Clusters are mapped to the clusters in the original dataset.

The third model uses data transformed by Principal Component Analysis (PCA) to reduce dimensions from seven to two- "pca1" and "pca2". Scatter plots are drawn for the newly transformed data for the given classes and the K-Means Clusters that are mapped to those classes.

## Conclusion
The first model with two features shows very different clusters as compared to the clusters of the given dataset. The second model's clusters are more similar to the original data points as the model uses all seven dimensions instead of just two. But, the clusters of the second model are quite ambigous and difficult to understand. The clusters of the third model are very similar to the 'Truth classes' and are easy to interpret, although they are predicted incorrectly in the areas where the data points in different clusters overlap.
