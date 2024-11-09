# EMNLP 2024: Neuron-Level Knowledge Attribution in Large Language Models

## Introduction

This repo is for the EMNLP 2024 paper: [Neuron-Level Knowledge Attribution in Large Language Models](https://zepingyu0512.github.io/neuron-attribution.github.io/).

This work introduces how to identify the important neurons for the prediction token in LLMs. It first identifies the "value FFN neurons" (usually in medium-deep layers) and "value attention neurons" (usually in medium-deep layers) using the log probability increase method. Then it identifies the "query FFN neurons" (usually in shallow-medium layers) by calculating the inner products between each query FFN neuron and the top30 value attention neurons.

The code in the jupyter notebook also introduces how to analyze the positional value-output vectors, inspired by [this repo](https://github.com/zepingyu0512/in-context-mechanism) in [this EMNLP 2024 paper](https://zepingyu0512.github.io/in-context-mechanism.github.io/).

The code in the jupyter notebook also introduces how to get the interpretability of the shallow FFN neurons, inspired by [this repo](https://github.com/zepingyu0512/arithmetic-mechanism) in [this EMNLP 2024 paper](https://zepingyu0512.github.io/arithmetic-mechanism.github.io/).

## running code

Environment versions: please see **environment.yml**

First, please use modeling_llama.py to replace the original file in the transformers path, which is usually in anaconda3/envs/YOUR_ENV_NAME/lib/python3.8/site-packages/transformers/models/llama. This modified file is useful for extracting the internal vectors during inference time. **Please remember to save the original file.** 

Then, run the code in Llama_view_knowledge.ipynb using jupyter notebook. This introduces how to identify and analyze the value neurons and query neurons for one sentence.

## cite us: 

```
@article{yu2023exploring,
  title={Exploring the Residual Stream of Transformers},
  author={Yu, Zeping and Yang, Kailai and Liu, Zhiwei and Ananiadou, Sophia},
  journal={arXiv preprint arXiv:2312.12141},
  year={2023}
}
```
