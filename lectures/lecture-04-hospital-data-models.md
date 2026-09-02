# Lecture 4: Models for Hospital Data

## Purpose

This lecture focuses on AI models for structured hospital data. We will examine how different clinical prediction models are designed, trained, and evaluated, progressing from traditional prediction models to multimodal AI systems and digital twins. Throughout the lecture, we will discuss how modeling choices influence clinical performance, fairness, and applicability.

## Assumed Background

The lecture will build on the topics below. If some of them are not familiar,
you can still follow the course, but you are expected to catch up independently
when needed.

- Supervised machine learning;
- Basic deep learning concepts;
- Common evaluation metrics such as AUC, precision-recall, calibration, sensitivity, and specificity.

## Preparation Focus

Read the papers for methodology, not for every implementation detail. Focus on
the progression:

- From prediction using a single patient snapshot to longitudinal patient modeling;
- From structured EHR data to multimodal patient representations;
- From predictive performance to fairness, robustness, and clinical evaluation.

## Required Preparation

Read the papers listed below. For each paper, identify (if applicable) the clinical task,
patient data, representation, model design, training strategy, sources of bias,
and evaluation methodology.

### Papers
1. Interpretable Machine Learning for Predicting Sepsis Risk in Emergency Triage Patients. https://www.nature.com/articles/s41598-025-85121-z


### Optional
- Patient Equity: Measuring and Mitigating Bias in Clinical AI. https://www.sciencedirect.com/science/article/pii/S1532046424000492?via%3Dihub
- Digital Twins in Healthcare. https://www.nature.com/articles/s41746-025-01910-w

## Key Conceptual Distinctions
As you read the papers, consider how each successive model changes the representation of the patient:
 
- Static prediction models, which make predictions from a single snapshot of patient data;
- Longitudinal models, which learn from patient trajectories over time;
- Multimodal models, which combine structured and unstructured patient information;
- Digital twins, which seek to model the evolving physiological state of an individual patient.

### Static versus longitudinal patient representations
What is lost when time is compressed into a single snapshot?
### Structured versus unstructured patient data
What additional information becomes available when clinical text, signals, or other unstructured data are incorporated?
### Single-modality versus multimodal models
When does combining modalities actually add clinically useful information?
### Task-specific models versus broader/foundation models
Does a more general representation necessarily produce a better clinical solution?
### Population-level prediction versus patient-specific modelling
What is the difference between predicting risk from a population and representing the evolving state of an individual?
### Prediction versus clinical decision support
A model can predict well without necessarily improving a clinical decision.
### Internal validation versus real-world evidence
What changes when moving from retrospective benchmark performance to external, prospective, and workflow-based evaluation?
### Performance versus clinical utility
Is the model accurate enough, at the right threshold, at the right time, and for the right user?
### Bias and data-generating processes
Where can bias enter through patient selection, measurements, labels, missingness, clinical practice, and deployment?

## Preparation Questions
Bring short notes on:
1. What is the clinical task or decision?
2. What patient data are available to the model?
3. How is the patient represented and is the model static, longitudinal, multimodal etc.?
4. When in the clinical workflow is the prediction or output generated?
5. How is the model trained, and is the training approach appropriate for the task?
6. How is performance evaluated, and are the evaluation metrics clinically meaningful?
7. What are the important sources of bias, uncertainty, and failure?
8. What evidence supports clinical usefulness and generalizability?

## In-Class Focus
We will compare:
 
- Static versus longitudinal patient models;
- Classical machine learning versus deep learning;
- Single-modality versus multimodal AI;
- Population-level prediction versus patient-specific digital twins;
- Sources of bias in clinical AI;
- Internal, external, and prospective validation;
- Predictive performance versus clinical utility.
