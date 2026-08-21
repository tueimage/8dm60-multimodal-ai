# Lecture 5: Integration of AI in Clinical Workflow

## Purpose

This lecture shifts the focus from model methodology to deployment. 
Most published models never reach clinical practice, and the gap is rarely about architecture. 
It is about how a model would actually be used, and what could go wrong when it is. 
We examine the clinical workflow as a system, the patterns by which AI models are integrated into it, validation for deployment versus validation for publication, the regulatory and governance environment, human and organizational factors, and the economics of sustaining a deployed model over time.

## Assumed Background

The lecture will build on the topics below. If some of them are not familiar,
you can still follow the course, but you are expected to catch up independently
when needed.

- Common medical imaging modalities, including radiology and digital
  pathology (whole-slide imaging);
- Types of AI systems covered earlier in the course (vision models, hospital
  data models);
- Common evaluation metrics such as sensitivity, specificity, and AUC;
- Basic familiarity with how a diagnostic result moves through a clinical
  department (acquisition, reporting, sign-off).

## Preparation Focus

Read the papers for background knowledge. They set the level of the current
debate around AI adoption in clinical care. Focus on the progression:

- From published model performance to real-world clinical adoption;
- From algorithm validation to deployment validation (internal, external, and
  prospective);
- From a single-task model to its place within an end-to-end clinical
  workflow (acquisition, processing, reporting, downstream care);
- From technical integration points (scanner, PACS/LIS, viewer, worklist) to
  organizational integration (standards, procurement, real-world evaluation).

When a paper discusses the intended clinical context of a model, compare it to
how the model would actually have to sit inside a real workflow: who reviews
its output, at what point, and with what consequence if it is wrong.

## Required Preparation
<!-- 
Read papers as a background for this class.
-->


Section 1 — Framing: why integration is the hard part

Cai L, Meng B, Huang J, et al. The adoption paradox of artificial intelligence in computational pathology: a three-stage maturity model from algorithms to clinical integration. 2025.

Berbís MA, et al. Computational pathology in 2030: a Delphi study forecasting the role of AI in pathology within the next decade. eBioMedicine. 2023. https://www.thelancet.com/journals/ebiom/article/PIIS2352-3964(22)00609-0/fulltext


Section 1b - Validation and FAIR AI:


 Lekadir K, Frangi A F, Porras A R, Glocker B, Cintas C, Langlotz C P et al. FUTURE-AI: international consensus guideline for trustworthy and deployable artificial intelligence in healthcare BMJ 2025; 388:e081554 doi:10.1136/bmj-2024-081554


MASAI trial - Mammography screening 
 Lång K, Josefsson V, et al. Interval cancer, sensitivity, and specificity comparing AI-supported mammography screening with standard double reading without AI in the MASAI study: a randomised, controlled, non-inferiority, single-blinded, population-based, screening-accuracy trial. The Lancet. 2026. DOI: 10.1016/S0140-6736(25)02464-X
https://www.thelancet.com/journals/lancet/article/PIIS0140-6736(25)02464-X/abstract

Section 2 — The clinical workflow as a system

Kohli M, Alkasab T, Wang K, et al. Integrating and Adopting AI in the Radiology Workflow: A Primer for Standards and Integrating the Healthcare Enterprise (IHE) Profiles. Radiology. 2024. https://pubs.rsna.org/doi/10.1148/radiol.232653 (open access via PMC: https://pmc.ncbi.nlm.nih.gov/articles/PMC11208735/)

Evans AJ, Brown RW, Bui MM, et al. Validating Whole Slide Imaging Systems for Diagnostic Purposes in Pathology: Guideline Update From the College of American Pathologists in Collaboration With the American Society for Clinical Pathology and the Association for Pathology Informatics. Arch Pathol Lab Med. 2022;146(4):440–450. https://meridian.allenpress.com/aplm/article/146/4/440/464968

Review and Commentary on Digital Pathology and Artificial Intelligence in Pathology [PPD-AI prostate trial commentary]. JCO Clinical Cancer Informatics. 2025. https://ascopubs.org/doi/10.1200/CCI-25-00017

Section 3 — Integration patterns and where the model sits

NHS England. Planning and implementing real-world artificial intelligence (AI) evaluations: lessons from the AI in Health and Care Award. https://www.england.nhs.uk/long-read/planning-and-implementing-real-world-ai-evaluations-lessons-from-the-ai-in-health-and-care-award/
Procurement and early deployment of artificial intelligence tools for chest diagnostics in NHS services in England: a rapid, mixed method evaluation. 2025. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC12675025/




## Integration Patterns

For every AI system discussed in this lecture, ask where it sits in the
clinical workflow and how much autonomy it has. Broad patterns include:

- **Pre-screen / triage** — runs before the clinician, reorders or flags
  cases (e.g., worklist prioritization);
- **Concurrent assistant** — runs alongside the clinician, e.g., an in-viewer
  overlay or report pre-population, informs the read without reordering work;
- **Second-reader / QC** — runs after a first read and flags discrepancies
  for review;
- **Autonomous** — produces a decision without clinician review, for a
  defined, low-risk scope.

Each pattern implies a different consequence of error and a different
required depth of validation. An autonomous system needs prospective,
site-specific validation before go-live; a second-reader QC system tolerates
more false positives because a clinician remains the final check. Ask, for
each paper and example discussed, which pattern is used and whether the
validation evidence matches the autonomy of that pattern.

## Preparation Questions

Bring short notes on:

1. What clinical problem does the system address, and at what point in the
   workflow is it applied?
2. What integration pattern is used (pre-screen/triage, concurrent assistant,
   second-reader/QC, or autonomous)?
3. What validation was performed, and how does it differ from validation for
   publication (internal vs. external vs. prospective)?
4. What operating point or metric was chosen for deployment, and how does
   that differ from a headline AUROC reported in the paper?
5. What regulatory pathway or classification applies (e.g., SaMD, CE-IVD/FDA
   clearance), and is the algorithm locked or adaptive?
6. Who is accountable for an AI-assisted decision, and how are errors
   detected, reported, and monitored after deployment?
7. What human factors are relevant (automation bias, alert fatigue, added
   workflow steps, trust calibration)?
8. Who pays for the system, and what does it cost to run and maintain it
   beyond initial deployment?

## In-Class Focus

We will compare:

- Published model performance versus real-world clinical adoption;
- Validation for publication versus validation for deployment (internal,
  external, and prospective);
- Integration patterns: pre-screen/triage, concurrent assistant,
  second-reader/QC, and autonomous use;
- Human-in-the-loop versus human-on-the-loop oversight;
- Locked versus adaptive algorithms under regulatory frameworks (SaMD,
  EU MDR/IVDR, FDA pathways, the EU AI Act);
- AI as augmenting versus replacing the clinician;
- Radiology's more mature PACS/AI ecosystem versus pathology's earlier-stage
  integration, as a reusable pattern for other domains.


<!--
We will close by tracing one deployed tool end-to-end from its clinical problem
and data flow through integration, validation, monitoring, and governance. A
design exercise will ask students to integrate a grading or triage model into a
specific clinical pathway, specifying data flow, integration pattern,
validation plan, failure modes, and mitigations.
-->
