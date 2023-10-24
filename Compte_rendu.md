# TP IA ESIR3 : Lab Sessions 1-2
### Autors

Students :
- Thomas Delapart 
- Yazid Benjamaa

Teacher :
- Zoltan Miklos (@zmiklos) ;
- Thibaut Le Marre (@18004558)

## I. Introduction

The goal for this first set of exercises is to familiarize yourself with the programming environment that we will use. Particularly with Keras, the deep learning python API that enables to program neural networks in a concise way.

We propose to create an environment with python version 3.5 in anaconda and install/update useful packages : Jupyter notebook, Numpy, Pandas, Matplotlib, seaborn, Scipy, scikit-learn, Tensorflow.

## II. Exercise 0

Create a conda environment with python 3.5

## III. Exercise 1 : Building a neural network to classify texts (multi-layer perceptron (MLP))

### III.1 Phenomena of over-fitting and under-fitting

- https://keras.io/datasets/
- Explore the dataset and calculate some basic statistics. Try to recover at least one review with the help of the dictionary mapping (based on this Tensorflow tutorial).
- Experiment with different network sizes : try to reduce or increase the network size, and observe the effect on the performance (accuracy of the prediction) and the running time.
- Change the network parameters to demonstrate the effects of over-fitting. Example.

## IV. Exercise 2 : Recurrent Neural Network and IMDB classification

In this exercise you will familiarize yourself with recurrent neural networks and in particular with LSTM.
- https://www.tensorflow.org/api_docs/python/tf/keras/datasets/imdb/load_data
- https://github.com/hansmichaels/sentiment-analysis-IMDB-Review-using-LSTM/blob/master/sentiment_analysis.py.ipynb

un the example code. Analyze the performance of the classifier on the test set and training set :
- If your training loss is smaller than test loss, then your network is likely to overfit. In that case, add (or increase) dropout and/or decrease the network size.
- If your training loss and test loss is almost the same, then your model is likely to underfit. In that case, increase the size of the network and/or the number of nodes/layer.
Do not forget to include all your remarks in your report !

- https://www.tensorflow.org/text/tutorials/text_classification_rnn?hl=fr
- https://machinelearningmastery.com/sequence-classification-lstm-recurrent-neural-networks-python-keras/
- https://colah.github.io/posts/2015-08-Understanding-LSTMs/

## V. Exercise 3 : Text classification on the Ohsumed dataset

The goal of this exercise is to realize a text classifier using deep neural networks. Your task is to construct a classifier, using the available training set, and evaluate it using the test set. The classifier should predict the category for the articles.

Dataset : We will work with the Ohsumed dataset that contains abstracts of scientific articles from a large medical publication database. The articles are related to one of 23 categories of cardiovascular diseases. ```IMDB_Dataset.zip```

Dataset description : The dataset has two versions :
- One that contains the first 20000 articles (split into training and test set), available on Moodle ;
- A more complete version that has all articles (50000 articles), available here.

You should work with the version that has 20000 articles, and only use the complete version only once you constructed and analyzed an efficient classifier for the smaller set. As usual, the dataset is split into two parts : a training set and a test set. Each article of the collection is labeled with one of the 23 categories. 

Overall strategy : To realize a classifier you should use an iterative approach : try to realize a simple classifier first, then analyze its performances (e.g. using the accuracy metric), then chose techniques to improve the performance (in terms of accuracy) of your classifier. 

Try to describe and document the development process in your report : which experiments did you run ? What were the results ? What did you
do to improve the performance and why ?
To implement your first text classifier from scratch, we advise you to :
- Look into the data, get familiar with its structure and the type of text you will process ;
- Explore the data and compute some basic statistics. For example, what is the size of the vocabulary ?

What is the number of examples in the training/test set per category ? What is the frequency of the words ? What is the most common, the least common ? Feel free to add anything you find relevant on the dataset ;

- Preprocessing : adjust your data to be able to pass them into a neural network ;
- Create a neural network with a simple architecture and train it ;
- Evaluate the performance of your classifier on the training set and the test set. These numbers can give hints about the quality of your classifier and can also can guide you to decide what to do in order to improve the performance. Beware of under-fitting and over-fitting ;
- Interpret your results (in plain text) and set your next objective (for example, if you had an over-fitting and you decide to add regularization, explain it) ;
- Iterate (many many many times) and try to improve your model. Tunning a network is sometimes difficult due to all the possibilities for the hyper-parameters. 

In order to improve your network during your iterations, you can try to :
- Invest time to do more preprocessing. For example, remove frequent words, remove stopwords, perform stemming. A quick introduction here ;
- Change the parameters of your algorithms and your optimizers, cost functions, etc ;
- Add dropout, early stopping, regularization ;
- Change the network topology/use different techniques (multilayer perceptron, LSTM, etc) ;
- Only when you managed to obtain good results, witch to the bigger dataset.

## Documentation

- https://docs.github.com/en/get-started/using-git/about-git
- https://www.tutorialspoint.com/git/index.html
- https://docs.anaconda.com/anaconda/navigator/getting-started/ and
- https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf
- https://www.dataquest.io/blog/jupyter-notebook-tutorial/
