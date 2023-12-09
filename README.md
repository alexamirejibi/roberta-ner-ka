# Georgian Named Entity Recognition Model
XLM-Roberta-Base fine-tuned on the Georgian [WikiANN](https://huggingface.co/datasets/wikiann) NER dataset. Huggingface link [here.](https://huggingface.co/alexamiredjibi/xlm-roberta-base-ka-ner) 

# Evaluation

| Metric    | Value  |
|-----------|--------|
| Loss      | 0.2031 |
| Precision | 0.8506 |
| Recall    | 0.8703 |
| F1        | 0.8603 |
| Accuracy  | 0.9425 |

## Usage
```python
# Use a pipeline as a high-level helper
from transformers import pipeline

pipe = pipeline("token-classification", model="alexamiredjibi/xlm-roberta-base-ka-ner")
```

```python
# Load model directly
from transformers import AutoTokenizer, AutoModelForTokenClassification

tokenizer = AutoTokenizer.from_pretrained("alexamiredjibi/xlm-roberta-base-ka-ner")
model = AutoModelForTokenClassification.from_pretrained("alexamiredjibi/xlm-roberta-base-ka-ner")
```
