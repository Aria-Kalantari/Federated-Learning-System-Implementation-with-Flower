# Federated Learning with Flower

Federated-learning experiments built on the **Flower (flwr)** framework using **FedAvg**
aggregation across simulated clients, exploring the federated training process, bandwidth,
hyperparameter tuning, and data-privacy considerations.

## Why This Project Matters

Federated learning trains a shared model across many clients **without centralizing their raw
data** — each client trains locally and only model updates are aggregated. This is valuable
when data is sensitive or distributed. The project uses Flower to run that workflow and study
its practical trade-offs.

## Tech Stack

- **Language:** Python (Jupyter Notebook)
- **Framework:** Flower (`flwr`)
- **Method:** FedAvg (federated averaging) aggregation
- **Libraries:** a deep-learning backend (e.g., PyTorch/TensorFlow) *(confirm exact framework in the notebooks)*

## Key Features

- Federated training loop with **FedAvg** aggregation via Flower.
- Notebooks exploring distinct aspects of the system:
  - `Federated_Learning_Process.ipynb` — the core federated training workflow
  - `Bandwidth.ipynb` — communication/bandwidth considerations
  - `Tuning.ipynb` — hyperparameter tuning
  - `Data_Privacy.ipynb` — data-privacy considerations
  - `Why_do_we_need_more_data.ipynb` — data-quantity effects

## Repository Structure

```text
Federated-Learning-System-Implementation-with-Flower/
├── Federated_Learning_Process.ipynb
├── Bandwidth.ipynb
├── Tuning.ipynb
├── Data_Privacy.ipynb
└── Why_do_we_need_more_data.ipynb
```

## How to Run

```bash
pip install flwr jupyter   # plus the DL backend used in the notebooks (confirm)
jupyter notebook Federated_Learning_Process.ipynb
```

## Example Output / Results

To be added after verification. *(Add accuracy/convergence across rounds, bandwidth findings,
and tuning results once confirmed from the notebooks.)*

## What I Learned

- Running a federated training workflow with Flower and FedAvg.
- Trade-offs in federated learning: communication cost, tuning, and data privacy.

## Future Improvements

- Add results (per-round accuracy, bandwidth/tuning findings) once verified.
- Consolidate the notebooks into a documented pipeline + `requirements.txt`.

## Limitations

- Coursework/portfolio experiments using FedAvg. **Not** a secure-aggregation implementation —
  this project does not add cryptographic secure aggregation on top of FedAvg.
- Results still to be surfaced here from the notebooks.
