# BanglaFact: A Benchmark for Evaluating Factuality of LLMs in Bangla

BanglaFact is a multi-dimensional benchmark designed to evaluate **factual accuracy**, **entailment consistency**, and **confidence calibration** of Large Language Models (LLMs) on Bangla text.  
This benchmark introduces fine-grained segment-level evaluation across multiple domains and provides a comprehensive framework for analyzing model behaviour, strengths, and failure patterns.

---

## 📌 Key Features

### ✅ **1. Multi-Domain Evaluation**
BanglaFact covers four core knowledge domains:
- **World Knowledge**
- **Science & Technology**
- **Mathematics**
- **Reasoning**

Each domain includes:
- Multi-segment prompts  
- Cleaned and verified Bangla text  
- Segment-level factuality labels  

---

### ✅ **2. Segment-Level Factuality Annotation**
Each response is evaluated along:
- **Factuality (True / False)**
- **Entailment**
- **Irrelevant Truths**
- **Hallucinations**
- **Correct segments**
- **Incorrect segments**

This provides a detailed picture of factual consistency across longer responses.

---

### ✅ **3. Factual Entailment Tracing (FET)**
For Science and World Knowledge, BanglaFact includes:
- Entailment Accuracy  
- Irrelevant Truth Rate  
- Hallucination Rate  

With reference-backed annotation based on:
- Encyclopedic sources  
- Peer-reviewed materials  

---

### ✅ **4. Confidence Calibration**
BanglaFact includes model self-reported confidence values.  
We compute:
- High Confidence Accuracy  
- Mid Confidence Accuracy  
- Low Confidence Accuracy  
- **Overconfident Error Rate**  
- Calibration gaps across confidence bins  

This enables deeper reliability analysis of LLMs.

---

### ✅ **5. Model Coverage**
The benchmark includes evaluation across:
- **GPT-4o-Mini**
- **Gemma-3 12B**
- **Qwen-2.5 7B**
- **Mistral-7B (Instruct & Nemo)**
- **GPT-3.5-Turbo**
- **LLaMA-3.1 8B**

Each model is tested on identical inputs with:
- Raw prompting
- CoT prompting  
- Link-augmented prompting  
- Content-augmented prompting
---
## 📊 Metrics Included

### **Factuality Metrics**
- Accuracy  
- Precision, Recall, F1  
- Segment-level correctness  

### **Entailment Metrics (FET)**
- Entailment Accuracy  
- Irrelevant Truth Rate  
- Hallucination Rate  

### **Calibration Metrics**
- Low confidence rate
- Mid confidence rate
- High confidence rate 
- Overconfident error rate
---
## 🔄 How to Reproduce

Follow these steps to fully reproduce the BanglaFact evaluation pipeline, results, and figures:

### **1. Clone the Repository**

Download or clone the project to your local environment or cloud workspace (Colab/Kaggle).
Make sure all directories under banglafact/ are kept intact, including prompts/, scripts/, models/, and results/.

### **2. Prepare the Environment**

Ensure you have:

- Python 3.10 or higher

- GPU access (recommended: T4, P100, V100, or A100)

- Required Python libraries (e.g., PyTorch, Pandas, NumPy, Matplotlib, Seaborn)

- OpenRouter API key for LLM inference

- Place your API key in an environment variable or your platform’s secret manager.

### **3. Dataset Setup**
- Download the dataset
- Integrate into the pipeline 1 to evaluate a model
- Run the output from pipeline 1 into pipeline 2
- Analyse the output files from pipeline 2 with analysis.py
