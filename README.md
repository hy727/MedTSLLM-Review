# Large Language Models in Medical Time Series Analysis

<p align="center">
  <b>An actively updated collection of studies on Large Language Models for Medical Time Series Analysis (MedTSLLMs)</b>
</p>

This repository accompanies our review:

> **Large Language Models in Medical Time Series Analysis**  
> Yu Han, Cigdem Beyan, Xiang Zhang, Xiaofeng Liu, Nan Liu, Jimeng Sun, Shenda Hong, Cheng Ding, and Vittorio Murino

Medical time series (MedTS), including electrocardiograms (ECG), electroencephalograms (EEG), photoplethysmography (PPG), vital signs, and wearable sensor data, are central to clinical diagnosis and health monitoring. This repository provides an actively maintained collection of studies on the integration of large language models (LLMs) with MedTS.

The repository complements our review by providing a continuously updated resource for newly published MedTSLLM studies beyond those included in the manuscript.

⭐ If you find this repository useful, please consider giving it a star to follow future updates.

---

## 📢 News

- **[2026-09]** Repository released.
- **[2026-XX]** Review paper released. *(Paper link will be added here.)*

---

## 📖 About This Review

Our review provides a structured overview of MedTSLLMs from both methodological and clinical perspectives.

We examine:

- MedTS tokenization and signal representation
- LLM architectures and model integration
- Pre-training and fine-tuning strategies
- Prompting strategies and prompt-template design
- Clinical applications of MedTSLLMs
- Evaluation protocols
- Challenges and future opportunities for real-world deployment

We use **MedTSLLM** as a broad term for LLM-based approaches to medical time-series analysis. These approaches may integrate language models with signal encoders, multimodal alignment modules, retrieval systems, or other task-specific components for representation learning, signal-language alignment, reasoning, generation, and agent-based analysis.

---

## 📚 Paper Collection

The papers are organized according to the six major application scenarios discussed in our review.

### 🩺 Medical Disease Diagnosis

