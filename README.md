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
-Now performs an analysis to create disjoint statements. The algorithm uses a greedy approach to find the maximum number of disjoint statements within a sentence that include an ARG0, an ARG1 and a B-V.

# To Do
-Named Entity Recognition at the start

-Coreference Resolution supported by NER - Choose the representation for all words, that are assigned the same meaning, as a named entity, if one is found within those words. Otherwise choose the first appearance.

-Combine multiple statements within a sentence and between sentences using RELATIOn-indicators, such as "and", "therefore", "because",...
