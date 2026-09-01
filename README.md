# Multimodal AI in Biomedicine (8DM60)

## Overview

Modern biomedical AI systems are increasingly multimodal, meaning that they can work with a wide variety of data, including medical histories and reports, medical images, and *omics. The main learning goal of the course is to develop a solid familiarity with and understanding of state of the art unimodal AI systems, and how these systems can be combined and extended towards multimodal models, such as vision language models. The course also introduces agentic AI systems, in which AI models can reason over multiple sources of information, use external tools, and coordinate sequences of actions to address more complex biomedical and clinical tasks.

The course setup assumes that you have prerequisite knowledge in basic machine
learning concepts, including neural networks and optimization/training of
neural networks. A very brief introduction of these concepts will nevertheless be
given as part of the first lecture.

The course covers:

- Language models (lecturer: M. Veta);
- Vision models (lecturer: M. Veta);
- Omics models (lecturer: F. Eduati);
- Hospital data models (lecturer: F. Relouw);
- Clinical workflow integration (lecturer: N. Stathonikos, UMC Utrecht);
- Agentic AI (lecturer: M. Veta);
- Developing AI-based products for healthcare (guest lecturer: B. van Ginneken).

## Teaching Format

Lecture 1 is a classical lecture with introduction to the course and language models. In
lectures 2-6, the course uses a reversed-classroom format: you prepare
assigned papers or other materials before class, and lecture time is used for
discussion, comparison, and critical evaluation. The preparation material will
include recent AI systems and papers, so the course reflects current
developments in the field.

Lecture 7 is a guest lecture on developing AI-based
products for healthcare and is **not part of the exam material**.

Lectures and guided self-study sessions have different roles:

- **Lectures** support learning of the fundamental concepts and methodology,
as well as their biomedical context.

- **Guided self-study sessions** practice applying what you have learned to new, unseen problems.
In essence, they simulate exam-style questions and reasoning.

The flipped-classroom lectures have two discussion rounds. First, the lecturer
introduces several topic questions intended to stimulate discussion of the
assigned papers. In the second round, you submit questions through Mentimeter.
The highest ranked questions are discussed first in small groups and
then with the whole class.

Each guided self-study session will aim to cover approximately four or five exam-style
questions. A question is introduced, followed by 10 minutes to think through
it individually and 10 minutes to discuss it in a plenary setting. Questions may draw directly on
the papers covered in the lectures or introduce related methods that require
you to apply the same concepts in a new setting.

## Note on General vs. Biomedical AI

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
| 3 | 16 September 2026 | Omics models | Vision models |
| 4 | 23 September 2026 | Models for hospital data | Omics models |
| 5 | 30 September 2026 | Integration of AI in clinical workflow | Models for hospital data |
| 6 | 7 October 2026 | Agentic AI | Integration of AI in clinical workflow |
| 7 | 14 October 2026 | Developing AI products for healthcare (guest lecture)| Agentic AI |

## Project Work

You will work in groups of five on a medical imaging project. Each group
chooses a focused research question within the project and builds and evaluates
a small AI system or analysis to answer it.

Deliverables are a one-page poster and code. Together, these count for **15%**
of the final grade.

> The written examination also contains group-specific project questions about the methods, implementation, and code, worth another **15%** of the final grade (see below).

The project work has two Canvas assignments:

| Canvas assignment | What to submit | Points | Due |
| --- | --- | ---: | --- |
| Define research topic/question for the project work | Up to 400 words describing the proposed research topic or research question. Optional figures and references do not count toward the word limit. Upload one `.doc`, `.pdf`, or `.md` file. | 0 | 11 September 2026, 23:59 |
| Project work | One `.zip` archive containing the one-page poster in PDF format and documented code that can fully reproduce the experiments. | 15 | 14 October 2026 |

Both assignments are available to everyone. The second deadline was supplied
without a time; consult Canvas for any additional deadline details.

Project description:

- [`project/medical-imaging.md`](project/medical-imaging.md)

## Assessment

| Component | Weight |
| --- | ---: |
| Project deliverables: poster and code | 15% |
| Multiple-choice exam questions | 20% |
| Group-specific project exam questions | 15% |
| General open/problem-based exam questions | 50% |

The written examination accounts for **85%** of the final grade. The
multiple-choice questions assess recall-based knowledge. The group-specific
questions assess your project work, including its methods, implementation, and
code. The general questions are open or problem-based, with each question
corresponding to one of the course topics. They follow the style practiced in
guided self-study, such as analysis of a given system or design for a
biomedical use case.

| Examination | Date | Time |
| --- | --- | --- |
| Written examination | 28 October 2026 | 13:30-16:30 |
| Resit written examination | 20 January 2027 | 18:00-21:00 |

## Course Materials

> Note that some material might not be ready when the course starts, but will be made available on time for the lecture.

| File | Description |
| --- | --- |
| [`lectures/lecture-01-introduction-language-models.md`](lectures/lecture-01-introduction-language-models.md) | Lecture 1 instructions |
| [`lectures/lecture-01-introduction-language-models/lecture-01-introduction-language-models.pdf`](lectures/lecture-01-introduction-language-models/lecture-01-introduction-language-models.pdf) | Lecture 1 slides: course outline and language models foundations |
| [`lectures/lecture-02-vision-models.md`](lectures/lecture-02-vision-models.md) | Lecture 2 preparation |
| [`lectures/lecture-03-omics-models.md`](lectures/lecture-03-omics-models.md) | Lecture 3 preparation |
| [`lectures/lecture-04-hospital-data-models.md`](lectures/lecture-04-hospital-data-models.md) | Lecture 4 preparation |
| [`lectures/lecture-05-clinical-workflow.md`](lectures/lecture-05-clinical-workflow.md) | Lecture 5 preparation |
| [`lectures/lecture-06-agentic-ai.md`](lectures/lecture-06-agentic-ai.md) | Lecture 6 preparation |

## Use of AI Tools in Course Material Preparation

AI tools were used to support the preparation and editing of these materials, in accordance with TU/e policy. All content was reviewed and approved by the lecturers, who remain responsible for the final content.
