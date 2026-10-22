NLP FOUNDATIONS: TEXT PROCESSING AND WORD EMBEDDINGS
=================================================

Suggested GitHub repository name:
nlp-foundations-text-processing-embeddings

PROJECT OVERVIEW
----------------
This project is a practical Natural Language Processing (NLP) assignment
implemented in Jupyter Notebook. It explores text preprocessing, word
frequencies, numerical representations of text, traditional and neural
word embeddings, contextual language models, and a small text analysis
pipeline. The notebook combines Python code, output tables, written
explanations, and manual calculations where required.

TOPICS COVERED
--------------
Part A3 - Environment setup
  - Created an isolated Python virtual environment named nlp-env.
  - Installed and verified key Python/NLP libraries.
  - Downloaded NLTK resources and the spaCy English model.

Part B - Python and numerical fundamentals
  - B1: Word frequency counting with a dictionary and Counter for ranking.
  - B2: NumPy dot product, L2 norms, cosine similarity, and manual check.
  - B3: Pandas document statistics, filtering, and mean word counts.

Part C - Text processing
  - C1: Compared whitespace, NLTK, and spaCy tokenization.
  - C2: Extracted email addresses, hashtags, URLs, and phone numbers
        using regular expressions.
  - C3: Cleaned text by removing HTML, URLs, punctuation, digits,
        and extra whitespace.
  - C4: Measured NLTK stop-word removal and preserved negations
        with a custom stop-word list.
  - C5: Compared Porter stemming, Snowball stemming, and WordNet lemmas.

Part D - Traditional word representations
  - D1: Created one-hot word vectors.
  - D2: Built count and binary Bag-of-Words document-term matrices.
  - D3: Computed TF-IDF by hand and with scikit-learn; compared
        document cosine similarities.
  - D4: Generated bigrams/trigrams and combined unigram-bigram features.
  - D5: Compared one-hot, Bag-of-Words, and TF-IDF limitations.

Part E - Neural and pretrained embeddings
  - E1: Worked through CBOW and Skip-Gram training examples.
  - E2: Trained Word2Vec CBOW and Skip-Gram models on Brown news text.
  - E3: Examined pretrained 100-dimensional GloVe similarities
        and analogies.
  - E4: Compared FastText and Word2Vec on out-of-vocabulary words.
  - E5: Compared contextual BERT embeddings for the word "bank".
  - E6: Compared Word2Vec, GloVe, FastText, and BERT conceptually.

Part F - Mini NLP pipeline
  - F1: Cleaned, tokenized, removed stop words, and lemmatized
        the first 500 selected 20 Newsgroups documents with spaCy.
  - F2: Built unigram/bigram TF-IDF features (up to 5,000) and
        identified the top 10 mean TF-IDF terms for sci.space and rec.autos.
  - F3: Reflected on TF-IDF limitations and possible improvements
        using GloVe or BERT.

TECHNOLOGIES
------------
Python, Jupyter Notebook, NumPy, Pandas, NLTK, spaCy, scikit-learn,
Gensim, PyTorch, and Hugging Face Transformers.

DATASETS AND PRETRAINED MODELS
-----------------------------
- Example sentences (D1-D3) supplied in the assignment
- NLTK Brown corpus, news category
- 20 Newsgroups dataset: sci.space and rec.autos
- spaCy en_core_web_sm
- Gensim glove-wiki-gigaword-100
- Hugging Face bert-base-uncased

HOW TO RUN (WINDOWS / VS CODE)
-----------------------------
1. Open a terminal in the repository folder.
2. Create and activate a virtual environment:

   python -m venv nlp-env
   .\nlp-env\Scripts\Activate.ps1

3. Install required packages:

   python -m pip install numpy pandas nltk spacy scikit-learn gensim torch transformers ipykernel notebook

4. Download the spaCy English model:

   python -m spacy download en_core_web_sm

5. Download required NLTK data (run this in Python or a notebook cell):

   import nltk
   for resource in ["brown", "punkt", "punkt_tab", "stopwords", "wordnet", "omw-1.4", "averaged_perceptron_tagger_eng"]:
       nltk.download(resource)

6. Register the Jupyter kernel:

   python -m ipykernel install --user --name nlp-env --display-name "Python (nlp-env)"

7. Open NLP_Assignment.ipynb in VS Code, select Python (nlp-env),
   and run the notebook cells in order.

NOTES
-----
- The first run may require an internet connection to download the
  datasets and pretrained models.
- Some model downloads are large and can take time.
- Similarity scores and model neighbours may vary with training runs,
  library versions, or available pretrained weights.
- Read notebook outputs alongside written explanations.
- Do not commit the nlp-env folder, caches, or downloaded model weights.

SUGGESTED REPOSITORY CONTENTS
-----------------------------
NLP_Assignment.ipynb   Main assignment notebook
README.md             Formatted GitHub overview
README.txt            Plain-text overview
.gitignore            Ignore virtual environment and cache files

PURPOSE
-------
A learning-focused project demonstrating the progression from basic
text processing and sparse word representations to pretrained and
contextual embeddings, ending with a small NLP document pipeline.
