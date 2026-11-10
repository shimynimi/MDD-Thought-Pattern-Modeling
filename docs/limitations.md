# Scope, evidence, and limitations

## What this repository documents

This repository documents a computational framework described in a poster presented at the 19th Swedish Cognitive Science Society Conference (SweCog 2024). The poster outlines a pipeline involving conversational data, concept-space representations, a large language model, and an inverse model using Bayesian and variational inference.

## Evidence available in the poster

The poster supports the following descriptions:

- conversations between psychologists and patients are the described data source;
- questions, responses, and thought-pattern labels are represented by (Q_i), (R_i), and (T_i);
- the diagram includes suicide, anxiety, and sadness as example thought-pattern categories;
- the generative component models an output/response conditioned on a concept and an input/question;
- the inverse component uses Bayesian inference and variational inference to infer a concept from an input and output.

## What is not established by the poster alone

The poster does not report or establish:

- a publicly available dataset or permission to redistribute conversational data;
- a complete implementation or executable pipeline;
- numerical performance, statistical significance, or comparison against baselines;
- external validation, prospective validation, or clinical validation;
- diagnostic accuracy, clinical utility, or readiness for clinical use.

Therefore, this repository must not be described as a clinically validated diagnostic system or a reproducible software release.

## Responsible handling of data

Psychologist–patient conversations can contain sensitive personal and health information. No identifiable, confidential, or otherwise restricted conversation data should be uploaded to this public repository. Any future data release or code that depends on data must follow the applicable consent, ethics, privacy, licensing, and institutional requirements.

## Future documentation

If original project materials become available and the co-authors agree, the repository may be extended with:

- implementation details and source code;
- dataset documentation and lawful access instructions;
- model specifications and training configuration;
- evaluation protocol, baselines, and numerical results;
- a reproducibility guide.

Any future additions should clearly distinguish the original poster framework from subsequent implementation or evaluation.
