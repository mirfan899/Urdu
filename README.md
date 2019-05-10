## POS dataset
Urdu dataset for POS training. This is a small dataset to be used for training parts of speech tagging for Urdu Language.
Structure of the dataset is simple i.e.
```text
word TAG
word TAG
```

The tagset used to build dataset is taken from [Sajjad's Tagset](http://www.cle.org.pk/Downloads/langproc/UrduPOStagger/UrduPOStagset.pdf)
To get large dataset, you need to purchase the license. Contact: `virtuoso.irfan@gmail.com`

## UNER Dataset
Happy to announce that UNER (Urdu Named Entity Recognition) dataset is available for NLP apps.
Here are NER tags which are used in the dataset:
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

## SpaCy
I've also contributed to famous NLP library `SpaCy`. You can use `Urdu` word tokenizing, POS tagging other NLP tasks. 
You can train your own model for `POS` using this dataset.