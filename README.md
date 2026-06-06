# ml-ops-fine-tuning-classification

## Overview
This project demonstrates fine-tuning a BERT-based transformer model for text classification using the Hugging Face `transformers` library on a Kaggle Notebook environment.

The notebook covers:
- Dataset loading and preprocessing
- Tokenization using Hugging Face Tokenizers
- Fine-tuning a transformer model
- Evaluation using Accuracy, F1-score, and Loss
- Experiment tracking with Weights & Biases (W&B)
- Model versioning and upload to Hugging Face Hub

---

# Project Structure

```bash
.
├── MLOps_Assignment_2_Fine_Tuning_Classificat.ipynb
├── README.md
└── outputs/
```

---

# Setup Instructions

## 1. Clone the Repository

```bash
git clone https://github.com/aniliter-cloud/mlops-assignment.git
cd mlops-assignment
```

---

## 2. Install Dependencies

Install the required Python packages:

```bash
pip install transformers datasets evaluate scikit-learn wandb accelerate torch huggingface_hub
```

If running locally with Jupyter:

```bash
pip install notebook ipykernel
```

---

# Running the Project

## Option 1 — Run on Kaggle (Recommended)

1. Open the Kaggle notebook
2. Add the following Kaggle Secrets:
   - `WANDB_API_KEY`
   - `HF_TOKEN`
3. Run all notebook cells sequentially

### Kaggle Notebook

https://www.kaggle.com/code/anilg25ait2009/mlops-assignment-2-fine-tuning-classification

---

## Option 2 — Run Locally

Start Jupyter Notebook:

```bash
jupyter notebook
```

Then open:

```text
MLOps_Assignment_2_Fine_Tuning_Classificat.ipynb
```

Run all cells in sequence.

---

# Training Configuration

| Parameter | Value |
|---|---|
| Model | DistilBERT |
| Epochs | 3 |
| Framework | Hugging Face Transformers |
| Experiment Tracking | Weights & Biases |
| Training Platform | Kaggle Notebook |

---

# Results

The final evaluation metrics obtained from the notebook output are shown below.

| Metric | Value |
|---|---|
| Accuracy | 0.6094 |
| F1 Score | 0.6099 |
| Evaluation Loss | 2.2038 |
| Training Loss | 2.1731 |

---

# Project Resources

| Resource | Link |
|---|---|
| GitHub Repository | https://github.com/aniliter-cloud/mlops-assignment/ |
| Hugging Face Model | https://huggingface.co/Maxii2tj/distilbert-goodreads-genres |
| W&B Dashboard | https://wandb.ai/maxi-i2tj-na/mlops-assignment2 |
| Kaggle Notebook | https://www.kaggle.com/code/anilg25ait2009/mlops-assignment-2-fine-tuning-classification |

---

# Features Implemented

- Fine-tuning transformer models
- Automated evaluation metrics
- W&B experiment tracking
- Hugging Face model integration
- Classification report generation
- Artifact logging

---

# Sample Logged Metrics

```python
wandb.log({
    "final/loss": eval_results["eval_loss"],
    "final/accuracy": eval_results["eval_accuracy"],
    "final/f1": eval_results["eval_f1"],
})
```

---

# Technologies Used

- Python
- PyTorch
- Hugging Face Transformers
- Hugging Face Datasets
- Scikit-learn
- Weights & Biases
- Kaggle Notebooks

---

# Notes

- Kaggle Secrets are used to securely store API keys.
- The notebook supports experiment reproducibility.
- Evaluation reports are saved as JSON artifacts and uploaded to W&B.

---

# Future Improvements

- Hyperparameter tuning
- Larger pretrained models
- Better class balancing
- More epochs and scheduler optimization
- Cross-validation

---

# Author

Anil Kumar Das
