# Text-Classification

This repository contains is implementation of text classification use case.

# README

## Finetuning Roberta-base for Email Spam Classification using LoRA

This repository contains code for finetuning the Roberta-base model on a text classification task using LoRA (Low-resource Adaptation) with a dataset comprising emails (subject + message) and labeled as spam or ham.

### Task

- **Text Classification**: The task involves classifying emails into spam or ham categories.

### Model

- **Roberta-base**: Pretrained Roberta-base model is utilized for the task.

### Dataset

- **Dataset**: The model was finetuned on truncated version of SetFit/enron_spam dataset. The original SetFit/enron_spam consists of 33716 rows. The truncated version consists of 1500 train samples and 1500 test samples with columns, text and label.

### Libraries Used

- `transformers`: For utilizing and fine-tuning the Roberta-base model.
- `huggingface-hub`: For accessing the model and tokenizer from the Hugging Face model hub.
- `peft`: For training and evaluation of the model.
- `datasets`: For handling and processing the dataset.
- `evaluate`: For evaluating the model performance.
- `numpy`: For numerical computations.
- `torch`: For building and training neural networks.

### Training Details

- **Pretrained Model**: Roberta-base.
- **Total Parameters**: 125,423,620
- **Trainable Parameters**: 776,450
- **Trainable Parameter Percentage**: 0.6191

### Hyperparameters

- **Weight Decay**: 0.01
- **Learning Rate**: 1e-3
- **Batch Size**: 4
- **Number of Epochs**: 10

### Results

Epoch Training Loss Validation Loss Accuracy
1 No log 0.200391 0.9653333333333334
2 0.324100 0.222317 0.954
3 0.130500 0.112250 0.9746666666666667
4 0.081100 0.159360 0.978
5 0.081100 0.204141 0.9753333333333334
6 0.035900 0.353647 0.9626666666666667
7 0.011500 0.302890 0.9733333333333334
8 0.005800 0.313860 0.9713333333333334
9 0.005800 0.250255 0.978
10 0.000000 0.267402 0.974

### Usage

- Clone the repository.
- Install the required libraries listed in `requirements.txt`.
- Run the training script with appropriate configurations.

### Acknowledgments

- The dataset used in this project is provided by likhith231 on Hugging Face datasets hub.
