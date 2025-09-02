# A Survey on Audio-Visual Large Language Models (AV-LLMs)

> Official repository for the paper: **“A Survey on Audio-Visual Large Language Models”**  
> Wenyi Yao, Roksana Yahyaabadi, Hossein Hassani, and Soodeh Nikan (Western University)

[PDF](./paper/Survey-3.pdf) · [Project Page](#) · [Datasets CSV](./pretraining-dataset.md) · [Model List](./data/models.csv)

[![AV-LLMs timeline](figures/AV-LLMs.png)](figures/AV-LLMs.pdf)

---

## ✨ Highlights
- **First dedicated survey on AV-LLMs.** We position AV-LLMs as a distinct research line beyond VLMs.  
- **Unified taxonomy.** We categorize by **modality scope**, **backbone origin**, and **generation objective**.  
- **Datasets crosswalk.** A task→dataset mapping for image–text, video–text, audio–text, and audio–video–text.  
- **Architecture & training.** Encoders, adapters/Q-Formers, tokenization, alignment objectives, instruction tuning.  
- **Applications.** Audio/Video captioning, multimodal dialogue, cross-modal retrieval.  
- **Challenges & Outlook.** Long-range temporal cost, hallucination mitigation, data alignment, safety & reliability.

---

## ✨ Quick links
| Item | Link |
|------|------|
| 📄 Paper (PDF) | `./paper/AVLLM_survey.pdf` |
| 🖼️ Key Figures | `./figures/` |
| 📊 Master Tables (CSV) | `./tables/` |
| 💬 Discussion | [GitHub Issues](https://github.com/your-org/av-llm-survey/issues) |
| 📜 License | [CC-BY-4.0](LICENSE) |

---

## Table of Contents
1. [Introduction](#1-introduction)
2. [Background & History](#2-background--history)  
   2.1 Transformers  
   2.2 Large Language Models  
   2.3 Vision–Language Models  
3. [Pre-training Datasets](#3-pre-training-datasets)
4. [Model Taxonomy](#4-model-taxonomy)  
   4.1 **Extended multimodal** (frozen backbones)  
   4.2 **From-scratch end-to-end**  
   4.3 **Backbone-based Alignment**  
   4.4 **Any-to-Any Generative Diffusion**
5. [Applications](#5-applications)  
   5.1 Video Understanding  
   5.2 Audio & Video Captioning  
   5.3 Conversational AI  
   5.4 Cross-modal Retrieval  
6. [Limitations & Open Problems](#6-limitations--open-problems)
7. [Future Directions](#7-future-directions)
8. [How to Cite](#8-how-to-cite)
9. [Contributing](#9-contributing)
10. [Acknowledgements](#10-acknowledgements)

---

## 1. Introduction
Audio-Visual Language Models (AVLMs) **extend Vision–Language Models by adding an auditory channel**.  
They enable machines to reason over images, video, sound and text *simultaneously*, unlocking tasks such as

* open-ended video question answering  
* scene-aware dialog  
* cross-modal generation (text → audio, video → caption, …)  


---

## 2. Background & History
### 2.1 Transformers
Global self-attention (Vaswani *et al.*, 2017) removed recurrency & convolution, opening a path to multimodal fusion.

### 2.2 Large Language Models (LLMs)
* **Encoder-only** (BERT, RoBERTa) – strong for understanding  
* **Decoder-only** (GPT family) – strong for generation  
* **Encoder–Decoder** (T5, PaLM) – sequence-to-sequence workhorses  
* **Mixture-of-Experts** – scale capacity without quadratic FLOPs

### 2.3 Vision–Language Models (VLMs)
Contrastive (CLIP), masked (FLAVA), generative (BLIP-2) and unified backbones (Kosmos, CogVLM) laid the foundation for adding **audio**.

> **Key takeaway:** AV-LLMs inherit the transformer stack but must *bond waveforms with pixels & tokens*.

---

## 3. Pre-training Datasets
| Task family | Example sets | Scale |
|-------------|--------------|-------|
| Image–Text Alignment | COCO, LAION-2B, CC-12M | 10⁶ – 10⁹ pairs |
| Video–Audio–Text | HowTo100M, WebVid-10M | 10⁶ clips |
| Speech–Text | LibriSpeech, AudioCaps, WavCaps | 10² – 10⁵ h |
| Pure Audio | AudioSet, VGGSound | 10⁶ clips |

See [`./tables/datasets.csv`](./tables/datasets.csv) for *30 +* curated resources with modality flags, licenses and download scripts.

---

## 4. Model Taxonomy
We group **43** public models into four archetypes:

| Category | Representatives | One-line summary |
|----------|-----------------|------------------|
| **Model with addtional modalities** | IMAGEBIND, OneLLM, PandaGPT | Plug frozen encoders + lightweight adapters into an LLM |
| **From-scratch** | VATT, MERLOT-Reserve, IMP | Jointly learn AV + T tokens end-to-end |
| **Backbone-based Alignment** | VALOR, Video-SALMONN, Dolphin | Contrastive / Q-Former bridges between CLIP, Whisper & LLaMA |
| **Any-to-Any Diffusion** | CoDi-2, NExT-GPT, C3Net | LLM conditions latent-diffusion for cross-modal generation |

Detailed comparison tables live in [`./tables/models.csv`](./tables/models.csv).

---

## 5. Applications
### 5.1 Video Understanding
AV-LLMs push state-of-the-art on MC-VQA, OE-VQA, AV-QA benchmarks such as STAR, Ego4D and MSRVTT-QA.

### 5.2 Audio & Video Captioning
Models like **VideoLLaMA-2** and **VAST** produce coherent, multi-sentence descriptions that blend what is *seen* and *heard*.

### 5.3 Conversational AI
X-InstructBLIP, OneLLM and PandaGPT demonstrate multi-turn dialog grounded in images, video segments and soundtracks.

### 5.4 Cross-modal Retrieval
GRAM, IMAGEBIND and CLIP4VLA align N modalities into a single embedding space for text ↔ audio/video search.

---

## 6. Limitations & Open Problems
* **Hallucination** – frozen LLM cores may invent non-existent sounds/objects.  
* **Long-range reasoning** – minute-scale videos strain GPU memory.  
* **Dataset gaps** – few large, license-clean AV-T corpora.  
* **Bias & safety** – multimodal toxicity and privacy issues under-explored.

---

## 7. Future Directions
* **Token pruning & VoRA** to trim latency without losing context.  
* **Embodied & edge deployment** for robotics, autonomous driving, AR.  
* **Healthcare audio** (heart, lung, respiratory) fused with vision for diagnostics.  
* **Explainability**: grounding every generated phrase in both waveform and pixel evidence.

---

## 8. How to Cite
```bibtex
  number  = {8},
  year    = {2015},
  note    = {arXiv:2404.xxxxx}
}
