## Computer-Science-Project-2020
#[GitLab Repository](https://gitlab.doc.gold.ac.uk/mzdun001/Computer-Science-Project-2020)

## Report: ["Deep Learning For Multi-Label Emotion Classification in Social Media Posts"](https://drive.google.com/file/d/1BpnTVBu1XYKJj-0GdWmxxM6iWVv6STsb/view?usp=sharing)

## Project's aim:
Emotions are manifested in facial expressions, body movements and reactions such
as increasing heart rate or blood pressure, as well as language, both verbal and written. While there has been a lot of 
research in categorizing emotion from facial expressions, affect in language and text is also gaining scientific interest.
The primary goal of my project is to automatically assign no emotion or 1, or
more emotion labels ("anger", "anticipation", "disgust", "fear", "joy", "love", "optimism", "pessimism", "sadness", "surprise" and "trust") to each text in the data set and
to find a model structure that would give the best results according to the metrics
typically used for evaluating models that deal with multi-label data: loss calculated
using a binary cross entropy function, accuracy, precision and recall, as well as metrics such as Jaccard index and F1 measure.

Since I am exploring the results given by the use of deep
learning models, the second goal is to achieve results that are better than a random
classifier model and non-deep learning baselines.
Most of my work goes in line with the [SemEval-2018 competition - Task
1: Affect in text](https://competitions.codalab.org/competitions/17751#learn_the_details) (subtask 5A: multi-label classification - English). I have used the
data set provided within the competition and investigated models proposed by the
participants of the competition. Jaccard index, as well as macro- and micro-averaged
f1 score, which I used to evaluate my models on the test set, were official metrics
used in the contest. Therefore, as part of the evaluation of my project, I compare
my results with the official results published, as well as the results achieved post
evaluation period.

### Directories
- Experiments that I describe in my report can all be found in **[SemEval models](SemEval models/)** :
(Experiment 0 to Experiment 7, and "Best models trained with (...) - dimensional Twitter embeddings").

- Data set I use can be found in [SemEval models/data](SemEval models/data)

- I evaluate experiments on test set at the end of each notebook, but [SemEval models/TEST.ipynb](SemEval models/TEST.ipynb)
is where I load one of the best performing models and create files with predictions on the SemEval test set :
[SemEval models/test_set_predictions.txt](SemEval models/test_set_predictions.txt), and on my own data set downloaded with Twint : [SemEval models/twint_data_predictions.txt](SemEval models/twint_data_predictions.txt).

- [SemEval models/E-C_en_pred.txt](SemEval models/E-C_en_pred.txt) is a file in a specific format needed to sumbit to automatic scoring in the [SemEval competition](https://competitions.codalab.org/competitions/17751#participate).

- [SemEval models/graphs/](SemEval models/graphs) : all graphs of model architectures

- [SemEval models/trained models](SemEval models/trained models/) : saved models

### Pre-trained embeddings:
In my experiments I use pre-trained embeddings that are not in this repository 
(and the path is set to:
` glove_dir = '/Users/goszk/Desktop/labs AI/datasets/pretrained word vectors/glove.6B/glove.6B.100d.txt' ` 
or
` glove_dir = '/Users/goszk/Desktop/labs AI/datasets/pretrained word vectors/glove.twitter.27B/glove.twitter.27B.200d.txt' ` )

Embeddings that I use, are [GloVe embeddings](https://nlp.stanford.edu/projects/glove/):
- Wikipedia 2014 + Gigaword 5 (6B tokens, 400K vocab, uncased, 50d, 100d, 200d, & 300d vectors, 822 MB download): **glove.6B.zip**
- Twitter (2B tweets, 27B tokens, 1.2M vocab, uncased, 25d, 50d, 100d, & 200d vectors, 1.42 GB download): **glove.twitter.27B.zip**

### Built using:
Python 3, Jupyter Notebook, Tensorflow, Keras, scikit-learn, Numpy, Matplotlib, Pandas

### Additional packages (outside built-in python modules) installed for experimenting with and final text pre-processing functions:
- [BeautifulSoup](https://pypi.org/project/beautifulsoup4/)
- [nltk](https://pypi.org/project/nltk/)
- [emoji](https://pypi.org/project/emoji/)
- [spacy](https://pypi.org/project/spacy/)



