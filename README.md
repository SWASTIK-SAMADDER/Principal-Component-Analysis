# Principal-Component-Analysis

### **PRINCIPAL COMPONENT ANALYSIS: A DIMENSIONALITY REDUCTION CASE STUDY ON BREAST CANCER DATASET** 💡
***
### **Introduction**
This report details a **Principal Component Analysis (PCA)** and **Logistic Regression** study performed using Python on the **Breast Cancer Wisconsin (Diagnostic) dataset**. The project aimed to demonstrate how PCA can be used as a **dimensionality reduction** technique to simplify complex, high-dimensional data while retaining crucial information.By reducing the number of features, the analysis facilitates faster computation and helps to visualize data that would otherwise be difficult to interpret.

***
### **Key Features** ✨
* **Dimensionality Reduction**: Using PCA to reduce **30 numerical features** into a smaller set of principal components.
* **Data Visualization**: Creating a Scree plot to identify the optimal number of principal components.
* **Quality of Representation**: Using a heatmap and biplot to visualize how well the original variables are represented by the principal components.
* **Machine Learning Integration**: Applying Logistic Regression on the reduced feature set to evaluate its effectiveness in a classification task.

***
### **Project Goals** 🎯
* To perform **dimensionality reduction** on a dataset with a large number of features to improve model efficiency and interpretability.
* To identify and prioritize the most important features contributing to the variance in the dataset.
* To build a classification model using the reduced feature set and evaluate its performance.

***
### **Data Description** 📄
The **Breast Cancer Wisconsin (Diagnostic) dataset** is a widely used multivariate dataset for machine learning classification tasks.
* **Instances**: It contains **569 instances**, each representing a patient with a breast tumor.
* **Objective**: The goal is to classify the tumor as either **malignant (cancerous)** or **benign (non-cancerous)**.
* **Features**: The dataset includes **30 numerical features** that describe various characteristics of the cell nuclei.These features are derived from **10 core measurements**, with each measurement reported as a mean, standard error, and "worst" (largest) value. The 10 core characteristics are:
    * Radius 
    * Texture 
    * Perimeter
    * Area 
    * Smoothness 
    * Compactness
    * Concavity 
    * Concave points 
    * Symmetry
    * Fractal dimension
This dataset is ideal for learning and applying machine learning algorithms like PCA due to its clear class separation and well-defined features.

***
### **Methodology** ⚙️
The analysis followed a structured approach using Python libraries such as pandas, numpy, scikit-learn, and matplotlib.
1.  **Data Standardization**: The first step was to standardize the data using **`StandardScaler`** to ensure all features contribute equally to the PCA.
2.  **PCA Implementation**: Principal Component Analysis was performed on the standardized data to transform the 30 features into principal components.
3.  **Scree Plot Analysis**: A Scree plot was generated to visualize the proportion of variance explained by each principal component. This helps in deciding how many components to retain.
4.  **Quality of Representation**: Heatmaps and biplots were used to visualize the "Quality of Representation" (Cos2) of the original variables on the principal components.
5.  **Model Training**: The top principal components were used to train a **Logistic Regression** model.
6.  **Model Evaluation**: The model's performance was evaluated using metrics such as **accuracy score** and a **classification report**.

***
### **Key Findings & Insights** 📈
* **Dimensionality Reduction Success**: PCA was able to effectively reduce the dimensionality of the dataset.The PCA summary table and Scree plot show that the first two principal components (**PC1** and **PC2**) explain a significant portion of the total variance, specifically **44.27%** and **18.97%**, respectively. This means that a large part of the data's structure can be captured in a two-dimensional space.The first five principal components alone capture approximately **84.73%** of the total variance.
* **Variable Contributions**: The bar plots of variable contributions reveal which original features are most influential in each principal component.
    * **PC1** is heavily influenced by "mean concave points," "mean concavity," and "worst concave points." These variables are highly indicative of tumor malignancy.
    * **PC2** is largely driven by features like "mean fractal dimension error," "worst fractal dimension," and "fractal dimension error".
* **Model Performance**: The Logistic Regression model, trained on a reduced feature set, achieved a high **accuracy score of 0.9766**. The classification report further demonstrated strong precision, recall, and f1-scores for both malignant and benign classes.This indicates that even with fewer features, the model can effectively and accurately classify the tumors.

***
### **Conclusion** ✅
This project successfully demonstrates the application of **Principal Component Analysis** for dimensionality reduction on the Breast Cancer Wisconsin dataset. By transforming the 30 original features into a smaller set of principal components, we were able to create a highly accurate **Logistic Regression** model while gaining valuable insights into the most influential variables.The findings confirm that PCA is a powerful tool for simplifying data complexity, enhancing model efficiency, and maintaining high predictive performance in machine learning classification tasks.
