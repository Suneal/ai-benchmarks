# GenAI Benchmarks
Tables—no small talk, just data

[Phi-4](https://huggingface.co/microsoft/phi-4/edit/main/README.md)

| **Category**                 | **Benchmark** | **phi-4** (14B) | **phi-3** (14B) | **Qwen 2.5** (14B instruct) | **GPT-4o-mini** | **Llama-3.3** (70B instruct) | **Qwen 2.5** (72B instruct) | **GPT-4o** |
|------------------------------|---------------|-----------|-----------------|----------------------|----------------------|--------------------|-------------------|-----------------|
| Popular Aggregated Benchmark | MMLU          | 84.8      | 77.9            | 79.9                 | 81.8                 | 86.3               | 85.3              | **88.1**            |
| Science                      | GPQA          | **56.1**      | 31.2            | 42.9                 | 40.9                 | 49.1               | 49.0              | 50.6            |
| Math                         | MGSM<br>MATH  | 80.6<br>**80.4** | 53.5<br>44.6 | 79.6<br>75.6 | 86.5<br>73.0 | 89.1<br>66.3* | 87.3<br>80.0              | **90.4**<br>74.6            |
| Code Generation              | HumanEval     | 82.6      | 67.8            | 72.1                 | 86.2                 | 78.9*               | 80.4              | **90.6**            |
| Factual Knowledge            | SimpleQA      | 3.0       | 7.6            | 5.4                 | 9.9                  | 20.9               | 10.2              | **39.4**             |
| Reasoning                    | DROP          | 75.5      | 68.3            | 85.5                 | 79.3                 | **90.2**               | 76.7              | 80.9            |

[Deepseek-V3](https://huggingface.co/deepseek-ai/DeepSeek-V3/edit/main/README.md)

| | **Benchmark (Metric)** | **DeepSeek V2-0506** | **DeepSeek V2.5-0905** | **Qwen2.5 72B-Inst.** | **Llama3.1 405B-Inst.** | **Claude-3.5-Sonnet-1022** | **GPT-4o 0513** | **DeepSeek V3** |
|---|---------------------|---------------------|----------------------|---------------------|----------------------|---------------------------|----------------|----------------|
| | Architecture | MoE | MoE | Dense | Dense | - | - | MoE |
| | # Activated Params | 21B | 21B | 72B | 405B | - | - | 37B |
| | # Total Params | 236B | 236B | 72B | 405B | - | - | 671B |
| English | MMLU (EM) | 78.2 | 80.6 | 85.3 | **88.6** | **88.3** | 87.2 | **88.5** |
| | MMLU-Redux (EM) | 77.9 | 80.3 | 85.6 | 86.2 | **88.9** | 88.0 | **89.1** |
| | MMLU-Pro (EM) | 58.5 | 66.2 | 71.6 | 73.3 | **78.0** | 72.6 | 75.9 |
| | DROP (3-shot F1) | 83.0 | 87.8 | 76.7 | 88.7 | 88.3 | 83.7 | **91.6** |
| | IF-Eval (Prompt Strict) | 57.7 | 80.6 | 84.1 | 86.0 | **86.5** | 84.3 | 86.1 |
| | GPQA-Diamond (Pass@1) | 35.3 | 41.3 | 49.0 | 51.1 | **65.0** | 49.9 | 59.1 |
| | SimpleQA (Correct) | 9.0 | 10.2 | 9.1 | 17.1 | 28.4 | **38.2** | 24.9 |
| | FRAMES (Acc.) | 66.9 | 65.4 | 69.8 | 70.0 | 72.5 | **80.5** | 73.3 |
| | LongBench v2 (Acc.) | 31.6 | 35.4 | 39.4 | 36.1 | 41.0 | 48.1 | **48.7** |
| Code | HumanEval-Mul (Pass@1) | 69.3 | 77.4 | 77.3 | 77.2 | 81.7 | 80.5 | **82.6** |
| | LiveCodeBench (Pass@1-COT) | 18.8 | 29.2 | 31.1 | 28.4 | 36.3 | 33.4 | **40.5** |
| | LiveCodeBench (Pass@1) | 20.3 | 28.4 | 28.7 | 30.1 | 32.8 | 34.2 | **37.6** |
| | Codeforces (Percentile) | 17.5 | 35.6 | 24.8 | 25.3 | 20.3 | 23.6 | **51.6** |
| | SWE Verified (Resolved) | - | 22.6 | 23.8 | 24.5 | **50.8** | 38.8 | 42.0 |
| | Aider-Edit (Acc.) | 60.3 | 71.6 | 65.4 | 63.9 | **84.2** | 72.9 | 79.7 |
| | Aider-Polyglot (Acc.) | - | 18.2 | 7.6 | 5.8 | 45.3 | 16.0 | **49.6** |
| Math | AIME 2024 (Pass@1) | 4.6 | 16.7 | 23.3 | 23.3 | 16.0 | 9.3 | **39.2** |
| | MATH-500 (EM) | 56.3 | 74.7 | 80.0 | 73.8 | 78.3 | 74.6 | **90.2** |
| | CNMO 2024 (Pass@1) | 2.8 | 10.8 | 15.9 | 6.8 | 13.1 | 10.8 | **43.2** |
| Chinese | CLUEWSC (EM) | 89.9 | 90.4 | **91.4** | 84.7 | 85.4 | 87.9 | 90.9 |
| | C-Eval (EM) | 78.6 | 79.5 | 86.1 | 61.5 | 76.7 | 76.0 | **86.5** |
| | C-SimpleQA (Correct) | 48.5 | 54.1 | 48.4 | 50.4 | 51.3 | 59.3 | **64.8** |

Note: All models are evaluated in a configuration that limits the output length to 8K. Benchmarks containing fewer than 1000 samples are tested multiple times using varying temperature settings to derive robust final results. DeepSeek-V3 stands as the best-performing open-source model, and also exhibits competitive performance against frontier closed-source models.


####  Open Ended Generation Evaluation

| Model | Arena-Hard | AlpacaEval 2.0 |
|-------|------------|----------------|
| DeepSeek-V2.5-0905 | 76.2 | 50.5 |
| Qwen2.5-72B-Instruct | 81.2 | 49.1 |
| LLaMA-3.1 405B | 69.3 | 40.5 |
| GPT-4o-0513 | 80.4 | 51.1 |
| Claude-Sonnet-3.5-1022 | 85.2 | 52.0 |
| DeepSeek-V3 | **85.5** | **70.0** |

Note: English open-ended conversation evaluations. For AlpacaEval 2.0, we use the length-controlled win rate as the metric.
