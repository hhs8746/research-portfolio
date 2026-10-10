# Research Portfolio

Hyeongsoon Hwang | M.S. student, DMIS Lab, Korea University

I work on document retrieval, scientific AI agents, and biomedical question answering. This portfolio describes the problems these projects address and my contributions to their data, retrieval systems, model training, and evaluation.

[Portfolio PDF (Korean)](portfolio.pdf) · [Publications and research contributions](PUBLICATIONS.md)

## Projects

### Visual Document Graph RAG

This project builds a search-and-answer system for company slides and dashboards, including questions that require evidence from several slides.

For a research collaboration with LG Electronics, I built the document database, retrieval and answer server, and evaluation pipeline. I combined text and vector search with entity relationships to connect evidence across documents, and created a shared benchmark to compare RAG systems.

On the same benchmark, single-hop Recall@10 and multi-hop Coverage@10 each improved by more than **20 percentage points** over the existing system.

[Project notes](projects/visual-document-rag.md)

### AI-CoScientist

AI-CoScientist trains agents to turn scientific research questions into analysis plans and carry them out with tools and code.

I synthesized planning data from research papers, collected tool-use demonstrations from a teacher model, and fine-tuned Qwen3.6-27B to execute planned analyses. I checked the demonstrations against the papers' analysis procedures, executed code, and results to identify fabricated data and missing tool executions.

The project is ongoing. Self-distillation and reinforcement learning are under consideration for the next stage.

[Project notes](projects/ai-coscientist.md)

### MedHopQA

MedHopQA is a biomedical question-answering task in which an answer requires combining evidence from multiple documents.

I implemented and compared three search approaches that generate answer candidates, then analyzed how the final decision model selects among them. Our submission placed **first** in the BioCreative IX challenge with an official test exact match (EM) score of **0.84**. The journal extension reached **0.87** under our internal evaluation setup. I am a co-first author of both papers.

[Project notes](projects/medhopqa.md) · [Workshop proceedings](https://zenodo.org/records/16875348)

## Other research

- **Meerkat2 and follow-up training:** Meerkat2 is a Korean-English medical reasoning model with knowledge of Korean medical laws. I validated legal QA and evaluated models on clinical benchmarks. In follow-up work, I selected SFT data and improved rubric-based reinforcement learning. HealthBench scores increased from 44.9 to 51.2 (14B) and from 46.3 to 55.3 (32B) relative to the Qwen3 baselines.
- **FineWeb-Reasoning:** This project studies how reasoning-rich web documents can improve language-model training. I reviewed the prompts and document samples used to score reasoning quality, then designed rewards against shortcuts and trained the pretrained base model with GRPO without an initial SFT stage. Scores increased from 12.1 to 43.0 on GSM8K and from 14.8 to 37.2 on LogiQA.
- **ArchEHR-QA:** This task asks systems to answer patient questions using evidence from electronic health records. I designed and tested a multi-agent pipeline that selects relevant sentences, asks specialist agents to review them, and combines the evidence into an answer. Our system ranked first on the public leaderboard; the paper appeared at the ACL 2025 BioNLP Workshop.
- **Adaptive Latent Block Insertion:** This research aims to improve an LLM's reasoning during answer generation without retraining the model. I ran experiments with an existing latent-reasoning method (LTPO) and trained SoftCoT projection modules, comparing these baselines with the proposed method on five benchmarks. The paper was accepted at EMNLP 2026 Main; I am the second author.

## Other projects

- **sLLM investment information retrieval:** This project built a chatbot that answers investment questions using evidence from securities reports. I led the team, built the report database, and designed hybrid keyword and vector search (BM25 and FAISS), including query expansion and HyDE. The team paired retrieval with a small language model trained on report-derived QA and Korean preference data. We won the Samsung Securities program grand prize.
- **Parkinson's disease progression prediction:** This Kaggle competition predicts disease progression from protein and peptide data. I built statistical and embedding features and applied NPX-based protein weighting. The submission earned a silver medal.
- **Wallpaper defect classification:** This DACON competition classifies wallpaper photos by defect type. I trained EfficientNetV2 with focal loss and image augmentation to handle rare defect classes. The submission finished in the top 3%.
- **AWS DeepRacer:** This competition uses reinforcement learning to train an autonomous racing agent. I designed rewards that penalize leaving the track or straying from its center and encourage appropriate speed on straight and curved sections. I finished seventh in the 2022 championship.

Other competition results include a Kaggle bronze medal in Vesuvius ink detection and seventh place in a DACON genome-based variety prediction competition.

## Publications

- **EMNLP 2026 Main, accepted:** Meerkat2 and Adaptive Latent Block Insertion. Second author on both papers.
- **Database, accepted:** MedHopQA journal extension. Co-first author.
- **IJCAI 2025 BioCreative IX Workshop:** MedHopQA. Co-first author.
- **ACL 2025 BioNLP Workshop:** ArchEHR-QA. Co-first author.

[Full titles, contributions, and public links](PUBLICATIONS.md)
