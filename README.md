<h1 align="center">Hi there <img src="https://raw.githubusercontent.com/MartinHeinz/MartinHeinz/master/wave.gif" width="30px"> I'm Abhitej</h1>

- 👨‍💻 I’m building cool technology at Chewy
- 🔭 I’m working on a JavaScript project to rate off-campus housing with @adp811
- 🌱 I’m currently learning Python & AWS
- 👯 I’m looking to collaborate on any web3.0 projects
- 🍩 I’m looking for help with opening up a donut shop lol
- 📚 I'm a Rutgers alum and I studied Computer Science & Data Science
- 📫 DM me on LinkedIn if you want to get in contact
- 💬 Ask me about Marvel, keeping aquariums, or philosophy

- 🐌 Fun fact: I own 5 snails and a shrimp 🦐 (I have 2 fishtanks)
- Check out my websites & social media: 

<p align="center"> 

<a href="https://abhitej-bokka.github.io/">![Abhitej Bokka](https://img.shields.io/badge/Abhitej_Bokka-816EFF?style=for-the-badge&logo=Three.js&logoColor=white)</a> 
<a href="https://bokka-bee-nfts.herokuapp.com/">![Bokka Bee NFTs](https://img.shields.io/badge/Bokka_Bee_NFTs-43B6B4?style=for-the-badge&logo=Ethereum&logoColor=white)</a> 
<a href="https://www.linkedin.com/in/abhitej-bokka/">![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)</a>
<a href="https://www.instagram.com/abhitej.bokka/">![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)</a>
  
</p>
# 🔍 Query-Focused EHR Summarization: Dataset, Task, and ClinicalBERT Model

## 📌 Summary
This pull request introduces a complete pipeline for **Query-Focused EHR Summarization**, based on the paper:  
[*Query-Focused EHR Summarization to Aid Imaging Diagnosis*](https://arxiv.org/abs/2004.04645)

### What's Included:
-  **New Dataset**: `EHRSummarizationDataset`  
  Inherits from `SampleEHRDataset` and processes notes into sentence-level inputs labeled using future ICD codes within a 30-day window.
-  **New Task**: `ehr_summarization_task`  
  A PyHealth-compatible task that returns sentence-level relevance samples.
-  **New Model**: `ClinicalBertSentenceClassifier`  
  A Huggingface Bio_ClinicalBERT-based classifier that uses CLS or average pooling to predict sentence relevance.
-  **New Unit Tests**:  
  Validates label generation, dataset iteration, and model forward pass behavior.

## 📂 Files Added
- `pyhealth/datasets/ehr_summarization.py`
- `pyhealth/tasks/ehr_summarization_task.py`
- `pyhealth/models/clinical_bert.py`
- `pyhealth/unittests/test_ehr_summarization.py`

## 🚀 Features
- SpaCy-based sentence tokenization
- Distant supervision using future ICD codes
- Plug-and-play with existing PyHealth infrastructure
- Reproducible and testable with clear unit tests

## 🧪 How to Run Tests
```bash
PYTHONPATH=. pytest pyhealth/unittests/test_ehr_summarization.py
```

🙌 Authors
Abhitej Bokka (abhitej2) ([@abhitej-bokka](https://github.com/abhitej-bokka))
Liam Shen (liams4) ([@liamshen10](https://github.com/liamshen10))

