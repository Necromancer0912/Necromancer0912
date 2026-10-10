<div align="center">

# Sayan Das

**Computer enthusiast**

M.Tech CSE at IIIT Delhi — speech and language models, retrieval systems,<br/>
and the networks and kernels underneath them.

<a href="https://hellosayan.vercel.app/"><img src="https://img.shields.io/badge/Portfolio-hellosayan.vercel.app-111113?style=flat-square&logo=vercel&logoColor=white" alt="Portfolio"/></a>
<a href="mailto:sayan20012002@gmail.com"><img src="https://img.shields.io/badge/Email-111113?style=flat-square&logo=gmail&logoColor=white" alt="Email"/></a>
<a href="https://linkedin.com/in/necromancer0912"><img src="https://img.shields.io/badge/LinkedIn-111113?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
<a href="https://monkeytype.com/profile/Sayan0912"><img src="https://img.shields.io/badge/Monkeytype-111113?style=flat-square&logo=monkeytype&logoColor=white" alt="Monkeytype"/></a>
<img src="https://hits.sh/github.com/Necromancer0912.svg?style=flat-square&label=views&color=111113&labelColor=111113" alt="Profile views"/>

<img src="https://media.giphy.com/media/LmNwrBhejkK9EFP504/giphy.gif" width="150"/>

</div>

---

## About

I build things at both ends of the stack: transformers and retrieval pipelines on one side,
kernel drivers and transport protocols on the other. Most of my work lately has been on
low-resource and code-switched Indian languages, and on the data-centre plumbing that
large models actually run over.

Three journal papers and a preprint on AI for computational physics and medical imaging
along the way.

**Right now** — third semester of my M.Tech, and a software engineering internship at Foodoscope.

---

## Experience

**Software Engineering Intern** · Foodoscope · *May 2026 – present*

- Led the team designing containerised RAG and semantic-search pipelines for the chatbot;
  moved lookups onto local SQLite to cut response latency, and enforced read-only SQL
  guardrails to curb hallucination and block unauthorised writes or data leakage.
- Built RESTful APIs for **FlavourDB** on MongoDB aggregation pipelines, mapping and
  retrieving the molecules associated with each food.

---

## Research

