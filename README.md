---
language: zulu
---

# zuBERTa
zuBERTa is a RoBERTa style transformer language model trained on zulu text.

## Intended uses & limitations
The model can  be used for getting embeddings to use on a down-stream task such as question answering.

#### How to use

```python
>>> from transformers import pipeline
>>> from transformers import AutoTokenizer, AutoModelWithLMHead

>>> tokenizer = AutoTokenizer.from_pretrained("MoseliMotsoehli/zuBERTa")
>>> model = AutoModelWithLMHead.from_pretrained("MoseliMotsoehli/zuBERTa")
>>> unmasker = pipeline('fill-mask', model=model, tokenizer=tokenizer)
>>> unmasker("Ntshopotse <mask> e godile.")
```
