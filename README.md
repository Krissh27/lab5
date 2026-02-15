# Face Clustering and Template Classification using K-Means

## Methodology

### Face Detection
- Used OpenCV's Haar Cascade classifier.
- Converted images to grayscale.
- Applied `detectMultiScale()` to locate faces.

### Feature Extraction
- Converted detected face regions from BGR to HSV color space.
- Extracted:
  - Mean Hue
  - Mean Saturation
- Created a 2D feature vector for each face.

### Clustering
- Applied K-Means clustering (`n_clusters = 2`).
- Trained model on extracted Hue-Saturation features.
- Obtained cluster centroids.

### Template Classification
- Detected face in template image.
- Extracted HSV features.
- Used `kmeans.predict()` to determine cluster membership.

---

## Visualisations

### Face Detection Output

![Face Detection](face%20detection.png)

---

### Hue-Saturation Feature Clustering

![Cluster Plot](ig.png)
- Green → Cluster 0  
- Blue → Cluster 1  
- X → Centroids  

### Template Classification Result

![Template Classification](fg.png)

The template image is plotted in the feature space and classified based on nearest centroid.

## Key Findings

- Hue and Saturation features can group faces based on color similarity.
- K-Means successfully separates faces into clusters.
- Template classification works using cluster centroids.
- However, clustering is based only on color distribution and not identity.





## Conclusion

This project demonstrates a complete machine learning workflow:
- Face detection
- Feature extraction
- Unsupervised learning (K-Means)
- Prediction and visualization





