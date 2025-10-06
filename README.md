# A Survey on Audio-Visual Large Language Models (AV-LLMs)

> Official repository for the paper: **“A Survey on Audio-Visual Large Language Models”**  
> Wenyi Yao, Roksana Yahyaabadi, Hossein Hassani, and Soodeh Nikan

[Paper](./paper/Survey.pdf) · [Datasets](#2-datasets) · [Model List](#1-model-taxonomy)

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

---

## 1. Model Taxonomy
![Model taxonomy overview](./figures/taxonomy.png)
| Title                                                                                                 | Model            | Code                                                        | Paper                                                                                                                                                                                        |
| ----------------------------------------------------------------------------------------------------- | ---------------- | ----------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CREMA: Generalizable and Efficient Video-Language Reasoning via Multimodal Modular Fusion             | CREMA            | [GitHub](https://github.com/Yui010206/CREMA)                | [arXiv](https://arxiv.org/abs/2402.05889)                                                                                                                                   |
| ImageBind: One Embedding Space to Bind Them All                                                       | ImageBind        | [GitHub](https://github.com/facebookresearch/ImageBind)     | [arXiv](https://arxiv.org/abs/2305.05665)                                                                                                                                                    |
| LanguageBind: Extending Video-Language Pretraining to N-modality by Language-based Semantic Alignment | LanguageBind     | [GitHub](https://github.com/PKU-YuanGroup/LanguageBind)     | [arXiv](https://arxiv.org/abs/2310.01852)                                                                                                                                                    |
| Meta-Transformer: A Unified Framework for Multimodal Learning                                         | Meta-Transformer | [GitHub](https://github.com/invictus717/MetaTransformer)                                                        | [arXiv](https://arxiv.org/abs/2307.10802)                                                                                                                                                    |
| OneLLM: One Framework to Align All Modalities with Language                                           | OneLLM           | [GitHub](https://github.com/csuhan/OneLLM)                 | [arXiv](https://arxiv.org/abs/2312.03700)                                           |
| PandaGPT: One Model to Instruction-Follow Them All                                                    | PandaGPT         | [GitHub](https://github.com/yxuansu/PandaGPT)               | [arXiv](https://arxiv.org/abs/2305.16355)                                                                                                                                                       |
| X-InstructBLIP: A Framework for aligning X-Modal instruction-aware representations to LLMs and Emergent Cross-modal Reasoning      | X-InstructBLIP   | [GitHub](https://github.com/salesforce/LAVIS/tree/main/projects/xinstructblip)                                                           | [arXiv](https://arxiv.org/abs/2311.18799)                                                                                                                                                    |
| Alternating Gradient Descent and Mixture-of-Experts for Integrated Multimodal Perception              | IMP              | —                                                           | [arXiv](https://arxiv.org/abs/2305.06324)                                                                                                                                       |
| MERLOT Reserve: Neural Script Knowledge through Vision and Language and Sound                            | MERLOT Reserve   | [GitHub](https://github.com/rowanz/merlot_reserve)          | [arXiv](https://arxiv.org/abs/2201.02639)                                                                                                                                     |
| VATT: Transformers for Multimodal Self-Supervised Learning from Raw Video, Audio and Text             | VATT             | [GitHub](https://github.com/google-research/google-research/tree/master/vatt)                                                           | [arXiv](https://arxiv.org/abs/2104.11178)                                                                                                                          |
| Audio-Visual LLM for Video Understanding                                                              | AV-LLM           | —                                                          | [arXiv](https://arxiv.org/abs/2312.06720)                                                                                                                                     |
| Bridging High-Quality Audio and Video via Language for Sound Effects Retrieval from Visual Queries    | AV-SFX           | —                                                           | [arXiv](https://arxiv.org/abs/2308.09089)                                                                                                                                     |
| Empowering LLMs with Pseudo-Untrimmed Videos for Audio-Visual Temporal Understanding                  | AVicuna          | —                                                           | [arXiv](https://arxiv.org/abs/2403.16276)                                                                                              |
| BuboGPT: Enabling Visual Grounding in Multi-Modal LLMs                                                | BuboGPT          | [GitHub](https://github.com/magic-research/bubogpt)         | [arXiv](https://arxiv.org/abs/2307.08581)                                                                                                      |
| Accommodating Audio Modality in CLIP for Multimodal Processing                             | CLIP4VLA         | [GitHub](https://github.com/ludanruan/CLIP4VLA)                                                           | [arXiv](https://arxiv.org/abs/2303.06591)                                                                                                          |
| Aligned Better, Listen Better for Audio-Visual Large Language Models                                  | Dolphin          | —                                                           | [arXiv](https://arxiv.org/abs/2504.02061)                                                                                                                       |
| EchoInk-R1: Exploring Audio-Visual Reasoning in Multimodal LLMs via Reinforcement Learning             | EchoInk-R1       | [GitHub](https://github.com/HarryHsing/EchoInk)                                                           | [arXiv](https://arxiv.org/abs/2505.04623)                                                                                                                                     |
| Fine-grained Audio-Visual Joint Representations for Multimodal Large Language Models           | FAVOR            | [GitHub](https://github.com/BriansIDP/AudioVisualLLM)       | [arXiv](https://arxiv.org/abs/2310.05863)                                                                                                                 |
| Gramian Multimodal Representation Learning and Alignment                            | GRAM             | [GitHub](https://github.com/ispamm/GRAM)                                                           | [arXiv](https://arxiv.org/abs/2412.11959)                                                                                                                                                        |
| InternVideo2: Scaling Foundation Models for Multimodal Video Understanding                           | InternVideo2     | [GitHub](https://github.com/OpenGVLab/InternVideo/tree/main/InternVideo2)         | [arXiv](https://arxiv.org/abs/2403.15377)                                                                                                                                      |
| Lyra: An Efficient and Speech-Centric Framework for Omni-Cognition                                    | Lyra             | [GitHub](https://github.com/dvlab-research/Lyra)            | [arXiv](https://arxiv.org/abs/2412.09501)                                                                                                                                  |
| Macaw-LLM: Multi-Modal Language Modeling with Image, Audio, Video, and Text Integration               | MACAW-LLM        | [GitHub](https://github.com/lyuchenyang/Macaw-LLM)          | [arXiv](https://arxiv.org/abs/2306.09093)                                                                                                                                   |
| Meerkat: Audio-Visual Large Language Model for Grounding in Space and Time                            | Meerkat          | [GitHub](https://github.com/schowdhury671/meerkat)                                                           | [arXiv](https://arxiv.org/abs/2407.01851)                                                                                                                                    |
| Vision-Speech Models: Teaching Speech Models to Converse about Images                      | MoshiVis         | [GitHub](https://github.com/kyutai-labs/moshivis)           | [arXiv](https://arxiv.org/abs/2503.15633)                                                                                                                                    |
| UnIVAL: Unified Model for Image, Video, Audio and Language Tasks                                      | UnIVAL           | [GitHub](https://github.com/mshukor/UnIVAL)                 | [arXiv](https://arxiv.org/abs/2307.16184)                                                                                                                                     |
| VALOR: Vision-Audio-Language Omni-Perception Pretraining Model and Dataset                            | VALOR            | [GitHub](https://casia-iva-group.github.io/projects/VALOR) | [arXiv](https://arxiv.org/abs/2304.08345)                                                                                                                                     |
| VAST: A Vision-Audio-Subtitle-Text Omni-Modality Foundation Model and Dataset                                                | VAST             | [GitHub](https://github.com/TXH-mercury/VAST)               | [arXiv](https://arxiv.org/abs/2305.18500)                                                                                                                                              |
| VideoChat: Chat-Centric Video Understanding                                                           | VideoChat        | [GitHub](https://github.com/OpenGVLab/Ask-Anything/tree/main/video_chat)         | [Paper](https://arxiv.org/abs/2305.06355)                                                                                                                                  |
| Video-LLaMA: An Instruction-tuned Audio-Visual Language Model for Video Understanding                 | Video-LLaMA      | [GitHub](https://github.com/DAMO-NLP-SG/Video-LLaMA)        | [arXiv](https://arxiv.org/abs/2306.02858)                                                                                                                                    |
| VideoLLaMA 2: Advancing Spatial-Temporal Modeling and Audio Understanding in Video-LLMs                | VideoLLaMA 2     | [GitHub](https://github.com/DAMO-NLP-SG/VideoLLaMA2)        | [arXiv](https://arxiv.org/abs/2406.07476)                                                                                                                                                    |
| video-SALMONN: Speech-Enhanced Audio-Visual Large Language Models                                     | video-SALMONN    | [GitHub](https://github.com/bytedance/SALMONN/)      | [arXiv](https://arxiv.org/abs/2406.15704)                                                                                                            |
| VITA: Towards Open-Source Interactive Omni Multimodal LLM                                             | VITA             | [GitHub](https://github.com/VITA-MLLM/VITA)                 | [arXiv](https://arxiv.org/abs/2408.05211)                                                                                                                                |
| X-LLM: Bootstrapping Advanced Large Language Models by Treating Multi-Modalities as Foreign Languages                  | X-LLM            | [GitHub](https://github.com/phellonchen/X-LLM)              | [arXiv](https://arxiv.org/abs/2305.04160)                                                                                                                                |
| AnyGPT: Unified Multimodal LLM with Discrete Sequence Modeling       | AnyGPT           | [GitHub](https://github.com/OpenMOSS/AnyGPT)               | [arXiv](https://arxiv.org/abs/2402.12226)                                                                                                                                                    |
| C3LLM: Conditional Multimodal Content Generation Using Large Language Models                          | C3LLM            | —                                                           | [arXiv](https://arxiv.org/abs/2405.16136)                                                                                                                                  |
| C3Net: Compound Conditioned ControlNet for Multimodal Content Generation                              | C3Net            | —                                                           | [arXiv](https://arxiv.org/abs/2311.17951) |
| CLIPSonic: Text-to-Audio Synthesis with Unlabeled Videos and Pretrained Language-Vision Models        | CLIPSonic        | —                                                           | [arXiv](https://arxiv.org/abs/2306.09635)                                                                                                                                                    |
| CLIPSynth: Learning Text-to-audio Synthesis from Videos using CLIP and Diffusion Models                                      | CLIPSynth        | —                                                           | [Paper](https://sightsound.org/papers/2023/Dong_CLIPSynth_Learning_Text-to-audio_Synthesis_from_Videos.pdf)                                                                                                                                                    |
| Any-to-Any Generation via Composable Diffusion                                                  | CoDi             | [GitHub](https://github.com/microsoft/i-Code/tree/main/i-Code-V3)                      | [arXiv](https://arxiv.org/abs/2305.11846)                                                                                                                                       |
| CoDi-2: In-Context, Interleaved, and Interactive Any-to-Any Generation                                | CoDi-2           | [GitHub](https://github.com/microsoft/i-Code/tree/main/CoDi-2)                        | [arXiv](https://arxiv.org/abs/2311.18775)     |
| EMOVA: Empowering Language Models to See, Hear and Speak with Vivid Emotions                                          | EMOVA            | [GitHub](https://github.com/emova-ollm/EMOVA)                                                           | [arXiv](https://arxiv.org/abs/2409.18042)                                                                                                                                                                       |
| MoCha: Towards Movie-Grade Talking Character Synthesis                                                                                                 | MoCha            |   [GitHub](https://github.com/congwei1230/MoChaBench)                                                   | [arXiv](https://arxiv.org/abs/2503.23307)                                                                                                                                                                    |
| NExT-GPT: Any-to-Any Multimodal LLM                                                                   | NExT-GPT         | [GitHub](https://github.com/NExT-GPT/NExT-GPT)              | [arXiv](https://arxiv.org/abs/2309.05519)                                                                                                                                 |
| SonicVisionLM: Playing Sound with Vision-Language Models                                              | SonicVisionLM    | [GitHub](https://github.com/Yusiissy/SonicVisionLM)         | [arXiv](https://arxiv.org/abs/2401.04394)                                                                                                                                    |



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
|                           | [AVU-dataset](https://arxiv.org/abs/2504.02061)                                                 |     2025 | Video, Audio, Text                  | 5.2M AV captions & Q&A tuples                        |
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

