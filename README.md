# Final Project for CSE 587

This is Ronak Singh's CSE 587 midterm project repository. The report containing all training and model details, as well as all experiments and results can be found in `report.pdf`.

## Quick Start

First, ensure that you have access to the `meta-llama/Llama-3.2-3B-Instruct` gated respository on Hugging Face (you can visit https://huggingface.co/meta-llama/Llama-3.2-3B-Instruct to request access). Access to the base model is required before running inference on the fine-tuned model.

To run inference on the fine-tuned model, open and run the `inference.ipynb` notebook, and follow the instructions present in the notebook.

To run the training pipeline, open and run the `train.ipynb` file. This will re-train the fine-tuned model from "scratch" (it will begin the fine-tuning process starting from the base model).

## Dataset

A dataset containing synthetic data (using OpenAI's GPT 4o-mini model) was generated to fine-tune the base model. The dataset contains 15321 different prompt/completion pairs (corresponding to research question/scientific approach pairs) spanning 61 different research topics. The generated dataset can be found in the `topic_question_approach.csv` file. A subset of 9148 prompt/completion pairs was selected to fine-tune the model (the shortened dataset can be found in `topic_question_approach_trunc.csv`).

## Model Details

This project utilizes a fine-tuned version of the Meta Llama-3.2-3B-Instruct language model as its core. While the base Llama-3.2-3B-Instruct model provides a strong foundation with its broad general knowledge and instruction-following capabilities, fine-tuning was essential to adapt it specifically for the task of generating approaches to research problems.

## Additional Details (for Reference)

- Although not required, you can run `pip install -r requirements.txt` to install all required dependencies (this allows you to skip running all `!pip install` cells in the notebooks).
- All training was performed on a rented NVIDIA A4000 GPU via Paperspace.
