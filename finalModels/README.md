# 📚 Project Files Overview

This folder contains the fine-tuned SOP generation models and related resources.

---

## 🛠️ Model 2 (Final Model)

- The **final fine-tuned model** (Model 2) is included inside the **zip files** provided.
- Model 2 was fine-tuned to generate Statements of Purpose (SOPs) based on a custom instruction dataset.

---

## 📄 Fine-Tuning Code and Explanation

- The **full fine-tuning code and explanation** for Model 2 are provided in the **Jupyter Notebook** (`.ipynb` file) located inside the **finalModels** folder.
- This notebook covers:
  - Dataset preparation
  - Tokenization
  - Model loading with quantization
  - LoRA-based fine-tuning
  - Inference and testing

---

## 📊 Model Comparison and Evaluation

- The **comparison of three models** (ModelA, ModelB, ModelC) and **choosing the best model** is documented in the `ComparingThreeModelsLLMJudge.ipynb` file.
- This notebook includes:
  - Generating SOPs for in-domain and out-of-domain prompts
  - Using GPT-4 as a judge to evaluate and compare SOP outputs
  - Final evaluation of **Model 2** based on structure, fluency, relevance, and completeness
  - Metric-based evaluations (e.g., ROUGE, BERTScore)

---

## 📂 Data Used for Fine-Tuning

- The data used to fine-tune the final model is located in the **data** folder.
- The key dataset files are:
  - `manasa_chatml_dataset_reformatted.jsonl`
  - `manasa_sop_formatted_updated.jsonl`
- These files contain:
  - Structured instruction–SOP–reasoning pairs
  - Cleaned and formatted SOP datasets for training and evaluation

---

✅ **Summary**:
- **Model 2** = Final Fine-Tuned Model (saved inside zip files)
- **Fine-tuning code** = In `finalModels/` folder (`Model2_finetuning.ipynb`)
- **Model comparison and evaluation** = In `ComparingThreeModelsLLMJudge.ipynb`
- **Training data** = In `data/` folder (`.jsonl` files)

---

# 📌 Quick Map

| Folder / File | Purpose |
|:---|:---|
| `finalModels/` | Fine-tuning code for Model 2 |
| `data/` | Training datasets (`.jsonl` files) |
| `ComparingThreeModelsLLMJudge.ipynb` | Model comparison and evaluation |
| `Model2.zip` | Final fine-tuned model |

