## POS dataset
Urdu dataset for POS training. This is a small dataset and can be used for training parts of speech tagging for Urdu Language.
Structure of the dataset is simple i.e.
```text
word TAG
word TAG
```

The tagset used to build dataset is taken from [Sajjad's Tagset](http://www.cle.org.pk/Downloads/langproc/UrduPOStagger/UrduPOStagset.pdf)
To get large dataset, you need to purchase the license. Contact: `virtuoso.irfan@gmail.com`

## UNER Dataset
Happy to announce that UNER (Urdu Named Entity Recognition) dataset is available for NLP apps.
Following are NER tags which are used to build the dataset:
```text
PERSON
LOCATION
ORGANIZATION
DATE
NUMBER
DESIGNATION
TIME
```
If you want to read more about the dataset check this paper [Urdu NER](https://www.researchgate.net/profile/Ali_Daud2/publication/312218764_Named_Entity_Dataset_for_Urdu_Named_Entity_Recognition_Task/links/5877354d08ae8fce492efe1f.pdf).
### Note
NER Dataset is in `utf-16` format.

## COUNTER (COrpus of Urdu News TExt Reuse) Dataset
This dataset is collected from journalism and can be used for Urdu NLP research.
Here is the link to the resource for more information
[COUNTER](http://ucrel.lancs.ac.uk/textreuse/counter.php).

## Roman Urdu Dataset
This dataset can be used for sentiment analysis for Roman Urdu. It has 3 classes for classification.
```textmate
Neutral
Positive
Negative
```
If you need more information about this dataset checkout the link [Roman Urdu Dataset](https://archive.ics.uci.edu/ml/datasets/Roman+Urdu+Data+Set).

## Urdu model for SpaCy
Urdu model for SpaCy is available now. You can use it to build NLP apps easily. Install the package in your working environment.
```shell
pip install ur_model-0.0.0.tar.gz
```

You can use it with following code.
```python
import spacy
nlp = spacy.load("ur_model")
doc = nlp("میں خوش ہوں کے اردو ماڈل دستیاب ہے۔ ")
```

### NLP Tutorials for Urdu
Checkout my articles related to Urdu NLP tasks
* POS Tagging [Urdu POS Tagging using MLP](https://www.urdunlp.com/2019/04/urdu-pos-tagging-using-mlp.html)
* NER [How to build NER dataset for Urdu language?](https://www.urdunlp.com/2019/08/how-to-build-ner-dataset-for-urdu.html), [Named Entity Recognition for Urdu](https://www.urdunlp.com/2019/05/named-entity-recognition-for-urdu.html)
* Word 2 Vector [How to build Word 2 Vector for Urdu language](https://www.urdunlp.com/2019/08/how-to-build-word-2-vector-for-urdu.html)
* Word and Sentence Similarity [Urdu Word and Sentence Similarity using SpaCy](https://www.urdunlp.com/2019/08/urdu-word-and-sentence-similarity-using.html)
* Tokenization [Urdu Tokenization using SpaCy](https://www.urdunlp.com/2019/05/urdu-tokenization-usingspacy.html)
* Urdu Language Model [How to build Urdu language model in SpaCy](https://www.urdunlp.com/2019/08/how-to-build-urdu-language-model-in.html)

These articles are available on [UrduNLP](https://www.urdunlp.com/).

### Some Helpful Tips
If you want to get only raw files(text or code) then use curl command i.e.
```shell script
curl -LJO https://github.com/mirfan899/Urdu/blob/master/ner/uner.txt
```

Command used to concatenate the files
```shell script
cd ner
cat */*.txt > uner.txt
```