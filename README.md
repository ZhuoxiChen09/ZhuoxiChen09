# Hi there, I'm Zhuoxi 'Derrick' Chen

**UC San Diego — Cognitive Science & Applied Mathematics**

---

## About Me

I'm an undergraduate at UC San Diego majoring in Cognitive Science (ML & Neural Computation) and Applied Mathematics, with minors in Computer Science and Philosophy. I work at the intersection of computational neuroscience, applied machine learning, and music-information retrieval.

I've built automated ImageJ pipelines for TH-intensity quantification in Parkinsonian mouse models, trained Transformers and DDSP-style synths from scratch for symbolic-to-audio music generation, and developed LLM-based decision-support tools including calendar and task-prioritization systems.

My interests center on how cognitive and statistical principles can be turned into reliable, interpretable computational systems — especially in settings where reproducibility, human understanding, and practical usability matter as much as raw performance.

---

## Projects

### Music & Audio ML

#### [leadsheet-to-audio](https://github.com/ZhuoxiChen09/leadsheet-to-audio)
End-to-end neural music pipeline: a from-scratch Transformer harmonizes a melody into a leadsheet, and a DDSP-style harmonic + filtered-noise synth renders it to audio. Trained from scratch in PyTorch on Nottingham (symbolic) and a MAESTRO subset (audio).
- Stage 1 — 4-layer Transformer (~2 M params): top-1 chord acc ≈ 58%, top-5 ≈ 91%, val perplexity ≈ 4.0
- Stage 2 — per-voice DDSP synth (48 harmonics + filtered noise) summed for arbitrary polyphony
- Both networks train from random init in under 10 minutes on a single laptop GPU
- Reproducible CLI pipeline, annotated notebook, and a 20-minute walkthrough video

#### [midi-audio-music-classification](https://github.com/ZhuoxiChen09/midi-audio-music-classification)
Three music-understanding tasks tackled with hybrid **classical + deep learning** ensembles, combined at the logit/probability level.
- **Composer ID** (8-way): 280-dim handcrafted features + HistGradientBoosting ⊕ 5-layer Transformer over note tokens — **0.663 test accuracy**
- **Next-Sequence Prediction** (binary): XGB / HGB / RF stack on pair features ⊕ 4-layer pair Transformer with forward+reverse TTA
- **Music Tagging** (10-way multi-label): 3-seed ResNet34 on log-mel + Δ + ΔΔ ⊕ AudioSet-pretrained AST fine-tune — **0.637 test mAP**

### Applied ML & Quantitative Research

#### [DEUCE](https://github.com/ZhuoxiChen09/DEUCE)
Python toolkit for **pre-match tennis research** on Kalshi-style binary contracts: market quotes, player context, calibrated win probabilities, edge signals, and bankroll backtests.
- End-to-end research stack: feature tiers, scikit-learn training pipeline, and pricing versus live market data
- **FastAPI** service with ingest orchestration and **SQLite** persistence; **Streamlit** UI for exploration and operations
- Backtesting library with configurable edge thresholds and stake rules; live score normalization across multiple providers
- Structured **CLI** (`deuce.cli`) for training, tiers, and workflows; pytest-backed CI

#### [Spotify Popularity Prediction](https://github.com/ZhuoxiChen09/spotify-popularity-prediction)
Machine learning project comparing KNN regression models to predict song popularity rankings using streaming-platform metrics.
- Systematic model evaluation with cross-validation and bias-variance analysis
- Analyzes the relationship between music metrics (streams, playlists, views) and song popularity
- Best model achieves 65% variance explained with distance-weighted KNN (k = 5)

### Cognitive Science & Productivity — *NoCrastination*

A broader project line exploring how to reduce procrastination using cognitive science, UX design, and LLM-based tooling.

#### [Calendar MVP](https://github.com/ZhuoxiChen09/calendar_mvp)
**Status:** In progress
Node.js + TypeScript backend and React frontend that parse university course syllabi (text or PDF) into prioritized task lists using an LLM.
- REST API for syllabus parsing with text / PDF endpoints and priority scoring
- PDF and text ingestion pipeline with sample syllabi and automated API tests
- Vite-based web UI to upload syllabi and view due dates, weights, and priority ordering

#### [NoCrastination — Concept Design](https://github.com/ZhuoxiChen09/NoCrastination-Concept)
Concept design for a productivity assistant grounded in cognitive science, informing the Calendar MVP implementation.
- Reduces decision fatigue through cognitive offloading and attention guidance
- Early UI screens, user flow concepts, and system architecture
- Integrates principles like task chunking and temporal motivation theory
- Visual identity and product direction documentation

### Research Tools & Experiments

#### [TH Intensity Measurement](https://github.com/ZhuoxiChen09/th-intensity-measurement)
A Java-based ImageJ plugin for semi-automated tyrosine hydroxylase (TH) signal intensity measurement from brain slice images.
- Standardizes ROI placement and scale calibration
- Supports manual ROI adjustment for precision
- Exports data in structured CSV format for statistical analysis
> Developed for dopaminergic neuron degeneration research in the UCSD Leutgeb Lab.

#### [mini-rag](https://github.com/ZhuoxiChen09/mini-rag)
A compact Retrieval-Augmented Generation (RAG) demo: embeds local text files and answers questions using instruction-tuned language models.
- Builds retrieval indices over `.txt` corpora
- Interactive query loop with context-aware generation
- Minimal, reproducible reference implementation

---

## Résumé
**Current Resume:**
[View / Download PDF](https://drive.google.com/file/d/1vwxEn6lcXiSiTCnq77Sh4szdDt27fjfU/view?usp=sharing)

---

## Technical Skills
**Programming:** Python, Java, JavaScript / TypeScript, MATLAB, HTML / CSS
**ML & Audio:** PyTorch, Transformers, DDSP / neural audio synthesis, Hugging Face (AST), scikit-learn, XGBoost, librosa, torchaudio
**Backend & UI:** FastAPI, Node.js, React, Vite, Streamlit, REST APIs
**Data & Tooling:** pandas, NumPy, SQLite, Git, ImageJ / Fiji, Figma, DaVinci Resolve, Vercel
**Specialties:** Reproducible research pipelines, model ensembling, neural-audio modeling, research automation, UI / UX prototyping

---

## Connect
📧 **Email:** [chenzhuoxi458@gmail.com](mailto:chenzhuoxi458@gmail.com)
🔗 **LinkedIn:** [linkedin.com/in/zhuoxi-chen09](https://linkedin.com/in/zhuoxi-chen09)

---

*Last updated: June 2026*
