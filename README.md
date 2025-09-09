


# Natural Language Processing & Information Retrieval

## Project Objective

This project compares the performance of **fine-tuned Transformer models (DistilBERT, T5)** and **pre-trained Large Language Models (ChatGPT, LLaMA 2)** on the **Question Answering (QA)** task, using the **SQuAD dataset** and evaluation metrics such as **F1 Score** and **Exact Match (EM)**.

## Repository Structure

* `notebooks/` → Jupyter Notebook containing training, Optuna experiments, and evaluation.
* `report/` → Full academic report (PDF) with methodology, results, and analysis.
* `README.md` → Project overview and documentation.

## Methodology

1. Data preparation and sampling from the **SQuAD** dataset.
2. **Fine-tuning** DistilBERT and T5 with **Optuna** (batch size & learning rate optimization).
3. Comparison with **LLMs** (ChatGPT, LLaMA-2) via prompt engineering.
4. Model evaluation using **Exact Match (EM)** and **F1 Score**.

## Key Results

* **T5** achieved the best **Exact Match** (64%), excelling at factual questions.
* **LLaMA-2** and **ChatGPT-mini** achieved the highest **F1 Scores (\~80%)**, performing better on open-ended questions.
* **DistilBERT** showed weaker results (51% EM, 66% F1), limited by its smaller architecture.

| Model        | EM (%) | F1 (%) |
| ------------ | ------ | ------ |
| DistilBERT   | 51     | 66.6   |
| T5           | 64     | 78.1   |
| ChatGPT-mini | 61     | 79.7   |
| LLaMA-2-7b   | 61     | 79.7   |

## Limitations

* Limited computational resources → only a small hyperparameter search was possible.
* Evaluation on a reduced test subset (100 questions).
* LLMs sometimes produced irrelevant or verbose outputs.




