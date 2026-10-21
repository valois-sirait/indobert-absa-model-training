# IndoBERT-Based Aspect-Based Sentiment Analysis (ABSA)

## Overview

This repository contains the Google Colab training implementation of an IndoBERT-based Aspect-Based Sentiment Analysis (ABSA) model for Indonesian restaurant reviews.

The model uses IndoBERT-Base-P1 and the Sentence Pair Classification (SPC) approach. It is designed to perform two tasks: aspect detection and sentiment classification.

This project was developed as part of an undergraduate thesis on IndoBERT-based aspect-level sentiment analysis of restaurant reviews.

## Model Architecture

The model employs a multi-task learning architecture with two output heads:

### 1. Aspect Detection

A binary classification task to determine whether a review mentions the target aspect.

- `0`: No Aspect
- `1`: Aspect Present

### 2. Sentiment Classification

A three-class classification task to predict the sentiment associated with the target aspect.

- `0`: Negative
- `1`: Neutral
- `2`: Positive

The two tasks are performed on review–aspect pairs using the shared IndoBERT representation.

## Aspect Categories

The model uses five predefined restaurant review aspects:

1. Food
2. Service
3. Price
4. Ambience
5. Location

Using Sentence Pair Classification, each review is paired with each predefined aspect for separate aspect-level predictions.

## Training Workflow

The training notebook covers the following steps:

1. Review text preprocessing.
2. Construction of review–aspect pairs.
3. Preparation of aspect and sentiment labels.
4. Training the IndoBERT-based model with two output heads.
5. Evaluation of aspect detection and sentiment classification.
6. Saving the trained model artifacts for inference.

The implementation details and training configuration are available in the notebook.

## Dataset and Privacy

The dataset consists of Google Maps reviews of a restaurant used as the research object.

The original dataset is not included in this repository due to privacy and confidentiality considerations regarding the restaurant and the research data.

The training notebook is provided to document the training workflow. Running the complete training process requires a separately obtained and appropriately prepared dataset.

## Reported Evaluation Results

The following results were reported in the undergraduate thesis:

| Task | Metric | Result |
|---|---|---:|
| Aspect Detection | Accuracy | 95.09% |
| Aspect Detection | F1-score | 92.08% |
| Sentiment Classification | Accuracy | 90.00% |
| Sentiment Classification | Macro F1-score | 85.56% |

These results correspond to the evaluation reported in the thesis. Reproducing them requires the original experimental data and corresponding evaluation setup, which are not publicly included in this repository.

## Technology Stack

- Python
- Google Colab
- PyTorch
- Hugging Face Transformers
- IndoBERT-Base-P1

## Repository Structure

```text
indobert-absa-model-training/
├── notebooks/
│   └── indobert_absa_training.ipynb
├── requirements.txt
└── README.md
```

The repository structure may differ depending on the files included in the published version.

## Usage

1. Open the training notebook in Google Colab.
2. Install the required dependencies.
3. Prepare a dataset that follows the format expected by the notebook.
4. Execute the notebook cells to perform preprocessing, model training, and evaluation.
5. Save the resulting model artifacts for subsequent inference.

The original research dataset is not distributed in this repository.

## Pretrained Model

The trained model is intended to be published separately on Hugging Face.

**Hugging Face model repository:** To be added after publication.

The model repository will provide the available model artifacts and relevant usage instructions. Refer to its documentation for details on loading and using the trained model.

## Limitations

- The model was trained and evaluated on a specific restaurant review dataset.
- The original research dataset is not publicly available in this repository.
- Evaluation results may differ when using a different dataset or training configuration.
- Predictions depend on the review text, target aspect, preprocessing procedure, and model configuration.
