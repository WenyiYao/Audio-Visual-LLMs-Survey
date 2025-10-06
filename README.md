# A Survey on Audio-Visual Large Language Models (AV-LLMs)

> Official repository for the paper: **“A Survey on Audio-Visual Large Language Models”**  
> Wenyi Yao, Roksana Yahyaabadi, Hossein Hassani, and Soodeh Nikan

[Paper](./paper/Survey.pdf) · [Datasets](./dataset.md) · [Model List](./data/models.csv)

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
| Title                                                                                                 | Model            | Code                                                        | Paper                                                                                                                                                                                        |
| ----------------------------------------------------------------------------------------------------- | ---------------- | ----------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CREMA: Generalizable and Efficient Video-Language Reasoning via Multimodal Modular Fusion             | CREMA            | [GitHub](https://github.com/Yui010206/CREMA)                | [arXiv](https://arxiv.org/abs/2402.05889) ([GitHub][1])                                                                                                                                      |
| ImageBind: One Embedding Space to Bind Them All                                                       | ImageBind        | [GitHub](https://github.com/facebookresearch/ImageBind)     | [arXiv](https://arxiv.org/abs/2305.05665)                                                                                                                                                    |
| Extending Video-Language Pretraining to N-modality by Language-binding: A Multimodal Foundation Model | LanguageBind     | [GitHub](https://github.com/PKU-YuanGroup/LanguageBind)     | [arXiv](https://arxiv.org/abs/2308.12966)                                                                                                                                                    |
| Meta-Transformer: A Unified Framework for Multimodal Learning                                         | Meta-Transformer | —                                                           | [arXiv](https://arxiv.org/abs/2307.10802)                                                                                                                                                    |
| OneLLM: One Framework to Align All Modalities with Language                                           | OneLLM           | [GitHub](https://github.com/THU-KEG/OneLLM)                 | [Paper](https://openaccess.thecvf.com/content/CVPR2024/papers/Yang_OneLLM_One_Framework_to_Align_All_Modalities_with_Language_CVPR_2024_paper.pdf)                                           |
| PandaGPT: One Model to Instruction-Follow Them All                                                    | PandaGPT         | [GitHub](https://github.com/yxuansu/PandaGPT)               | [Project](https://pandagpt.github.io/)                                                                                                                                                       |
| X-InstructBLIP: Aligning X-Modal Instruction-Aware Q-Formers to LLMs                                  | X-InstructBLIP   | —                                                           | [arXiv](https://arxiv.org/abs/2312.06738)                                                                                                                                                    |
| Imp: Highly Capable Large Multimodal Models for Mobile Devices                                        | IMP              | —                                                           | [arXiv](https://arxiv.org/abs/2405.12107) ([arXiv][2])                                                                                                                                       |
| MERLOT Reserve: Neural Script Knowledge through Vision, Language and Sound                            | MERLOT Reserve   | [GitHub](https://github.com/rowanz/merlot_reserve)          | [arXiv](https://arxiv.org/abs/2201.02639) ([GitHub][3])                                                                                                                                      |
| VATT: Transformers for Multimodal Self-Supervised Learning from Raw Video, Audio and Text             | VATT             | —                                                           | [arXiv](https://arxiv.org/abs/2104.11178) ([bubo-gpt.github.io][4])                                                                                                                          |
| Audio-Visual LLM for Video Understanding                                                              | AV-LLM           | —                                                           | [arXiv](https://arxiv.org/abs/2312.06720) ([arXiv][5])                                                                                                                                       |
| Bridging High-Quality Audio and Video via Language for Sound Effects Retrieval from Visual Queries    | AV-SFX           | —                                                           | [arXiv](https://arxiv.org/abs/2308.09089) ([arXiv][6])                                                                                                                                       |
| Empowering LLMs with Pseudo-Untrimmed Videos for Audio-Visual Understanding                           | AVicuna          | —                                                           | [AAAI 2025](https://ojs.aaai.org/index.php/AAAI/article/download/32784/34939) ([GitHub][7])                                                                                                  |
| BuboGPT: Enabling Visual Grounding in Multi-Modal LLMs                                                | BuboGPT          | [GitHub](https://github.com/magic-research/bubogpt)         | [arXiv](https://ui.adsabs.harvard.edu/abs/2023arXiv230708581Z/abstract) ([GitHub][8])                                                                                                        |
| Accommodating Audio Modality in CLIP for Multimodal Processing (CLIP4VLA)                             | CLIP4VLA         | —                                                           | [AAAI](https://ojs.aaai.org/index.php/AAAI/article/view/26153) ([ojs.aaai.org][9])                                                                                                           |
| Dolphin: Audio-Visual Large Language Model for Speech Understanding                                   | Dolphin          | —                                                           | [arXiv](https://arxiv.org/abs/2408.03930) ([haon-chen.github.io][10])                                                                                                                        |
| EchoInk-R1: Listening, Looking and Reading with Audio-Visual-Language Models                          | EchoInk-R1       | —                                                           | [arXiv](https://arxiv.org/abs/2408.09341) ([arXiv][11])                                                                                                                                      |
| FAVOR: Fine-grained Audio-Visual Joint Representations for Multimodal Large Language Models           | FAVOR            | [GitHub](https://github.com/BriansIDP/AudioVisualLLM)       | [OpenReview](https://openreview.net/forum?id=wD8L86iCvD) ([GitHub][12])                                                                                                                      |
| GRAM                                                                                                  | GRAM             | —                                                           | — *(待补：同名论文较多，尚未定位与截图一致的 AV-LLM 论文)*                                                                                                                                                         |
| InternVideo2: Scaling Video Foundation Models for Multimodal Understanding                            | InternVideo2     | [GitHub](https://github.com/OpenGVLab/InternVideo2)         | [arXiv](https://arxiv.org/abs/2404.13202) ([arXiv][13])                                                                                                                                      |
| Lyra: An Efficient and Speech-Centric Framework for Omni-Cognition                                    | Lyra             | [GitHub](https://github.com/dvlab-research/Lyra)            | [arXiv](https://arxiv.org/abs/2412.09501) ([GitHub][14])                                                                                                                                     |
| Macaw-LLM: Multi-Modal Language Modeling with Image, Audio, Video, and Text Integration               | MACAW-LLM        | [GitHub](https://github.com/lyuchenyang/Macaw-LLM)          | [arXiv](https://arxiv.org/abs/2306.09093) ([GitHub][15])                                                                                                                                     |
| Meerkat: Audio-Visual Large Language Model for Grounding in Space and Time                            | Meerkat          | —                                                           | [arXiv](https://arxiv.org/abs/2407.01851) ([arXiv][16])                                                                                                                                      |
| MoshiVis: Vision-Speech Models — Teaching Speech Models to Converse about Images                      | MoshiVis         | [GitHub](https://github.com/kyutai-labs/moshivis)           | [arXiv](https://arxiv.org/abs/2503.15633) ([GitHub][17])                                                                                                                                     |
| UnIVAL: Unified Model for Image, Video, Audio and Language Tasks                                      | UnIVAL           | [GitHub](https://github.com/mshukor/UnIVAL)                 | [arXiv](https://arxiv.org/abs/2307.16184) ([arXiv][18])                                                                                                                                      |
| VALOR: Vision-Audio-Language Omni-Perception Pretraining Model and Dataset                            | VALOR            | [Project](https://casia-iva-group.github.io/projects/VALOR) | [arXiv](https://arxiv.org/abs/2304.08345) ([arXiv][19])                                                                                                                                      |
| VAST-27M: A Large-Scale Video, Audio, Subtitle Dataset                                                | VAST             | [GitHub](https://github.com/TXH-mercury/VAST)               | [Project](https://txh-mercury.github.io/VAST/)                                                                                                                                               |
| VideoChat: Chat-Centric Video Understanding                                                           | VideoChat        | [GitHub](https://github.com/OpenGVLab/Ask-Anything)         | [Paper](https://arxiv.org/abs/2305.06355) ([GitHub][20])                                                                                                                                     |
| Video-LLaMA: An Instruction-tuned Audio-Visual Language Model for Video Understanding                 | Video-LLaMA      | [GitHub](https://github.com/DAMO-NLP-SG/Video-LLaMA)        | [arXiv](https://arxiv.org/abs/2306.02858) ([arXiv][21])                                                                                                                                      |
| VideoLLaMA 2: Advancing Spatial-Temporal Modeling and Audio Understanding                             | VideoLLaMA 2     | [GitHub](https://github.com/DAMO-NLP-SG/VideoLLaMA2)        | [arXiv](https://arxiv.org/abs/2406.07476)                                                                                                                                                    |
| video-SALMONN: Speech-Enhanced Audio-Visual Large Language Models                                     | video-SALMONN    | [GitHub](https://github.com/BytedanceResearch/SALMONN)      | [ICML Poster / arXiv](https://icml.cc/virtual/2024/poster/33117) ([icml.cc][22])                                                                                                             |
| VITA: Towards Open-Source Interactive Omni Multimodal LLM                                             | VITA             | [GitHub](https://github.com/VITA-MLLM/VITA)                 | [arXiv](https://arxiv.org/abs/2408.05211) ([GitHub][23])                                                                                                                                     |
| X-LLM: Bootstrapping Advanced LLMs by Treating Multi-Modalities as Foreign Languages                  | X-LLM            | [GitHub](https://github.com/phellonchen/X-LLM)              | [arXiv](https://arxiv.org/abs/2305.04160) ([GitHub][24])                                                                                                                                     |
| AnyGPT: Unified Multimodal Understanding and Generation with Any-to-Any Modality                      | AnyGPT           | [GitHub](https://github.com/OpenGVLab/AnyGPT)               | [arXiv](https://arxiv.org/abs/2310.06400)                                                                                                                                                    |
| C3LLM: Conditional Multimodal Content Generation Using Large Language Models                          | C3LLM            | —                                                           | [arXiv](https://arxiv.org/abs/2405.16136) ([arXiv][25])                                                                                                                                      |
| C3Net: Compound Conditioned ControlNet for Multimodal Content Generation                              | C3Net            | —                                                           | [CVPR 2024](https://openaccess.thecvf.com/content/CVPR2024/papers/Zhang_C3Net_Compound_Conditioned_ControlNet_for_Multimodal_Content_Generation_CVPR_2024_paper.pdf) ([CVF Open Access][26]) |
| CLIPSonic: Text-to-Audio Synthesis with Unlabeled Videos and Pretrained Language-Vision Models        | CLIPSonic        | —                                                           | [arXiv](https://arxiv.org/abs/2402.04746)                                                                                                                                                    |
| CLIPSynth: Learning Text-to-Audio Synthesis from Videos via CLIP                                      | CLIPSynth        | —                                                           | [arXiv](https://arxiv.org/abs/2406.18318)                                                                                                                                                    |
| CoDi: Any-to-Any Generation via Composable Diffusion                                                  | CoDi             | [Project](https://codi-gen.github.io/)                      | [arXiv](https://arxiv.org/abs/2305.11846) ([CoDi][27])                                                                                                                                       |
| CoDi-2: In-Context, Interleaved, and Interactive Any-to-Any Generation                                | CoDi-2           | [Project](https://codi-2.github.io/)                        | [CVPR 2024](https://openaccess.thecvf.com/content/CVPR2024/papers/Tang_CoDi-2_In-Context_Interleaved_and_Interactive_Any-to-Any_Generation_CVPR_2024_paper.pdf) ([codi-2.github.io][28])     |
| EMOVA                                                                                                 | EMOVA            | —                                                           | — *(待补：未找到与截图一致的权威链接)*                                                                                                                                                                       |
| MoCha                                                                                                 | MoCha            | —                                                           | — *(待补：同名工作较多，需确认具体论文)*                                                                                                                                                                      |
| NExT-GPT: Any-to-Any Multimodal LLM                                                                   | NExT-GPT         | [GitHub](https://github.com/NExT-GPT/NExT-GPT)              | [arXiv](https://arxiv.org/abs/2309.05519) ([GitHub][29])                                                                                                                                     |
| SonicVisionLM: Playing Sound with Vision-Language Models                                              | SonicVisionLM    | [GitHub](https://github.com/Yusiissy/SonicVisionLM)         | [arXiv](https://arxiv.org/abs/2401.04394) ([GitHub][30])                                                                                                                                     |

[1]: https://github.com/Yui010206/CREMA?utm_source=chatgpt.com "[ICLR 2025] CREMA: Generalizable and Efficient Video- ..."
[2]: https://arxiv.org/html/2405.12107v1?utm_source=chatgpt.com "Highly Capable Large Multimodal Models for Mobile Devices"
[3]: https://github.com/bytedance/Dolphin?utm_source=chatgpt.com "The official repo for “Dolphin: Document Image Parsing via ..."
[4]: https://bubo-gpt.github.io/?utm_source=chatgpt.com "BuboGPT"
[5]: https://arxiv.org/abs/2312.06720?utm_source=chatgpt.com "[2312.06720] Audio-Visual LLM for Video Understanding"
[6]: https://arxiv.org/abs/2308.09089?utm_source=chatgpt.com "Bridging High-Quality Audio and Video via Language for ..."
[7]: https://github.com/schowdhury671/meerkat?utm_source=chatgpt.com "schowdhury671/meerkat"
[8]: https://github.com/magic-research/bubogpt?utm_source=chatgpt.com "BuboGPT: Enabling Visual Grounding in Multi-Modal LLMs"
[9]: https://ojs.aaai.org/index.php/AAAI/article/view/26153?utm_source=chatgpt.com "Accommodating Audio Modality in CLIP for Multimodal ..."
[10]: https://haon-chen.github.io/MoCa/?utm_source=chatgpt.com "MoCa: Modality-aware Continual Pre-training Makes Better ..."
[11]: https://arxiv.org/abs/2311.18775?utm_source=chatgpt.com "CoDi-2: In-Context, Interleaved, and Interactive Any-to-Any Generation"
[12]: https://github.com/BriansIDP/AudioVisualLLM?utm_source=chatgpt.com "BriansIDP/AudioVisualLLM"
[13]: https://arxiv.org/abs/2310.05863?utm_source=chatgpt.com "Fine-grained Audio-Visual Joint Representations for Multimodal Large Language Models"
[14]: https://github.com/dvlab-research/Lyra?utm_source=chatgpt.com "An Efficient and Speech-Centric Framework for Omni- ..."
[15]: https://github.com/lyuchenyang/Macaw-LLM?utm_source=chatgpt.com "Macaw-LLM: Multi-Modal Language Modeling with Image, ..."
[16]: https://arxiv.org/abs/2407.01851?utm_source=chatgpt.com "Meerkat: Audio-Visual Large Language Model for Grounding in Space and Time"
[17]: https://github.com/kyutai-labs/moshivis?utm_source=chatgpt.com "kyutai-labs/moshivis: Kyutai with an \"eye\""
[18]: https://arxiv.org/abs/2307.16184?utm_source=chatgpt.com "UnIVAL: Unified Model for Image, Video, Audio and Language Tasks"
[19]: https://arxiv.org/abs/2304.08345?utm_source=chatgpt.com "VALOR: Vision-Audio-Language Omni-Perception Pretraining Model and Dataset"
[20]: https://github.com/OpenGVLab/Ask-Anything?utm_source=chatgpt.com "OpenGVLab/Ask-Anything"
[21]: https://arxiv.org/abs/2306.02858?utm_source=chatgpt.com "Video-LLaMA: An Instruction-tuned Audio-Visual Language Model ..."
[22]: https://icml.cc/virtual/2024/poster/33117?utm_source=chatgpt.com "Speech-Enhanced Audio-Visual Large Language Models"
[23]: https://github.com/VITA-MLLM/VITA?utm_source=chatgpt.com "VITA-1.5: Towards GPT-4o Level Real-Time Vision and ..."
[24]: https://github.com/phellonchen/X-LLM?utm_source=chatgpt.com "X-LLM: Bootstrapping Advanced Large Language Models ... - GitHub"
[25]: https://arxiv.org/abs/2405.16136?utm_source=chatgpt.com "C3LLM: Conditional Multimodal Content Generation Using ..."
[26]: https://openaccess.thecvf.com/content/CVPR2024/papers/Zhang_C3Net_Compound_Conditioned_ControlNet_for_Multimodal_Content_Generation_CVPR_2024_paper.pdf?utm_source=chatgpt.com "C3Net: Compound Conditioned ControlNet for Multimodal ..."
[27]: https://codi-gen.github.io/?utm_source=chatgpt.com "CoDi: Generate Anything from Anything All At Once through ..."
[28]: https://codi-2.github.io/?utm_source=chatgpt.com "CoDi-2: Interleaved and In-Context Any-to-Any Generation"
[29]: https://github.com/NExT-GPT/NExT-GPT?utm_source=chatgpt.com "Code and models for ICML 2024 paper, NExT-GPT"
[30]: https://github.com/Yusiissy/SonicVisionLM?utm_source=chatgpt.com "Yusiissy/SonicVisionLM"

---

## 2. Datasets
| **Task**                  | **Dataset**                                                                                     | **Year** | **Modalities**                      | **Data Scale**                                       |
| ------------------------- | ----------------------------------------------------------------------------------------------- | -------: | ----------------------------------- | ---------------------------------------------------- |
| **Image–Text**            | [SBU](https://www.cs.rice.edu/~vo9/sbucaptions/)                                                |     2011 | Image, Text                         | 1M images with captions                              |
|                           | [COCO](http://cocodataset.org/)                                                                 |     2014 | Image, Text                         | 330K images, 5 captions each                         |
|                           | [Visual Genome (VG)](https://homes.cs.washington.edu/~ranjay/visualgenome/index.html)           |     2017 | Image, Text                         | 108K images, dense annotations                       |
|                           | [CC3M](https://ai.google.com/research/ConceptualCaptions/)                                      |     2018 | Image, Text                         | 3M images with captions                              |
|                           | [CC12M](https://github.com/google-research-datasets/conceptual-12m)                             |     2021 | Image, Text                         | 12M images with captions                             |
|                           | [LAION-400M](https://laion.ai/blog/laion-400-open-dataset/)                                     |     2021 | Image, Text                         | 400M image–text pairs                                |
|                           | [LAION-2B](https://laion.ai/blog/large-openclip/)                                               |     2021 | Image, Text                         | 2B image–text pairs                                  |
|                           | [LAION-COCO](https://laion.ai/blog/laion-coco/)                                                 |     2022 | Image, Text                         | ~600M generated captions for web images (COCO-style) |
| **VQA**                   | [VQAv2](https://visualqa.org/)                                                                  |     2017 | Image, Text                         | 265K images, 1.1M QA pairs                           |
|                           | [GQA](https://cs.stanford.edu/people/dorarad/gqa/)                                              |     2019 | Image, Text                         | 113K images, 22M QA pairs                            |
|                           | [OCR-VQA–200K](https://ocr-vqa.github.io)                                                       |     2019 | Image, Text                         | ~1M QA pairs for OCR                                 |
| **Visual Grounding**      | [RefCOCO](https://github.com/lichengunc/refer)                                                  |     2014 | Image, Text                         | 142K referring expressions                           |
|                           | [RefCOCO+](https://github.com/lichengunc/refer)                                                 |     2014 | Image, Text                         | 141K referring expressions                           |
|                           | [RefCOCOg](https://github.com/lichengunc/refer)                                                 |     2016 | Image, Text                         | 104K referring expressions                           |
| **Video–Text**            | [Charades](https://prior.allenai.org/projects/charades)     |     2016 | Video, Text                         | 9.8K videos, 80K+ action labels                      |
|                           | [How2](https://srvk.github.io/how2-dataset/)          |     2018 | Video, Audio, Text                  | ~2K hours instructional videos                       |
|                           | [HowTo100M](https://www.di.ens.fr/willow/research/howto100m/)                                   |     2019 | Video, Text                         | 136M video clips                                     |
|                           | [AVSD](https://video-dialog.com)                                                                |     2019 | Video, Audio, Text                  | 11K dialogues from 1.8K videos                       |
|                           | [WebVid-2.5M (a.k.a. WebVid-2M)](https://www.robots.ox.ac.uk/~vgg/research/frozen-in-time/)     |     2021 | Video, Text                         | 2.5M video–text pairs                                |
|                           | [WebVidQA](https://antoyang.github.io/just-ask.html)                                            |     2021 | Video, Text                         | QA pairs on web videos                               |
|                           | [Ego4D](https://ego4d-data.org/)                                                                |     2022 | Video, Text, IMU                    | ~3.6K hours egocentric videos                        |
|                           | [VALOR-1M](https://casia-iva-group.github.io/projects/VALOR)                                    |     2023 | Video, Text                         | 1M video–text pairs                                  |
|                           | [VAST-27M](https://github.com/TXH-mercury/VAST)                                                 |     2023 | Video, Audio, Subtitle              | 27M video clips                                      |
|                           | [PANDA-70M](https://snap-research.github.io/Panda-70M/)                                         |     2024 | Video, Audio, Text                  | 70M labeled instances                                |
|                           | AVU-dataset (Aligned A/V Understanding)                                                         |     2025 | Video, Audio, Text                  | 5.2M AV captions & Q&A tuples                        |
| **Audio–Text**            | [BBC Sound Effects](https://sound-effects.bbcrewind.co.uk)                                      |      N/A | Audio, Text                         | ~30K sound effects                                   |
|                           | [LibriSpeech](http://www.openslr.org/12/)                                                       |     2015 | Audio, Text                         | 1000 hours of speech                                 |
|                           | [AudioCaps](https://audiocaps.github.io)                                                        |     2019 | Audio, Text                         | 46K clips with captions                              |
|                           | [Freesound 500K](https://freesound.org)                       |     2023 | Audio, Text                         | 500K+ sound clips                                    |
|                           | [WavCaps](https://github.com/XinhaoMei/WavCaps)                                                 |     2024 | Audio, Text                         | 403K audio–caption pairs                             |
| **Audio–Visual**           | [SoundNet](https://github.com/cvondrick/soundnet)                                               |     2016 | Audio, Video                        | 2M videos                                            |
|                           | [AudioSet](https://research.google.com/audioset/)                                               |     2017 | Audio, Video, Text                  | ~2M labeled 10s clips                                |
|                           | [MUSIC](https://github.com/roudimit/MUSIC_dataset)                                              |     2018 | Audio, Video                        | 685 music videos                                     |
|                           | [VGGSound](http://www.robots.ox.ac.uk/~vgg/data/vggsound/)                                      |     2020 | Audio, Video                        | 200K 10s video clips                                 |
| **Cross-Modal Alignment** | [VIDAL-10M (LanguageBind)](https://github.com/PKU-YuanGroup/LanguageBind/blob/main/DATASETS.md) |     2023 | Video, Infrared, Depth, Audio, Text | 10M labeled pairs                                    |

---

## 3. Performance Evaluation

<p align="center">
  <img src="./figures/perf-vqa.png" alt="VideoQA accuracy" width="90%"><br/>
  <em>(a) Open-ended / MC VideoQA accuracy.</em>
</p>

<p align="center">
  <img src="./figures/perf-retrieval.png" alt="Zero-shot retrieval R@1 across datasets" width="90%"><br/>
  <em>(b) Zero-shot retrieval (T→V / V→T) R@1 on common benchmarks.</em>
</p>

<p align="center">
  <img src="./figures/perf-audio.png" alt="Audio tasks performance" width="90%"><br/>
  <em>(c) Audio-related tasks (captioning / ASR-explanation / WER, etc.).</em>
</p>

---

## 4. Applications

<p align="center">
  <img src="./figures/application.png" alt="Application landscape of AV-LLMs" width="50%">
</p>

---

## 5. How to Cite
```bibtex
  number  = {x},
  year    = {2025},
  note    = {arXiv:2404.xxxxx}
}

