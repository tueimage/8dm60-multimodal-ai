# Lecture 1: Introduction and Language Models

## Purpose

This first lecture introduces the course setup, the assessment structure, and
a first overview of language models with focus on biomedical AI applications.

This lecture is more classical than the later lectures. The reversed-classroom
format starts from Lecture 2.

## Learning Outcomes

After this lecture, you will be able to:

- Explain language modelling as a machine-learning problem based on
  self-supervised next-token prediction, including its strengths and
  limitations;
- Describe how tokenization, contextual representations, attention, and
  autoregressive prediction are used in Transformer language models;
- Compare prompting, retrieval-augmented generation, and fine-tuning as
  adaptation strategies;
- Explain why full fine-tuning is expensive and how PEFT and LoRA reduce the
  number of trainable parameters;
- Explain quantization and how QLoRA combines a quantized frozen base model
  with trainable LoRA adapters;
- Distinguish an adaptation mechanism from its training objective, including
  instruction tuning;
- Identify important evaluation and deployment considerations for biomedical
  language-model systems, including evidence, limitations, human and tool
  interaction, and monitoring.

## Preparation

Before the lecture:

1. Read the course README;
2. Review the medical-imaging project description and starter notebook.

No paper preparation is required for this first lecture.

## Suggested Literature

The papers below are optional. Use them to explore particular concepts from
the lecture in more depth.

### Transformer and language-model foundations

1. Vaswani et al. **Attention Is All You Need**.
   [arXiv](https://arxiv.org/abs/1706.03762)
2. Brown et al. **Language Models are Few-Shot Learners**.
   [NeurIPS](https://proceedings.neurips.cc/paper/2020/file/1457c0d6bfcb4967418bfb8ac142f64a-Paper.pdf)

### Adaptation and efficient fine-tuning

3. Lewis et al. **Retrieval-Augmented Generation for Knowledge-Intensive NLP
   Tasks**.
   [arXiv](https://arxiv.org/abs/2005.11401)
4. Chung et al. **Scaling Instruction-Finetuned Language Models**.
   [JMLR](https://www.jmlr.org/papers/v25/23-0870.html)
5. Hu et al. **LoRA: Low-Rank Adaptation of Large Language Models**.
   [arXiv](https://arxiv.org/abs/2106.09685)
6. Dettmers et al. **QLoRA: Efficient Finetuning of Quantized LLMs**.
   [NeurIPS](https://proceedings.neurips.cc/paper_files/paper/2023/hash/1feb87871436031bdc0f2beaa62a049b-Abstract-Conference.html)

### Biomedical use and evaluation

7. Singhal et al. **Large Language Models Encode Clinical Knowledge**.
   [Nature](https://www.nature.com/articles/s41586-023-06291-2)

## In-Class Focus

We will discuss:

- Course structure, project work, and assessment;
- Language modelling as a machine-learning problem;
- Tokenization, embeddings, Transformers, attention, and autoregressive
  generation;
- Self-supervised next-token pretraining and its limitations;
- Prompting, retrieval-augmented generation, and fine-tuning;
- PEFT and LoRA, including their computational trade-offs;
- Quantization and QLoRA;
- Instruction tuning and the distinction between adaptation methods and
  training objectives;
- An introduction to biomedical applications and the evaluation and deployment
  questions covered later in the course.
