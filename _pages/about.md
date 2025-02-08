---
permalink: /
title: "LLMs in Chemistry: A Deep Dive into AI's Understanding of Chemical Reactions"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
<style>
p {
    text-align: justify;
}
</style>

# Introduction

Large Language Models (LLMs) have revolutionized the field of natural language processing, demonstrating impressive capabilities in understanding, generating, and reasoning about text. These models have shown potential in various domains, including science, finance, and software engineering. However, their application in the field of chemistry remains underexplored. This seminar aims to delve into the capabilities of LLMs in chemistry through a comprehensive benchmark evaluation of eight practical chemistry tasks.

This blog explores the potential of LLMs in advancing chemistry research and development. It discusses the benchmarking process, the tasks evaluated, and the performance of five popular LLMs: GPT-4, GPT-3.5, Davinci-003, Llama, and Galactica. By the end of this seminar, insights will be provided into the strengths, weaknesses, and limitations of LLMs in chemistry-related tasks, along with practical recommendations for leveraging these models in the future.

# Background on LLMs and Chemistry


Large Language Models (LLMs) have become a cornerstone in the field of natural language processing (NLP), showcasing remarkable abilities to understand, generate, and reason with text. These models, such as GPT-4 and Llama, have not only revolutionized text-based applications but have also begun to make inroads into scientific domains, including chemistry.

example llms-in-chemistry.jpg
Figure 1: The intersection of LLMs and Chemistry

## The Rise of LLMs

LLMs have demonstrated their prowess in a variety of tasks, from answering complex questions to generating coherent and contextually relevant text. This has led to their application in diverse fields such as healthcare, where they assist in diagnosing diseases, and in software engineering, where they help generate code. However, their potential in specialized scientific domains like chemistry has only recently started to be explored.

## Chemistry: A New Frontier for LLMs

Chemistry, as a scientific discipline, involves understanding and manipulating molecules, reactions, and materials. Traditionally, this field has relied heavily on experimental methods and specialized computational tools. The advent of LLMs presents an opportunity to augment these traditional methods with powerful AI-driven solutions.

## Challenges in Evaluating LLMs for Chemistry

Despite the potential, evaluating LLMs for chemistry tasks is not straightforward. Chemistry tasks often require a deep understanding of molecular structures, reaction mechanisms, and chemical properties. LLMs, which are primarily trained on natural language data, may struggle with the specialized knowledge and reasoning required for these tasks.
Moreover, the evaluation of LLMs in chemistry involves several challenges:

1. **Understanding Molecular Representations**: Chemistry tasks often involve molecular structures represented in formats like SMILES (Simplified Molecular Input Line Entry System). LLMs need to accurately interpret these representations to perform tasks effectively.

2. **Reasoning and Prediction**: Tasks such as predicting reaction outcomes or designing new molecules require not just understanding but also reasoning about chemical properties and reactions.

3. **Data and Evaluation Metrics**: Chemistry datasets are often complex and require specialized metrics for evaluation. Ensuring that LLMs can perform well on these metrics is crucial for their practical application.

## Previous Work

Previous research has shown that LLMs can be applied to specific chemistry tasks, such as predicting molecular properties or generating chemical reactions. However, these studies have been limited in scope, focusing on individual tasks rather than a comprehensive evaluation across multiple tasks.

This seminar aims to fill this gap by providing a comprehensive benchmark evaluation of LLMs across a diverse set of chemistry tasks. The goal is to gain a deeper understanding of the capabilities and limitations of LLMs in the field of chemistry.

# The Comprehensive Benchmark


