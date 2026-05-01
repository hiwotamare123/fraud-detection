Financial Transaction Intelligence: Anomaly Detection System


Kujenga Final Assignment

📌 Project Overview

This project represents a strategic pivot from reactive Middleware management to proactive Data Intelligence. Developed as the final assignment for the Kujenga program, this repository demonstrates an end-to-end machine learning pipeline designed to identify fraudulent banking activities and brute-force login attempts using unsupervised learning.
The core mission was to transform raw transactional logs into "Banking Intelligence," providing actionable insights into system vulnerabilities and high-risk user behavior.

🛠️ Tech Stack

•	Language: Python
•	Libraries: Pandas, NumPy, Scikit-Learn (Isolation Forest), Matplotlib/Seaborn
•	Environment: Jupyter Notebook / Kaggle
•	Model Type: Unsupervised Anomaly Detection

🧪 Data Engineering & Feature Logic

To move beyond basic monitoring, I engineered specific features that simulate real-world banking risk parameters:
•	Login Risk Factor: A weighted heuristic calculated as $(LoginAttempts \times 0.7) + (NormalizedAmount \times 0.3)$. This prioritizes access friction over transaction size, reflecting modern security logic.
•	Temporal Features: Extraction of Hour from timestamps to identify "Off-Hours" anomalies, which are typical indicators of automated bot attacks.
•	Data Scaling: Implementation of StandardScaler to ensure that high-magnitude features like AccountBalance do not overshadow critical low-magnitude features like LoginAttempts.

🤖 The Model: Isolation Forest

Given that fraudulent transactions are rare and often lack labels in real-time environments, I utilized the Isolation Forest algorithm.
•	Logic: Instead of profiling "normal" behavior, the model identifies "anomalies" by isolating observations that are few and different.
•	Contamination: Set to 1% to reflect a realistic threshold for high-sensitivity banking alerts.

📈 Key Insights & Results

The model successfully isolated high-risk clusters with the following findings:
•	The "When" Factor: Anomalous transactions showed a 744.91% increase in the Hour factor compared to normal transactions, proving that timing is the strongest indicator of risk.
•	Brute Force Detection: Transactions flagged as anomalies had significantly higher login attempts, validating the "Login Risk Factor" engineered during preprocessing.
•	Minimal False Positives: The distribution of the anomaly scores suggests a high degree of confidence in the outliers detected.

📂 Project Structure

Plaintext
├── data/                  # Placeholder for dataset (Kaggle-sourced)
├── notebooks/             # Final_Project_Kujenga.ipynb
├── README.md              # Project documentation


________________________________________
Author: [Hiwot Amare /GitHub Handle]
Context: Final Assignment for the Kujenga Data Program.

