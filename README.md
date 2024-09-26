# EMNLP 2024: Neuron-Level Knowledge Attribution in Large Language Models

This repo is for the EMNLP 2024 paper: [Neuron-Level Knowledge Attribution in Large Language Models](https://arxiv.org/pdf/2312.12141).

This work introduces how to identify the important neurons for the prediction token in LLMs. It first identifies the "value FFN neurons" (usually in medium-deep layers) and "value attention neurons" (usually in medium-deep layers) using the log probability increase method. Then it identifies the "query FFN neurons" (usually in shallow-medium layers) by calculating the inner products between each query FFN neuron and the top30 value attention neurons.

The code in the jupyter notebook also introduces how to analyze the positional value-output vectors, inspired by [this repo](https://github.com/zepingyu0512/in-context-mechanism) in EMNLP 2024 paper: [How do Large Language Models Learn In-Context? Query and Key Matrices of In-Context Heads are Two Towers for Metric Learning](https://arxiv.org/pdf/2402.02872).

The code in the jupyter notebook also introduces how to get the interpretability of the shallow FFN neurons, inspired by [this repo](https://github.com/zepingyu0512/arithmetic-mechanism) in EMNLP 2024 paper: [Interpreting Arithmetic Mechanism in Large Language Models through Comparative Neuron Analysis](https://arxiv.org/pdf/2409.14144).

## cite us: 

@article{yu2024neuron,
  title={Neuron-Level Knowledge Attribution in Large Language Models},
  author={Yu, Zeping and Ananiadou, Sophia},
  journal={arXiv preprint arXiv:2312.12141},
  year={2024}
}
