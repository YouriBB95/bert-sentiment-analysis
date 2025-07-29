# 🎬 Sentiment Analysis on IMDB with BERT

This project fine-tunes the `bert-base-uncased` model from Hugging Face Transformers to classify movie reviews as positive or negative.

## 📊 Dataset
- **Source**: [IMDB Movie Reviews](https://huggingface.co/datasets/imdb)
- 50,000 labeled reviews (25k train, 25k test)
- Balanced: 50% positive, 50% negative

## 🧠 Model
- **Base model**: `bert-base-uncased` (from Hugging Face Transformers)
- Fine-tuned using the `Trainer` API
- Optimized on 10,000 training samples for faster iteration

## 📈 Results
Evaluated on a balanced 1,000-sample subset of the test set:

- **Accuracy**: 92.1%
- **F1-score**: 0.92
- **Precision**: 0.91
- **Recall**: 0.93

## 🧪 Techniques Used
- Tokenization with `BertTokenizer`
- Training with `Trainer` and `TrainingArguments`
- Evaluation using `scikit-learn` (confusion matrix, classification report)
- Visualization using `matplotlib` and `seaborn`

## 📁 Files
- `bert_imdb_sentiment_analysis.ipynb`: Complete notebook (from loading to evaluation)
- `requirements.txt`: All dependencies used

## 🛠 Installation

```bash
pip install -r requirements.txt
```

## 🚀 How to Run

Run the notebook step-by-step in Jupyter or Google Colab:
```bash
jupyter notebook bert_imdb_sentiment_analysis.ipynb
```

## 📦 Model Output

Model and tokenizer are saved locally:
- `bert-imdb-sentiment/`
  - `pytorch_model.bin`
  - `config.json`
  - `tokenizer_config.json`, etc.

You can reload them using:
```python
from transformers import BertForSequenceClassification, BertTokenizer
model = BertForSequenceClassification.from_pretrained("bert-imdb-sentiment")
tokenizer = BertTokenizer.from_pretrained("bert-imdb-sentiment")
```

## 📜 License

MIT License
...

---
📬 Questions or feedback? Reach me via [LinkedIn] https://www.linkedin.com/in/youri-benschop-133045b1/
