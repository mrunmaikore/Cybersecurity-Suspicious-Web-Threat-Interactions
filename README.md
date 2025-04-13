🔐 Suspicious Web Traffic Detection using AWS CloudWatch Logs
This project focuses on detecting and analyzing suspicious or potentially malicious web traffic using real-world-style logs collected through AWS CloudWatch. By leveraging Python-based data analysis and machine learning tools, the project identifies anomalies in web interactions that could indicate cyber threats such as scanning, brute-force attempts, or DDoS activity.

🧠 Project Objectives
Analyze web traffic behavior patterns to identify outliers and suspicious sessions.

Engineer meaningful features to improve interpretability and anomaly detection accuracy.

Apply machine learning techniques to detect abnormal traffic using an unsupervised approach.

Visualize insights to support cybersecurity monitoring and decision-making.

📁 Dataset Overview
The dataset includes network traffic metadata captured from a web server environment, with fields such as:

bytes_in, bytes_out – Volume of incoming and outgoing data.

creation_time, end_time – Session timestamps for duration calculation.

src_ip, dst_ip, protocol, dst_port, response.code

rule_names, observation_name – Labels and metadata for suspicious activity detection.

detection_types – Types of detection methods used.

📊 Key Steps & Contributions
🔹 1. Data Preprocessing
Handled missing values and inconsistent timestamps.

Converted time-related fields to datetime format.

Filtered and cleaned data for analysis.

🔹 2. Feature Engineering
Created new metrics like duration_sec and total_traffic (bytes_in + bytes_out).

Extracted temporal features (e.g., hour of the day) for pattern analysis.

Normalized and scaled numerical features for model input.

🔹 3. Exploratory Data Analysis (EDA)
Visualized data distributions using histograms, KDEs, boxplots, and violin plots.

Performed descriptive and correlation analysis across traffic attributes.

Identified patterns in data volume, response codes, and access times.

🔹 4. Anomaly Detection
Implemented Isolation Forest, an unsupervised anomaly detection model.

Labeled traffic sessions as normal or anomalous based on model predictions.

Visualized anomalies using scatterplots and time-based charts.

🔹 5. Results Interpretation
Found clusters of anomalous sessions linked to specific response codes, IP ranges, and traffic spikes.

Analyzed high-volume, short-duration sessions which may indicate potential abuse or scanning activity.

🛠️ Tools & Technologies Used
Python (Pandas, NumPy, datetime)

Matplotlib & Seaborn for visual analytics

scikit-learn for Isolation Forest anomaly detection

Jupyter Notebook for interactive exploration

🎯 Outcome
The project successfully demonstrates how real-time traffic logs can be analyzed for anomalies using feature engineering and unsupervised ML techniques. It provides a foundational approach for developing threat detection pipelines in cloud-based infrastructures.
