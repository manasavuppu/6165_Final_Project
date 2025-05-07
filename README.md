## Personalized AI Writing Assistant

### DSBA 6165 – AI & Deep Learning (Spring 2025)
### Authors: Lasya Reddy Edunuri, Manasa Sree Vuppu, Brinda Vijayakumar

### Introduction
Generating high-quality personalized writing remains one of the most complex and omnipresent problems in today’s world of generative writing. Despite the growth and rapid development of Large Language Models (LLMs), generating text that consistently reflects an individual’s unique style and tone, preserving the nature of their personal voice, remains an open challenge. This project presents an end-to-end system for a Personalized AI Writing Assistant designed to emulate an individual’s unique voice across both short-form and long-form content.

### Project Objective
To build an AI assistant capable of generating emotionally resonant, style-aligned writing that reflects the personal tone of the user, while also evaluating generated content using an authorship classifier.

### Folder structure
<pre> ```Personalized AI Writing Assistant
│
├── 📁 baselineModels/ # Short form text models GPT-2, BART, and T5 
├── 📁 finalModels/ # Long form text models TinyLlama, Meta Llama, Mistral
├── 📁 preprocessing/ # Scripts and notebooks for data cleaning, OCR, tagging
├── 📁 presentation/ # Final project presentation
├── 📁 report/ # Final written report ``` </pre>


### Methods Overview
- **Data Collection**: Curated personalized dataset including quotes, SOPs, blogs, essays and academic letters.
- **Short-Form Generation**:
  - GPT-2 with static prompting
  - BART with STYLEMC-based reranking
  - T5 with few-shot prompting
  - T5 with metadata conditioning
- **Long-Form Generation**:
  - Fine-tuned TinyLlama 1.1B
  - Fine-tuned Meta Llama 3.2 3B with prompt augmentation
  - Fine-tuned Mistral 7B with instruction-based SOP modeling
- **Evaluation**:
  - Quantitative: BERTScore, ROUGE, TF-IDF authorship classifier
  - Qualitative: Human assessment of tone, structure, fluency

### Conclusion
Our multi-stage pipeline effectively mimics authorial voice using LLMs and logistic regression. Metadata-aware conditioning, prompt engineering, LoRA fine-tuning and stylistic reranking greatly improved both coherence and personalization. Classifier scores confirmed stylistic fidelity in most generations.

### Future Work
We aim to expand and diversify the dataset by incorporating more long-form personal writing samples such as essays, letters, and academic reflections and extend this system into a real-time writing assistant embedded in platforms like Google Docs. Future iterations will explore multimodal inputs (e.g., voice notes, video transcripts) to capture broader stylistic signals. 

### Main References
- Khan, A., Wang, A., Hager, S. and Andrews, N. (2023). Learning to Generate Text in Arbitrary Writing Styles. arXiv preprint arXiv:2312.17242.
- Riley, P., Constant, N., Guo, M., Kumar, G., Uthus, D. and Parekh, Z. (2020). TextSETTR: Few-shot text style extraction and tunable targeted restyling. arXiv preprint arXiv:2010.03802.
- Sawicki, P., Grzes, M., Góes, L.F., Brown, D., Peeperkorn, M., Khatun, A. and Paraskevopoulou, S. (2023). On the power of special-purpose GPT models to create and evaluate new poetry in old styles.
- Wei, J., Bosma, M., Zhao, V. Y., Guu, K., Yu, A. W., Lester, B., ... & Le, Q. V. (2021). Finetuned language models are zero-shot learners. arXiv preprint arXiv:2109.01652.

### Acknowledgments  
Special thanks to **Prof. Dr Archit Parnami** for our project guidance.
