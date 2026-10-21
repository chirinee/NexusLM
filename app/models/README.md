# Model files

The large model files are not stored in this repository (GitHub limits files to 100 MB).

## NexusLM (`nexus_pubmed_big/`)

Included: `config.json`, `metadata.json`, `vocab_pubmed_big.pkl`.

Missing: `model.weights.h5` (about 96 MB).
Download it here: _add your link_ and place it in `app/models/nexus_pubmed_big/`.

## Biomedical NER (`biomedbert_ner_bc5cdr/`)

The NER model is the public model `Glasgow-AI4BioMed/bioner_bc5cdr` from Hugging Face (BiomedBERT fine-tuned on BC5CDR).
To download it into the right folder, run this from the `app/` folder:

```bash
python -c "from transformers import AutoTokenizer, AutoModelForTokenClassification as M; n='Glasgow-AI4BioMed/bioner_bc5cdr'; p='models/biomedbert_ner_bc5cdr'; AutoTokenizer.from_pretrained(n).save_pretrained(p); M.from_pretrained(n).save_pretrained(p)"
```
