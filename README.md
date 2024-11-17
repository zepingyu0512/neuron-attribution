# EMNLP 2024: Neuron-Level Knowledge Attribution in Large Language Models

## Introduction

This repo is for the EMNLP 2024 paper: [Neuron-Level Knowledge Attribution in Large Language Models](https://zepingyu0512.github.io/neuron-attribution.github.io/).

This work introduces how to identify the important neurons for the prediction token in LLMs. It first identifies the "value FFN neurons" (usually in medium-deep layers) and "value attention neurons" (usually in medium-deep layers) using the log probability increase method. Then it identifies the "query FFN neurons" (usually in shallow-medium layers) by calculating the inner products between each query FFN neuron and the top30 value attention neurons.

This work also uses the techniques and insights in:

[EMNLP 2024: How do Large Language Models Learn In-Context? Query and Key Matrices of In-Context Heads are Two Towers for Metric Learning](https://zepingyu0512.github.io/in-context-mechanism.github.io/)

[EMNLP 2024: Interpreting Arithmetic Mechanism in Large Language Models through Comparative Neuron Analysis](https://zepingyu0512.github.io/arithmetic-mechanism.github.io/)

## Tips for understanding neurons in LLMs

Understand the value neurons' interpretability when projecting in unembedding space: 

If the neuron's coefficient score is larger than zero, the top tokens' probabilities are increased, and the last tokens' probabilities are decreased.

If the neuron's coefficient score is smaller than zero, the top tokens' probabilities are decreased, and the last tokens' probabilities are increased.

## Running code

Before running the code, you can directly have a look at the jupyter notebook file in Llama_view_knowledge.ipynb or GPT2_view_knowledge.ipynb. The interpretability findings are visualized, without running the code yourself.

Environment versions: please see **environment.yml**

First, please use modeling_llama.py or modeling_gpt2.py to replace the original file in the transformers path, which is usually in anaconda3/envs/YOUR_ENV_NAME/lib/python3.8/site-packages/transformers/models/llama or anaconda3/envs/YOUR_ENV_NAME/lib/python3.8/site-packages/transformers/models/gpt2. This modified file is useful for extracting the internal vectors during inference time. **Please remember to save the original files.** 

Then, run the code in Llama_view_knowledge.ipynb or GPT2_view_knowledge.ipynb using jupyter notebook. This introduces how to identify and analyze the value neurons and query neurons for one sentence.

## cite us: 

```
@inproceedings{yu2024neuron,
  title={Neuron-Level Knowledge Attribution in Large Language Models},
  author={Yu, Zeping and Ananiadou, Sophia},
  booktitle={Proceedings of the 2024 Conference on Empirical Methods in Natural Language Processing},
  pages={3267--3280},
  year={2024}
}
```
