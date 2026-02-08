# GuardianGaze: Anomaly-Based Network Intrusion Detection System

GuardianGaze is an anomaly-based NIDS that combines percolation-theory inspired thresholding with machine learning classifiers to reduce the amount of traffic that requires deep analysis. The goal is to keep detection accurate while lowering computational burden on high‑throughput networks.

**What’s In This Repo**
- `guitest5.py`: Prototype GUI with packet capture and a `PercolationAnomalyDetector` class.
- `PTL_models.ipynb`, `PTL_models_final.ipynb`: Model exploration and training notebooks.
- `*_model.pkl` / `*_model.joblib`: Trained model artifacts (RF, Extra Trees, Naive Bayes, XGBoost, ensemble).
- `subset_50000.csv`: Sample dataset slice for quick experiments.

**Method Overview**
1. Capture packets with `scapy`.
2. Apply percolation-style thresholds to focus on higher‑risk traffic.
3. Run ML models on the filtered packets to classify anomalies.

**Percolation Thresholding**
The percolation threshold logic is implemented in `guitest5.py` as `PercolationAnomalyDetector`. The report describes adaptive thresholds based on historical statistics and moving averages to keep the system responsive to changing traffic patterns.

**Results (From Project Report)**
See `RESULTS.md` for the summarized tables of detection time and accuracy comparisons (percolation vs. no percolation) and overall evaluation metrics.

**Quick Demo (GUI Prototype)**
```
python guitest5.py
```
Notes:
- Packet capture uses `scapy` and requires appropriate permissions.
- The interface name in `guitest5.py` is currently set to `\\Device\\NPF_Loopback` (Windows). Update this for your system.
- The GUI is a prototype and may require minor wiring to connect the percolation thresholds directly into the live capture pipeline.

**Dataset**
The report uses NF‑UQ‑NIDS‑v2. The notebooks refer to a local path; you may need to update paths to your environment.

