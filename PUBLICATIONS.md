# Publications and Research Contributions

This page lists my papers and the work I contributed to each project.

[Back to portfolio](README.md) · [Portfolio PDF (Korean)](portfolio.pdf)

## Accepted papers

### Meerkat2: Bridging Global Reasoning and Local Knowledge for Efficient Medical AI

**EMNLP 2026 Main. Accepted. Second author.**

- Validated synthetic QA against Korean medical law using LF-Eval and manual review.
- Evaluated the models on three clinical benchmarks, including HealthBench.

In follow-up experiments, I worked on rubric-based SFT, reinforcement learning, reward design, and evaluation. HealthBench scores increased from 44.9 to 51.2 for the 14B model and from 46.3 to 55.3 for the 32B model. These are follow-up results, separate from those in the original paper.

### Adaptive Latent Block Insertion via Online Reward Optimization

**EMNLP 2026 Main. Accepted. Second author.**

- Trained and evaluated the LTPO and SoftCoT comparison methods.
- Compared the methods on five benchmarks under the same experimental conditions.
- Contributed to research on training-free optimization during inference.

### Ensemble Multi-Retrieval Methodologies with Reasoning Model Decision in Multi-Step Biomedical QA

**Database, Oxford University Press. Accepted. Co-first author.**

- Compared retrieval, answer generation, and final answer selection in MedHopQA.
- Analyzed the decision model's preference for its own generated answers.
- Evaluated separate generation and decision models, reaching an EM score of 0.87 under our internal evaluation setup.

[Project notes](projects/medhopqa.md)

## Workshop papers

### DMIS Lab at MedHopQA-2025: Ensemble Multi-Retrieval Methodologies with Reasoning Language Model Decision

**IJCAI 2025 BioCreative IX Workshop. Co-first author.**

- Implemented and compared Query2Doc, rationale-based retrieval, and web search.
- Our submission placed first in the BioCreative IX MedHopQA challenge with an official test EM score of 0.84.

[Workshop paper list](https://www.ncbi.nlm.nih.gov/research/bionlp/biocreative9) · [Proceedings](https://zenodo.org/records/16875348) · [Project notes](projects/medhopqa.md)

### DMIS Lab at ArchEHR-QA 2025: Evidence-Grounded Answer Generation for EHR-based QA via a Multi-Agent Framework

**ACL 2025 BioNLP Workshop. Co-first author.**

- Worked on a multi-agent framework that selects, reviews, and combines evidence from electronic health records to answer patient questions.
- Test scores: Factuality 58.6, Relevance 48.8, Overall 53.7.
- Our system ranked first on the public leaderboard.

[ACL Anthology](https://aclanthology.org/2025.bionlp-share.15/) · [Paper PDF](https://aclanthology.org/2025.bionlp-share.15.pdf)

## Additional research

**FineWeb-Reasoning:** Checked reasoning-quality scoring prompts and document samples across score ranges, designed GRPO rewards, and trained a base model. Scores increased from 12.1 to 43.0 on GSM8K and from 14.8 to 37.2 on LogiQA.

**AI-CoScientist:** Synthesized planning examples from research papers, validated and selected execution traces, and fine-tuned and evaluated an executor model. Self-distillation and reinforcement learning are being considered for the next stage. [Project notes](projects/ai-coscientist.md)
