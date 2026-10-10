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

- **Meerkat2 follow-up training:** I worked on rubric-based SFT, reinforcement learning, reward design, and evaluation. HealthBench scores increased from 44.9 to 51.2 for the 14B model and from 46.3 to 55.3 for the 32B model. These experiments followed the original paper.
- **FineWeb-Reasoning:** I checked reasoning-quality scoring prompts and document samples, designed rewards, and trained a base model with GRPO. Scores increased from 12.1 to 43.0 on GSM8K and from 14.8 to 37.2 on LogiQA.
- **ArchEHR-QA:** I worked on a multi-agent framework for selecting evidence from electronic health records. Our system ranked first on the public leaderboard. The paper appeared at the ACL 2025 BioNLP Workshop.

## Publications

- **EMNLP 2026 Main, accepted:** Meerkat2 and Adaptive Latent Block Insertion. Second author on both papers.
- **Database, accepted:** MedHopQA journal extension. Co-first author.
- **IJCAI 2025 BioCreative IX Workshop:** MedHopQA. Co-first author.
- **ACL 2025 BioNLP Workshop:** ArchEHR-QA. Co-first author.

[Full titles, contributions, and public links](PUBLICATIONS.md)
