# MSc Thesis: Leveraging Large Language Model Capabilities for Big Five Personality Trait Classification

This repository contains the code, data, and results from my master's thesis titled **"Leveraging Large Language Model Capabilities for Big Five Personality Trait Classification"**. The project was conducted as part of the MSc IT & Cognition program at the University of Copenhagen.

The thesis explores the use of prompt engineering techniques with large language models (LLMs) to classify the Big Five personality traits from stream-of-consciousness essays (The Essays Dataset). The study includes semantic chunking, feature extraction, and various input configurations to assess the impact on classification performance.

---

## Repository Structure

The repository is organized as follows:

### 📂 `notebooks/`
Contains the Jupyter notebooks used for data analysis, feature extraction, and personality classification tasks.

- **big5 classification/**: Notebooks related to the personality trait classification experiment.
  - `all_results_classification.ipynb`: Aggregates results from different classification setups.
  - `text_only_cot.ipynb`, `text_semfeat_cot.ipynb`, etc.: Notebooks containing specific experimental condition setups.

- **semantic chunking/**: Contains the code for dividing stream-of-consciousness essays into coherent chunks.
  - `semantic_chunking.ipynb`: Implements the semantic chunking methodology.

- **feature extraction/**: Notebooks used for extracting programmatic and LLM-based semantic features from the text data.
  - `semfeat_extraction_cot.ipynb`: Focuses on extracting semantic features using Chain-of-Thought (CoT) prompting.
  - `chunks_eda_progfeat_extraction.ipynb`: Explores the semantic chunks dataset and conducts programmatic feature extraction.

### 📂 `results/`
Contains the output files from the feature extraction and classification experiments.

- **big5 classification/**
  - `complete_results.csv.zip`: Compressed file containing the full results from the Big Five classification task.
  - Various JSON files (e.g., `text_only_cot.json`, `text_semfeat_cot.json`): Structured outputs from different classification setups.

- **semantic chunking/**
  - `semantic_chunking.json`: Contains the chunked essays created using semantic chunking methods.

- **feature extraction/**
  - `progfeat_extraction.json`: Results of the programmatic feature extraction.
  - `semfeat_extraction_cot.json`: Results of the LLM-based semantic feature extraction.

### 📂 `data/`
Contains the dataset used for this study.

- `essaytrain.csv`: The origianl dataset of stream-of-consciousness essays paired with Big Five personality labels (The Essays Dataset). 

---

## Project Overview

The main research questions explored in this thesis are:

1. How effectively can LLMs predict personality traits from semantically coherent text chunks?
2. What is the impact of incorporating programmatic and LLM-based semantic features on classification accuracy?
3. How do different prompting techniques, specifically Chain-of-Thought (CoT), influence model performance?

---

## Methodology Summary

The project involves several key stages:

1. **Semantic Chunking**: The original essay dataset was divided into coherent text chunks using semantic similarity measures. This ensured the LLM received inputs that maintained thematic coherence.

2. **Feature Extraction**:
   - **Programmatic Features**: Linguistic features such as lexical diversity, sentiment, and part-of-speech distributions were extracted using traditional NLP tools.
   - **LLM-Based Semantic Features**: Higher-level semantic features (e.g., Cognitive Flexibility, Emotional Tone) were extracted using the GPT-4o model and CoT prompting.

3. **Personality Trait Classification**: The Big Five traits were classified using various input configurations and prompting techniques, including zero-shot baseline and CoT prompting.

---

## Research Context

This work builds on existing literature in computational personality psychology, NLP, and prompt engineering. It aims to advance the use of LLMs for nuanced personality assessment and provides insights into the trade-offs between interpretability and accuracy when using LLMs as decision making agents.

For more details, please refer to the thesis document.

---

**Author**: Sophia De Spiegeleire  
**Program**: MSc IT & Cognition, University of Copenhagen  
**Submission Date**: January 2024
