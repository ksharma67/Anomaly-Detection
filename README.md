# Anomaly-Detection-On-Temperature-Device-Failure
A typical anomaly detection task and performing KMeans, PCA, Gaussian distribution, and Isolation Forest

1) Plotting / visualizing the 'original' dataset (hint: this is a Time Series object)

2) Performing Feature Engineering on the dataset such that new features are to be added. Specifically, you need to create a feature that will indicate the day of the week and the time of the day. Namely, there should be four (4) categories (clusters?) for the feature, name it 'dtcat' (date-time-category):
- Weekday Day
- Weekday Night
- Weekend Day
- Weekend Night
Note: Some features such as ‘dayofweek’, ‘hours’, ‘day’, etc. may remain in the dataset.
We define the duration of ‘Day’ and Night’ as follows: 
Duration of 'Day' should be defined: 7:00am - 7:00pm 
Duration of 'Night' should be defined: 7:01pm - 6:59am
Ultimately, we would like to figure out when (weekday, weekend, day, or night) the device fails!

3) Applying the K-Means algorithm to the revised dataset and determining the best value for K. Testing K in the range of [1, 20]. Plotting a graph showing the number of clusters (K) with the score of each K-Means model. 

4) After determining the best value of K, plot (scatter plot) all these K clusters by choosing 2 features from the dataset. Should the dataset has more than 2 features (which most likely will be the case), applying PCA to derive those 2 features (2 Principal Components) [pca = PCA(n_components=2), then 'fit' pca into the dataset]

All following steps were executed twice:
- for outliers_fraction = 0.01 (1%), assume that someone gave us this figure
- calculate outliers_fraction by finding the total number of outliers utilizing the IQR Method; specifically use the 1.5xIQR rule.

5) Applying the Gaussian distribution (EllipticEnvelope) algorithm, as defined in step 2. 
Listing anomalies (if any) in each category and showing them graphically.

6) Applying the Isolation Forest algorithm at each category, as defined in step 2.  
Listing anomalies (if any) in each category and showing them graphically.

