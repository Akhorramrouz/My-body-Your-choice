# Detailed README for Python Script

## Overview

This Python script performs text entailment analysis on Persian sentences, specifically focusing on the topic of abortion. It utilizes OpenAI's GPT-4 model to determine the logical relationship between two sentences. Additionally, the script processes a dataset by applying this analysis and saves the results. This script is intended for use in Google Colab, as it includes commands for mounting Google Drive.

## Dependencies

- `pandas`: For data manipulation and analysis.
- `time`: For adding delays during processing.
- `openai`: The OpenAI Python client library for accessing GPT-4.
- `google.colab`: For mounting Google Drive in Colab notebooks.

## Setup

1. **Mount Google Drive**: The script starts by mounting Google Drive to access files stored there.
2. **Change Directory**: It changes the current working directory to the specified path in Google Drive.
3. **Set OpenAI API Key**: You need to set your OpenAI API key for authentication.

## Functions

### `text_entailment(hypothesis, premise)`

- **Purpose**: Analyzes the logical relationship between two Persian sentences.
- **Parameters**:
  - `hypothesis`: The hypothesis sentence in Persian.
  - `premise`: The premise sentence in Persian.
- **Returns**: The type of logical relationship (`entailment`, `neutral`, `contradiction`) and an explanation.
- **Error Handling**: Prints an error message if an exception occurs.

### `process_data(data, start_index, step_index, hypothesis)`

- **Purpose**: Processes the provided dataset by applying text entailment analysis to each row.
- **Parameters**:
  - `data`: The dataset to process.
  - `start_index`: The starting index for processing the dataset.
  - `step_index`: The number of rows to process in each step.
  - `hypothesis`: The hypothesis sentence to use for entailment analysis.
- **Functionality**:
  - Iterates over the dataset in steps.
  - Applies `text_entailment` to each row.
  - Saves the results in a CSV file.
- **Additional Note**: Introduces a delay of 5 seconds after processing each batch to manage API usage and avoid potential rate limiting.

## Data Processing

- **Loading Data**: Loads a CSV file into a pandas DataFrame. The file contains topics related to abortion.
- **Hypothesis Definition**: Sets a hypothesis sentence regarding pressure or suggestion for abortion.



# Fine-Tuning Persian BERT Model for Sentiment Analysis

This Jupyter notebook provides a comprehensive guide to fine-tuning a Persian BERT model for sentiment analysis. It includes steps for installing required packages, preprocessing data, model training, and evaluation.

## Table of Contents
1. Installation of Required Packages
2. Importing Libraries
3. Data Mounting and Access
4. Data Loading and Preprocessing
5. Data Cleaning and Normalization
6. Handling Unbalanced Data
7. Model Fine-Tuning
8. Model Evaluation
9. Conclusion and Further Steps

## 1. Installation of Required Packages
- Install necessary Python packages: `transformers`, `hazm`, and `clean-text`.

## 2. Importing Libraries
- Import essential libraries like `numpy`, `pandas`, `sklearn`, `transformers`, `hazm`, and `plotly`.

## 3. Data Mounting and Access
- Instructions for mounting Google Drive to access stored data.

## 4. Data Loading and Preprocessing
- Load data using Pandas. The data involves sentiment labels and comments for analysis.

## 5. Data  pre-processing and Normalization
- Steps for pre-processing the data, including fixing unicodes, removing special characters, HTML cleaning, normalizing, and removing emojis.

## 6. Handling Unbalanced Data
- Techniques used to handle unbalanced data by cutting the dataset randomly based on the fewer label, in this case, the negative class.

## 7. Model Fine-Tuning
- Detailed process for fine-tuning the Persian BERT model, including setting up model architecture and training parameters.

## 8. Model Evaluation
- Evaluation of the model's performance using metrics like F1-score and classification reports.


