# Lecture 4: Models for Hospital Data

## Purpose

This lecture focuses on **how clinical patient data are represented and modeled for prediction**. We will examine how different modeling approaches are shaped by the type, structure, and temporal nature of hospital data, progressing from traditional prediction models to longitudinal, multimodal, and patient-specific representations.

The lecture emphasizes the relationship between **clinical data, patient representation, model design, and evaluation**. We will examine what information is captured or lost by different representations, how modeling choices affect predictive performance and robustness, and how bias and uncertainty can arise from the clinical data-generating process.

The following lecture will build on these models by asking a different question: **how can a validated AI model be integrated safely and effectively into clinical practice?**

## Assumed Background

The lecture will build on the topics below. If some of them are not familiar,
you can still follow the course, but you are expected to catch up independently
when needed.

* Supervised machine learning;
* Basic deep learning concepts;
* Common evaluation metrics such as AUC, precision-recall, calibration, sensitivity, and specificity.

## Preparation Focus

Read the papers for methodology, not for every implementation detail. Focus on
the progression:

* From prediction using a single patient snapshot to longitudinal patient modeling;
* From structured EHR data to multimodal patient representations;
* From task-specific models to broader patient representations;
* From predictive performance to robustness, uncertainty, and fairness.

The emphasis is on understanding **how clinical data become a patient representation and how that representation is used to generate a prediction**.

## Required Preparation

Read the papers listed below. For each paper, identify (if applicable) the clinical task,
patient data, representation, model design, training strategy, sources of bias,
and evaluation methodology.

### Papers

1. A targeted real-time early warning score (TREWScore) for septic shock. https://www.researchgate.net/publication/280911361_A_targeted_real-time_early_warning_score_TREWScore_for_septic_shock
2. Development and external validation of a multimodal artificial intelligence mortality prediction model of critically ill patients using multicenter data. https://arxiv.org/abs/2512.19716
3. Predicting 30-day hospital readmissions using ClinicalT5 with structured and unstructured electronic health records. https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0328848

### Optional

* Patient Equity: Measuring and Mitigating Bias in Clinical AI. https://www.sciencedirect.com/science/article/pii/S1532046424000492?via%3Dihub
* Digital Twins in Healthcare. https://www.nature.com/articles/s41746-025-01910-w

## Key Conceptual Distinctions

As you read the papers, consider how each successive modeling approach changes the
representation of the patient and the information available to the model:

* **Static prediction models**, which make predictions from a single snapshot of patient data;
* **Longitudinal models**, which learn from patient trajectories over time;
* **Multimodal models**, which combine structured and unstructured patient information;
* **Patient-specific models and digital twins**, which seek to represent the evolving state of an individual patient.

### Static versus longitudinal patient representations

What is lost when time is compressed into a single snapshot?

### Structured versus unstructured patient data

What additional information becomes available when clinical text, signals, imaging, or other unstructured data are incorporated?

### Single-modality versus multimodal models

When does combining modalities actually add useful information, and when does it simply add complexity?

### Task-specific models versus broader/foundation models

Does a more general representation necessarily produce a better solution for a specific clinical task?

### Population-level prediction versus patient-specific modelling

What is the difference between predicting risk from a population and representing the evolving state of an individual?

### Model architecture versus data structure

How should the structure of the model reflect the structure of the available clinical data?

### Prediction versus representation

What is the difference between learning to predict a particular outcome and learning a broader representation of the patient?

### Performance versus robustness

Does good performance on a test set imply that the model will behave reliably under changes in patients, institutions, measurements, or clinical practice?

### Bias and data-generating processes

Where can bias enter through patient selection, measurements, labels, missingness, clinical practice, and other characteristics of the data-generating process?

### Uncertainty and failure

What kinds of uncertainty and failure are difficult to capture using standard performance metrics?

### Internal versus external/temporal validation

How can we test whether a model generalizes beyond the population, time period, or institution used for training?

## Preparation Questions

Bring short notes on:

1. What is the clinical prediction task?
2. What patient data are available to the model?
3. How is the patient represented: static, longitudinal, multimodal, or patient-specific?
4. What information is captured by this representation, and what information may be lost?
5. How does the model architecture reflect the structure of the patient data?
6. How is the model trained, and is the training approach appropriate for the task?
7. How is performance evaluated, and are the chosen metrics appropriate for the prediction task?
8. What are the important sources of bias, uncertainty, and failure?
9. Does the evaluation provide evidence that the model generalizes beyond the training data?

## In-Class Focus

We will compare:

* Static versus longitudinal patient representations;
* Structured versus multimodal patient representations;
* Classical machine learning versus deep learning;
* Task-specific models versus broader/foundation models;
* Population-level prediction versus patient-specific modelling;
* Model architecture in relation to the structure of clinical data;
* Discrimination, calibration, robustness, and uncertainty;
* Sources of bias in the clinical data-generating process;
* Dataset shift, missingness, label quality, and generalizability.

The lecture will conclude with the transition from **patient data → representation → model → prediction**.

The next lecture will continue from **prediction → clinical workflow → decision → outcome**, focusing on integration, validation for deployment, human factors, governance, and monitoring.
