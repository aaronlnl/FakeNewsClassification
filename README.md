# FakeNewsClassification

This project explores the application and fine-tuning of various state-of-the-art NLP models for fake news classification using the **LIAR dataset**.

## Project Overview

Fake news detection is a critical task to mitigate the spread of misinformation. In this work, we adopt and fine-tune multiple NLP models to identify the veracity of short political statements from the LIAR dataset. We experiment with both zero-shot and fine-tuned approaches to evaluate model performance.

## Dataset

- **LIAR Dataset**: A benchmark dataset containing 12,836 short statements labeled with six fine-grained truthfulness classes (e.g., pants-fire, false, barely-true, half-true, mostly-true, true).
- Source: https://www.cs.ucsb.edu/~william/data/liar_dataset.zip

## Models Used

| Model                      | Approach               | Description                                      |
|----------------------------|-----------------------|------------------------------------------------|
| BART large MNLI            | Zero-shot             | Using BART large model fine-tuned on MNLI for zero-shot classification via NLI inference. |
| BART large MNLI            | Fine-tuned            | Fine-tuned on LIAR dataset for direct classification. |
| Llama 3.2 1B (Work in Progress) | Zero-shot prompt-based| Prompting Llama 3.2 1B for classification without additional training. |
| Llama 3.2 1B (Work in Progress) | Fine-tuned with head  | Added classification head to LLaMA 3.2 1B and fine-tuned on LIAR. |

### Prerequisites

- Python 3.8+
- PyTorch
- Transformers (Hugging Face)
- Datasets
- Other dependencies as per `requirements.txt`
