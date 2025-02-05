# Fine-Tuning FLAN-T5 for Text Summarization

This repository fine-tunes FLAN-T5 for text summarization using Parameter-Efficient Fine-Tuning (PEFT) with LoRA and BitsAndBytes quantization.

## Features

- **FLAN-T5 Fine-Tuning**: Adapts FLAN-T5 for sequence-to-sequence summarization.
- **LoRA & BitsAndBytes**: Efficient training with low-rank adaptation and 4-bit quantization.
- **Dataset Preparation**: Uses the BillSum dataset for training.
- **Training Pipeline**: Utilizes Hugging Face `Trainer` for efficient model training.
- **Evaluation**: Computes ROUGE scores for summarization quality.

## Files

1. **`LoRA_BnB_TextSummarizer.ipynb`**: Python script implementing the training pipeline.
2. **Dataset**: BillSum dataset for text summarization tasks.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/AbdulrahmanAhmed20072/FineTune-FLAN-T5-Summarization.git
   ```
2. Install the required dependencies:
   ```bash
   pip install datasets bitsandbytes accelerate evaluate transformers torch peft rouge_score numpy
   ```

## Usage

1. Load and preprocess the dataset.
2. Fine-tune FLAN-T5 with LoRA and quantization.
3. Evaluate model performance.
4. Generate summaries for input documents.

Run the script:
```bash
python LoRA_BnB_TextSummarizer.ipynb
```

## Outputs

- Fine-tuned FLAN-T5 model for text summarization.
- ROUGE score evaluation on test data.
- Generated summaries for input documents.

## Example

Input Text:
```
The Inflation Reduction Act lowers prescription drug costs, health care costs, and energy costs. It's the most aggressive action on tackling the climate crisis in American history, which will lift up American workers and create good-paying, union jobs across the country.
```

Generated Summary:
```
The Inflation Reduction Act lowers costs for healthcare, prescriptions, and energy while creating union jobs and addressing climate change.
```
