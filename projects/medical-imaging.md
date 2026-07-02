# Medical Imaging Project

## Topic

Chest X-ray image-report analysis using the Indiana University Chest X-ray /
OpenI dataset.

## Goal

Choose one clear research question that can be addressed with this dataset,
then build and evaluate a small AI system or analysis to answer it. The project
should connect to the course themes: multimodal biomedical data, model
adaptation, evaluation, validation, and risk.

Possible research questions include:

- How well can a pretrained vision-language model retrieve the matching report
  for a chest X-ray study?
- Does using multiple views improve image-report retrieval compared with a
  single frontal image?
- Which findings are easiest or hardest for a retrieval or generative model to
  represent correctly?
- Are generated chest X-ray descriptions grounded in the image, or do they miss
  or invent clinically relevant findings?

You may also define your own question, as long as it is specific, feasible on
the available compute, and answerable with the dataset.

## Dataset

Use the **Indiana University Chest X-ray / OpenI** dataset, which contains
chest X-ray images paired with radiology reports.

- Dataset overview: [IU X-Ray](https://github.com/openmedlab/Awesome-Medical-Dataset/blob/main/resources/IU-Xray.md)
- Original source: [OpenI](https://openi.nlm.nih.gov/)
- Download mirror only: [Kaggle](https://www.kaggle.com/datasets/raddar/chest-xrays-indiana-university/download)

Use OpenI and the dataset overview for provenance and documentation. Use the
Kaggle link only as a convenient way to download the files.

Use study-level splits. If a report has multiple images, keep those images in
the same split and explain how they are represented.

## Minimum Requirements

Your project must include:

- A focused research question;
- A clear train/validation/test split, or a justified alternative if no
  training is performed;
- A simple baseline;
- A model or analysis method appropriate for the question;
- Quantitative evaluation where possible;
- Qualitative examples of success and failure;
- A short discussion of limitations and risks.

Suitable approaches include image-report retrieval, evaluation of a generative
vision-language model, comparison of image representations, finding-specific
analysis, or another well-justified method.

## Design Choices

Make the main choices explicit:

1. What question are you answering? Why is this question important?
2. Which data fields, images, and report sections do you use? Are they sufficient to answer the question?
3. How do you represent studies with multiple images?
4. Which model, baseline, or analysis method do you use and why? What alternatives did you consider?
5. How do you evaluate the result?
6. What are the main limitations and risks?

The project should be feasible on a single 2080 Ti GPU. Use frozen pretrained
encoders, lightweight adaptation, small batches, or subset-based evaluation
when needed.

## Deliverables

Submit:

1. A one-page poster.
2. Code that reproduces the main results or figures.

The poster/report must be self-contained. It should include the research
question, dataset, method, key design choices, baseline, main result,
qualitative example, limitation, and interpretation. Do not rely on extra
repository notes for information needed to understand or assess the work.

The code is assessed as supporting evidence for reproducibility: it should make
it possible to reproduce the main results or figures, but it is not a substitute
for explaining the project clearly in the poster.
