# Patient Recovery Monitoring System

## AI-Driven Post-Discharge Health Monitoring

The Patient Recovery Monitoring System is an intelligent post-discharge monitoring solution designed to detect early signs of patient deterioration at home using wearable sensor data and machine learning.

It continuously analyzes vital parameters and recovery patterns to generate automated risk alerts and recovery trend insights, enabling proactive clinical intervention.

---

##  Problem Statement

After hospital discharge, patients are typically monitored through periodic follow-ups rather than continuous observation. This creates several risks:

- Undetected health deterioration  
- Delayed complication identification  
- Increased hospital readmissions  
- Lack of real-time recovery tracking  

Consumer wearables track vitals but do not analyze recovery deviation patterns or provide predictive clinical alerts.

---

##  Solution Overview

The system provides:

- Continuous monitoring of:
  - Heart Rate  
  - SpO₂ (Oxygen Saturation)  
  - Body Temperature  
  - Activity Levels  

- Time-series aggregation of sensor data  
- Feature engineering based on physiological deviation  
- Unsupervised anomaly detection  
- Recovery trajectory modeling  
- Risk visualization for medical review  

The system automatically identifies abnormal recovery behavior and flags potential risks.

---

##  Technical Workflow

###  Data Processing
- Timestamp normalization and chronological sorting  
- minutes based time-series resampling  
- Aggregation of statistical features (mean, standard deviation, minimum)

###  Feature Engineering
- Heart rate deviation from baseline  
- SpO₂ drop detection (< 95%)  
- Activity trend calculation (minute-to-minute change)  
- Physiological variability metrics  

###  Anomaly Detection
- Using Isolation Forest (Unsupervised ML,best suited for anomaly detection)  
- Considers 5% contamination assumption for rare abnormal patterns  
- Binary risk labeling:
  - `0` → Normal  
  - `1` → Risk  

###  Recovery Trend Modeling
- Linear Regression applied to activity progression  
- Positive slope → Improving recovery  
- Negative slope → Possible deterioration  

---

##  System Outputs

- Vital sign trend graphs  
- Activity recovery curve  
- Anomaly detection timeline  
- Risk alerts for early intervention
  <img width="1022" height="484" alt="image" src="https://github.com/user-attachments/assets/d566f53d-0cbf-47cd-8a12-215b8d522321" />
  <img width="1015" height="471" alt="image" src="https://github.com/user-attachments/assets/282db407-a77d-4bdd-9266-2903e4688a31" />


---

##  Tech Stack

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib  

---

##  Impact

This system aims to:

- Reduce preventable hospital readmissions  
- Enable early detection of recovery deviation  
- Improve patient safety at home  
- Support data-driven clinical decisions  

---


