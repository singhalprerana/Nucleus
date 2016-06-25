Quickly train, evaluate and deploy an optimum classifier for your text classification task. Currently, it allows you to use CNN, RNN< LSTM and fully connected layers to build the text classifier. Using this toolkit, you should be able to design a neural network architecture and train a classifier for most of the text classification tasks (multi-class and multi-label) without writing a single piece of code.

The main features of Nucleus are:
1. Easily design and train a deep learning based classifier
2. Config driven to make arrangement of layers to build the network, hyperparameter tuning, and experimentation easy

Code requires Python 2.7 and Theano 0.7. You can go to the Setting Up page, for instructions on how to quickly set up the python environment required for Optimus. Requirements are also listed in the requirements.txt file.

Word embeddings:
Google pre-trained word vectors are available at https://code.google.com/archive/p/word2vec/

Sample files for dataset, configuration and neural network layer arrangement are provided in files folder.


-------------------------------------------------------------------------------
Cross-validation
-------------------------------------------------------------------------------
python cv.py
	<configuration file path>
	<network layers file path>
	<folder to store information file>
	<path(s) of 1 or more data files>

-------------------------------------------------------------------------------
Train
-------------------------------------------------------------------------------
python training.py
	<configuration file path>
	<network layers file path>
	<existing training model file path (NO_MODEL if do not want to load model)>
	<existing static word-vectors file path (NO_STATIC if do not want to load model)>
	<existing nonstatic word-vectors file path (NO_NONSTATIC if do not want to load model)>
	<folder to store information and model files>
	<validation data file path (NO_VALIDATION_FILE if do not have such file)>
	<path(s) of 1 or more data files>

-------------------------------------------------------------------------------
Test
-------------------------------------------------------------------------------
python testing.py
	<model file path>
	<static word-vectors file path>
	<nonstatic word-vectors file path>
	<data file path (csv file with delimiter=',')>
	<folder to store information and output files>
	<path(s) of 1 or more word vector files (NO_FILE if no wordvecfiles)>

-------------------------------------------------------------------------------
Deploy
-------------------------------------------------------------------------------
python classify.py
	<model file path>
	<static word-vectors file path>
	<nonstatic word-vectors file path>
	<data file path (NO_FILE if do not want to classify data in a file)>
	<path(s) of 1 or more word vector files (NO_FILE if no wordvecfiles>

