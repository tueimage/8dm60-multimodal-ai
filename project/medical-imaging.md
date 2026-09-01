# Medical Imaging Project

## Topic

Chest X-ray image-report analysis using the Indiana University Chest X-ray /
OpenI dataset.

## Starter Notebook

The completed [Medical imaging with MedGemma](medical-imaging-starter.ipynb)
notebook provides a starting point for the project, using the MedGemma vision-language model.
It covers dataset preparation, radiology report generation, image-feature exploration, QLoRA fine-tuning,
and comparison of reports before and after adaptation. Use its examples and
discussion questions to develop your own focused research question; the
notebook does not itself constitute a complete project. Your project should go
beyond what is included in the starter notebook.

## Goal

Define a focused research question that can be answered using this dataset,
then build and evaluate a small AI system or conduct an analysis to answer it.
Suitable directions include image-report retrieval, evaluation of a generative
vision-language model, comparison of image representations, and
finding-specific analysis.

Example research questions include:

- How well can a pretrained vision-language model retrieve the matching report
  for a chest X-ray study?
- Does using multiple views improve image-report retrieval compared with a
  single frontal image?
- Which findings are easiest or hardest for a retrieval or generative model to
  represent correctly?
- Are generated chest X-ray descriptions grounded in the image, or do they miss
  or invent clinically relevant findings?
- Can model adaptation improve the clinical accuracy of generated chest X-ray
  reports compared with the pretrained model?
- Does providing multiple views of a study improve report generation compared
  with using only the frontal image?
- Which clinical findings are most often correctly described, missed, or
  hallucinated in generated reports?
- How sensitive are generated reports to changes in prompt wording and report
  format instructions?

> These examples are starting points, not prescribed topics. Define your own question and ensure that it is specific, feasible with the available compute, and answerable using the dataset. Other approaches are welcome when they are well justified.

## Dataset

Use the **Indiana University Chest X-ray / OpenI** dataset, which contains
chest X-ray images paired with radiology reports.

- Dataset overview: [IU X-Ray](https://github.com/openmedlab/Awesome-Medical-Dataset/blob/main/resources/IU-Xray.md)
- Original source: [OpenI](https://openi.nlm.nih.gov/)
- Download mirror: [Kaggle](https://www.kaggle.com/datasets/raddar/chest-xrays-indiana-university/download)

Use OpenI and the dataset overview for documentation. Use the
Kaggle link only as a convenient way to download the files (the starter notebook shows how to do this programatically).

Use study-level splits. If a report has multiple images, keep those images in
the same split and explain how they are represented.

## Minimum Requirements

Your project must include:

- A focused research question;
- A clear train/validation/test split, or a justified alternative if, for example, no
  training is performed;
- A simple baseline;
- A model or analysis method appropriate for the question;
- Quantitative evaluation where possible;
- Qualitative examples of success and failure;
- A short discussion of limitations and risks.

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

## Canvas Assignments

### Define research topic/question for the project work

- **Due:** 11 September 2026 at 23:59;
- **Points:** 0;
- **Submission:** one file upload in `.doc`, `.pdf`, or `.md` format;
- **Available to:** everyone.

Submit up to 400 words describing the research topic or research question that
you want to address with the project work. Optional figures and references do
not count toward the 400-word limit.

### Project work

- **Due:** 14 October 2026;
- **Points:** 15;
- **Submission:** one `.zip` file upload;
- **Available to:** everyone.

Submit one ZIP archive containing the one-page poster in PDF format and the
documented code needed to fully reproduce the experiments. The supplied
deadline does not specify a time; consult Canvas for any additional deadline
details.

## Final Deliverables

The Project work ZIP archive must contain:

1. A one-page poster in PDF format.
2. Documented code that fully reproduces the experiments, including the main
   results or figures.

The poster/report must be self-contained. It should include the research
question, dataset, method, key design choices, baseline, main result,
qualitative example, limitation, and interpretation. Do not rely on extra
repository notes for information needed to understand or assess the work.
Use the TU/e house style template for scientific posters (available on the intranet).

> The poster should follow a scientific poster format rather than presenting a short paper compressed into a poster template. See [Ten Simple Rules for a Good Poster Presentation](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.0030102) for practical guidance.

The code is assessed as supporting evidence for reproducibility: it should make

it possible to reproduce the main results or figures, but it is not a substitute
for explaining the project clearly in the poster.
