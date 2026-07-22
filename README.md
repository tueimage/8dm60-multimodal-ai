# Multimodal AI in Biomedicine (8DM60)

## Overview

This MSc course introduces state-of-the-art AI systems in biomedicine and
teaches you how to reason about them systematically. You will study current
methods and applications, and learn how to analyze what problem is being solved, 
what data are used, how the model is constructed and trained, how it is evaluated, 
and what risks it introduces if applied in practice.

The course covers:

- Language models;
- Vision models;
- Molecular data models;
- Hospital data models;
- Clinical workflow integration;
- Agentic AI;
- Developing AI-based products for healthcare (as part of a guest lecture).

## Teaching Format

Lecture 1 is a classical lecture with introduction to the course and language models. In
lectures 2-6, the course uses a reversed-classroom format: you prepare
assigned papers or other materials before class, and lecture time is used for
discussion, comparison, and critical evaluation. The preparation material will
include recent AI systems and papers, so the course reflects current
developments in the field. The analytical framework below provides a stable
structure for analyzing them. Lecture 7 is a guest lecture on developing AI-based products
for healthcare.

Lectures and guided self-study sessions have different roles:

- **Lectures** support learning through explanation, discussion, and synthesis
  of the prepared papers and examples. The goal is to understand both the
  methods and their biomedical context.
- **Guided self-study sessions** use new, unseen problems. They simulate
  exam-style reasoning and help you apply the same concepts to unfamiliar
  cases.

Lecture discussions will usually include a short introduction, polling or
pooled questions, group discussion, and plenary discussion. 

In guided self-study, you will mainly practice two question types:

1. Analyzing a given biomedical AI system, for example from a paper;
2. Designing an AI system, or parts of one, for a biomedical use case.

## Analytical Framework

The course uses one recurring analytical framework for all topics. For every
biomedical AI method, ask:

1. What task is being solved?
2. What data are used?
3. How are the data preprocessed and represented?
4. What architecture is used?
5. What learning objective is optimized?
6. How is the model trained or adapted?
7. How is it evaluated and validated?
8. How would it be used in practice?
9. What could go wrong, and how can risks be reduced?

This framework is used in lectures, guided self-study sessions, project work,
and exam questions. It is meant to give you a stable structure for comparing
very different AI methods. Not every question will require all nine dimensions
in equal depth, but the framework can help identify which issues matter.

### General vs. Biomedical AI

General AI methods are often the starting point when developing biomedical 
AI systems, so some of the reading material will not be on biomedical applications
but on general AI methods. When analyzing such papers, first ask
what the reusable methodological idea is. Then ask what additional
considerations appear in the biomedical use case: data quality, labels,
workflow, intended users, safety, and consequences of errors. A method that
works on a general benchmark may still need substantial adaptation and
validation before it is useful in medical applications.

## Schedule

Lectures: Wednesdays 08:45-10:45. Guided self-study: Wednesdays 10:45-12:45.

| Week | Date | Lecture | Guided self-study |
| --- | --- | --- | --- |
| 1 | 2 September 2026 | Introduction and language models | Introduction to project work |
| 2 | 9 September 2026 | Vision models | Language models |
| 3 | 16 September 2026 | Molecular data models | Vision models |
| 4 | 23 September 2026 | Models for hospital data | Molecular data models |
| 5 | 30 September 2026 | Integration of AI in clinical workflow | Models for hospital data |
| 6 | 7 October 2026 | Agentic AI | Integration of AI in clinical workflow |
| 7 | 14 October 2026 | Developing AI products for healthcare (guest lecture)| Agentic AI |

## Project Work

You will work in groups of five on the medical-imaging project. Each group
chooses a focused research question within the project and builds and evaluates
a small AI system or analysis to answer it.

Deliverables are a one-page poster and code. Together, these count for **15%**
of the final grade. The written exam also contains group-specific project
questions, which may ask about methods, implementation details, or code. The
project-specific questions are an additional **15%** of the final grade.

Project description:

- [`project/medical-imaging.md`](project/medical-imaging.md)

## Assessment

| Component | Weight |
| --- | ---: |
| Project deliverables: poster and code | 15% |
| Group-specific project exam questions | 15% |
| Multiple-choice exam questions | 20% |
| General exam questions | 50% |

General exam questions follow the style practiced in guided self-study:
analysis of a given system and design for a biomedical use case, using (part of)
the analytical framework.

| Examination | Date | Time |
| --- | --- | --- |
| Written examination | 28 October 2026 | 13:30-16:30 |
| Resit written examination | 20 January 2027 | 18:00-21:00 |

## Course Materials

| File | Description |
| --- | --- |
| [`lectures/lecture-01-introduction-language-models.md`](lectures/lecture-01-introduction-language-models.md) | Lecture 1 instructions |
| [`lectures/lecture-02-vision-models.md`](lectures/lecture-02-vision-models.md) | Lecture 2 preparation |
| [`lectures/lecture-03-molecular-data-models.md`](lectures/lecture-03-molecular-data-models.md) | Lecture 3 preparation |
| [`lectures/lecture-04-hospital-data-models.md`](lectures/lecture-04-hospital-data-models.md) | Lecture 4 preparation |
| [`lectures/lecture-05-clinical-workflow.md`](lectures/lecture-05-clinical-workflow.md) | Lecture 5 preparation |
| [`lectures/lecture-06-agentic-ai.md`](lectures/lecture-06-agentic-ai.md) | Lecture 6 preparation |
| [`lectures/lecture-07-healthcare-ai-products.md`](lectures/lecture-07-healthcare-ai-products.md) | Lecture 7 preparation |
