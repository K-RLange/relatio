# Multiple-Sentence-relatio
Based on the RELATIO-package "[Text Semantics Capture Political and Economic Narratives" (2021)](https://arxiv.org/abs/2108.01720).

```bash
# upgrade pip, wheel and setuptools
python -m pip install -U pip wheel setuptools

# install the package
!pip install -U git+https://github.com/K-RLange/relatio.git

# download SpaCy and NLTK additional resources
python -m spacy download en_core_web_sm
python -m nltk.downloader punkt wordnet stopwords averaged_perceptron_tagger
```

# Current Contributions
-Added "start" and "end" parameters for each statement, so that different statements within a sentence can be located.

# To Do
-Filter for statements that do not overlap - choose the maximum of disjunct statements per sentence.
-Combine multiple statements within a sentence and between sentences using "RELATIOn-indicators, such as "and", "therefore", "because",...
