# Fine-Tuning BART for Natural Language to SQL Query Generation

## Project Overview
This project fine-tunes a pre-trained BART model (`facebook/bart-base`) to translate natural language questions into structured SQL queries. The fine-tuning was performed on a curated subset of the Gretel synthetic text-to-SQL dataset.

The project covers:
- Dataset preparation and cleaning
- Model fine-tuning with hyperparameter optimization
- Model evaluation against baseline
- Error analysis and suggested improvements
- Inference pipeline via Gradio app

## Folder Structure
```
.
├── train.py              # Fine-tuning script
├── inference.py          # Gradio app for query generation
├── utils.py              # Utility functions
├── dataset/              # Data preparation scripts
├── models/               # Saved model checkpoints
├── outputs/              # Generated outputs and logs
├── requirements.txt      # Project dependencies
└── README.md             # Project overview and instructions
```

## Setup Instructions

1. **Clone the repository**
```bash
git clone <your-repository-link>
cd <repository-folder>
```

2. **Create and activate a virtual environment (optional but recommended)**
```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install the required packages**
```bash
pip install -r requirements.txt
```

4. **Prepare the Dataset**
Download the subset of the Gretel dataset or generate it using the provided script inside the `dataset/` folder.

5. **Train the Model**
```bash
python train.py
```

6. **Launch the Gradio Inference App**
```bash
python inference.py
```

## Requirements
See `requirements.txt` file.

---

# requirements.txt
torch
transformers
datasets
gradio
wandb

## Notes
- Training was performed on a Google Colab Pro environment with T4 GPU.
- For best results, ensure you have a CUDA-capable GPU if training locally.

## License
This project is intended for educational purposes only.

## Acknowledgments
- [Hugging Face](https://huggingface.co/) for model and tokenizer libraries
- [Gretel Synthetic SQL Dataset](https://gretel.ai/)
- [Gradio](https://gradio.app/) for easy app building

---

Happy Querying! 🚀
