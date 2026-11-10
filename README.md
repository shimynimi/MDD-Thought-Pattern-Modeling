# Identifying Thought Patterns in Major Depressive Disorder

**Using Variational Inference and Large Language Models Integrated with Concept Space**

Conference poster presented at the **19th Swedish Cognitive Science Society Conference (SweCog 2024)**, Stockholm, Sweden.

**Authors:** Mariam Marlen Mirström, Mohammad-Hossein Heydari Beni, and Shima Rezai  
**Poster number:** 42 (P42)

[Conference proceedings / abstract](https://www-static.swecog.se/wp-content/uploads/2026/04/SweCog2024_Proceedings.pdf)

---

## Project overview

This repository documents the research framework presented in the SweCog 2024 poster. The poster describes a computational approach to representing and inferring thought patterns associated with Major Depressive Disorder (MDD) from psychologist–patient conversational data.

The proposed framework combines:

- conversational data represented through questions, responses, and thought-pattern labels;
- a **concept-space representation** of thought patterns;
- a **generative language model** that models responses conditioned on a question and a thought-pattern concept; and
- an **inverse model** using Bayesian inference and variational inference to infer a latent thought-pattern concept from an observed question–response pair.

This repository is a **research documentation archive for the conference poster**. It is not presented as a complete, independently reproducible implementation or as a clinically validated diagnostic tool.

## Framework at a glance

### 1. Conversational dataset

The poster describes collecting conversations between psychologists and patients with different known thought patterns. The data are preprocessed into vector representations:

| Symbol | Meaning in the poster |
| --- | --- |
| (Q_i) | Question |
| (R_i) | Response |
| (T_i) | Thought pattern |

The poster illustrates categories including **suicide**, **anxiety**, and **sadness**. These are the categories shown in the poster diagram; this repository does not claim that the dataset is publicly available.

### 2. Generative model: LLM and concept space

The concept space is used to represent thought patterns. The poster describes training a language model to map a thought-pattern representation and a question to a corresponding response.

The generative component is expressed as:

`P(Output | Concept, Input)`

Here, the input is the question, the output is the response, and the concept represents a thought pattern.

### 3. Inverse model: Bayesian and variational inference

The poster then describes using the trained generative model as part of an inverse inference procedure. Given a conversation (question and corresponding response), the inverse model aims to infer the associated thought-pattern concept.

The poster frames this step in Bayesian terms, including a prior over the concept space and questions, and identifies **variational inference** as the inference technique.

For a poster-grounded description of the pipeline, see [the methodology note](docs/methodology.md).

## Research themes

- Computational modeling of cognition and thought patterns
- Concept-space representations
- Natural language processing and large language models
- Generative modeling
- Bayesian inference and variational inference
- Computational approaches related to mental health research

## What this repository contains

This repository currently provides a structured description of the framework presented in the conference poster:

- [Methodology and framework](docs/methodology.md)
- [Scope, evidence, and limitations](docs/limitations.md)
- [Citation information](CITATION.cff)

The conference poster and proceedings should be treated as the primary records of the presented work. No implementation, model checkpoint, patient conversation, quantitative result, or clinical evaluation is claimed here unless it is separately added with appropriate documentation and permission.

## Scope and limitations

The poster presents a framework and its conceptual pipeline. The poster image and the available proceedings description do not, by themselves, establish:

- a publicly distributable dataset;
- a complete source-code implementation or trained model;
- quantitative performance metrics or statistical validation;
- clinical validation or diagnostic accuracy; or
- evidence that the framework can be used for clinical decision-making.

Accordingly, this repository describes the **conference-poster framework**, not a validated MDD assessment system. See [limitations](docs/limitations.md).

## Conference record and citation

Mariam Marlen Mirström, Mohammad-Hossein Heydari Beni, and Shima Rezai.  
*Identifying Thought Patterns in Major Depressive Disorder Using Variational Inference and Large Language Models Integrated with Concept Space.*  
Poster presented at the 19th Swedish Cognitive Science Society Conference (SweCog 2024), Stockholm, Sweden. Poster 42.

Please cite the conference record rather than treating this GitHub repository as a peer-reviewed journal article.

## Authors

- Mariam Marlen Mirström
- Mohammad-Hossein Heydari Beni
- Shima Rezai

