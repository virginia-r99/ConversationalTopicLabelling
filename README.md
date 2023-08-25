# Automatic Topic Label Generation Using Conversational Models _(CPTL)_

## Approach 
![TFM_Approach](https://github.com/virginia-r99/ConversationalTopicLabelling/assets/61234891/a7f3d1f0-970e-410e-9bab-188d21b4a593)

# Language Models Answers Generation and Similarities

## Evaluation process
![TFM_Evaluation](https://github.com/virginia-r99/ConversationalTopicLabelling/assets/61234891/b27423b6-7fe1-44f6-99af-e36a9aa189c8)

_Note: The experiments presented were carried out on the first semester of 2023._ 

To generate the Language Models Answers, their embeddings, and their similarities, we used the programming language Python in its 3.9 version and a series of its libraries:

## Libraries Used:
We made use of the following Python libraries for this project:

* **Transformers (version 4.26.1)**: Provides APIs and tools to easily download and train state-of-the-art pre-trained neural models.
* **Sentence Transformers (version 2.2.2)**: Provides a framework for state-of-the-art sentence, text, and image embeddings.
* **Numpy (version 1.21.5)**: Provides support for large, multi-dimensional arrays and matrices, along with a large collection of high-level mathematical functions to operate on these arrays.
* **Os (Python 3.9 version)**: Provides a portable way of using operating system dependent functionality.
* **Torch (version 1.13.1)**: Provides tensor computation with strong GPU acceleration and Deep Neural Networks built on a tape-based autograd system.
* **Pandas (version 1.4.4)**: Provides an open-source data analysis and manipulation tool.
* **RegEx (version 2022.7.9)**: Provides regular expression matching operations similar to those found in Perl.


## Files used to evaluate the proposed approach:
### Code files _(in "Code" folder)_, in order of use:

**_1._ Conv_Models_answers.ipynb**→ Jupyter Notebook to generate the Conversational Models' Answers as topic labels. 

_Note: The ChatGPT answers were obtained manually directly from OpenAI's ChatGPT website interface given that there was no official python wrapper at the time of this experiment._

**_1b._ QA_models_answers.ipynb**→ Jupyter Notebook to generate the QA Models' Answers given the Conversational Models' Answers as topic labels

**_1c._ bart-tl_answers.ipynb**→ Jupyter Notebook to generate the BART-TL topic labels predictions

**_2._ compute_embeddings.ipynb**→ Jupyter Notebook to, given a text _(in this case the ground truth topic labels, and the Conversational and QA Answers)_, generate the sentence embeddings

**_3._ compute_similarities.ipynb**→ Jupyter Notebook to, given a set of embeddings, compute their cosine similarity _(in this case, of the answers-ground truth topic label pairs)_

To employ these files, please follow the indications presented in the coments and descriptions of each Python Notebook presented.

### Topic models file _(in "Code" folder)_:

**topics_20news.json** → JSON file that contains the 20newsgroup dataset topic models provided by [LibrAIry](https://librairy.github.io). 

## Folder list:
**Results**→ Contains the Excel files presenting the results obtained for each step of our experiment

### Files in _Results_ folder:
* **QuestStruct_Evaluation.xlsx** → Presents the similarity results of the diferent question structures tested along the evaluation process.
* **Num_Evaluation.xlsx** → Presents the similarity results of the diferent number of topic words tested along the evaluation process.
* **QAMod_Evaluation.xlsx** → Presents the similarity results of the diferent QA models tested along the evaluation process.
* **Final_Evaluation.xlsx** → Presents the overall similarity results and the evaluation of the previous modules.
* **Bart-tl_Evaluation.xlsx** → Presents the similarity results and comparison of _CPTL_ best performing results with [BART-TL](https://aclanthology.org/2021.eacl-main.121).
* **topic_rel_evaluation.xlsx** → Presents the similarity and euclidean distance results of the relationship between the ground truth label of the topic models and the topic words used to describe them.


# Setting Up the CPTL Conda Environment and Deploying a Jupyter Notebook

This guide will walk you through the process of creating a Conda environment called "CPTL" using a `requirements.txt` file and deploying a Python notebook in Jupyter notebooks using this environment.

## Prerequisites

- _Anaconda_ or _Miniconda_ installed on your system.

## Creating the CPTL Conda Environment

1. Open a terminal or command prompt.

2. Navigate to the root directory of your project (where your `requirements.txt` file is located).

3. Create the `CPTL` Conda environment by running the following command:

   ```bash
   conda create --name CPTL python=3.9
   ```

   Replace `3.9` with your desired Python version if necessary.

4. Activate the `CPTL` environment:

   ```bash
   conda activate CPTL
   ```

5. Install the required packages listed in the `requirements.txt` file using pip, given that some of the libraries' versions used are not available in Conda:

   ```bash
   pip install -r requirements.txt
   ```

## Deploying a Python Notebook in Jupyter Notebooks

1. Make sure the `CPTL` Conda environment is activated (if not, run `conda activate CPTL`).

3. Launch Jupyter Notebook by running:

   ```bash
   jupyter notebook
   ```

   This will open a web browser with the Jupyter Notebook interface.

   _You may need to install jupyter notebook and ipywidgets to be able to run the notebooks in Jupyter Notebook. Install these dependencies by running:_

   ```bash
   pip install notebook
   ```

   ```bash
   pip install ipywidgets
   ```

5. Navigate to the directory where your Jupyter notebook (`*.ipynb`) is located.

6. Click on the notebook file to open it in Jupyter.

7. In the Jupyter interface, select the `CPTL` kernel as the Python environment for your notebook. You can do this from the "Kernel" menu.

8. You can now run and work with your Python notebook using the `CPTL` environment.

9. Remember to save your notebook after making changes.

## Deactivating the CPTL Environment

When you're done working in the `CPTL` environment, you can deactivate it by running:

```bash
conda deactivate
```

This will return you to the base Conda environment or whichever environment you were previously using.


# Contact Information

If you have any questions, suggestions, or need further information, feel free to reach out to me:

- Email: [virginia.ramon@alumnos.upm.es](mailto:virginia.ramon@alumnos.upm.es)
