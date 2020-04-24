# Machine Comprehension Using BiDAF on SQuAD
### Abstract
The  aim  of  the  project  is  to  build  and  traina  model  to  perform  contextual  question  answering,  i.e.   to  be  able  to  learn  a  text  and then answer simple questions based on it.  Wehave  chosen  to  train  a  BiDAF  model,  using BERT and ALBERT as baselines.  We are using  the  SQuAD  1.1  dataset  for  our  training, using the approach of fine-tuning pre-trained models.  The model could have various practical applications in the field of large text comprehension

### Content
The repository contains the following content:
*   /data: contains one prediction file generated by the model, and it will contain the training data that are to be downloaded due to large size;
*   bidaf.py: contains the main BiDAF model with all the layers implemented;
*   utils.py: contains LSTM and Linear NN models that are often used in bidaf.py;
*   memory.py: contains a class to memorize the parameters of the trained model;
*   evaluate.py: contains the official code taken from SQuAD to evaluate the development data;
*   squad.py: contains a class for preprocessing the data and building splits to use as batch iterations;
*   requirements.txt: python libraries to be used;
*   team_13_final_report: the final report where we illustrate our work.

### Installation
To run the code you can clone the repo onto your machine using the following command on terminal
```
 git clone https://github.com/PietroDomiGT/cs4650-team13.git
```
Then you need to download the training data into the /data folder. On the same terminal run
```
 (cd data && wget "https://github.com/rajpurkar/SQuAD-explorer/raw/master/dataset/dev-v1.1.json" && wget "https://github.com/rajpurkar/SQuAD-explorer/raw/master/dataset/train-v1.1.json")
```
Then you need to make sure you have the required python libraries. Run
```
 pip install -r requirements.txt
```
### Execution
Finally, you can run the model by doing
```
 python main.py
```
We ran the models on a Colab notebooks to make use of the available GPU. To use it click on th following:

BiDAF - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Pe6WuBVGRMpGcuqOFfmzMlEi8UCaSZOm)
ALBERT - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
(https://colab.research.google.com/drive/1Bh3d1h_cmE-ExxLbALq104LtcayBQXG3)
BERT - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
https://colab.research.google.com/drive/1ZctjDf4bz7XbmQqHvmWNzQaSHI8M0uSj

To show the possible parameters to change and tune differently, run
```
 pyhton main.py -h
```
