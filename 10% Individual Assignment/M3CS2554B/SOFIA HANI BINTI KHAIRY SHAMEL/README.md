# ITT440: Parallelized Network Service Auditor

## 1. Project Overview 🎯
This project is an advanced network auditing engine developed for the ITT440 Network Programming course. It evaluates the performance of service discovery using three distinct execution paradigms: **Sequential**, **Concurrent**, and **Parallel**.

## 2. Environment Specifications 💻
| Category | Details |
| :--- | :--- |
| **Attacker OS** | Kali Linux (Virtual Machine) |
| **Target Environment** | Localhost (127.0.0.1) |
| **Processor** | Intel Core i5 |
| **Memory (RAM)** | 8GB |
| **Language** | Python 3.10 |
| **Network** | VirtualBox NAT |

## 3. Methodology ⚙️
The auditor utilizes a multi-paradigm approach to identify open service ports. The logic is as follows:
* **Batch Processing:** To prevent memory overflow during the 2,000,000-task execution, the engine processes tasks in chunks of 50,000.
* **Vulnerability Scoring:** Post-audit, the engine performs a heuristic analysis to identify high-risk ports (e.g., SSH, FTP, SQL) and assigns a Risk Exposure Score.

## 4. Key Findings 📊
| Paradigm | Execution Time (2M Tasks) |
| :--- | :--- |
| **Sequential** | ~13.77s |
| **Concurrent** | ~59.16s |
| **Parallel** | ~13.61s |

*Note: Performance variance is attributed to OS-level thread scheduling and hypervisor resource allocation.*

## 5. Implementation 🛠️
```python
# Insert your final auditor.py code here
