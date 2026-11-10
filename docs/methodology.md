# Methodology described in the SweCog 2024 poster

This note summarizes only the framework shown in the conference poster titled *Identifying Thought Patterns in Major Depressive Disorder Using Variational Inference and Large Language Models Integrated with Concept Space*.

## 1. Conversational data representation

The poster describes collecting psychologist–patient conversations associated with different known thought patterns. It then describes preprocessing the data into vector representations:

- (Q_i): question
- (R_i): response
- (T_i): thought pattern

The poster diagram displays the categories suicide, anxiety, and sadness. It does not provide a dataset release link, sample size, annotation protocol, or a detailed description of the vectorization procedure.

## 2. Generative model

The proposed generative component combines a concept-space representation with a large language model.

The concept space represents a thought pattern. The language model is described as learning to map a particular thought-pattern concept and a question to a response.

The conditional relationship shown in the poster is:

`P(Output | Concept, Input)`

In the notation used here, **Input** refers to the question and **Output** refers to the response.

## 3. Inverse model

The poster describes an inverse model intended to infer a thought-pattern concept from an observed conversation. It uses the trained generative model and Bayesian inference, with variational inference named as the inference technique.

The inverse task can be summarized conceptually as estimating:

`P(Concept | Input, Output)`

The poster also states that an appropriate prior over the concept space and questions is considered.

This repository does not add an unreported variational objective, parameterization, optimization algorithm, prior distribution, or model architecture. Those details would require additional project materials from the authors.

## 4. Pipeline summary

1. Collect psychologist–patient conversational data associated with known thought patterns.
2. Preprocess the questions, responses, and thought-pattern labels into representations.
3. Use a concept space and an LLM as a generative model of responses conditioned on a question and a thought-pattern concept.
4. Use an inverse model with Bayesian and variational inference to estimate a thought-pattern concept from a question–response pair.

## 5. Information not specified in the poster

The poster does not provide enough detail to reconstruct the complete experiment. In particular, it does not specify:

- the dataset size, source, or access conditions;
- the full preprocessing and vectorization procedure;
- the LLM identity, configuration, or training details;
- the mathematical form and parameterization of the concept space;
- the variational family, objective, or optimization procedure;
- quantitative evaluation metrics, baselines, or numerical results.

These items should be added only if supported by the original project materials or confirmed by the co-authors.
