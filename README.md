<div align="center">

# Large Language Models in Medical Time Series Analysis

**An actively updated companion repository for our review on Large Language Models for Medical Time Series Analysis (MedTSLLMs).**

[![Papers](https://img.shields.io/badge/reviewed%20studies-62-blue)](#-paper-collection)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/hy727/MedTSLLM-Review?style=social)](https://github.com/hy727/MedTSLLM-Review/stargazers)

**Last updated: September 2026**

</div>

## 📌 Overview

This repository accompanies the review:

> **Large Language Models in Medical Time Series Analysis**  
> Yu Han, Cigdem Beyan, Xiang Zhang, Xiaofeng Liu, Nan Liu, Jimeng Sun, Shenda Hong, Cheng Ding, and Vittorio Murino

Medical time series (MedTS), including electrocardiograms (ECG), electroencephalograms (EEG), photoplethysmography (PPG), vital-sign recordings, and wearable sensor data, are central to clinical diagnosis and health monitoring. This repository provides a curated and continuously updated collection of studies that connect MedTS with large language models (LLMs), including work on representation learning, signal-language alignment, reasoning, generation, retrieval, and agent-based analysis.

The current manuscript reviews **62 studies** and organizes them into six clinically oriented application scenarios. Because the field is evolving rapidly, this repository serves as a living companion resource for tracking studies that appear after the literature collection used in the manuscript.

> **Scope.** We use **MedTSLLM** as a broad term for LLM-based approaches to MedTS analysis rather than for a single model architecture. MedTSLLMs may combine language models with signal encoders, multimodal alignment modules, retrieval systems, or other task-specific components. The scope therefore includes different forms of LLM involvement in MedTS representation learning, signal-language alignment, reasoning, generation, and agent-based analysis.

## 🗂️ Table of Contents

- [News](#-news)
- [Review Snapshot](#-review-snapshot)
- [Paper Collection](#-paper-collection)
  - [Medical Disease Diagnosis](#-medical-disease-diagnosis)
  - [Clinical Report Generation](#-clinical-report-generation)
  - [Medical Question Answering](#-medical-question-answering)
  - [Neuro-Signal Translation](#-neuro-signal-translation)
  - [Health Assessment Support](#-health-assessment-support)
  - [Physiological Signal Synthesis](#-physiological-signal-synthesis)
- [Recent Additions](#-recent-additions)
- [Contributing](#-contributing)
- [Citation](#-citation)

## 📢 News

- **2026-09** — Repository released with the literature collection from the current review manuscript.
- **2026-XX** — Paper link and final citation will be added after publication.

## 📊 Review Snapshot

The **62 studies** summarized in the current manuscript are organized according to their primary clinical application in Table 4:

| Application | # Studies |
|---|---:|
| Medical disease diagnosis | 16 |
| Clinical report generation | 8 |
| Medical question answering | 13 |
| Neuro-signal translation | 12 |
| Health assessment support | 9 |
| Physiological signal synthesis | 4 |

The reviewed literature spans ECG, EEG, PPG, vital signs, wearable sensors, and multimodal physiological data. Modality counts are not mutually exclusive because some studies use more than one signal type.

## 📚 Paper Collection

The organization below follows the clinical application taxonomy used in **Table 4 of the review**. Some studies naturally span multiple applications; for consistency, each study is listed under its primary application in the manuscript.

> **Metadata note.** Year and venue information follows the bibliography used for the current manuscript. As preprints are formally published, the repository can be updated to link to the final versions while preserving the original review corpus.

**Legend:** `—` indicates that a public code repository was not listed in the manuscript or verified at the time of this update.

### 🩺 Medical Disease Diagnosis

**16 studies**

| Study | Year | Modality | Primary LLM role | Main task | Venue | Code |
|---|---:|---|---|---|---|---|
| **HeartBEiT**<br>[A foundational vision transformer improves diagnostic performance for electrocardiograms](https://www.nature.com/articles/s41746-023-00840-9) | 2023 | ECG | Backbone | Cardiac disease diagnosis (LVEF, HCM, STEMI) | npj Digital Medicine | [code](https://github.com/akhilvaid/HeartBEiT) |
| **sEHR-ECG-Text**<br>[Ecg representation learning with multi-modal ehr data](https://openreview.net/forum?id=UxmvCwuTMG) | 2023 | ECG + EHR | Text encoder | Multimodal ECG representation learning and diagnosis | TMLR | — |
| **ECGBERT**<br>[Ecgbert: Understanding hidden language of ecgs with self-supervised representation learning](https://arxiv.org/abs/2306.06340) | 2023 | ECG | Backbone | Arrhythmia diagnosis and sleep-apnea detection | arXiv | — |
| **METS**<br>[Frozen language model helps ecg zero-shot learning](https://proceedings.mlr.press/v227/li24a.html) | 2024 | ECG + clinical text | Text encoder | Zero-shot ECG diagnosis | MIDL | — |
| **MERL-CKEPE**<br>[Zero-shot ecg classification with multimodal learning and test-time clinical knowledge enhancement](https://arxiv.org/abs/2403.06659) | 2024 | ECG + clinical notes | Prompt generator | Zero-shot ECG classification / abnormality diagnosis | arXiv | [code](https://github.com/cheliu-computation/MERL) |
| **Zero-shot RAG**<br>[Zero-shot ECG diagnosis with large language models and retrieval-augmented generation](https://proceedings.mlr.press/v225/yu23b.html) | 2023 | ECG | Text decoder | Zero-shot arrhythmia and sleep-apnea diagnosis | ML4H | — |
| **ECG-GPT**<br>[Automated diagnostic reports from images of electrocardiograms at the point-of-care](https://www.medrxiv.org/content/10.1101/2024.02.17.24302976v1) | 2024 | ECG image | Text decoder | Free-text ECG diagnostic interpretation | medRxiv | — |
| **CardioGPT**<br>[Cardiogpt: An ecg interpretation generation model](https://doi.org/10.1109/ACCESS.2024.3384349) | 2024 | ECG | Classifier | ECG interpretation and abnormality diagnosis | IEEE Access | — |
| **CQA-ESI**<br>[Ecg semantic integrator (esi): A foundation ecg model pretrained with llm-enhanced cardiological text](https://arxiv.org/abs/2405.19366) | 2024 | ECG + clinical text | Text encoder + decoder | Knowledge-enhanced ECG diagnosis | arXiv | [code](https://github.com/comp-well-org/ESI) |
| **EEG-GPT**<br>[EEG-GPT: exploring capabilities of large language models for EEG classification and interpretation](https://arxiv.org/abs/2401.18006) | 2024 | EEG | Classifier | EEG classification and interpretation | arXiv | — |
| **ETP**<br>[Etp: Learning transferable ecg representations via ecg-text pre-training](https://arxiv.org/abs/2309.07145) | 2024 | ECG + clinical reports | Text encoder | Transferable ECG representation / zero-shot diagnosis | ICASSP 2024 | — |
| **GPT-PPG**<br>[GPT-PPG: a GPT-based foundation model for photoplethysmography signals](https://doi.org/10.1088/1361-6579/add988) | 2025 | PPG | Backbone | PPG foundation modeling and downstream diagnosis | Physiological Measurement | — |
| **GPT-4 ECG interpretation**<br>[Beyond text: the impact of clinical context on GPT-4’s 12-lead electrocardiogram interpretation accuracy](https://www.sciencedirect.com/science/article/abs/pii/S0828282X25001321) | 2025 | ECG + clinical context | Text decoder | Clinical-context-aware ECG interpretation | Canadian Journal of Cardiology | — |
| **GEM**<br>[Gem: Empowering mllm for grounded ecg understanding with time series and images](https://arxiv.org/abs/2503.06073) | 2025 | ECG time series + image + text | Text decoder + image/time-series encoder | Grounded ECG understanding | arXiv | [code](https://github.com/lanxiang1017/GEM) |
| **MedualTime**<br>[MedualTime: A dual-adapter language model for medical time series-text multimodal learning](https://arxiv.org/abs/2406.06620) | 2024 | ECG + EEG + clinical text | Backbone | Medical time-series/text multimodal classification | arXiv | [code](https://github.com/start2020/MedualTime) |
| **ZETA**<br>[Interpretable multimodal zero shot ECG diagnosis via structured clinical knowledge alignment](https://www.nature.com/articles/s44325-025-00099-x) | 2026 | ECG | Text encoder + observation generator | Interpretable zero-shot ECG diagnosis | npj Cardiovascular Health | [code](https://github.com/Tang-Jia-Lu/Zeta) |

### 📝 Clinical Report Generation

**8 studies**

| Study | Year | Modality | Primary LLM role | Main task | Venue | Code |
|---|---:|---|---|---|---|---|
| **JoLT**<br>[JoLT: jointly learned representations of language and time-series for clinical time-series interpretation (student abstract)](https://ojs.aaai.org/index.php/AAAI/article/view/30423) | 2024 | ECG + text | Text decoder | Clinical time-series interpretation / report generation | AAAI 2024 | — |
| **SignalGPT**<br>[BioSignal Copilot: Leveraging the power of LLMs in drafting reports for biomedical signals](https://www.medrxiv.org/content/10.1101/2023.06.28.23291916v1) | 2023 | Biomedical signals + text | Agent | Biomedical signal report drafting | medRxiv | — |
| **MEIT**<br>[MEIT: Multimodal Electrocardiogram Instruction Tuning on Large Language Models for Report Generation](https://aclanthology.org/2025.findings-acl.749/) | 2025 | ECG | Prompt generator + text decoder | ECG report generation | Findings of ACL 2025 | [code](https://github.com/AIoT-MLSys-Lab/MEIT) |
| **PhysioLLM**<br>[Physiollm: Supporting personalized health insights with wearables and large language models](https://arxiv.org/abs/2406.19283) | 2024 | Wearable / Fitbit | Agent | Personalized wearable-data interpretation | IEEE BHI 2024 | — |
| **ECG-Chat**<br>[Ecg-chat: A large ecg-language model for cardiac disease diagnosis](https://arxiv.org/abs/2408.08849) | 2025 | ECG | Backbone + report generator | ECG report generation | IEEE ICME 2025 | [code](https://github.com/YubaoZhao/ECG-Chat) |
| **ECG-ReGen**<br>[Electrocardiogram Report Generation and Question Answering via Retrieval-Augmented Self-Supervised Modeling](https://arxiv.org/abs/2409.08788) | 2025 | ECG + retrieved reports | Text encoder + decoder | Retrieval-augmented ECG report generation | ICASSP 2025 | — |
| **ECG-Bench**<br>[Retrieval-Augmented Generation for Electrocardiogram-Language Models](https://arxiv.org/abs/2510.00261) | 2025 | ECG + retrieved reports | Backbone | Retrieval-augmented ECG-language generation | arXiv | [code](https://github.com/willxxy/ECG-Bench) |
| **DiagECG**<br>[DiagECG: An LLM-Driven Framework for Diagnostic Reasoning via Discretized ECG Tokenization](https://arxiv.org/abs/2508.15338) | 2025 | ECG | Backbone + report generator | Diagnostic reasoning and ECG report generation | arXiv | — |

### 💬 Medical Question Answering

**13 studies**

| Study | Year | Modality | Primary LLM role | Main task | Venue | Code |
|---|---:|---|---|---|---|---|
| **ECG-QA**<br>[Ecg-qa: A comprehensive question answering dataset combined with electrocardiogram](https://arxiv.org/abs/2306.15681) | 2023 | ECG | Answer generator | ECG question answering | NeurIPS 2023 | [code](https://github.com/Jwoo5/ecg-qa) |
| **GPT-4V clinical image interpretation**<br>[GPT-4V (ision) unsuitable for clinical care and education: a clinician-evaluated assessment](https://arxiv.org/abs/2403.12046) | 2023 | ECG / EEG + medical images | Answer generator | Multimodal clinical image interpretation | arXiv | — |
| **ChatGPT ECG assessment**<br>[Comparison of emergency medicine specialist, cardiologist, and chat-GPT in electrocardiography assessment](https://doi.org/10.1016/j.ajem.2024.03.017) | 2024 | ECG | Answer generator | ECG question answering / diagnostic assessment | American Journal of Emergency Medicine | — |
| **AutoHeart**<br>[Automated HEART score determination via ChatGPT: Honing a framework for iterative prompt development](https://doi.org/10.1002/emp2.13133) | 2024 | Clinical notes / ECG-related context | Answer generator | Automated HEART score calculation | JACEP Open | — |
| **openCHA**<br>[Conversational health agents: A personalized llm-powered agent framework](https://arxiv.org/abs/2310.02374) | 2023 | PPG + IMU + EHR + images | Agent | Conversational personalized health QA | arXiv | [code](https://github.com/Institute4FutureHealth/CHA) |
| **ECG-LM**<br>[ECG-LM: Understanding Electrocardiogram with a Large Language Model](https://doi.org/10.34133/hds.0221) | 2025 | ECG + clinical text | Answer generator | ECG QA and interpretation | Health Data Science | — |
| **PULSE**<br>[Teach multimodal llms to comprehend electrocardiographic images](https://arxiv.org/abs/2410.19008) | 2024 | ECG image + text | Answer generator + evaluator | ECG visual QA and report understanding | arXiv | [code](https://github.com/AIMedLab/PULSE) |
| **LLMs in clinical cardiology**<br>[The pulse of artificial intelligence in cardiology: a comprehensive evaluation of state-of-the-art large language models for potential use in clinical cardiology](https://www.medrxiv.org/content/10.1101/2023.08.08.23293689v1) | 2023 | Cardiology text / ECG context | Answer generator | Clinical cardiology reasoning | medRxiv | — |
| **CHA-PPGHR**<br>[An LLM-Powered Agent for Physiological Data Analysis: A Case Study on PPG-based Heart Rate Estimation](https://arxiv.org/abs/2502.12836) | 2025 | PPG | Agent | PPG-based heart-rate estimation and QA | arXiv | [code](https://github.com/mohammadfeli/CHA-PPGHR) |
| **Zero-shot VQA**<br>[Assessing the performance of zero-shot visual question answering in multimodal large language models for 12-lead ECG image interpretation](https://doi.org/10.3389/fcvm.2025.1458289) | 2025 | ECG image | Answer generator | Zero-shot visual ECG question answering | Frontiers in Cardiovascular Medicine | — |
| **ECG-Expert-QA**<br>[ECG-Expert-QA: A Benchmark for Evaluating Medical Large Language Models in Heart Disease Diagnosis](https://arxiv.org/abs/2502.17475) | 2025 | ECG + clinical reports | Answer generator | Expert-level ECG question answering | arXiv | [code](https://github.com/Zaozzz/ECG-Expert-QA) |
| **EEG Emotion Copilot**<br>[EEG emotion copilot: Optimizing lightweight LLMS for emotional EEG interpretation with assisted medical record generation](https://doi.org/10.1016/j.neunet.2025.107848) | 2025 | EEG | Agent | Emotion interpretation and assisted medical records | Neural Networks | [code](https://github.com/NZWANG/EEG_Emotion_Copilot) |
| **EEG-MedRAG**<br>[EEG-MedRAG: Enhancing EEG-based Clinical Decision-Making via Hierarchical Hypergraph Retrieval-Augmented Generation](https://arxiv.org/abs/2508.13735) | 2025 | EEG + clinical context | Agent | Retrieval-augmented EEG clinical decision support | arXiv | [code](https://github.com/yi9206413-boop/EEG-MedRAG) |

### 🧠 Neuro-Signal Translation

**12 studies**

| Study | Year | Modality | Primary LLM role | Main task | Venue | Code |
|---|---:|---|---|---|---|---|
| **EEG-ETB**<br>[Integrating llm, eeg, and eye-tracking biomarker analysis for word-level neural state classification in semantic inference reading comprehension](https://arxiv.org/abs/2309.15714) | 2023 | EEG + eye tracking | Classifier | Word-level neural-state classification / reading comprehension | arXiv | — |
| **DeWave**<br>[Dewave: Discrete eeg waves encoding for brain dynamics to text translation](https://arxiv.org/abs/2309.14030) | 2023 | EEG | Text decoder | EEG-to-text translation | arXiv | [code](https://github.com/duanyiqun/DeWave) |
| **MTAM**<br>[Can brain signals reveal inner alignment with human languages?](https://aclanthology.org/2023.findings-emnlp.120/) | 2023 | EEG + language context | Text encoder | EEG-language alignment / semantic classification | Findings of EMNLP 2023 | [code](https://github.com/Jielin-Qiu/EEG_Language_Alignment) |
| **CFEHC**<br>[Contextual feature extraction hierarchies converge in large language models and the brain](https://www.nature.com/articles/s42256-024-00925-4) | 2024 | iEEG + language context | Backbone | Brain–LLM representational alignment | Nature Machine Intelligence | — |
| **iEEG-GPT**<br>[Enhancing neural decoding with large language models: A GPT-based approach](https://doi.org/10.1109/BCI60775.2024.10480499) | 2024 | iEEG + spectral/topographic features | Text decoder | Neural decoding and interpretation | IEEE BCI 2024 | — |
| **WERE**<br>[From word embedding to reading embedding using large language model, eeg and eye-tracking](https://arxiv.org/abs/2401.15681) | 2024 | EEG + eye tracking | Text encoder + classifier | Reading embedding / neural-state classification | IEEE EMBC 2024 | [code](https://github.com/Xemin0/ReadingEmbedding) |
| **Neuro-GPT**<br>[Neuro-gpt: Towards a foundation model for eeg](https://arxiv.org/abs/2311.03764) | 2024 | EEG | Text decoder | EEG foundation modeling and interpretation | IEEE ISBI 2024 | [code](https://github.com/wenhui0206/NeuroGPT) |
| **BELT**<br>[BELT: bootstrapped EEG-to-language training by natural language supervision](https://doi.org/10.1109/TNSRE.2024.3450795) | 2024 | EEG | Text decoder | EEG-to-language decoding | IEEE TNSRE | — |
| **BELT-2**<br>[Belt-2: Bootstrapping eeg-to-language representation alignment for multi-task brain decoding](https://arxiv.org/abs/2409.00121) | 2024 | EEG | Text decoder | Multi-task EEG-to-language decoding | arXiv | — |
| **CET-MAE**<br>[Enhancing eeg-to-text decoding through transferable representations from pre-trained contrastive eeg-text masked autoencoder](https://arxiv.org/abs/2402.17433) | 2024 | EEG | Text decoder | EEG-to-text decoding | arXiv | — |
| **BSLA**<br>[LLMs Help Alleviate the Cross-Subject Variability in Brain Signal and Language Alignment](https://arxiv.org/abs/2501.02621) | 2025 | EEG | Backbone + text decoder | Cross-subject brain-signal/language alignment | arXiv | — |
| **Thought2Text**<br>[Thought2Text: text generation from EEG signal using large language models (LLMs)](https://arxiv.org/abs/2410.07507) | 2025 | EEG + image stimulus | Caption generator + evaluator | EEG-to-text generation | Findings of NAACL 2025 | [code](https://github.com/abhijitmishra/Thought2Text) |

### ⌚ Health Assessment Support

**9 studies**

| Study | Year | Modality | Primary LLM role | Main task | Venue | Code |
|---|---:|---|---|---|---|---|
| **ALPHA**<br>[Alpha: Anomalous physiological health assessment using large language models](https://arxiv.org/abs/2311.12524) | 2023 | PPG + HR + SpO₂ | Classifier | Physiological health assessment | arXiv | [code](https://github.com/McJackTang/LLM-HealthAssistant) |
| **Health-Learner**<br>[Large language models are few-shot health learners](https://arxiv.org/abs/2305.15525) | 2023 | Wearable biosignals | Predictor | Few-shot health prediction | arXiv | — |
| **AdaCT**<br>[Large transformers are better eeg learners](https://arxiv.org/abs/2308.11654) | 2023 | EEG + activity sensors | Backbone + classifier | Seizure, sleep-stage and activity classification | arXiv | [code](https://github.com/wangbxj1234/AdaCE) |
| **Health-LLM**<br>[Health-llm: Large language models for health prediction via wearable sensor data](https://arxiv.org/abs/2401.06866) | 2024 | Wearable / Fitbit | Classifier | Health prediction from wearable sensor data | arXiv | [code](https://github.com/mitmedialab/Health-LLM) |
| **CBPM-LLaMA**<br>[Large language models for cuffless blood pressure measurement from wearable biosignals](https://arxiv.org/abs/2406.18069) | 2024 | ECG + PPG | Predictor | Cuffless blood-pressure estimation | ACM BCB 2024 | — |
| **WDAI-LLM**<br>[Large language models for wearable data analysis and interpretation](https://openreview.net/forum?id=GoWD6logcd) | 2024 | Wearable / Fitbit | Predictor | Wearable-data analysis and health prediction | Tiny Papers @ ICLR 2024 | — |
| **PSRT**<br>[The Prediction of Stress in Radiation Therapy: Integrating Artificial Intelligence with Biological Signals](https://doi.org/10.3390/cancers16111964) | 2024 | ECG + PPG + EEG + wearable | Classifier | Stress prediction | Cancers | — |
| **PH-LLM**<br>[Towards a personal health large language model](https://arxiv.org/abs/2406.06474) | 2024 | Wearable / Fitbit | Backbone | Personalized sleep and fitness assessment | arXiv | — |
| **SensorLM**<br>[SensorLM: Learning the Language of Wearable Sensors](https://arxiv.org/abs/2506.09108) | 2025 | Wearable sensors | Text decoder | Sensor-to-text / health assessment | arXiv | — |

### 🫀 Physiological Signal Synthesis

**4 studies**

| Study | Year | Modality | Primary LLM role | Main task | Venue | Code |
|---|---:|---|---|---|---|---|
| **Auto-TTE**<br>[Text-to-ecg: 12-lead electrocardiogram synthesis conditioned on clinical text reports](https://arxiv.org/abs/2303.09395) | 2023 | ECG + clinical text | Text decoder | Text-conditioned 12-lead ECG synthesis | ICASSP 2023 | [code](https://github.com/TClife/text_to_ecg) |
| **ECG-LLM**<br>[ECG-LLM: Leveraging Large Language Models for Low-Quality ECG Signal Restoration](https://doi.org/10.1109/BIBM62325.2024.10822461) | 2024 | ECG | Backbone | Low-quality ECG restoration | IEEE BIBM 2024 | [code](https://github.com/dragonlfy/ECG-LLM) |
| **BCG2ECG**<br>[Adapting LLMs for Ballistocardiographic Signals: A Multi-Task Learning Framework for BCG to ECG Reconstruction](https://doi.org/10.1109/RICAI64321.2024.10911542) | 2024 | BCG + ECG + PPG | Backbone | BCG-to-ECG reconstruction | RICAI 2024 | — |
| **DiffuSETS**<br>[DiffuSETS: 12-Lead ECG generation conditioned on clinical text reports and patient-specific information](https://doi.org/10.1016/j.patter.2025.101291) | 2025 | ECG + clinical text + patient context | Backbone | Text-conditioned 12-lead ECG generation | Patterns | [code](https://github.com/Raiiyf/DiffuSETS_Exp) |

## 🆕 Recent Additions

This section is reserved for relevant MedTSLLM studies that appeared **after the literature collection used in the current manuscript**. Newly added studies will be kept separate from the original 62-study review corpus so that the provenance of the published review remains clear.

| Study | Year | Modality | Application | Paper | Code | Added |
|---|---:|---|---|---|---|---|
| *New studies will be added here.* | — | — | — | — | — | — |

## 🤝 Contributing

We welcome contributions from the community to keep this resource up to date. If you would like to add a relevant MedTSLLM study, please open an [Issue](https://github.com/hy727/MedTSLLM-Review/issues) or submit a [Pull Request](https://github.com/hy727/MedTSLLM-Review/pulls).

Please provide the following information when suggesting a paper:

- **Paper title**
- **Authors**
- **Venue and year**
- **Paper URL**
- **Code/model URL**, if available
- **MedTS modality** (e.g., ECG, EEG, PPG, wearable sensors, vital signs)
- **Primary clinical application**
- **Primary role of the LLM** in the pipeline

For consistency, please use one of the six primary application categories adopted in the review:

1. Medical Disease Diagnosis
2. Clinical Report Generation
3. Medical Question Answering
4. Neuro-Signal Translation
5. Health Assessment Support
6. Physiological Signal Synthesis

Suggested entry format:

```markdown
| **Model/Study Name**<br>[Paper title](PAPER_URL) | 2026 | ECG | Answer generator | ECG question answering | Venue | [code](CODE_URL) |
```

### Inclusion note

This repository focuses on studies in which an LLM or language-model-style architecture plays a substantive role in medical time-series modeling, interpretation, reasoning, generation, or multimodal alignment. General medical LLM studies without a MedTS component and conventional time-series models without meaningful LLM involvement are outside the primary scope.

## 📑 Citation

If you find this review or repository useful, please consider citing our work. The final bibliographic information will be updated after publication.

```bibtex
@misc{han2026medtsllm,
  title  = {Large Language Models in Medical Time Series Analysis},
  author = {Han, Yu and Beyan, Cigdem and Zhang, Xiang and Liu, Xiaofeng and Liu, Nan and Sun, Jimeng and Hong, Shenda and Ding, Cheng and Murino, Vittorio},
  year   = {2026},
  note   = {Review manuscript}
}
```

## ⭐ Stay Updated

We will continue to update this repository as new MedTSLLM models, datasets, benchmarks, and clinical applications emerge. If you find the resource useful, please consider giving the repository a ⭐ and submitting an Issue or Pull Request when relevant work is missing.

---

**Maintained by the authors of the review.**