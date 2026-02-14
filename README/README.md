#  Machine Learning and Pattern Recognition  
## Lab 5 – Face Detection and K-Means Clustering

---

##  Overview

This lab demonstrates the application of distance-based learning techniques in computer vision. The task involves detecting faces using Haar Cascade, extracting HSV color features, performing K-Means clustering, and classifying a template image into one of the learned clusters.

---

##  Aim

- Detect faces in a group image using OpenCV Haar Cascade.
- Extract Hue and Saturation features from detected faces.
- Apply K-Means clustering (k=2).
- Classify a template image using learned cluster centroids.
- Visualize clustering results.

---

##  Methodology

### 1️) Face Detection  
The Haar Cascade classifier was used to detect faces in `Plaksha_Faculty.jpg`.  
Grayscale conversion and parameter tuning (scaleFactor, minNeighbors, minSize) improved detection accuracy.

### 2️) Feature Extraction  
Detected face regions were converted from BGR to HSV color space.  
For each face, the following features were extracted:

- Mean Hue  
- Mean Saturation  

Each face was represented as a 2D feature vector:


### 3️) K-Means Clustering  
K-Means clustering (k = 2) grouped faces based on similarity in HSV feature space.  
The algorithm minimized Euclidean distance between data points and cluster centroids.

### 4️) Template Classification  
The template image `Dr_Shashi_Tharoor.jpg` was processed similarly:
- Face detection
- HSV conversion
- Mean Hue & Saturation extraction

The trained K-Means model predicted the cluster label based on minimum distance to centroids.

---

##  Results

- Faces were successfully detected in the group image.
- HSV features enabled clustering based on color similarity.
- Two clusters were formed using K-Means.
- The template image was classified into the nearest cluster.
- Visualizations confirmed cluster separation.

---

##  Visualizations

### 🔹 Face Detection Output
![Face Detection](outputs/face_detection.png)

### 🔹 K-Means Clustering Plot
![Clustering](outputs/clustering_plot.png)

### 🔹 Template Classification Result
![Template Classification](outputs/template_classification.png)

---

##  Distance Metric Used

K-Means uses **Euclidean distance**, defined as:

$d(x, y) = \sqrt{\sum_{i=1}^{n} (x_i - y_i)^2}$.

This measures straight-line distance between feature vectors in 2D space.

---

##  Bias-Variance Insight (KNN Concept)

- Small K → Low bias, High variance (overfitting)
- Large K → High bias, Low variance (underfitting)

Selecting appropriate hyperparameters ensures balanced performance.

---

##  Key Observations

- Haar Cascade requires parameter tuning for accurate detection.
- HSV color space is useful for clustering facial features.
- Consistent feature extraction is critical for correct classification.
- Distance-based learning is simple yet effective for pattern recognition.

---

##  Conclusion

This lab demonstrates how classical computer vision techniques combined with distance-based machine learning algorithms can solve practical clustering and classification problems. The experiment highlights the importance of feature engineering, clustering, and visualization in machine learning workflows.

---

##  Technologies Used

- Python  
- OpenCV  
- NumPy  
- Matplotlib  
- Scikit-learn  

---

##  Author

**Rejin Prasad**  
Machine Learning and Pattern Recognition – Spring 2026  
