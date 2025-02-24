# **K-Nearest Neighbors (KNN) Algorithm Implementation for Student Depression Prediction**  

## **Introduction**  
Depression is a critical mental health concern among students, often influenced by **academic stress, financial burden, peer pressure, and lifestyle habits**. Early detection of students at risk can help in providing **counseling, support systems, and preventive measures**.  

This project focuses on **implementing the K-Nearest Neighbors (KNN) algorithm**, a popular supervised **machine learning classification technique**, to predict whether a student is likely to suffer from **depression (Yes/No)** based on multiple behavioral, psychological, and demographic attributes.  

### **🔹 What is K-Nearest Neighbors (KNN)?**  
KNN is a **non-parametric, instance-based learning algorithm** used for classification and regression tasks. It classifies new data points by identifying **K nearest neighbors** in the training dataset, using a **distance-based approach** (e.g., Euclidean distance). The majority class among these neighbors determines the classification.  

---

## **Dataset Overview**  
The **Student Depression Dataset** is a structured survey dataset containing **demographic, lifestyle, behavioral, and health-related attributes** that influence mental well-being. The target variable, **Depression Status**, is a **binary classification** (Yes/No).  
this dataset is taken from kaggle and here is the link-https://www.kaggle.com/code/gustavors/depression-dataset-prediction
### **🔹 Features in the Dataset:**  
| **Feature**          | **Description** |
|---------------------|------------------|
| **ID** | Unique identifier for students (not used in modeling) |
| **Age** | Age of the student |
| **Gender** | Gender of the student (Male/Female) |
| **Smoking** | Whether the student smokes (Yes/No) |
| **Alcohol Consumption** | Frequency of alcohol consumption |
| **Financial Stress** | Level of financial stress experienced |
| **Peer Pressure** | Influence of peer pressure |
| **Anxiety** | Whether the student has anxiety issues |
| **Fatigue** | Experience of fatigue or tiredness |
| **Chronic Disease** | Presence of any chronic diseases |
| **Wheezing** | Experience of wheezing or breathing difficulty |
| **Coughing** | Frequent coughing occurrences |
| **Shortness of Breath** | Difficulty in breathing |
| **Chest Pain** | Experience of chest pain |
| **Depression Status** | **Target Variable (Yes = Depressed, No = Not Depressed)** |

- **Total Rows:** **309 students**  
- **Total Features:** **15 (14 predictors + 1 target variable)**  

---

## **Step-by-Step Implementation of KNN Algorithm**  

### **1️⃣ Data Loading & Preprocessing**  
- **Reading the dataset** and inspecting its structure.  
- **Checking for missing values** and handling them by replacing them with the most frequent values (mode).  
- **Dropping the ‘ID’ column**, as it does not contribute to prediction.  
- **Encoding categorical variables** (like Gender, Smoking, Anxiety, etc.) into numerical form using **Label Encoding** for model compatibility.  

---

### **2️⃣ Splitting Data into Features & Target Variable**  
- **Defining the feature matrix (X)**, which includes all predictor variables.  
- **Defining the target variable (y)**, which contains the depression status (Yes/No).  

---

### **3️⃣ Splitting Data into Training & Testing Sets**  
- **Dividing the dataset** into **70% training data and 30% testing data** using stratified sampling to ensure an even distribution of classes.  

---

### **4️⃣ Feature Scaling Using Standardization**  
- Since KNN is **distance-based**, different feature scales can negatively impact the model.  
- **StandardScaler** is applied to ensure all features have equal weight in distance computation.  

---

### **5️⃣ Training the KNN Model**  
- **Initializing the KNN classifier** with **k=7**, meaning it considers the 7 nearest neighbors for classification.  
- **Training the model** using the preprocessed training data.  

---

### **6️⃣ Making Predictions on Test Data**  
- The trained KNN model is used to **predict depression status** on the **test dataset**.  

---

### **7️⃣ Evaluating Model Performance**  

#### **Confusion Matrix Analysis**  
- A **confusion matrix** is generated to visualize the number of **correct and incorrect predictions** made by the model.  
- The confusion matrix provides insights into **true positives, false positives, true negatives, and false negatives**.  

#### **Accuracy Score & Classification Report**  
- The **accuracy score** is computed to evaluate the overall performance of the model.  
- A **classification report** is generated, providing **precision, recall, and F1-score** for both depressed and non-depressed students.  

---

## **Conclusion**  
This project successfully implements **KNN classification** to predict student depression status based on **behavioral, psychological, and demographic factors**.  

