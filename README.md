# indobert-absa-model-training
Google Colab implementation of IndoBERT-based Aspect-Based Sentiment Analysis (ABSA) using Sentence Pair Classification (SPC) for Indonesian restaurant reviews.

## Overview

This repository contains the model training and evaluation workflow for an Aspect-Based Sentiment Analysis (ABSA) system for Indonesian restaurant reviews. The model uses IndoBERT-Base-P1 and the Sentence Pair Classification (SPC) approach to analyze aspect presence and sentiment polarity.

This project was developed as part of an undergraduate thesis on aspect-based sentiment analysis and interactive visualization of restaurant reviews.

## Research Objectives

- Identify whether a review mentions a predefined restaurant aspect.
- Classify sentiment as negative, neutral, or positive for the relevant aspect.
- Prepare a trained model for integration into a web-based review analysis system.

## Aspect Categories

The model uses five predefined aspects:
1. Food
2. Service
3. Price
4. Ambience
5. Location

## Methodology

The training workflow includes:
1. Review text preprocessing.
2. Construction of text–aspect pairs using Sentence Pair Classification.
3. IndoBERT-based model training.
4. Model evaluation using held-out evaluation data.
5. Saving the trained model artifacts for inference.

## Technology Stack

- Python
- Google Colab
- PyTorch
- Hugging Face Transformers
- IndoBERT-Base-P1

## Repository Structure

- `notebooks/`: Model training and evaluation notebooks.
- `data/`: Dataset documentation or instructions for obtaining the data.
- `results/`: Evaluation results and experiment records.
- `model/`: Instructions for accessing trained model artifacts.

## Evaluation

The final model reported in the thesis achieved:

- Aspect detection accuracy: 95.09%
- Aspect detection F1-score: 92.08%
- Sentiment classification accuracy: 90.00%
- Sentiment classification Macro F1-score: 85.56%

These values are reported thesis results. Refer to the evaluation notebook and experiment configuration for the corresponding evaluation procedure.

## Usage

Open the training notebook in Google Colab, prepare the required dataset and dependencies, and follow the notebook cells in order.

The trained model can be used by the companion web application after ensuring that the model architecture, tokenizer, preprocessing steps, and label mappings are consistent.

## Dataset and Data Privacy

The dataset used in this project consists of Google Maps reviews of a restaurant. To respect the restaurant's privacy and maintain the confidentiality of the research data, the dataset is not included in this repository.

The training notebook is provided to document the model training and evaluation workflow. However, running the notebook requires access to the original dataset, which is not publicly distributed.
