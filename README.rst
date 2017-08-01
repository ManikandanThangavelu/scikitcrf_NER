
====================================
Entity recognition using scikit CRF
====================================

^^^^^^^^^^^^^
Decscription
^^^^^^^^^^^^^

This is a simple python applicaion that uses `sklearn-crfsuite <https://sklearn-crfsuite.readthedocs.io/en/latest/>`_ for entity recognition using ``CRF``.

^^^^^^^^^^^^^
Installation
^^^^^^^^^^^^^

Install this package using pip by running the follwing command::

	pip install scikitcrf_ner

^^^^^^
Usage
^^^^^^

* import the package using::

	from scikitcrf_ner import entityRecognition
* Train the model using::

	entityRecognition.train("path\\to\\trainingfile.json")
* Refer the sample training file(``sample_train.json``), the training file should be json formatted
* Predict the entities by::

	entityRecognition.predict("Utterance")

^^^^^^^^^^^^
Sample code
^^^^^^^^^^^^

Refer this sample code::

	from scikitcrf_ner import entityRecognition as ner
	ner.train("sample_train.json")
	entities = ner.predict("show me some Indian restaurants")
	print(entites)

^^^^^^^^
License
^^^^^^^^
* ``MIT``
