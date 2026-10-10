# Research Portfolio

Hyeongsoon Hwang | M.S. student, DMIS Lab, Korea University

I work on document retrieval, scientific AI agents, and biomedical question answering. This portfolio describes my work on data preparation, retrieval, model training, and evaluation.

[Portfolio PDF (Korean)](portfolio.pdf) · [Publications and research contributions](PUBLICATIONS.md)

## Projects

### Visual Document Graph RAG

I designed and implemented a document retrieval system and its evaluation pipeline for a research collaboration with LG Electronics.

The system extracts entities and relationships from slides and dashboards, stores them in PostgreSQL with pgvector, and combines four search indexes with reciprocal rank fusion and graph expansion. I also built the benchmark and FastAPI evaluation server.

On the same benchmark, single-hop Recall@10 and multi-hop Coverage@10 each improved by more than **20 percentage points** over the existing system.

[Project notes](projects/visual-document-rag.md)

### AI-CoScientist

I build and validate training data for scientific analysis agents and train the executor model.

I synthesized planning examples from research papers, collected teacher execution traces, and fine-tuned a Qwen3.6-27B executor. I validated and selected traces for further training by comparing them with the papers' analysis plans and the executed code.

The project is ongoing. Self-distillation and reinforcement learning are under consideration for the next stage.

[Project notes](projects/ai-coscientist.md)

### MedHopQA

I am a co-first author of the workshop paper and its journal extension. I implemented and compared three retrieval methods and analyzed bias in the final answer selection.

Our submission placed **first** in the BioCreative IX MedHopQA challenge with an official test exact match (EM) score of **0.84**. The journal extension reached **0.87** under our internal evaluation setup.

[Project notes](projects/medhopqa.md) · [Workshop proceedings](https://zenodo.org/records/16875348)

## Other research

- **Meerkat2 and follow-up training:** I validated Korean medical-law QA and evaluated models on clinical benchmarks, then worked on rubric-based SFT and reinforcement learning with improved reward scoring and judge-output parsing. In follow-up experiments, HealthBench scores increased from 44.9 to 51.2 (14B) and from 46.3 to 55.3 (32B).
- **FineWeb-Reasoning:** I checked reasoning-quality scoring prompts and document samples, designed rewards to penalize reward hacking, and trained a base model with GRPO without an initial SFT stage. Scores increased from 12.1 to 43.0 on GSM8K and from 14.8 to 37.2 on LogiQA.
- **ArchEHR-QA:** I designed and tested a multi-agent framework for patient-context generation, EHR evidence selection, specialist review, and final answer synthesis. Our system ranked first on the public leaderboard. The paper appeared at the ACL 2025 BioNLP Workshop.
- **Adaptive Latent Block Insertion:** I ran LTPO experiments and trained SoftCoT projection modules for comparison with a method that optimizes latent vectors during inference without retraining the main model. We compared the methods on five benchmarks. EMNLP 2026 Main, accepted; second author.

## Other projects

- **sLLM investment information retrieval:** I led the team, built a securities-report database, and designed a RAG pipeline with BM25, FAISS, query expansion, and HyDE. We combined report-derived QA for SFT with Korean preference data for DPO and won the Samsung Securities program grand prize.
- **Parkinson's disease progression prediction:** I used protein and peptide statistics, embedding features, and NPX-based protein weighting. Kaggle silver medal.
- **Wallpaper defect classification:** I trained EfficientNetV2 with focal loss and image augmentation for rare defect classes. Top 3% in DACON.
- **AWS DeepRacer:** I designed reinforcement-learning rewards for staying on track and adjusting speed on straight and curved sections. Seventh place in the 2022 championship.

Other competition results include a Kaggle bronze medal in Vesuvius ink detection and seventh place in a DACON genome-based variety prediction competition.

## Publications

- **EMNLP 2026 Main, accepted:** Meerkat2 and Adaptive Latent Block Insertion. Second author on both papers.
- **Database, accepted:** MedHopQA journal extension. Co-first author.
- **IJCAI 2025 BioCreative IX Workshop:** MedHopQA. Co-first author.
- **ACL 2025 BioNLP Workshop:** ArchEHR-QA. Co-first author.

[Full titles, contributions, and public links](PUBLICATIONS.md)
