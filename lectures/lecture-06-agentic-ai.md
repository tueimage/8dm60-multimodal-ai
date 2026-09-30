# Lecture 6: Agentic AI

## Purpose

This lecture examines how AI models become parts of systems that select tools,
carry out actions, observe their results, and decide what to do next. We will
connect the language, vision, omics, and hospital-data models covered earlier
in the course to biomedical research and clinical tasks that require several
steps and multiple sources of information.

The central question is how to design and evaluate the whole system: what
information it receives, which actions it can perform, how it responds to
failure, when it should stop or ask for human input, and how to evaluate the
reasoning behind its answers.

## Learning Outcomes

After preparation and discussion, you should be able to:

1. Explain what tools are and how a language model that only generates text
   can call and use them.
2. Distinguish a predefined workflow from an agent that
   dynamically selects its next action.
3. Trace an agent's actions and observations, explaining how its available
   context, tools, and stopping conditions affect its behaviour.
4. Compare the use of one agent and a simpler
   fixed workflow for a biomedical task.
5. Evaluate an agent both on its final answer and on how it reached it,
   including its reasoning, the actions it took, and their cost.
6. Decide where an agent should stop, run an automatic check, or ask a human
   for approval, and justify these choices by the consequences of an error.

## Assumed Background

This lecture will mostly build on the topics covered in previous lectures.

- Language models, prompting, context windows, and retrieval-augmented
  generation (Lecture 1);
- The role of specialist models for images, omics, and hospital data
  (Lectures 2–4);
- Basic evaluation concepts: held-out data, baselines, generalization, and bias;
- Clinical workflow integration, human oversight, and consequences of errors
  (Lecture 5);
- The idea of a software function or API: an operation with defined inputs
  and outputs. Prior experience implementing agents or protocols is not required.

## Preparation Focus

Read the materials for their main ideas and skip implementation details.
Focus on the progression:

- Tools: operations with defined inputs and outputs, such as a literature
  search, a database query, or a segmentation model;
- From language models that generate text to language models that call and
  use tools;
- From predefined workflows to agents that choose their next action based on
  new observations;
- From checking the final answer to evaluating the reasoning and actions
  behind it.

**From generating text to calling tools.** A language model can only generate
text (Lecture 1). The model runs inside a larger program, often called the
agent harness. The harness builds the prompt, including a short description of
each tool (its name, what it does, and what input it needs), sends it to the
model, and reads the reply. If a tool would help, the model replies with a
request in a fixed format, for example a request to segment the tissue in an
image. When the reply is a tool request, the harness runs the tool, adds the
result to the conversation, and calls the model again. It also enforces limits,
such as a maximum number of steps. In short, the model writes requests and the
harness carries them out. Models learn to write such requests from examples,
either in the prompt or during training.

A reply can contain three kinds of generated text: reasoning, which stays in
the conversation and guides the next step; a tool request, which the harness
executes; and a final answer for the user. Many current models write their
reasoning in a separate thinking section, which applications may hide or
summarize. This written reasoning is generated like any other text, so it may
differ from how the model actually reached its answer (Lecture 1).

Earlier lectures focused on the model itself: its architecture, objective, and
training. In agentic systems the model is usually used as it is, and the main
design choices concern what surrounds it: which tools it can use, which steps
are fixed in advance, and when a human must approve an action.

**Example: combining imaging tools.** A researcher asks, “Which
tissue regions in this microscopy image have the highest density of nuclei?”
The language model can call a tissue-segmentation model, a nucleus detector,
and tools for reading image metadata and calculating measurements. In this
hypothetical example, one possible sequence is:

| Model request or answer | What the harness does |
| --- | --- |
| Read the image metadata. | Returns image dimensions and pixel size. |
| Segment the tissue regions. | Runs the segmentation model and returns region identifiers and references to their masks. |
| Detect nuclei in the image. | Runs the detection model and returns a reference to the nuclei coordinates and confidence scores. |
| Calculate nuclei density in each region. | Passes the masks, coordinates, and pixel size to a measurement tool, which returns counts, segmented tissue areas, and nuclei per mm². |
| Report which regions have the highest estimated nuclei density. | Shows the comparison with its supporting measurements and ends the loop. |

## Required Preparation

Read the specified parts of the three materials below: a research paper, an
engineering article, and a commentary. Consider what kind of evidence each
source provides. The learning objectives define the reading focus; API syntax,
framework installation, and benchmark scores are not required.

### 1. From generating text to using tools: ReAct

