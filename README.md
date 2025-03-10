# 🚗 Car Insurance Claims - Process Mining & Anomaly Detection

## Overview  
This repository contains a **Jupyter Notebook** that explores an event log dataset for **car insurance claims**. The dataset is designed for **process mining**, enabling analysis of bottlenecks, automation opportunities, conformance issues, reworks, and potential fraud detection.  

The primary focus of my analysis is **anomaly detection** across different attributes of the claims process.  

---

## Dataset Description  
The dataset represents the standard **car insurance claims process**, which follows this workflow:  

### **Standard Process Flow:**  
> **First Notification of Loss (FNOL)** → **Assign Claim** → **Claim Decision** → **Set Reserve** → **Payment Sent** → **Close Claim**  

### **Attributes:**  
- `case ID` → Unique identifier for each claim  
- `activity name` → Stage in the claims process  
- `timestamp` → Time of event occurrence  
- `claimant name` → Name of the person filing the claim  
- `agent name` → Agent handling the claim  
- `adjuster name` → Adjuster responsible for assessing the claim  
- `claim amount` → Amount requested in the claim  
- `claimant age` → Age of the claimant  
- `type of policy` → Insurance policy type (e.g., Collision, Comprehensive, Liability)  
- `car make` → Manufacturer of the insured vehicle  
- `car model` → Model of the insured vehicle  
- `car year` → Year of manufacture of the insured vehicle  
- `date and time of the accident` → When the accident occurred  
- `type of accident` → Nature of the accident (e.g., Rear-end, Side-impact, Head-on)  
- `user type` → Whether the claim was processed by a human or an automated system (RPA)  

---

## Notebook Structure  

### **1️⃣ Data Cleaning**  
- Handling missing values  
- Formatting timestamps and sorting events  
- Removing duplicates and inconsistencies  

### **2️⃣ Exploratory Data Analysis (EDA)**  
- Understanding the distribution of claims  
- Identifying trends and seasonality  
- Visualizing claim amounts and processing times  
- Analyzing the lifecycle of claims  

### **3️⃣ Anomaly Detection**  
- **Statistical Methods:** Z-Score, IQR  
- **Clustering:** K-Means, DBSCAN  
- **Machine Learning:** One-Class SVM  
- **Deep Learning:** Autoencoders  
- **Process Flow Analysis:** Checking if events follow the correct sequence  

#### **Scenarios Considered for Anomalies:**  
- **Unusual claim amounts** _(depends on car year & accident type)_  
- **Duplicate or multiple claims by the same claimant**  
- **Delays between process stages**  
- **Unusual age patterns among claimants**  
- **Adjusters with abnormal damage assessments**  
- **Events that do not follow the expected process flow**  

### **Evaluation of Results**  
Identifying common anomalies across methods  
Comparing detection accuracy and effectiveness  
Visualizing flagged cases  

---

## How to Use This Repository  

### **Requirements**  
Install dependencies using:  
```bash
pip install pandas numpy scikit-learn tensorflow matplotlib seaborn
