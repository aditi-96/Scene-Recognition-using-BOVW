# Scene Recognition using Bag of Visual Words

- Implemented a basic bag of visual words model by training and testing to classify images belonging to a subset of the SUN dataset into 8 classes.
- Built a vocabulary of visual words by sampling local features from the training set and then clustering them with kmeans
  - Computed SIFT features on the images.
  - Used KMeans to cluster the SIFT features into desired number of clusters (size of bag of words).
  - For each image, computed the histogram by finding the number of SIFT features of that image in each cluster
  - Performed TF-IDF on the histogram to enhance the importance of discriminative features and downweigh the uninformative features that occur in a lot of images.
- Performed classification by training one-vs-all linear SVM.
- Accuracy of 0.69375 for 900 clusters