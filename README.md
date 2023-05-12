# Automatic Topic Label Generation Using Conversational Models
## File list:
**topics_20news.json** → JSON file that contains the 20newsgroup dataset topic models

**Conv_Models_answers.ipynb**→ Jupyter Notebook to generate the Conversational Models' Answers as topic labels

**QA_models_answers.ipynb**→ Jupyter Notebook to generate the QA Models' Answers given the Conversational Models' Answers as topic labels

**bart-tl_answers.ipynb**→ Jupyter Notebook to generate the BART-TL topic labels predictions

**compute_embeddings.ipynb**→ Jupyter Notebook to, given a text _(in this case the ground truth topic labels, and the Conversational and QA Answers)_, generate the sentence embeddings

**compute_similarities.ipynb**→ Jupyter Notebook to, given a set of embeddings, compute their cosine similarity _(in this case the answers-ground truth topic label pairs)_

## Folder list:
**Results**→ Contains the Excel files presenting the results for each step of our experiment
