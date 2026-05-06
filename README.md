# Reliable Question Answering with LLMs

### Self-Consistency • RAG • Calibration • Conformal Prediction

##  Overview

This project investigates how to improve the **reliability of Large Language Model (LLM) question answering systems**.

Modern LLMs often produce:

*  Hallucinated answers
*  Overconfident incorrect responses

We address this using a unified pipeline combining:

*  Self-Consistency Sampling
*  Retrieval-Augmented Generation (RAG)
*  Selective Prediction (Thresholding)
*  Calibration Analysis (ECE)
*  Conformal Prediction

---

##  Methods

### 1. Self-Consistency

Generate multiple answers and select the most frequent.

### 2. RAG

Ground responses using external documents.

### 3. Thresholding

Abstain when confidence is low.

### 4. Calibration

Evaluate how well confidence reflects correctness.

### 5. Conformal Prediction

Provide statistically valid acceptance/rejection decisions.

---

##  Installation

```bash
pip install -r requirements.txt
```

---

##  Usage Example

```python
from src.self_consistency import self_consistency

result = self_consistency("What is Numerical Linear Algebra?", n_samples=10)

print(result)
```

---

##  Sample Results

| Threshold | Coverage | Accuracy |
| --------- | -------- | -------- |
| 0.2       | 0.40     | 0.87     |
| 0.3       | 0.40     | 1.00     |
| 0.4       | 0.35     | 0.86     |
| 0.5       | 0.40     | 0.87     |
| 0.6       | 0.25     | 1.00     |

---

##  Key Insights

* Self-consistency improves stability
* RAG significantly improves technical answers
* Confidence is often miscalibrated
* Conformal prediction improves reliability

---

##  Project Structure

* `notebooks/` → step-by-step experiments
* `src/` → modular implementation
* `data/` → datasets
* `results/` → outputs and figures
* `report/` → research paper

---

##  Reproducibility

All experiments are fully reproducible via the notebooks.

---

##  Future Work

* Larger datasets (SQuAD, Natural Questions)
* LoRA fine-tuning
* Efficiency optimization

---

## 👤 Author

Morad Ahmadnasab
PhD in Applied Mathematics
Montreal, Canada

---

##  If you find this useful, consider starring the repo!
