# Entity recognition using scikit CRF

## Decscription

This is a simple python applicaion that uses [sklearn-crfsuite](https://sklearn-crfsuite.readthedocs.io/en/latest/) for entity recognition using `CRF`.

## Installation

Install this package using pip by running the follwing command

> pip install scikitcrf_ner

###### if you face any issues while installing sklearn_crfsuite [This may help](https://github.com/scrapinghub/python-crfsuite/issues/51#issuecomment-283244262)

Make sure you download spacy english model using

> python -m spacy download en

## Usage

Import the package using

> from scikitcrf_ner import entityRecognition

Train the model using

> entityRecognition.train("path/to/trainingfile.json")

Refer the sample training file(`sample_train.json`), the training file should be json formatted
Predict the entities by

> entityRecognition.predict("Utterance")

## Sample code

Refer this sample code:
``` python
from scikitcrf_ner import entityRecognition as ner
ner.train("sample_train.json")
entities = ner.predict("show me some Indian restaurants")
print(entites)
```

## License
`MIT`
