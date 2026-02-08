**Results Summary (From Report)**

These tables are extracted from the project report and summarize detection time and accuracy with and without percolation thresholding.

**Detection Time (Percolation vs. No Percolation)**

| Attack | Percolation Applied | Without Percolation |
|---|---|---|
| Slowloris | Very Fast (~5s) | Slow (~15-20s) |
| SQL Injection (SQLMap) | Fast (~6s) | Moderate (~18s) |
| Brute Force (Hydra) | Fast (~7s) | Moderate (~20s) |
| Nmap Scanning | Very Fast (~4s) | Slow (~17s) |
| Directory Bruteforce (Dirb) | Fast (~8s) | Moderate (~21s) |

**Detection Accuracy (Percolation vs. No Percolation)**

| Attack | Percolation Applied | Without Percolation |
|---|---|---|
| Slowloris | 99% | 91% |
| SQL Injection (SQLMap) | 98% | 90% |
| Brute Force (Hydra) | 97% | 89% |
| Nmap Scanning | 99% | 92% |
| Directory Bruteforce (Dirb) | 97% | 88% |

**Overall Metrics (Report Table 2)**
- Accuracy: 0.98
- Precision: 0.98 (macro/weighted)
- Recall: 0.98 (macro/weighted)
- F1-score: 0.98 (macro/weighted)

