# Purpose of the Project:
1. Recognize how AI and ML improve marketing departments through effective market segmentation.
2. Conduct preliminary data analysis, refine data, and create dynamic data visualizations with Plotly.
3. Grasp the fundamentals of autoencoders.
4. Develop and train models using autoencoders for reducing dimensions with Keras and TensorFlow 2.0.
5. Comprehend the workings of the K-means clustering technique.
6. Determine the ideal number of clusters by employing the elbow method.
7. Utilize the K-means clustering approach in scikit-learn to segment the market.
8. Learn about Principal Component Analysis (PCA) and its purpose.
9. Implement PCA to achieve dimensionality reduction. <br />

Marketing is a critical component of any business to ensure its growth and sustainability. Marketing helps build the company's brand, grow revenue, and drive customer engagement. There are four functions of any marketing department:
1. Educating the value proposition of products and services to customers and potential customers.
2. Ensuring customer engagement and understanding customer needs.
3. Driving traffic to products and services.
4. Empowering business growth by contacting new and potential customers. <br />

In our project, we will try to understand our customers by grouping them into distinctive groups and then correspodingly tailor a targetted marketing ad campaign, instead of sending out the same ad campaign to everybody. As a result, the fundamental learning outcome of this project is to perform market segmentation using AI/ML techniques (unsupervised ML techniques in particular).

We have extensive data about customers for the duration of 2.5 years. We will divide the customers into at least 3 distinct groups and create a targeted ad marketing campaign for each of them. 

In our data, we have features like order number, number of items ordered, price of item, amount of sales for the item, date of order, and the shipping status of the order. We also have the quarter, month, and year in which the order was placed, the product category, and the name and phone number of the customer placing the order. Moreover, we have the address to which the product needs to be shipped, the city, state, postal code, country, and territory in which the person resides, the size of the order, and finally the contact person's first and last name.

# Understanding K-Means Clustering:
K-Means is an unsupervised machine learning algorithm, which works by trying to group some data points together as per similar attribute values by estimating the Euclidian distance between them.

The following is the K-Means algorithm:
1. Choose a number of clusters, call it K.
2. Select K points on random that would serve as the centroids of each cluster.
3. Assign each data point to the nearest centroid to create K number of clusters.
4. Calculate the new centroid of each cluster.
5. Re-assign each data point to the new closest centroid.
6. Repeat from step 4 until the clusters and centroids are determined. <br />

How can we calculate the optimal number of clusters? We can use the elbow method to solve this.

First, we calculate the Within Cluster Sum of Squares(WCSS), which is the sum of the squares of the distances of each data point and its corresponding centroid of each cluster (based on cluster number K(i)).

As the number of clusters increases, WCSS decreases, since the distance between data points and the centroids of the clusters decreases.

In the elbow method, we choose the optimal number of K by plotting the WCSS with respect to the number of clusters K. As K increases, WCSS decreases. We choose K when the change in WCSS becomes almost linear at the specific breakpoint, mimicking an elbow point.

The elbow method is a heuristic method of interpretation within cluster analysis.

# Understanding Principle Component Analysis (PCA) for Dimensionality Reduction:
PCA is an unsupervised ML algorithm which performs dimensionality reduction while ensuring that the original information/essence of the data remains unchanged.

PCA tries to find a new set of features, called components, which are composites of the given input features that are uncorrelated.

PCA moves the data into a 2D component space from the original 3D data space. PCA reduces the amount of features by representing the data with less memory and computational requirements. It also ensures data confidentiality by encoding secret customer information.

# Understanding Autoencoders:
Autoencoders are a kind of Artificial Neural Networks that perform data encoding or representation learning. They utilize the same input data for both input and output. So, we will feed our data into an autoencoder to encode our data and use that encoded data to train our K Means and principal components to perform clustering.

Autoencoders work by including a bottleneck that forces the network to generate an encoded/compressed version of the original input. If correlations exist between input data, autoencoders perform well. If the input data is independent, autoencoders do not work.

If the weights of the encoder and decoder are equal, we call these tied weights.
