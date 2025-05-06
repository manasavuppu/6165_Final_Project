# DSBA 6165 AI and Deep Learning Project (Spring 2025)
## 👥 Group 8 – Personalized AI Writing Assistant

🔍 Project Overview
This project aims to develop a multi-model AI-powered writing assistant capable of generating both short-form (quotes, reflections) and long-form (SOPs, essays) texts in the unique writing style of the user. The solution leverages style conditioning, semantic alignment, and authorship verification to ensure stylistic authenticity and minimal hallucination.

📁 Project Structure
📦 AI-Writing-Assistant/
├── 📂 report/                   # Final report and supplementary documentation
│   ├── 6165_Final_Report_Group_8.pdf
│   ├── Final_model_documentation.docx
├── 📂 models/                   # Fine-tuned and baseline model scripts
│   ├── gpt2_style_model.py
│   ├── bart_longform_generator.py
│   ├── t5_text_rewriter.py
│   └── authorship_classifier.py
├── 📂 data/                     # Preprocessed datasets (quotes, blogs, SOPs)
│   ├── quotes_personal.csv
│   ├── sop_samples.csv
│   └── author_labels.csv
├── 📂 notebooks/               # EDA, training logs, metric visualizations
│   ├── shortform_generation.ipynb
│   └── authorship_eval.ipynb
├── README.md                   # Project summary and usage guide

🔧 Technologies & Models Used
| Purpose                   | Model                               | Notes                                       |
| ------------------------- | ----------------------------------- | ------------------------------------------- |
| Short-form generation     | GPT-2 (LoRA fine-tuned)             | Controlled via metadata & few-shot examples |
| Long-form generation      | BART, Meta LLaMA, Mistral           | Chosen based on fluency and coherence       |
| Style rewriting           | T5 + TextSETTR                      | For tone-specific quote transformation      |
| Evaluation                | BERTScore, SpaCy, Custom Classifier | Ensures semantic and stylistic fidelity     |
| Authorship Classification | Logistic Regression                 | Predicts if text matches user's style       |

🎯 Key Features
Style Conditioning: Metadata tags like tone, theme, and formality help guide generation.

Few-shot Prompting: Stabilizes model behavior using examples.

Style Verification: Ensures generated content matches the author's signature style.

Custom Post-Processing: Removes hallucinations and ensures emotional coherence.

📊 Evaluation Highlights
BERTScore (F1): 0.84 on short-form quotes

Classifier Accuracy: 88.5% on authorship validation

Human Evaluation: 9/10 testers agreed generated content matched the author’s style

🧠 Future Scope
Add reinforcement learning with human feedback (RLHF) for emotional alignment.

Expand authorship classifier to support multi-author confusion matrix.

Explore integration with web UIs like Streamlit or Gradio for public demo.

🙌 Acknowledgments
Special thanks to Prof. Fox for project guidance.

Base models: HuggingFace Transformers, TinyLLaMA, and TextSETTR.
