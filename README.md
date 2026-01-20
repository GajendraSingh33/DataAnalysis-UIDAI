## UIDAI Aadhaar Data Analysis:

This project explores **Aadhaar enrolment** and **update behaviour** (demographic and biometric) using UIDAI-provided datasets.  
The goal is to uncover **regional patterns**, **time-based trends**, **age-wise behaviour**, and **anomalies** that can guide **policy and system improvements**.

All analysis is implemented in **Python** using **Jupyter notebooks**.



## Problem Statement:

UIDAI faces three key operational challenges:

Uneven Aadhaar enrolment and update coverage across states and districts

Ageing demographic and biometric data due to migration, lifecycle changes, and wear

Hidden authentication risk, especially in regions with low update activity

These issues are not always visible through raw counts or operational dashboards.


## Solution Approach:

Instead of treating enrolments and updates as isolated transactions, this project analyzes them as signals of population behavior, data ageing, and service stress.
The solution framework includes:

Regional aggregation at state and district levels

Age-group analysis to capture lifecycle-driven updates

Time-series trends to identify campaign-driven spikes

Anomaly detection (IQR method) to flag under- and over-performing regions

Summary dashboards for decision-level visibility


## Key Analyses:

Regional patterns: Top states and districts.

Gender & age insights: Lifecycle-driven updates.

Time trends: Campaign-based vs baseline activity.

Anomaly detection: IQR-based over/under-performing regions.

Summary dashboards: High-level monitoring metrics.


## 1. Aadhaar Enrolment Analysis

### 1.1 Regional Pattern Analysis (State-wise)
<img width="944" height="700" alt="image" src="https://github.com/user-attachments/assets/ed888e38-861a-4ab8-9b11-ddb618fa6849" />


### 1.2 Trend Analysis (Time-based)
<img width="940" height="700" alt="image" src="https://github.com/user-attachments/assets/93e19e33-8e5c-4655-8fa2-cf180feaa84b" />


### 1.3 Comparison Analysis (Age Group Distribution)
<img width="944" height="702" alt="image" src="https://github.com/user-attachments/assets/feb0f709-7855-43bb-a009-4d5981b76869" />


### 1.4 Summary Metrics
<img width="1785" height="1187" alt="image" src="https://github.com/user-attachments/assets/53a37ac2-bfa8-4411-84ce-48c5e121eb6f" />



- Enrolment demand is **uneven across states**, with a few large states dominating volume.
- Enrolment shows **clear temporal surges** rather than a flat trend.
- The **18+ age group** contributes the largest share of enrolments.
- Anomaly analysis highlights states that may be **overloaded** or **under-utilising** enrolment infrastructure.

---

## 2. Aadhaar Biometric Updates Analysis

### 2.1 State-wise Biometric Update Intensity (Top 10 States)
<img width="1184" height="881" alt="image" src="https://github.com/user-attachments/assets/ac861ac3-15dc-46e6-889b-6dfd77c2e31a" />


### 2.2 Time Trend of Biometric Updates
<img width="1484" height="731" alt="image" src="https://github.com/user-attachments/assets/b3180c8b-fe9c-4489-a950-89bc8a951f39" />


### 2.3 Age-group Distribution of Biometric Updates
<img width="884" height="709" alt="image" src="https://github.com/user-attachments/assets/5771270f-a0da-4912-9d4b-881091f3d70a" />


### 2.4 District-level Hotspots for Biometric Updates
<img width="1483" height="881" alt="image" src="https://github.com/user-attachments/assets/b61f25dc-4cac-48d2-bc05-cc7af56f2c5a" />


### 2.5 Anomaly Detection
<img width="1184" height="731" alt="image" src="https://github.com/user-attachments/assets/74c51041-c84d-4bc5-8cda-0df6cc43af9a" />


- Demographic updates are **concentrated in a few states and districts**, often urban or high-migration hubs.
- Update volume over time shows **peaks**, likely linked to campaigns, scheme linkages, or migration cycles.
- Adults (18+) drive the majority of demographic updates, while child updates are smaller but policy-critical.
- Outlier states (very high or low) point to potential **infrastructure stress** or **access/awareness gaps**.

---

## 3. Aadhaar Demographic Updates Analysis

### 3.1 State-wise Demographic Update Intensity
<img width="1184" height="881" alt="image" src="https://github.com/user-attachments/assets/cf6068b4-5188-4dc4-a629-2b4890f76b18" />


### 3.2 Time Trend of Demographic Updates
<img width="1484" height="731" alt="image" src="https://github.com/user-attachments/assets/2105c962-af24-4db5-aae7-0923d63f4f65" />


### 3.3 Age-group Distribution of Demographic
<img width="883" height="709" alt="image" src="https://github.com/user-attachments/assets/78a153dd-937d-4c3e-8ddb-8481aac39da5" />


### 3.4 District-level Hotspots for Demographic Updates
<img width="1484" height="881" alt="image" src="https://github.com/user-attachments/assets/25b5e6f2-93eb-47aa-860d-8150d1f14166" />


### 3.5 Anomaly Detection (State-wise Demographic Updates using IQR)
<img width="1184" height="731" alt="image" src="https://github.com/user-attachments/assets/70469cce-c53d-4098-8fbd-29f8756cc309" />


### 3.6 Summary Dashboard
<img width="1485" height="887" alt="image" src="https://github.com/user-attachments/assets/8f647e35-6837-4123-b093-13e7553f6f18" />


- Biometric updates are **highly uneven**, with some states/districts doing heavy refresh and others very little.
- Time trends show **campaign-like surges** in biometric updates rather than steady refresh.
- Adults again dominate, but child/teen biometrics are crucial for long-term authentication reliability.
- Anomalies help flag states where **biometric quality risk** or **under-reporting** may be present.

---

## How to Run the Notebooks Locally

1. **Clone the repository**

```bash
git clone https://github.com/GajendraSingh33/DataAnalysis-UIDAI.git
cd DataAnalysis-UIDAI
```

2. **Create and activate a virtual environment (optional but recommended)**

```bash
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```

3. **Install dependencies**

```bash
pip install pandas numpy matplotlib jupyter
```

4. **Launch Jupyter**

```bash
jupyter notebook
```

5. Open each notebook in `CODE/` and run all cells (`Kernel → Restart & Run All`) to generate all charts and dashboards.


---

## Intended Audience and Use

- **UIDAI / Government stakeholders**: for planning enrolment and update capacity, and monitoring performance.
- **Data analysts / students**: to learn how to perform EDA, anomaly detection, and dashboard-style summarisation on real public infrastructure data.
- **Researchers / policy teams**: to prototype models of enrolment and update demand and test policy ideas.

The notebooks are written to be **readable and modular**, so you can extend them with your own models (forecasting, clustering, risk scoring) as needed.