| Method | Year | Modality | Main Task | Paper | Code |
|---|---:|---|---|---|---|
| HeartBEiT | 2023 | ECG | Cardiac disease diagnosis | [Paper](LINK) | [Code](https://github.com/akhilvaid/HeartBEiT) |
| ECGBERT | 2023 | ECG | Arrhythmia / sleep apnea diagnosis | [Paper](LINK) | - |
| MERL-CKEPE | 2024 | ECG | Zero-shot ECG classification | [Paper](LINK) | [Code](https://github.com/cheliu-computation/MERL) |
| ETP | 2024 | ECG | ECG representation / diagnosis | [Paper](LINK) | - |
| MedualTime | 2024 | ECG / EEG | Medical time-series classification | [Paper](LINK) | [Code](https://github.com/start2020/MedualTime) |
| GEM | 2025 | ECG | Grounded ECG understanding | [Paper](LINK) | [Code](https://github.com/lanxiang1017/GEM) |
| GPT-PPG | 2025 | PPG | Physiological signal diagnosis | [Paper](LINK) | - |
| ZETA | 2026 | ECG | Zero-shot ECG diagnosis | [Paper](LINK) | [Code](https://github.com/Tang-Jia-Lu/Zeta) |

---

### 📝 Clinical Report Generation

| Method | Year | Modality | Main Task | Paper | Code |
|---|---:|---|---|---|---|
| JoLT | 2023/2024 | ECG | ECG interpretation | [Paper](LINK) | - |
| SignalGPT | 2023 | Biosignals | Biomedical report generation | [Paper](LINK) | - |
| MEIT | 2025 | ECG | ECG report generation | [Paper](LINK) | [Code](https://github.com/AIoT-MLSys-Lab/MEIT) |
| ECG-Chat | 2025 | ECG | ECG report generation | [Paper](LINK) | [Code](https://github.com/YubaoZhao/ECG-Chat) |
| ECG-ReGen | 2025 | ECG | Report generation / QA | [Paper](LINK) | - |
| ECG-Bench | 2025 | ECG | Retrieval-augmented report generation | [Paper](LINK) | [Code](https://github.com/willxxy/ECG-Bench) |
| DiagECG | 2025 | ECG | Diagnostic report generation | [Paper](LINK) | - |

---

### 💬 Medical Question Answering

| Method | Year | Modality | Main Task | Paper | Code |
|---|---:|---|---|---|---|
| ECG-QA | 2023 | ECG | ECG question answering | [Paper](LINK) | - |
| openCHA | 2023 | Wearable | Conversational health assistant | [Paper](LINK) | [Code](https://github.com/Institute4FutureHealth/CHA) |
| PULSE | 2024/2025 | ECG | ECG visual QA | [Paper](LINK) | [Code](https://github.com/AIMedLab/PULSE) |
| ECG-LM | 2025 | ECG | ECG QA / interpretation | [Paper](LINK) | - |
| CHA-PPGHR | 2025 | PPG | Heart-rate analysis agent | [Paper](LINK) | [Code](https://github.com/mohammadfeli/CHA-PPGHR) |
| ECG-Expert-QA | 2025 | ECG | Expert-level ECG QA | [Paper](LINK) | [Code](https://github.com/Zaozzz/ECG-Expert-QA) |
| EEG-MedRAG | 2025 | EEG | Retrieval-augmented EEG QA | [Paper](LINK) | [Code](https://github.com/yi9206413-boop/EEG-MedRAG) |

---

### 🧠 Neuro-Signal Translation

| Method | Year | Modality | Main Task | Paper | Code |
|---|---:|---|---|---|---|
| DeWave | 2023 | EEG | EEG-to-text | [Paper](LINK) | [Code](https://github.com/duanyiqun/DeWave) |
| BELT | 2024 | EEG | EEG-language alignment | [Paper](LINK) | - |
| BELT-2 | 2024 | EEG | Multi-task brain decoding | [Paper](LINK) | - |
| Neuro-GPT | 2024 | EEG | EEG foundation modeling | [Paper](LINK) | [Code](https://github.com/wenhui0206/NeuroGPT) |
| Thought2Text | 2025 | EEG | EEG-to-text generation | [Paper](LINK) | [Code](https://github.com/abhijitmishra/Thought2Text) |

---

### ⌚ Health Assessment Support

| Method | Year | Modality | Main Task | Paper | Code |
|---|---:|---|---|---|---|
| Health-Learner | 2023 | Wearable | General health prediction | [Paper](LINK) | - |
| ALPHA | 2023 | Physiological signals | Health assessment | [Paper](LINK) | [Code](https://github.com/McJackTang/LLM-HealthAssistant) |
| Health-LLM | 2024 | Wearable | Health prediction | [Paper](LINK) | [Code](https://github.com/mitmedialab/Health-LLM) |
| WDAI-LLM | 2024 | Wearable | Wearable data interpretation | [Paper](LINK) | - |
| PH-LLM | 2024 | Wearable | Personalized health reasoning | [Paper](LINK) | - |
| CBPM-LLaMA | 2024 | ECG / PPG | Cuffless blood pressure | [Paper](LINK) | - |
| SensorLM | 2025 | Wearable | Sensor-language modeling | [Paper](LINK) | - |

---

### 🫀 Physiological Signal Synthesis

| Method | Year | Modality | Main Task | Paper | Code |
|---|---:|---|---|---|---|
| Auto-TTE | 2023 | ECG | Text-to-ECG generation | [Paper](LINK) | [Code](https://github.com/TClife/text_to_ecg) |
| DiffuSETS | 2024 | ECG | Text-conditioned ECG synthesis | [Paper](LINK) | [Code](https://github.com/Raiiyf/DiffuSETS_Exp) |
| ECG-LLM | 2025 | ECG | ECG forecasting / restoration | [Paper](LINK) | [Code](https://github.com/dragonlfy/ECG-LLM) |
| BCG2ECG | 2025 | BCG / ECG | Physiological signal translation | [Paper](LINK) | - |

---

## 📊 Datasets and Benchmarks

Representative datasets and benchmarks used in MedTSLLM research include:

### ECG
- PTB-XL
- MIMIC-IV-ECG
- ECG-QA
- ECGInstruct
- ECG-Expert-QA
- CPSC2018
- CODE-15
- Chapman

### EEG
- ZuCo
- TUH EEG
- CHB-MIT
- Sleep-EDF
- FACED

### Wearable and Physiological Sensors
- Fitbit datasets
- WESAD
- PAMAP2
- PMData
- LifeSnaps
- GLOBEM

This section will be continuously expanded as new datasets and benchmarks become available.

---

## 🆕 Recent Additions

This section tracks relevant studies that appeared after the literature collection used for the current version of our review.

<!--
Example:

- **[2026] Model Name** — Paper title.  
  Modality: ECG  
  Application: Medical Disease Diagnosis  
  [[Paper]](LINK) [[Code]](LINK)
-->

---

## 🤝 Contributing

We welcome contributions from the community to keep this repository up to date.

If you would like to add a relevant MedTSLLM study, please open an **Issue** or submit a **Pull Request**.

When submitting a paper, please provide:

- Paper title
- Authors
- Publication venue and year
- Paper URL
- Code/model URL, if available
- Medical time-series modality
- Main clinical application
- Brief description of the role of the LLM

Suggested Markdown format:

```markdown
- **[Venue, Year] Model Name**: Paper title. [[Paper]](LINK) [[Code]](LINK)