Yao et al. **ReAct: Synergizing Reasoning and Acting in Language Models**.
*ICLR* (2023).
[Paper](https://arxiv.org/abs/2210.03629),
[full text](https://arxiv.org/html/2210.03629v3)

**Reading focus:** Read the introduction, Section 2, and Sections 3.1 and 3.2,
and study Figure 1. Note how each action is written as text in a fixed format,
such as `search[entity]` for a Wikipedia search, and how examples in the prompt
teach the model this format.

**After reading, you should be able to:**

- Explain how actions written as text are executed by the harness and
  returned as observations, and trace how reasoning, actions, and observations
  lead to each next decision.
- Explain why, in the paper's comparisons, reasoning alone can produce invented
  facts, and how reasoning helps the model keep track of its plan while acting.

### 2. Workflows, agents, and orchestration

Anthropic. **Building effective agents** (2024).
[Engineering article](https://www.anthropic.com/engineering/building-effective-agents)

**Reading focus:** Read “What are agents?”, “When (and when not) to use agents”,
and “Building blocks, workflows, and agents”, including the diagrams. The first
building block, the augmented LLM, is a model with retrieval, tools, and memory.

**After reading, you should be able to:**

- Explain the distinction between predefined workflows and agents that choose
  their actions dynamically, recognizing that terminology varies.
- Compare prompt chaining, routing, parallelization, orchestrator-workers, and
  evaluator-optimizer, and justify when an agent's flexibility is worth its
  cost compared with a simpler workflow.

### 3. Evaluating agents in clinical settings

Mehandru et al. **Evaluating large language models as agents in the clinic**.
*npj Digital Medicine* 7, 84 (2024).
[Article](https://www.nature.com/articles/s41746-024-01083-y)

**Reading focus:** Read the full short commentary, especially the proposed
Artificial Intelligence Structured Clinical Examinations (AI-SCE) framework.
Read it as a proposal for how clinical agents should be evaluated.
Its “agent-based models” simulate patients and clinicians, a different sense
of “agent”.

**After reading, you should be able to:**

- Explain why static medical question answering does not fully test an
  interactive agent in a clinical workflow.
- Propose assessments of intermediate actions, tool use, interactions,
  outcomes, and cost in a simulated task, and identify the further evidence
  needed for real clinical use.

### Optional

These readings are not part of the exam.

- Model Context Protocol. **Architecture overview** (version 2026-07-28).
  [Documentation](https://modelcontextprotocol.io/docs/2026-07-28/learn/architecture).
  How applications describe tools to a model and run them in a standard way.
- Miao et al. **Reimagining research papers as interactive and reliable AI
  agents**. *Nature* (2026).
  [Paper](https://www.nature.com/articles/s41586-026-11044-y).
  Turns the code of published biomedical methods into tested tools for agents.
- Anthropic. **Previewing the Model Hardware Standard** (27 August 2026).
  [Announcement](https://www.anthropic.com/news/model-hardware-standard-research-preview).
  A research preview of agents controlling laboratory equipment, with early
  partner demonstrations.
- Trost et al. **An agentic framework for autonomous scientific discovery in
  cancer pathology / SPARK**. *Nature Medicine* (2026).
  [Article](https://www.nature.com/articles/s41591-026-04357-y).
  Agents turn biological ideas into tissue measurements computed with existing
  segmentation and cell-detection models.
- Two MICCAI 2026 challenges that score the reasoning of agents along with
  their answers: [CHIMERA-agent](https://zenodo.org/records/19818695), on
  prostate cancer decisions with imaging and pathology tools, and
  [REG²](https://zenodo.org/records/19848983), on pathology report generation.
  The links go to the challenge design documents.

## Key Conceptual Distinctions

Use these questions to connect the readings.

| Distinction | Question to ask |
| --- | --- |
| Written request versus executed action | The model writes a request to use a tool. Which part of the system runs the tool, and what does the model see afterwards? |
| Model versus complete agent system | Which behaviour comes from the model itself, and which from the harness: its tools, instructions, and limits? |
| Fixed workflow versus agent | Can the steps be fixed in advance, as in the retrieve-then-generate RAG pipeline of Lecture 1, or must the next step depend on what the system observes? |
| One multimodal model versus orchestration of specialist tools | Should one model, such as a vision-language model (Lecture 2), process all inputs, or should an agent call separate specialist models and combine their outputs? |
| Agreement between agents versus independent checking | If several copies of the same model agree, is that evidence of a correct answer, or could they all repeat the same mistake? |
| Correct answer versus sound reasoning | Can a system give the right answer with a wrong or unsupported explanation, and how would an evaluation detect this? |
| Written reasoning versus internal computation | The reasoning a model writes is generated text. How could you check whether it reflects how the answer was actually produced? |
| Demonstration versus evidence of reliability | Which cases, repeated runs, baselines, and failure conditions were actually tested? |

## In-Class Focus

We will discuss an example of a biomedical agent, exploring how it combines
AI models and tools to address a research question.
