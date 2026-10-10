# AI-CoScientist

This project uses research papers and tool execution traces to train agents that plan and perform scientific data analysis.

**My role:** Planning data synthesis and filtering, executor SFT, execution-trace validation, and benchmark evaluation.

[Back to portfolio](../README.md) · [Portfolio PDF (Korean)](../portfolio.pdf)

## Training data

The agents needed examples of how to turn a research question into an analysis plan and execute it with tools.

I started from the analysis procedures in research papers and worked backward to synthesize questions and plans, then filtered the examples for training.

I collected tool execution traces from Kimi K2.6 and used them to fine-tune a Qwen3.6-27B executor with supervised fine-tuning (SFT). I evaluated the executor and analyzed failures on benchmarks including BiomniBench and BixBench.

## Execution-trace validation

Checking whether a generated plan and trace agreed with each other was insufficient. Traces could pass that check even when they analyzed fabricated data.

| Issue | Added check |
| --- | --- |
| A plan and trace can agree while using fabricated data | Compare the trace with the analysis plan from the source paper, the executed code, and its results |
| A final answer can hide missing tool executions | Review tool calls and execution outputs together |
| A valid alternative method can differ from the reference plan | Manually review alternative methods before excluding them |

These checks helped me select execution traces for further training.

## Current work

Planning data preparation, teacher-trace collection, executor SFT, evaluation, and the revised validation checks have been completed. Self-distillation and reinforcement learning are under consideration for the next stage.

**Tools:** Python, LLM-based data synthesis, tool calling, Qwen3.6-27B, SFT, execution-trace validation.