To systematically evaluate the capabilities of Large Language Models (LLMs) in chemistry, a comprehensive benchmark was developed to assess their performance across eight diverse chemistry tasks. This benchmark provides a holistic view of how well LLMs can understand, reason, and explain chemistry-related problems. ![Figure 4: Overview of the Comprehensive Benchmark](https://example.com/benchmark-overview.jpg)

https://example.com/benchmark-overview.jpg
Figure 4: Overview of the Comprehensive Benchmark

## The Eight Chemistry Tasks

1. **Name Prediction**: Translating between different chemical naming conventions, such as SMILES to IUPAC names.

2. **Property Prediction**: Predicting chemical and physical properties of molecules based on their structure.

3. **Yield Prediction**: Estimating the efficiency of chemical reactions.

4. **Reaction Prediction**: Predicting the products of chemical reactions given reactants.

5. **Retrosynthesis**: Identifying reactants needed to produce a given product.

6. **Text-Based Molecule Design**: Generating new molecules based on textual descriptions.

7. **Molecule Captioning**: Generating textual descriptions of molecular structures.

8. **Reagents Selection**: Recommending the best reagents for a given reaction.

Each task is designed to test different aspects of LLMs' capabilities, from basic understanding to complex reasoning and generation.

## Datasets and Evaluation Metrics

To ensure a fair and comprehensive evaluation, widely recognized datasets such as BBBP, Tox21, PubChem, USPTO, and ChEBI were utilized. These datasets provide a rich variety of chemistry problems, ranging from molecular property prediction to reaction yield estimation.

| Ability       | Task                          | Task Type        | Dataset                                              | #ICL candidates     | #test | Evaluation Metrics           |
|---------------|-------------------------------|------------------|-----------------------------------------------------|---------------------|-------|------------------------------|
| **Understanding** | Name Prediction                | Generation       | PubChem                                             | 500                 | 100   | Accuracy                     |
|               | Property Prediction            | Classification   | BBBP, HIV, BACE, Tox21, ClinTox                    | 2053, 41127, 1514, 8014, 1484 | 100   | Accuracy, F1 score           |
| **Reasoning**     | Yield Prediction               | Classification   | Buchwald-Hartwig, Suzuki-Miyaura                   | 3957, 5650          | 100   | Accuracy                     |
|               | Reaction Prediction            | Generation       | USPTO-Mixed                                        | 409035              | 100   | Accuracy, Validity           |
|               | Reagents Selection             | Ranking          | Suzuki-Miyaura                                     | 5760                | 100   | Accuracy                     |
|               | Retrosynthesis                 | Generation       | USPTO-50k                                          | 40029               | 100   | Accuracy, Validity           |
|               | Text-Based Molecule Design     | Generation       | ChEBI-20                                           | 26407               | 100   | BLEU, Exact Match, etc.      |
| **Explaining**    | Molecule Captioning            | Generation       | ChEBI-20                                           | 26407               | 100   | BLEU, Chemists, etc.         |


For evaluation, metrics tailored to each task were employed. For example, accuracy and F1 score were used for classification tasks like property prediction, while BLEU and exact match were used for text generation tasks like molecule captioning.

## LLMs Evaluated

Five popular LLMs were evaluated: GPT-4, GPT-3.5, Davinci-003, Llama, and Galactica. These models were tested in both zero-shot and few-shot in-context learning settings to understand their performance with varying levels of context.

### Benchmark Process

The benchmark process involved several steps:

1. **Prompt Design**: Crafting prompts that effectively guide LLMs to perform each task.

2. **In-Context Learning**: Providing a few examples to help LLMs understand the task context.

3. **Evaluation**: Running multiple trials to ensure reliable results, considering the randomness in LLM outputs.

This structured approach was designed to provide a reliable and systematic evaluation of LLMs’ capabilities in chemistry.

# Evaluation of LLMs

This section delves into the performance of five Large Language Models (LLMs) evaluated in the comprehensive benchmark. The models—GPT-4, GPT-3.5, Davinci-003, Llama, and Galactica—were tested across eight chemistry tasks in both zero-shot and few-shot in-context learning settings. The goal was to understand their capabilities and limitations in the context of practical chemistry problems.

![Evaluation overview](_pages\images\eval_overview.png "Overview of the evaluation process")
Overview of the Evaluation Process

## Zero-Shot vs. Few-Shot In-Context Learning

Zero-shot learning involves evaluating the LLMs without providing any examples, relying solely on their pre-trained knowledge. In contrast, few-shot in-context learning provides a few examples to help the models understand the task context. This approach mimics real-world scenarios where models might have limited data but need to perform effectively.

## Performance Metrics

A variety of metrics were used to evaluate the models, tailored to each task. For classification tasks like property prediction, accuracy and F1 score were used. For text generation tasks like molecule captioning, BLEU, exact match, and other natural language processing metrics were applied. These metrics helped assess both the qualitative and quantitative performance of the LLMs.

## Key Findings

1. **Overall Performance**: GPT-4 consistently outperformed the other models across most tasks. This suggests that more advanced LLMs can better handle the complexities of chemistry tasks.

2. **Task-Specific Insights**:
   - **Name Prediction**: LLMs struggled with translating between different chemical naming conventions, indicating a need for better understanding of molecular representations.
   - **Property Prediction**: GPT models showed strong performance, especially when property labels were included in the prompts.
   - **Yield Prediction**: While GPT-4 performed well, it still lagged behind specialized models like UAGNN, highlighting areas for improvement.
   - **Reaction Prediction and Retrosynthesis**: These tasks, which require deep understanding of chemical reactions, were challenging for LLMs, with performance significantly lower than specialized models.
   - **Text-Based Molecule Design and Molecule Captioning**: GPT models demonstrated strong capabilities, generating chemically valid molecules and accurate descriptions, though exact matches were lower.

3. **Impact of In-Context Learning**: Providing a few examples significantly improved the performance of LLMs, especially in tasks requiring complex reasoning. This highlights the importance of context in enhancing model performance.

4. **Limitations**: Despite their capabilities, LLMs exhibited limitations in understanding molecular SMILES strings and generating accurate chemical reactions. This suggests that while LLMs can provide valuable insights, they may not yet replace specialized chemistry tools.

# Detailed Analysis of Each Task

This section provides a detailed analysis of the performance of five LLMs across each of the eight chemistry tasks. This analysis helps in understanding the strengths and weaknesses of these models in specific chemistry-related problems.

## 1. Name Prediction

**Task Description**: Name prediction involves translating between different chemical naming conventions, such as SMILES to IUPAC names, IUPAC names to SMILES, SMILES to molecular formulas, and IUPAC names to molecular formulas.

**Results:**

| Model             | SMILES to IUPAC | IUPAC to SMILES | SMILES to Formula | IUPAC to Formula |
|--------------------|-----------------|-----------------|-------------------|------------------|
| GPT-4             | 0.000           | 0.012           | 0.086            | 0.084           |
| GPT-3.5           | 0.000           | 0.010           | 0.052            | 0.044           |
| Davinci-003       | 0.000           | 0.000           | 0.006            | 0.018           |
| Llama2-13B-chat   | 0.000           | 0.000           | 0.010            | 0.000           |
| GAL-30B           | 0.000           | 0.000           | 0.000            | 0.000           |

**Observations:**

- LLMs struggled significantly with understanding and translating between different chemical naming conventions.
- The complexity of SMILES strings and the need for precise understanding of molecular structures contributed to the poor performance.

**Case Studies:**

- Example input: SMILES string "CCOC(=O)C(C(C)=O)=C(C)N"
- Expected output: IUPAC name "ethyl 2-acetyl-3-aminobut-2-enoate"
- GPT-4 output: "ethyl 2-methyl-5-oxo-2-azahept-4-en-3-oate"

![Performance Chart](_pages\images\name_prediction.png "Comparison of different LLMs on Name Prediction accuracy")

## 2. Property Prediction

**Task Description**: Property prediction involves predicting chemical and physical properties of molecules based on their structure. Datasets like BBBP, HIV, BACE, Tox21, and ClinTox were used.

**Results:**

| Model              | BBBP F1 Score | BACE F1 Score | HIV F1 Score | Tox21 F1 Score | ClinTox F1 Score |
|---------------------|---------------|---------------|--------------|----------------|------------------|
| GPT-4              | 0.587         | 0.666         | 0.797        | 0.563          | 0.736            |
| GPT-3.5            | 0.463         | 0.406         | 0.807        | 0.529          | 0.369            |
| Davinci-003        | 0.378         | 0.649         | 0.832        | 0.518          | 0.850            |
| Llama2-13B-chat    | 0.002         | 0.045         | 0.069        | 0.047          | 0.001            |
| GAL-30B            | 0.074         | 0.025         | 0.014        | 0.077          | 0.081            |

**Observations:**

- GPT-4 outperformed other models, especially when property labels were included in the prompts.
- The inclusion of property labels significantly improved performance, indicating the importance of context.

**Case Studies:**

- Example input: SMILES string "CCOC(=O)C(C(C)=O)=C(C)N"
- Expected output: Property prediction (e.g., inhibits HIV replication: yes/no)
- GPT-4 output: "Inhibits HIV replication: yes"

![Performance Chart](_pages\images\property_prediction.png "Comparison of different LLMs on Property Prediction accuracy")

## 3. Yield Prediction

**Task Description**: Yield prediction involves estimating the efficiency of chemical reactions, typically formulated as a binary classification problem (high yield or not).

**Results:**

| Method                     | Buchwald-Hartwig Accuracy (↑) | Suzuki-Coupling Accuracy (↑) |
|----------------------------|-------------------------------|------------------------------|
| UAGNN [34]                | 0.965                         | 0.957                        |
| GPT-4 (zero-shot)          | 0.322 ± 0.034                | 0.214 ± 0.019               |
| GPT-4 (random, k=8)        | 0.800 ± 0.008                | 0.764 ± 0.013               |
| GPT-4 (random, k=4)        | 0.574 ± 0.045                | 0.324 ± 0.018               |
| GPT-3.5 (random, k=8)      | 0.585 ± 0.045                | 0.542 ± 0.011               |
| Davinci-003 (random, k=8)  | 0.467 ± 0.013                | 0.341 ± 0.017               |
| Llama2-13B-chat            | 0.008 ± 0.007                | 0.006 ± 0.004               |
| GAL-30B                    | 0                            | 0.008 ± 0.010               |

**Observations:**

- GPT-4 performed well but still lagged behind specialized models like UAGNN, which achieved an accuracy of 0.965 on Buchwald-Hartwig and 0.957 on Suzuki-Miyaura.
- The performance improved with more demonstration examples in few-shot settings.

**Case Studies:**

- Example input: Reactants and products of a Buchwald-Hartwig reaction
- Expected output: High yield (yes/no)
- GPT-4 output: "High yield: yes"

![Performance Chart](_pages\images\yield_prediction.png "Impact of Few-Shot Examples on Accuracy")

## 4. Reaction Prediction

**Task Description:** Reaction prediction involves predicting the products of chemical reactions given the reactants.

**Results:**

| Model              | Top-1 Accuracy | Invalid SMILES |
|--------------------|---------------|---------------|
| GPT-4            | 0.230         | 7.0%          |
| GPT-3.5          | 0.184         | 15.6%         |
| Davinci-003      | 0.218         | 11.4%         |
| Llama2-13B-chat  | 0.032         | 27.8%         |
| GAL-30B         | 0.036         | 5.2%          |

**Observations:**

- LLMs struggled with understanding the intricacies of chemical reactions, leading to lower accuracy.
- The complexity of SMILES strings and the need for precise reaction mechanisms contributed to the challenges.

**Case Studies:**

- Example input: Reactants "CCOC(=O)C(C(C)=O)=C(C)N" and reagents
- Expected output: Products of the reaction
- GPT-4 output: "Invalid SMILES generated"

## 5. Retrosynthesis

**Task Description**: Retrosynthesis involves identifying the reactants needed to produce a given product. 

**Results:**

| Model              | Top-1 Accuracy | Invalid SMILES |
|--------------------|---------------|---------------|
| GPT-4             | 0.096         | 10.4%         |
| GPT-3.5           | 0.022         | 6.4%          |
| Davinci-003       | 0.122         | 6.0%          |
| Llama2-13B-chat   | 0.000         | 27.2%         |
| GAL-30B           | 0.016         | 5.2%          |

**Observations**:

- Similar to reaction prediction, GPT-4’s performance was limited, with a 40% lower accuracy than Chemformer. This reflects the need for deeper molecular reasoning capabilities.

- LLMs found retrosynthesis challenging, likely due to the complexity of understanding reaction mechanisms and molecular transformations.

**Case Studies**:

- Example input: Product "CCOC(=O)C(C(C)=O)=C(C)N"
- Expected output: Reactants needed for the reaction
- GPT-4 output: "Invalid SMILES generated"

## 6. Text-Based Molecule Design

**Task Description:** Text-based molecule design involves generating new molecules based on textual descriptions.

**Results:**

| Model              | BLEU Score | Exact Match | Levenshtein Distance | Validity |
|--------------------|------------|-------------|----------------------|----------|
| GPT-4             | 0.816      | 0.174       | 21.160               | 0.888    |
| GPT-3.5           | 0.479      | 0.094       | 82.008               | 0.854    |
| Davinci-003       | 0.741      | 0.100       | 25.648               | 0.936    |
| Llama2-13B-chat   | 0.626      | 0.020       | 33.956               | 0.782    |
| GAL-30B           | 0.004      | 0.000       | 2738.136             | 0.956    |

**Observations**:

- GPT-4 demonstrated strong capabilities in generating chemically valid molecules, though exact matches were lower.
- The generated molecules often met the requirements described in the input text.

**Case Studies**:

- Example input: Description "Generate a molecule with a benzene ring and a hydroxyl group"
- Expected output: SMILES string of the generated molecule
- GPT-4 output: "Cc1ccccc1O"

## 7. Molecule Captioning

**Task Description:** Molecule captioning involves generating textual descriptions of molecular structures. 

![Example of Molecule Captioning](_pages\images\molecule_captioning.png "Examples of molecules generated by different models.")

**Results**:

| Model              | BLEU-2 | BLEU-4 | ROUGE-1 | ROUGE-2 | ROUGE-L | METEOR |
|--------------------|--------|--------|---------|---------|---------|--------|
| GPT-4             | 0.464  | 0.365  | 0.545   | 0.362   | 0.459   | 0.519  |
| GPT-3.5           | 0.468  | 0.368  | 0.534   | 0.355   | 0.457   | 0.497  |
| Davinci-003       | 0.488  | 0.391  | 0.532   | 0.359   | 0.465   | 0.478  |
| Llama2-13B-chat   | 0.197  | 0.140  | 0.331   | 0.193   | 0.265   | 0.372  |
| GAL-30B           | 0.008  | 0.002  | 0.019   | 0.004   | 0.015   | 0.043  |

**Observations:**

- GPT-4 demonstrated strong performance, with chemically valid captions in over 89% of cases. Yet, occasional inaccuracies in chemical facts were noted.
- The generated captions often contained minor inaccuracies but were generally useful.

**Case Studies**

![Example of Molecule Captioning](_pages\images\mol_cap_example.png "Examples captions generated by different models. Descriptions that violate chemical factsare marked in grey.")

## 8. Reagents Selection

**Task Description:** Reagents selection involves recommending the best reagents for a given reaction.

**Results:**

| Model              | Reactant Selection Accuracy | Solvent Selection Accuracy | Ligand Selection Accuracy |
|--------------------|---------------------------|----------------------------|---------------------------|
| GPT-4             | 0.299                      | 0.526                      | 0.534                     |
| GPT-3.5           | 0.400                      | 0.368                      | 0.436                     |
| Davinci-003       | 0.178                      | 0.463                      | 0.432                     |
| Llama2-13B-chat   | 0.145                      | 0.050                      | 0.284                     |
| GAL-30B           | 0.107                      | 0.104                      | 0.030                     |

**Observations:**

- GPT-4 and GPT-3.5 performed comparatively well in reagent selection tasks.
- GPT-4 achieved competitive accuracy (40%-50%), benefiting from in-context learning. However, performance remains far from task-specific models.
- This suggests a promising potential for LLMs in the realm of reagent selection.

**Case Studies:**

- Example input: Reactants and reagents for a Suzuki coupling reaction
- Expected output: Best reagents for the reaction
- GPT-4 output: "Recommended reagents: Pd(PPh3)4, K2CO3"

![Heatmap of Reagents Selection](_pages\images\reagent_selection.png "Selection accuracy across models")

# Discussion and Insights

This section delves into the broader implications of the findings, discusses the limitations of current LLMs in chemistry tasks, and explores potential avenues for future research and development.

### Limitations of LLMs in Understanding Molecular SMILES

One of the most significant limitations of LLMs in chemistry is their struggle with understanding molecular representations in SMILES strings. SMILES (Simplified Molecular Input Line Entry System) is a widely used textual representation for chemical structures. However, LLMs often fail to accurately interpret these strings due to several reasons:

1. Implicit Hydrogen Atoms: Hydrogen atoms are not explicitly represented in SMILES strings, which can lead to confusion for LLMs.

2. Multiple Valid Representations: A single molecule can have multiple valid SMILES representations, leading to ambiguity.

3. Tokenization Issues: LLMs treat SMILES strings as sequences of characters or subwords, which can break the molecular structure and properties.

These limitations are evident in tasks requiring precise understanding and generation of SMILES strings, such as reaction prediction, retrosynthesis, and name prediction. For example, GPT models often fail to correctly translate between SMILES and IUPAC names, as seen in the name prediction task.

### Impact of In-Context Learning

The experiments highlight the significant impact of in-context learning (ICL) on the performance of LLMs. Providing a few examples as context can significantly enhance the models' ability to perform chemistry tasks. For instance, in the property prediction task, GPT-4 achieved an F1 score of 0.797 on the HIV dataset when provided with context, compared to 0.977 without context.

The quality and quantity of ICL examples play a crucial role in improving performance. Using scaffold similarity to retrieve the most relevant examples often outperforms random sampling. Additionally, increasing the number of ICL examples generally leads to better results, as seen in the yield prediction task.

### Ethical Considerations and Potential Misuse

The potential for LLMs to generate chemically valid molecules raises ethical concerns. While advancements in AI-enabled chemistry can lead to groundbreaking discoveries, they can also be misused to create hazardous substances. It is crucial to establish robust safeguards and ethical guidelines to prevent harmful applications.

# Broader Impacts and Future Work

The comprehensive benchmark provides valuable insights into the capabilities and limitations of LLMs in chemistry. The findings suggest that while LLMs can perform competitively in some tasks, they still lag behind specialized models in others. Future research should focus on improving LLMs' understanding of molecular structures and developing more effective in-context learning strategies.

Additionally, there is a need for more chemistry-specific evaluation metrics that can accurately assess the performance of LLMs in generating and understanding chemical structures. Collaborative efforts between AI researchers and chemists will be essential in advancing the application of LLMs in chemistry.

# Final Thoughts

In this exploration of Large Language Models (LLMs) in chemistry, we've uncovered both potential and limitations. LLMs, particularly GPT-4, have shown promise in tasks like property prediction and molecule captioning, where their language generation capabilities shine. However, they struggle with tasks requiring deep molecular understanding, such as reaction prediction and retrosynthesis. This highlights the need for enhanced molecular representation handling and more chemistry-specific training. The significant boost in performance from in-context learning underscores the importance of context in complex tasks. Ethical considerations around the potential misuse of these models to generate harmful substances also demand robust safeguards.

Moving forward, improving LLMs' grasp of molecular structures and refining in-context learning strategies are crucial steps. Developing custom evaluation metrics tailored to chemistry tasks will provide more accurate assessments of these models' capabilities. Continued collaboration between AI researchers and chemists will be essential in driving advancements and ensuring that LLMs can effectively contribute to the field of chemistry. While challenges remain, the potential for LLMs to accelerate research and development in chemistry is undeniable, and with further refinement, they could become powerful tools in the chemist's arsenal.

# References

1. Guo, Taicheng, et al. "What can large language models do in chemistry? A comprehensive benchmark on eight tasks." *Advances in Neural Information Processing Systems*, vol. 36, 2023, pp. 59662-59688.










