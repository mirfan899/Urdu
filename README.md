## POS dataset
Urdu dataset for POS training. This is a small dataset and can be used for training parts of speech tagging for Urdu Language.
Structure of the dataset is simple i.e.
```text
word TAG
word TAG
```

The tagset used to build dataset is taken from [Sajjad's Tagset](http://www.cle.org.pk/Downloads/langproc/UrduPOStagger/UrduPOStagset.pdf)
To get large dataset, you need to purchase the license. Contact: `virtuoso.irfan@gmail.com`

## NER Datasets
Following are the datasets used for NER tasks.

### UNER Dataset
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
NER Dataset is in `utf-16` format.

### MK-PUCIT Dataset
Latest for Urdu NER is available. Check this paper for more information [MK-PUCIT](https://www.researchgate.net/publication/332653135_URDU_NAMED_ENTITY_RECOGNITION_CORPUS_GENERATION_AND_DEEP_LEARNING_APPLICATIONS).

Entities used in the dataset are
```text
Other
Organization
Person
Location
```

`MK-PUCIT` author also provided the `Dropbox` link to download the data. [Dropbox](https://www.dropbox.com/sh/1ivw7ykm2tugg94/AAB9t5wnN7FynESpo7TjJW8la)

## Datasets for Sentiment Analysis
### IMDB Urdu Movie Review Dataset.
This dataset is taken from [IMDB Urdu](https://www.kaggle.com/akkefa/imdb-dataset-of-50k-movie-translated-urdu-reviews).
It was translated using Google Translator. It has only two labels i.e.
```text
positive
negative
```

### Roman Dataset
This dataset can be used for sentiment analysis for Roman Urdu. It has 3 classes for classification.
```textmate
Neutral
Positive
Negative
```
If you need more information about this dataset checkout the link [Roman Urdu Dataset](https://archive.ics.uci.edu/ml/datasets/Roman+Urdu+Data+Set).

### Products & Services dataset
This dataset is collected from different sources like social media and web for various products and services for sentiment analysis.
It contains 3 classes.
```textmate
pos
neg
neu
```

### Urdu Dataset
Here is a small dataset for sentiment analysis. It has following classifying labels 
```textmate
P
N
O
```
Link to the paper [Paper](https://www.researchgate.net/publication/338396518_Urdu_Sentiment_Corpus_v10_Linguistic_Exploration_and_Visualization_of_Labeled_Dataset_for_Urdu_Sentiment_Analysis)
Github link to data [Urdu Corpus V1](https://github.com/MuhammadYaseenKhan/Urdu-Sentiment-Corpus)

## News Datasets
### Urdu News Dataset 1M
This dataset(`news/urdu-news-dataset-1M.tar.xz`) is taken from [Urdu News Dataset 1M](https://data.mendeley.com/datasets/834vsxnb99/3). It has 4 classes and can be used for classification
and other NLP tasks. I have removed unnecessary columns.
```text
Business & Economics
Entertainment
Science & Technology
Sports
```

### Real-Fake News dataset
This dataset(`news/real_fake_news.tar.gz`) is used for classification of real and fake news in [Fake News Dataset](https://github.com/MaazAmjad/Datasets-for-Urdu-news) 
Dataset contains following domain news.
```text
Technology 
Education 
Business
Sports
Politics
Entertainment
```

### News Headlines
Headlines(`news/headlines.csv.tar.gz`) dataset is taken from [Urd News Headlines](https://github.com/mwaseemrandhawa/Urdu-News-Headline-Dataset). Original dataset is in Excel format,
I've converted to csv for experiments. Can be used for clustering and classification.
### RAW corpus and models
## COUNTER (COrpus of Urdu News TExt Reuse) Dataset
This dataset is collected from journalism and can be used for Urdu NLP research.
Here is the link to the resource for more information
[COUNTER](http://ucrel.lancs.ac.uk/textreuse/counter.php).

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

## Some Helpful Tips

### Download Single file from Github
If you want to get only raw files(text or code) then use curl command i.e.
```shell script
curl -LJO https://github.com/mirfan899/Urdu/blob/master/ner/uner.txt
```

### Concatenate files
```shell script
cd data
cat */*.txt > file_name.txt
```

### MK-PUCIT
Concatenate files of MK-PUCIT into single file using.
```shell script
cat */*.txt > file_name.txt
```

Original dataset has a bug like `Others` and `Other` which are same entities, if you want to use the dataset 
from `dropbox` link, use following commands to clean it.
```python
import pandas as pd
data = pd.read_csv('ner/mk-pucit.txt', sep='\t', names={"tag", "word"})
data.tag.replace({"Others":"Other"}, inplace=True)
# save according you need as csv or txt by changing the extension
data.to_csv("ner/mk-pucit.txt", index=False, header=False, sep='\t')
```
Now csv/txt file has format 
```text
word tag
```

## Note
If you have a dataset(link) and want to contribute, feel free to create PR.