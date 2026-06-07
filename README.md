# Federated Learning with Flower (flwr) + PyTorch

**A hands-on study of federated learning: training a shared PyTorch model across simulated decentralized clients with the Flower framework and FedAvg aggregation, then probing the core trade-offs of the paradigm — communication cost, data privacy, hyperparameter tuning, and how much data clients actually need.**

![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)
![Flower](https://img.shields.io/badge/Flower-flwr-EE4C2C)
![PyTorch](https://img.shields.io/badge/PyTorch-model%20training-EE4C2C?logo=pytorch&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-notebooks-F37626?logo=jupyter&logoColor=white)

---

## Overview

Federated learning (FL) trains a shared model across many clients that **keep their data local** — only model updates, never raw data, are exchanged with a central server. This project implements that workflow with the **Flower (`flwr`)** framework and **PyTorch**, aggregating client updates on the server with **FedAvg** (federated averaging), and uses a set of focused experiments to explore *when* and *why* federated learning helps.

> **Accuracy of claims:** this project uses standard **FedAvg** aggregation. It is *not* cryptographic secure aggregation or differential privacy — the privacy benefit here comes from keeping training data on-device, which the experiments examine directly.

---

## Experiments

Each notebook isolates one question about the federated setting:

| Notebook | Focus |
|---|---|
| `Federated_Learning_Process.ipynb` | The core FL loop: client training, FedAvg aggregation, and global-model convergence over rounds. |
| `Bandwidth.ipynb` | Communication cost — the bandwidth implications of exchanging model updates each round. |
| `Data_Privacy.ipynb` | The privacy angle: what stays local vs. what is shared, and why that matters. |
| `Tuning.ipynb` | Hyperparameter tuning in the federated regime (local epochs, client participation, etc.). |
| `Why_do_we_need_more_data.ipynb` | A data-scaling study of how client data quantity affects the global model. |

*(Quantitative results live inside the notebooks; this README intentionally does not quote specific accuracy/bandwidth figures so that every number a recruiter sees is one you can reproduce on the spot.)*

---

## What it demonstrates

- Standing up a working **federated learning pipeline** with Flower + PyTorch (client/strategy/aggregation roles).
- Implementing and reasoning about **FedAvg** parameter aggregation across simulated clients.
- Treating FL as a **systems trade-off**, not just an algorithm — quantifying communication cost and the data/quantity/privacy tensions, rather than only chasing accuracy.
- Structured experimentation: one question per notebook, each independently runnable.

---

## Tech stack

Python · Flower (`flwr`) · PyTorch · NumPy · Matplotlib · Jupyter.

## Repository contents

```text
Federated-Learning-System-Implementation-with-Flower/
├── Federated_Learning_Process.ipynb
├── Bandwidth.ipynb
├── Data_Privacy.ipynb
├── Tuning.ipynb
└── Why_do_we_need_more_data.ipynb
```

```bash
pip install flwr torch numpy matplotlib jupyter
jupyter notebook Federated_Learning_Process.ipynb
```

---

## Skills demonstrated

Federated learning (Flower / FedAvg) · PyTorch model training · decentralized / distributed-ML concepts · privacy-aware machine learning · communication-efficiency analysis · experimental design and reporting.

---

*Author: Arya Kalantari · [github.com/Aria-Kalantari](https://github.com/Aria-Kalantari)*
