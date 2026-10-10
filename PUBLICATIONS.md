# Publications and Research Contributions

This page introduces the research behind each paper and my contribution to it.

[Back to portfolio](README.md) · [Portfolio PDF (Korean)](portfolio.pdf) · [Project pages (Korean)](projects/README.md)

## Conference papers

### Meerkat2: Bridging Global Reasoning and Local Knowledge for Efficient Medical AI

**EMNLP 2026 Main. Accepted. Second author.**

Meerkat2 is a Korean-English medical reasoning model designed to combine clinical reasoning with knowledge of Korean medical laws. Its training separates reasoning learned from teacher models from legal facts learned from source texts, while reducing the long answers inherited from teachers.

**My contribution:** I validated synthetic medical-law QA against source texts using LF-Eval and manual review, and evaluated the models on three clinical benchmarks, including HealthBench Hard.

In follow-up research, I selected SFT data, improved rubric-based reinforcement-learning rewards, and evaluated the models. I changed scoring to evaluate individual rubric items and strengthened judge-output parsing to stabilize training. Relative to the Qwen3 baselines, HealthBench scores increased from 44.9 to 51.2 for the 14B model and from 46.3 to 55.3 for the 32B model. These results are separate from the original paper.

[Portfolio pages](projects/meerkat2.md) · [Publication listing](https://dmis.korea.ac.kr/publications)

### Adaptive Latent Block Insertion via Online Reward Optimization

**EMNLP 2026 Main. Accepted. Second author.**

This paper studies how to improve an LLM's reasoning during answer generation without retraining the model. The method detects sustained uncertainty, inserts latent vectors, and optimizes them using confidence from short trial continuations.

**My contribution:** I ran LTPO experiments and trained SoftCoT projection modules on Qwen3 and Ministral. I compared these existing latent-reasoning approaches with the proposed method on five benchmarks under the same experimental conditions.

[Portfolio pages](projects/adaptive-latent-block.md) · [Publication listing](https://dmis.korea.ac.kr/publications)

## Journal article

### Ensemble Multi-Retrieval Methodologies with Reasoning Model Decision in Multi-Step Biomedical QA

**Database, Oxford University Press. Published October 8, 2026. Co-first author.**

This paper extends MedHopQA, a task that answers biomedical questions by combining evidence from multiple documents. It examines how retrieval, answer generation, and final answer selection each affect accuracy.

**My contribution:** I compared the components and model combinations, identified the decision model's preference for answers it had generated itself, and evaluated separate generation and decision models. This configuration reached EM 0.87 in post-challenge experiments with an updated model configuration, reported separately from the official challenge result.

[Journal article](https://doi.org/10.1093/database/baag061) · [Portfolio pages](projects/medhopqa.md)

## Workshop papers

### DMIS Lab at MedHopQA-2025: Ensemble Multi-Retrieval Methodologies with Reasoning Language Model Decision

**IJCAI 2025 BioCreative IX Workshop. Co-first author.**

This paper presents a system for biomedical questions that require evidence from several documents. It uses hypothetical-document search (Query2Doc), reasoning-based search, and web search to generate answer candidates, then a separate decision model selects or derives the final answer.

**My contribution:** I implemented and compared the three retrieval methods. Our submission placed first in the BioCreative IX MedHopQA challenge with an official test EM score of 0.84.

[Workshop paper list](https://www.ncbi.nlm.nih.gov/research/bionlp/biocreative9) · [Proceedings](https://zenodo.org/records/16875348) · [Portfolio pages](projects/medhopqa.md)

### DMIS Lab at ArchEHR-QA 2025: Evidence-Grounded Answer Generation for EHR-based QA via a Multi-Agent Framework

**ACL 2025 BioNLP Workshop. Co-first author.**

This paper presents a system that answers patient questions using evidence from electronic health records. Its multi-agent framework creates patient context, selects relevant EHR sentences, has specialist agents review the evidence, and produces an answer with supporting record IDs.

**My contribution:** I designed and tested the overall pipeline, including sentence-level evidence decisions and specialist review. Our system ranked first on the public leaderboard, with test scores of Factuality 58.6, Relevance 48.8, and Overall 53.7.

[ACL Anthology](https://aclanthology.org/2025.bionlp-share.15/) · [Paper PDF](https://aclanthology.org/2025.bionlp-share.15.pdf) · [Portfolio pages](projects/archehr-qa.md)

## Additional research

**FineWeb-Reasoning:** This project studies whether selecting web documents with stronger reasoning can produce a stronger base language model. I checked reasoning-quality scoring prompts and document samples, then designed rewards against shortcuts and applied GRPO to the pretrained base model without an initial SFT stage. Scores increased from 12.1 to 43.0 on GSM8K and from 14.8 to 37.2 on LogiQA. [Portfolio pages](projects/fineweb-reasoning.md)

**AI-CoScientist:** This project trains agents to plan scientific analyses and execute them with tools and code. I synthesized planning examples from research papers, validated execution records against the papers and executed code, and fine-tuned and evaluated the model that carries out the analyses. Self-distillation and reinforcement learning are under consideration for the next stage. [Portfolio pages](projects/ai-coscientist.md)
