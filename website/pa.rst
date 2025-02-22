Programming Assignments
=======================

* Assignment 1: Due October 8
* Assignment 2: Due October 22
* Assignment 3: TBD
* Assignment 4: TBD

Please submit the assignments via `Gradescope <https://www.gradescope.com>`_. You should have already received an email from Gradescope on CMSC35200 enrollment.


Assignment 1: Due October 8
----------------------------

Goal: Gain familiarity with Google Colab, Keras, and the impact of hyperparameters on model performance

You are given a dataset, ``combined_rnaseq_data_lincs1000_combat``, of expression levels for 942 different genes (columns) in 15197 different cancer samples (rows). 
We want to determine to what extent the data for one gene can be predicted given the values for the 941 others.
Your task is to use Keras to build such a predictive model.

In this `Google Drive folder <https://drive.google.com/drive/folders/1-jkm2bUYWOftKm8is6rx3dKP9UIz2hCC?usp=sharing>`_ you will find:

* ``combined_rnaseq_data_lincs1000_combat``: A file with 15198 rows, each with 943 tab-separated columns: the data
* ``Assignment-1.ipynb``: A notebook that shows how to connect to, and access, your UChicago Google Drive, and then define and run a simple Keras model.

Proceed as follows:

1. Use `Random.Org <https://www.random.org/integers/>`_ to generate 3 random numbers in the range 2..941 (inclusive). These 3 numbers plus the numbers [0,1] together identify the 5 genes for which you will construct models. (For example, if you obtain random numbers 56, 452, and 593, then you want to compute on genes [0, 1, 56, 452, 593], i.e., the columns of the same number in the ``data`` array of ``Assignment-1.ipynb``.)

2. Make sure that you can run the code in ``Assignment-1.ipynb`` on Google Colaboratory. Use TensorBoard to study its progress.

3. For each of your 5 genes, experiment with different hyperparameters to find a set that generate a low ``val_loss``. (E.g., you can change the number and size of layers, use different activation functions, use a different optimizer.)

4. submit the assignment via Gradescope. Check in a Colab notebook containing:
    - a markdown block containing a brief description of what you tried and what you learned. What hyperparameters did you vary? Which proved important? Did you find that the same model worked well for all genes?
    - code blocks for 5 models, each headed with a markdown cells:
        <*gene-number*>, <*val-loss*>
    
        where:
            - <*gene-number*> is an integer gene number
            - <*val-loss*> is the best validation loss that you achieved

        You may name one model for all 5 genes, or a different model for each. Training history should present to allow us to verify the reported val-loss


Assignment 2: Due October 22
----------------------------

Goal: Gain experience evaluating the performance of models, frameworks and
hardware architectures

* Pick two frameworks (e.g., TensorFlow, Pytorch , Mxnet, PlaidML , CNTK, Keras/X, Keras/Y)
* Pick two different models (e.g., VGG, ResNet, MobileNet) for which pretrained version of ImageNet are available
* Build a custom version of the `Kaggle cats-and-dogs classification problem <https://www.kaggle.com/c/dogs-vs-cats>`_ (which re-trains known image models) on some classification task of your choice.
* You have to choose some image topics to gather for classification using the retuned model(s)
* Measure the performance of training *and* inference of the models (for two different models (e.g., vgg vs. resnet) and two different frameworks (e.g., TF vs. Pytorch) on CPU, GPU and TPU or something else (e.g., your laptop; goal is to compare two different platforms to CPUs for a total of three platforms)
* Write up: Explain and account for the performance differences in terms of architecture elements, software stack, framework implementation strategy, and model structure
* Submit the assignment via Gradescope. Check in a Colab notebook file containing:
    - a markdown block documenting the studies that you performed and noting lessons learned
    - a markdown block documenting the required performance measurements on your chosen platfoms
    - code blocks including the models used to obtain those results, with execution traces

