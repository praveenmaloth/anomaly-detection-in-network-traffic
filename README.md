Anomaly Detection in Network Traffic

This project implements a **Hybrid Machine Learning Model** for detecting **anomalies in network traffic** using both **LSTM (Long Short-Term Memory)** and **Isolation Forest** algorithms.  
It aims to identify **malicious, suspicious, or unusual patterns** in network activity that may indicate intrusions, attacks, or abnormal behavior.

---

Project Overview

Modern networks generate vast amounts of data, making it challenging to detect abnormal behavior manually.  
This project leverages the **power of deep learning (LSTM)** to understand time-dependent traffic behavior and **unsupervised anomaly detection (Isolation Forest)** to identify outliers effectively.

Hybrid Approach
- **LSTM Model (Supervised)** → Learns temporal dependencies from labeled network data.
- **Isolation Forest (Unsupervised)** → Detects anomalous points without labels.
- **Combined Decision** → Improves robustness by merging predictions from both models.

---

Features

Detects network anomalies in real-time or batch mode  
Combines deep learning and unsupervised learning techniques  
Scalable for large datasets (tested on CIC-IDS-2017 / BCCC-CIC-IDS-2017)  
Visualizes anomalies and detection performance  
Built and trained in Google Colab for easy reproducibility  

---


 Tech Stack

| Category | Tools / Frameworks |
|-----------|--------------------|
| Language | Python |
| Deep Learning | TensorFlow / Keras |
| ML Algorithm | Isolation Forest (Scikit-Learn) |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Environment | Google Colab |

---

 Dataset

- **Dataset Used:** [BCCC-CIC-IDS-2017 / CICIDS2017](https://www.unb.ca/cic/datasets/ids-2017.html)  
- **Description:** A real-world network traffic dataset containing normal and attack flows (e.g., DoS, DDoS, PortScan, Botnet).  
- **Features:** 80+ extracted traffic features (Flow duration, Packet size, Protocol type, etc.)

---

 Model Workflow

1. **Data Preprocessing**
   - Handle missing values
   - Feature selection & normalization
   - Label encoding

2. **LSTM Model Training**
   - Trained on sequential time-series network features
   - Captures temporal relationships in traffic patterns

3. **Isolation Forest**
   - Identifies anomalies/outliers from feature space
   - Works without labeled data

4. **Hybrid Detection**
   - Combines LSTM and Isolation Forest outputs
   - Improves anomaly classification accuracy

5. **Evaluation**
   - Accuracy, Precision, Recall, F1-Score
   - ROC-AUC and Confusion Matrix plots

---

 Results

| Metric | Score |
|--------|--------|
| Accuracy | 98.5% |
| Precision | 97.9% |
| Recall | 98.2% |
| F1-Score | 98.0% |

*(Results may vary depending on dataset preprocessing and parameters.)*

---

 Installation & Setup

```bash
# Clone the repository
git clone https://github.com/praveenmaloth/anomaly-detection-in-network-traffic.git
cd anomaly-detection-in-network-traffic

# Install dependencies
pip install -r requirements.txt

