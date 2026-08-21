# Lecture 2: Vision Models

## Purpose

This lecture assumes basic knowledge of medical imaging and machine learning.
We will focus on what changes methodologically when medical vision models move
from task-specific systems to foundation vision models and vision-languge models.

## Learning Outcomes

After this lecture, you will be able to:

- Explain the progression from task-specific vision models to self-supervised
  foundation models and vision-language models;
- Distinguish image-only, contrastive image-text, and generative
  vision-language models by representation, objective, and output;
- Compare the general and biomedical model pairs covered by the required
  papers;
- Critique their evaluation, biomedical validation, limitations, and workflow
  relevance.

## Assumed Background

The lecture will build on the topics below. If some of them are not familiar,
you can still follow the course, but you are expected to catch up independently
when needed.

- Common medical imaging modalities;
- Supervised classification and segmentation;
- Convolutional neural networks and vision transformers;
- Common metrics such as area under the ROC curve (AUC), Dice coefficient,
  sensitivity, and specificity.

## Preparation Focus

Read the papers for methodology, not for every implementation detail. Focus on
the progression:

- From supervised medical imaging models to self-supervised visual
  representation learning;
- From general self-supervised vision methods to medical vision foundation
  models;
- From image-only models to contrastive image-text models;
- From retrieval and matching to generative vision-language models;
- From benchmark evaluation to biomedical validation and workflow relevance.

## Required Preparation

Read all six papers. For each paper, identify (if applicable) the task, data, representation,
architecture, objective, training or adaptation strategy, and evaluation.

### Self-supervised vision models

1. Oquab et al. **DINOv2: Learning Robust Visual Features without
   Supervision**.
   [arXiv](https://arxiv.org/abs/2304.07193),
   [OpenReview](https://openreview.net/forum?id=a68SUt6zFt)
2. Chen et al. **Towards a general-purpose foundation model for computational
   pathology / UNI**.
   [PubMed](https://pubmed.ncbi.nlm.nih.gov/38504018/),
   [Nature Medicine](https://www.nature.com/articles/s41591-024-02857-3),
   [PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC11403354/)

### Contrastive vision-language models

3. Radford et al. **Learning Transferable Visual Models From Natural Language
   Supervision / CLIP**.
   [PMLR](https://proceedings.mlr.press/v139/radford21a.html),
   [arXiv](https://arxiv.org/abs/2103.00020)
4. Zhang et al. **BiomedCLIP: a multimodal biomedical foundation model
   pretrained from fifteen million scientific image-text pairs**.
   [arXiv](https://arxiv.org/abs/2303.00915),
   [model](https://huggingface.co/microsoft/BiomedCLIP-PubMedBERT_256-vit_base_patch16_224)

### Generative vision-language models

5. Liu et al. **Visual Instruction Tuning / LLaVA**.
   [arXiv](https://arxiv.org/abs/2304.08485),
   [project](https://llava-vl.github.io/)
6. Li et al. **LLaVA-Med: Training a Large Language-and-Vision Assistant for
   Biomedicine in One Day**.
   [arXiv](https://arxiv.org/abs/2306.00890),
   [OpenReview](https://openreview.net/forum?id=GSuP99u2kR)

## Vision-Language Distinction

For vision-language models, distinguish between:

- **Contrastive VLMs**, which align image and text embeddings for retrieval,
  matching, and zero-shot classification;
- **Generative VLMs**, which condition on images and text prompts to generate
  captions, answers, explanations, or reports.

Ask what the model is optimized to do. Matching an image to a report is not the
same objective as generating a report, and the evaluation risks are different.

Retrieval is a central use case for contrastive VLMs. Ask what is being
retrieved:

- An image given a text query;
- A report or caption given an image;
- Similar cases using image features, text features, or both.

For biomedical retrieval, also ask whether the retrieved item is clinically
meaningful, whether similar-looking images imply similar diagnoses, and whether
the evaluation uses realistic queries.

## Preparation Questions

Bring short notes on:

1. What is the general method?
2. What biomedical problem or data type is used?
3. What representation is learned?
4. What objective is optimized?
5. Is the model image-only, contrastive image-text, or generative image-text?
6. What is retrieved or generated?
7. What kind of validation is used?
8. What changes when moving from general AI benchmarks to biomedical use?

## In-Class Focus

We will compare:

- Task-specific models versus foundation models;
- Supervised labels versus self-supervised, image-text, or prompt-based
  supervision;
- Pure vision foundation models versus vision-language models;
- Contrastive VLMs versus generative VLMs;
- Classification, segmentation, retrieval, and generation as different tasks;
- Image-only models versus vision-language models;
- Benchmark performance versus evidence for clinical use.
