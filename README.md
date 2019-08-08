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
Here is the link to the resource for more information.
[COUNTER](http://ucrel.lancs.ac.uk/textreuse/counter.php)

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
## SpaCy
I've also contributed to famous NLP library `SpaCy`. You can use `Urdu` word tokenizing, POS tagging and other NLP tasks. 
You can train your own `POS` model using this dataset.