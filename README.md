# A Survey on Audio-Visual Large Language Models (AV-LLMs)

> Official repository for the paper: **“A Survey on Audio-Visual Large Language Models”**  
> Wenyi Yao, Roksana Yahyaabadi, Hossein Hassani, and Soodeh Nikan

[Paper](./paper/Survey.pdf) · [Datasets CSV](./dataset.md) · [Model List](./data/models.csv)

[![AV-LLMs timeline](figures/AV-LLMs.png)](figures/AV-LLMs.pdf)

---

## ✨ Highlights
- **First dedicated survey on AV-LLMs.** We position AV-LLMs as a distinct research line beyond VLMs.  
- **Unified taxonomy.** We categorize by **modality scope**, **backbone origin**, and **generation objective**.  
- **Datasets crosswalk.** A task→dataset mapping for image–text, video–text, audio–text, and audio–video–text.  
- **Architecture & training.** Encoders, adapters/Q-Formers, alignment objectives, instruction tuning.  
- **Applications.** Audio/Video captioning, multimodal dialogue, cross-modal retrieval.  
- **Challenges & Outlook.** hallucination, social biases, computational cost.

---

## Table of Contents

1. [Model Taxonomy](#1-model-taxonomy)  
2. [Datasets](#2-datasets)
3. [Performance Evaluation](#3-performance-evaluation)
4. [Applications](#4-applications)
5. [How to Cite](#5-how-to-cite) 

---

## 1. Model Taxonomy
![Model taxonomy overview](./figures/taxonomy.png)

---

## 2. Datasets
See [`./tables/datasets.csv`](./tables/datasets.csv) for *30 +* curated resources with modality flags, licenses and download scripts.

---

## 3. Performance Evaluation

<p align="center">
  <img src="./figures/perf-vqa.png" alt="VideoQA accuracy" width="90%"><br/>
  <em>(b) Open-ended / MC VideoQA accuracy.</em>
</p>

<p align="center">
  <img src="./figures/perf-retrieval.png" alt="Zero-shot retrieval R@1 across datasets" width="90%"><br/>
  <em>(a) Zero-shot retrieval (T→V / V→T) R@1 on common benchmarks.</em>
</p>

<p align="center">
  <img src="./figures/perf-audio.png" alt="Audio tasks performance" width="90%"><br/>
  <em>(c) Audio-related tasks (captioning / ASR-explanation / WER, etc.).</em>
</p>

---

## 4. Applications

<p align="center">
  <img src="./figures/application.png" alt="Application landscape of AV-LLMs" width="90%">
</p>

---

## 5. How to Cite
```bibtex
  number  = {x},
  year    = {2025},
  note    = {arXiv:2404.xxxxx}
}

