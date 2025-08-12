# Principal-Component-Analysis

### **PRINCIPAL COMPONENT ANALYSIS: A DIMENSIONALITY REDUCTION CASE STUDY ON BREAST CANCER DATASET** 💡
***
### **Introduction**
[cite_start]This report details a **Principal Component Analysis (PCA)** and **Logistic Regression** study performed using Python on the **Breast Cancer Wisconsin (Diagnostic) dataset**[cite: 3, 4]. [cite_start]The project aimed to demonstrate how PCA can be used as a **dimensionality reduction** technique to simplify complex, high-dimensional data while retaining crucial information[cite: 3]. [cite_start]By reducing the number of features, the analysis facilitates faster computation and helps to visualize data that would otherwise be difficult to interpret[cite: 10].

***
### **Key Features** ✨
* [cite_start]**Dimensionality Reduction**: Using PCA to reduce **30 numerical features** into a smaller set of principal components[cite: 6].
* **Data Visualization**: Creating a Scree plot to identify the optimal number of principal components.
* [cite_start]**Quality of Representation**: Using a heatmap and biplot to visualize how well the original variables are represented by the principal components[cite: 3].
* [cite_start]**Machine Learning Integration**: Applying Logistic Regression on the reduced feature set to evaluate its effectiveness in a classification task[cite: 3].

***
### **Project Goals** 🎯
* To perform **dimensionality reduction** on a dataset with a large number of features to improve model efficiency and interpretability.
* To identify and prioritize the most important features contributing to the variance in the dataset.
* To build a classification model using the reduced feature set and evaluate its performance.

***
### **Data Description** 📄
[cite_start]The **Breast Cancer Wisconsin (Diagnostic) dataset** is a widely used multivariate dataset for machine learning classification tasks[cite: 4].
* [cite_start]**Instances**: It contains **569 instances**, each representing a patient with a breast tumor[cite: 5, 10].
* [cite_start]**Objective**: The goal is to classify the tumor as either **malignant (cancerous)** or **benign (non-cancerous)**[cite: 5].
* [cite_start]**Features**: The dataset includes **30 numerical features** that describe various characteristics of the cell nuclei[cite: 6]. [cite_start]These features are derived from **10 core measurements**, with each measurement reported as a mean, standard error, and "worst" (largest) value[cite: 7]. The 10 core characteristics are:
    * [cite_start]Radius [cite: 9]
    * [cite_start]Texture [cite: 9]
    * [cite_start]Perimeter [cite: 9]
    * [cite_start]Area [cite: 9]
    * [cite_start]Smoothness [cite: 9]
    * [cite_start]Compactness [cite: 9]
    * [cite_start]Concavity [cite: 9]
    * [cite_start]Concave points [cite: 9]
    * [cite_start]Symmetry [cite: 9]
    * [cite_start]Fractal dimension [cite: 9]
[cite_start]This dataset is ideal for learning and applying machine learning algorithms like PCA due to its clear class separation and well-defined features[cite: 10].

***
### **Methodology** ⚙️
[cite_start]The analysis followed a structured approach using Python libraries such as pandas, numpy, scikit-learn, and matplotlib[cite: 3].
1.  [cite_start]**Data Standardization**: The first step was to standardize the data using **`StandardScaler`** to ensure all features contribute equally to the PCA[cite: 3].
2.  [cite_start]**PCA Implementation**: Principal Component Analysis was performed on the standardized data to transform the 30 features into principal components[cite: 3].
3.  **Scree Plot Analysis**: A Scree plot was generated to visualize the proportion of variance explained by each principal component. This helps in deciding how many components to retain.
4.  **Quality of Representation**: Heatmaps and biplots were used to visualize the "Quality of Representation" (Cos2) of the original variables on the principal components.
5.  **Model Training**: The top principal components were used to train a **Logistic Regression** model.
6.  [cite_start]**Model Evaluation**: The model's performance was evaluated using metrics such as **accuracy score** and a **classification report**[cite: 3].

***
### **Key Findings & Insights** 📈
* **Dimensionality Reduction Success**: PCA was able to effectively reduce the dimensionality of the dataset. [cite_start]The PCA summary table and Scree plot show that the first two principal components (**PC1** and **PC2**) explain a significant portion of the total variance, specifically **44.27%** and **18.97%**, respectively[cite: 3]. This means that a large part of the data's structure can be captured in a two-dimensional space. [cite_start]The first five principal components alone capture approximately **84.73%** of the total variance[cite: 3].
* **Variable Contributions**: The bar plots of variable contributions reveal which original features are most influential in each principal component.
    * **PC1** is heavily influenced by "mean concave points," "mean concavity," and "worst concave points." [cite_start]These variables are highly indicative of tumor malignancy[cite: 3].
    * [cite_start]**PC2** is largely driven by features like "mean fractal dimension error," "worst fractal dimension," and "fractal dimension error"[cite: 3].
* [cite_start]**Model Performance**: The Logistic Regression model, trained on a reduced feature set, achieved a high **accuracy score of 0.9766**[cite: 3]. [cite_start]The classification report further demonstrated strong precision, recall, and f1-scores for both malignant and benign classes[cite: 3]. [cite_start]This indicates that even with fewer features, the model can effectively and accurately classify the tumors[cite: 3].

***
### **Conclusion** ✅
[cite_start]This project successfully demonstrates the application of **Principal Component Analysis** for dimensionality reduction on the Breast Cancer Wisconsin dataset[cite: 3]. By transforming the 30 original features into a smaller set of principal components, we were able to create a highly accurate **Logistic Regression** model while gaining valuable insights into the most influential variables. [cite_start]The findings confirm that PCA is a powerful tool for simplifying data complexity, enhancing model efficiency, and maintaining high predictive performance in machine learning classification tasks[cite: 3].
