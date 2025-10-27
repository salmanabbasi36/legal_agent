# 🧠 LexGLUE–LEDGAR DistilBERT Legal Clause Classifier

**Author:** Salman Abbasi  
**Affiliation:** Beijing Institute of Technology, China  
**Research Area:** NLP × Agentic AI × Prompt Engineering  
**Date:** October 2025  

---

## 📝 Model Overview

This model is a **DistilBERT-based legal clause classifier** fine-tuned on the **LexGLUE–LEDGAR** dataset.  
It predicts the **type of contract clause** (e.g., *Confidentiality*, *Termination*, *Liability*, *Payment*, etc.) given a legal paragraph or clause.

- **Base Model:** `distilbert-base-uncased`  
- **Dataset:** `coastalcph/lex_glue` (`ledgar` configuration)  
- **Task Type:** Multi-class text classification  
- **Language:** English  
- **Domain:** Legal / Contractual Texts  

This model achieves **strong performance** despite its small size, making it efficient for deployment in legal NLP systems and agentic AI applications.

---

## 🚀 Model Performance

| Metric | Score |
|:--------|:------:|
| **Accuracy** | 0.8618 |
| **Macro F1** | 0.7842 |
| **Validation Loss** | 0.5756 |
| **Epochs** | 3 |
| **Batch Size** | 8 |
| **Learning Rate** | 2e-5 |
| **Max Sequence Length** | 512 |

---
How to use it:

from transformers import pipeline

pipe = pipeline("text-classification", model="SalmanAbbasi/lexglue-ledgar-distilbert")

text = "This clause sets out the obligations of each party regarding confidentiality."
print(pipe(text))


## 📚 Dataset — LexGLUE LEDGAR

The **LEDGAR** dataset contains contract clauses annotated with one of **100+ provision types**.  
It is part of the [LexGLUE benchmark](https://huggingface.co/datasets/coastalcph/lex_glue), which evaluates legal text understanding models.

Each sample includes:
```json

@misc{abbasi2025ledgar,
  author = {Abbasi, Salman},
  title = {DistilBERT Fine-Tuned on LexGLUE LEDGAR for Legal Clause Classification},
  year = {2025},
  howpublished = {\url{https://huggingface.co/SalmanAbbasi/lexglue-ledgar-distilbert}},
  note = {Fine-tuned using Hugging Face Transformers and Datasets}
}


# legal_agent
