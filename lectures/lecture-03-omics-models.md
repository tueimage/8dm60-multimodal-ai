# Lecture 3: Omics Models

## Purpose

This lecture focuses on how AI models learn from omics data, with single-cell
transcriptomics as the main example. We will examine how models move from
representing observed molecular states to predicting how cells respond to
interventions, and what evidence is needed to claim that these predictions
generalize beyond the training data.

The emphasis is not on surveying model architectures. Instead, we will use a
small set of papers to compare different modelling assumptions and ask what
their evaluation actually demonstrates.

## Assumed Background

The lecture will build on the topics below. If some of them are not familiar,
you can still follow the course, but you are expected to catch up independently
when needed.

- Basic molecular biology: genes, transcription, gene expression;
- Basic familiarity with bulk and single-cell RNA sequencing;
- Dimensionality reduction and latent representations;
- Neural networks, autoencoders and transformers;
- Basic concepts of supervised and self-supervised learning.

## Preparation Focus

Read the papers for methodology and scientific reasoning, not for every
implementation detail. Focus on the progression:

- From noisy molecular measurements to representations of cell state;
- From task-specific latent representations to large pretrained models;
- From representation learning to prediction of perturbation responses;
- From interpolation within observed conditions to prediction of unseen
  interventions;
- From architectural complexity to critical evaluation of what a model has
  actually learned.

Across the papers, pay particular attention to what kind of generalization is
claimed and what evidence supports that claim.

## Required Preparation

Read all six papers. For each paper, identify the task, data, representation,
architecture, objective, training strategy, evaluation setting, and main
assumptions.

### Representing molecular state

1. Lopez et al. **Deep generative modeling for single-cell transcriptomics /
   scVI**. *Nature Methods* (2018).  
   [Nature Methods](https://www.nature.com/articles/s41592-018-0229-2),
   [PubMed](https://pubmed.ncbi.nlm.nih.gov/30504886/)

### Large-scale pretrained representations

2. Cui et al. **scGPT: toward building a foundation model for single-cell
   multi-omics using generative AI**. *Nature Methods* (2024).  
   [Nature Methods](https://www.nature.com/articles/s41592-024-02201-0),
   [PubMed](https://pubmed.ncbi.nlm.nih.gov/38409223/)

3. Kedzierska et al. **Zero-shot evaluation reveals limitations of single-cell
   foundation models**. *Genome Biology* (2025).  
   [Genome Biology](https://link.springer.com/article/10.1186/s13059-025-03574-x),
   [PubMed](https://pubmed.ncbi.nlm.nih.gov/40251685/)

### Predicting perturbation response

4. Lotfollahi et al. **Predicting cellular responses to complex perturbations
   in high-throughput screens / CPA**. *Molecular Systems Biology* (2023).  
   [Molecular Systems Biology](https://www.embopress.org/doi/full/10.15252/msb.202211517),
   [PubMed](https://pubmed.ncbi.nlm.nih.gov/36920779/)

5. Roohani et al. **Predicting transcriptional outcomes of novel multigene
   perturbations with GEARS**. *Nature Biotechnology* (2024).  
   [Nature Biotechnology](https://www.nature.com/articles/s41587-023-01905-6),
   [PubMed](https://pubmed.ncbi.nlm.nih.gov/37592036/)

### What does good prediction actually mean?

6. Ahlmann-Eltze, Huber & Anders. **Deep-learning-based gene perturbation
   effect prediction does not yet outperform simple linear baselines**.
   *Nature Methods* (2025).  
   [Nature Methods](https://www.nature.com/articles/s41592-025-02772-6),
   [PubMed](https://pubmed.ncbi.nlm.nih.gov/40759747/)

## Key Conceptual Distinctions

### Measurement versus biological state

Gene-expression measurements provide a noisy and partial view of a cell's biological state.
Models therefore need to distinguish biologically meaningful variation from
technical variation introduced by the measurement process.

### Representation versus prediction

A useful representation for clustering or cell-type annotation does not
necessarily contain the information required to predict how a cell will respond
to an intervention.

### Generating observations versus predicting biological consequences

Generative models can reconstruct or sample plausible molecular measurements.
Perturbation-response models make a stronger claim: that they can predict an
unobserved biological response. These require different forms of validation.

### Interpolation versus extrapolation

Always ask what is held out during evaluation. Predicting new cells from a
known condition is different from predicting a new patient, cell type,
perturbation, perturbation combination, or biological context.

### Data scale versus biological priors

Large pretrained models aim to learn reusable structure from large datasets.
Other approaches explicitly incorporate assumptions or prior biological
knowledge. Neither automatically guarantees biological generalization.

## Preparation Questions

Bring short notes on:

1. What biological or methodological problem is being addressed?
2. What data and representations are involved?
3. What model or modelling assumption is being evaluated?
4. Does the work focus on representing biological states, predicting transitions
   or responses, or evaluating these capabilities?
5. What kind of generalization is claimed or tested?
6. What assumptions, prior knowledge, baselines, or evaluation choices are
   important?

## In-Class Focus

We will compare:

- Representing molecular states versus predicting changes between states;
- Task-specific models versus large pretrained models;
- Data scale versus biological prior knowledge;
- Different assumptions for predicting perturbation responses;
- Interpolation versus extrapolation to new contexts or interventions;
- Complex models versus simple baselines;
- Benchmark performance versus evidence of transferable biology.

A recurring question throughout the discussion will be:

> **What evidence would convince you that a model has learned transferable
> biology rather than statistical regularities in its training data?**
