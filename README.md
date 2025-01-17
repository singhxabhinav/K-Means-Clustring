
<h2>K-Means Clustring Algorithm code from scratch : </h2>

**K-Means Clustering** is an Unsupervised Learning algorithm, which groups the unlabeled dataset into different clusters.

(It will help if you think of items as points in an n-dimensional space).  The algorithm will categorize the items into k groups or clusters of similarity. To calculate that similarity, we will use the euclidean distance as measurement.

The algorithm works as follows:  

1. First, we initialize k points, called means or cluster centroids, randomly.
2. We categorize each item to its closest mean and we update the mean’s coordinates, which are the averages of the items categorized in that cluster so far.
3. We repeat the process for a given number of iterations and at the end, we have our clusters.

The “points” mentioned above are called means because they are the mean values of the items categorized in them. To initialize these means, we have a lot of options. An intuitive method is to initialize the means at random items in the data set. Another method is to initialize the means at random values between the boundaries of the data set (if for a feature x the items have values in [0,3], we will initialize the means with values for x at [0,3]).

The above algorithm in pseudocode is as follows:  

Initialize k means with random values

  --> For a given number of iterations:
    
       --> Iterate through items:
    
        --> Find the mean closest to the item by calculating 
        the euclidean distance of the item with each of the means
        
        --> Assign item to mean
        
        --> Update mean by shifting it to the average of the items in that cluster