**Novel Deep Learning Architectures for Classification and Segmentation of Brain Tumors from MRI Images**
<br/><sub>**Sayan Das**, A. Biswas · *arXiv preprint* · 2025 · [code](https://github.com/Necromancer0912/SAETCN-and-SASNET-Architectures)</sub>

**AI-optimized analysis of hybrid nanoparticles-infused milk flow in a rapidly moving electromagnetic channel with oscillating thermal ramping**
<br/><sub>**Sayan Das**, Poly Karmakar, Sukanya Das, Sanatan Das · *Soft Computing* 30(1), Springer · 2026 · [10.1007/s00500-025-10973-6](https://doi.org/10.1007/s00500-025-10973-6)</sub>

**AI-led study of dynamic changes in milk containing hybrid nanoparticles in an electromagnetically vibrated channel subjected to thermal oscillations and rapid pressure changes**
<br/><sub>Sanatan Das, Poly Karmakar, **Sayan Das**, Saeed Dinarvand · *Chinese Journal of Physics*, Elsevier · 2025 · [10.1016/j.cjph.2024.11.025](https://doi.org/10.1016/j.cjph.2024.11.025)</sub>

**Neuro-computational simulation of blood flow loaded with gold and maghemite nanoparticles inside an electromagnetic microchannel under rapid and unexpected change in pressure gradient**
<br/><sub>Poly Karmakar, Sukanya Das, **Sayan Das**, Sanatan Das · *Electromagnetic Biology and Medicine*, Taylor &amp; Francis · 2025 · [10.1080/15368378.2025.2453923](https://doi.org/10.1080/15368378.2025.2453923)</sub>

<div align="center">
<img src="https://media.giphy.com/media/L1R1tvI9svkIWwpVYr/giphy.gif" width="200"/>
</div>

---

## Projects

### Language, speech and retrieval

**[Vidhi — Indian legal QA](https://github.com/Necromancer0912/vidhi)** · [live](https://project-vidhi.vercel.app)
<br/>Plain-language answers to questions about Indian law, grounded in 494 official documents
and checked claim by claim, across 11 languages. Stateful multi-agent graph, hybrid
vector + sparse retrieval, Redis semantic caching and conversation memory, SSE streaming,
local LLM, frontend on Vercel against a self-hosted backend over Tailscale Funnel.
<br/>`LangGraph` `FastAPI` `Qdrant` `Redis` `BGE reranker` `React`

**[Code-Mixed Speech Recognition](https://github.com/Necromancer0912/Enhancing-Code-Mixed-Speech-Recognition-using-Whisper-Fine-Tuning-and-LLM-Based-Contextual-Rescoring)**
<br/>Bengali–English code-switched ASR: fine-tuned the Whisper decoder with prompt
conditioning and added LLM *n*-best rescoring (GPT-2, BLOOM, Qwen2.5), taking WER from
195% zero-shot down to **39.6%**. Extends CLEAR (ICNLSP 2025) with ASR–LLM score
interpolation, MBR decoding, and a LoRA domain-adapted rescorer for a further 4% relative gain.
<br/>`PyTorch` `Hugging Face` `LoRA` `MBR decoding` *· guide: Dr. Md Shad Akhtar*

**[HindiMiniGPT](https://github.com/Necromancer0912/HindiMiniGPT)**
<br/>A decoder-only Hindi language model written from scratch — attention, RoPE and RMSNorm —
verified against PyTorch's own implementation, where the modern variant beat the vanilla one
by **4.3%** validation perplexity at equal size. Benchmarked FP32 / FP16 / INT8 and a
distilled student to measure real speed-versus-quality trade-offs.
<br/>`PyTorch` `SentencePiece` `LoRA` `quantization` `distillation`

### Systems and networks

**[Ultra Ethernet Transport in ns-3](https://github.com/Necromancer0912/ultra-ethernet-transport-ns3)** · [explorer](https://uetexplorer.vercel.app)
<br/>The Ultra Ethernet Consortium's SES and PDS sublayers implemented in ns-3, which ships no
UET support: full wire formats, PDC state machines, RUD/ROD/RUDI/UUD delivery modes and
SACK/RTO loss recovery, reaching byte-exact message delivery. Reproduces IRN's core
SIGCOMM 2018 result — selective retransmission with a receiver-side reorder buffer lifts
completion from 8% to 100% under 1% packet loss.
<br/>`C++17` `ns-3` `RDMA` `RoCEv2` *· guide: Prof. Rinku Shah*

**[Kubernetes CNI benchmarking](https://github.com/Necromancer0912/kubernetes-cni-performance-benchmarking)**
<br/>Flannel-VXLAN, Calico-BGP/VXLAN and Cilium-eBPF measured head to head across a
multi-node cluster at 128 MB, 512 MB and 1024 MB workloads — throughput, latency, CPU and
memory — to find the most efficient networking backend.
<br/>`Kubernetes` `eBPF` `iPerf3` `Bash` *· guide: Prof. Rinku Shah*

**[Linux PCIe driver](https://github.com/Necromancer0912/Linux-PCIe-driver-DMA-iouring-ebpf)**
<br/>A PCI kernel driver from scratch: MSI interrupts, coherent DMA, `io_uring` async
passthrough, and eBPF interrupt-latency profiling, on QEMU/HVF on Apple Silicon.
<br/>`C` `kernel` `io_uring` `eBPF`

**[Cellular network simulator](https://github.com/Necromancer0912/cellular-network-simulator)**
<br/>2G-through-7G capacity modelling with a hand-rolled terminal dashboard, a real
ThreadPool concurrency benchmark, and a QoS-aware load balancer.
<br/>`C++17` `concurrency`

**[Concurrent academic ERP](https://github.com/Necromancer0912/concurrent-academic-erp)**
<br/>Multithreaded university ERP: parallel merge-sort, a template-based multi-university
architecture, and indexed fast search.
<br/>`C++17` `threads` `templates`

Two more written deliberately without the standard library, on hand-rolled syscall wrappers:
a [no-std student registry](https://github.com/Necromancer0912/nostd-student-db) with its own
allocator, strings and trie, and a
[no-std BibTeX engine](https://github.com/Necromancer0912/nostd-bibtex-engine).

### Medical imaging

**[SAETCN and SASNET](https://github.com/Necromancer0912/SAETCN-and-SASNET-Architectures)** · [demo](https://huggingface.co/spaces/arghadip2002/NeuroGuard-Web-Application)
<br/>The classification and segmentation architectures behind the brain-tumour paper above —
multi-class tumour detection from MRI, and pixel-level boundary segmentation for surgical
planning.
<br/>`PyTorch` `ResNet` `Inception` `U-Net`

**[LungInsight](https://github.com/Necromancer0912/LungInsight)**
<br/>A local-first lung diagnostics console: an Electron + React UI over Flask and Ollama,
orchestrating audio and X-ray models to generate follow-up questions and structured,
clinician-ready reports with severity highlights.
<br/>`Electron` `React` `Flask` `Ollama`

<details>
<summary><b>Earlier work</b> — the NLP and deep-learning notebooks I learned on</summary>

<br/>

| Project | What it is |
|:--|:--|
| [English → Bengali translator](https://github.com/Necromancer0912/English-to-Bengali-Translator-Model-using-Glove-and-Seq2seq) | Neural machine translation with GloVe embeddings, seq2seq and attention |
| [Toxic comment classification](https://github.com/Necromancer0912/jigsaw-toxic-comment-classification-using-CNN-Glove-and-TF2) | Multi-label text classification on the Jigsaw set with a CNN over GloVe |
| [Poetry generator](https://github.com/Necromancer0912/Poetry-Generator-using-Deep-Learning-Approach) | LSTM text generation trained on classical poetry |
| [BiLSTM image classification](https://github.com/Necromancer0912/BiLSTM-Image-Classification) | Images read as sequences by a bidirectional LSTM |
| [CIFAR CNN](https://github.com/Necromancer0912/CIFAR-Classification-using-CNN-in-PyTorch) | CIFAR-10/100 with augmentation and transfer learning |
| [Chanakya AI Discord bot](https://github.com/Necromancer0912/Chanakya-AI-Discord-Bot) | LLaMA 3.1 conversation and Stable Diffusion image generation in a bot |
| [Named entity recognition](https://github.com/Necromancer0912/Named-Entity-Recognition-NER-using-TensorFlow-2) | Sequence labelling in TensorFlow 2 |
| [Text summarisation](https://github.com/Necromancer0912/TextRank-Text-Summarization) | Extractive summarisation with TextRank |
| [Topic modelling](https://github.com/Necromancer0912/Topic-Modeling-using-NMF-Non-negative-Matrix-Factorization-) | NMF topic models, alongside an [LDA](https://github.com/Necromancer0912/Latent-Dirichlet-Allocation) notebook |
| [Spam detection](https://github.com/Necromancer0912/Spam-Detection-Machine-Learning-approach) | Classical classifiers over NLP preprocessing |
| [Movie recommendation](https://github.com/Necromancer0912/Movie-Recommendation-Using-Machine-Learning-Approach) | Collaborative filtering from scratch |
| [CBOW](https://github.com/Necromancer0912/CBOW-in-TensorFlow-2) · [POS tagging](https://github.com/Necromancer0912/POS-tagging-using-TF2) · [Markov classifier](https://github.com/Necromancer0912/Markov-Model-Classifier) | Word embeddings and classical sequence models, hand-built |

</details>

<div align="center">
<img src="https://media.giphy.com/media/WUlplcMpOCEmTGBtBW/giphy.gif" width="200"/>
</div>

---

## Toolbox

| | |
|:--|:--|
| **Languages** | Python · C · C++ · Java · JavaScript · Kotlin · SQL |
| **ML and NLP** | PyTorch · Hugging Face · TensorFlow · Keras · scikit-learn · NumPy · Pandas · OpenCV · LangGraph · LangChain |
| **Systems** | Linux (Debian, Mint) · Docker · Kubernetes · Bash · Redis · Nginx |
| **Networking** | ns-3 · HTSIM · RDMA / RoCEv2 · eBPF · io_uring · iPerf3 |
| **Web** | Next.js · React · Node.js · FastAPI · Tailwind · Bootstrap |
| **Data** | MySQL · PostgreSQL · MongoDB · SQLite · Qdrant |
| **Tooling** | Git · LaTeX · Jupyter · VS Code · Android Studio |
| **Design** | Figma · Blender · Unreal Engine · Photoshop · Illustrator · After Effects |

---

## Education

| | | | |
|:--|:--|:--|:--|
| **M.Tech**, Computer Science | IIIT Delhi | 2025 – present | CGPA **7.76** <sub>through 2nd sem</sub> |
| **B.Tech**, Computer Science | Ramkrishna Mahato Government Engineering College | 2021 – 2025 | CGPA **8.83** |
| Higher Secondary, WBCHSE | Midnapore Collegiate School (Boys) | 2018 – 2020 | **93.4%** |
| Secondary, WBBSE | Sarada Vidyamandir, Midnapore | 2018 | **93.14%** |

**Electives** — Natural Language Processing · Machine Learning · Usable Security and Privacy · Information Integration and Applications

---

## Teaching and achievements

- **Teaching Assistant**, Network Security · IIIT Delhi · *Jan – May 2026*
- **Teaching Assistant**, Introduction to Programming · IIIT Delhi · *Aug – Dec 2025*
- **GATE** CSE and DA qualified · 2024 and 2025

---

## GitHub

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api?username=Necromancer0912&show_icons=true&hide_border=true&hide_title=true&theme=github_dark&icon_color=58a6ff"/>
  <img width="420" src="https://github-readme-stats.vercel.app/api?username=Necromancer0912&show_icons=true&hide_border=true&hide_title=true&theme=graywhite" alt="GitHub statistics"/>
</picture>
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://streak-stats.demolab.com?user=Necromancer0912&hide_border=true&theme=dark"/>
  <img width="420" src="https://streak-stats.demolab.com?user=Necromancer0912&hide_border=true&theme=graywhite" alt="Contribution streak"/>
</picture>

<img src="https://media.giphy.com/media/du3J3cXyzhj75IOgvA/giphy.gif" width="130"/>

</div>

---

## Elsewhere

**Portfolio** — [hellosayan.vercel.app](https://hellosayan.vercel.app/) · built with Next.js, WebGL particles and live diagrams
<br/>**Email** — [sayan20012002@gmail.com](mailto:sayan20012002@gmail.com) · [sayan25041@iiitd.ac.in](mailto:sayan25041@iiitd.ac.in)
<br/>**LinkedIn** — [necromancer0912](https://linkedin.com/in/necromancer0912)
<br/>**Monkeytype** — [Sayan0912](https://monkeytype.com/profile/Sayan0912)

Open to research collaborations, open source, and interesting problems.
Off-screen, I draw.

<div align="center">

<br/>

<sub>Thank you — have a nice day.</sub>

<img src="https://raw.githubusercontent.com/saadeghi/saadeghi/master/dino.gif" width="300"/>

</div>
