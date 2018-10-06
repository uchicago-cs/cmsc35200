Programming Assignments
=======================


Assignment 1: Due October 12
----------------------------

You are given a dataset, ``combined_rnaseq_data_lincs1000_combat``, of expression levels for 942 different genes (columns) in 15197 different cancer samples (rows). 
We want to determine to what extent the data for one gene can be predicted given the values for the 941 others.
Your task is to use Keras to build such a predictive model.

In this `Google Drive folder <https://drive.google.com/drive/folders/1-jkm2bUYWOftKm8is6rx3dKP9UIz2hCC?usp=sharing>`_ you will find:

* ``combined_rnaseq_data_lincs1000_combat``: A file with 15198 rows, each with 943 tab-separated columns: the data
* ``Assignment-1.ipynb``: A notebook that shows how to connect to, and access, your UChicago Google Drive, and then define and run a simple Keras model.

Proceed as follows:

1. Use `Random.Org <https://www.random.org/integers/>`_ to generate 3 random numbers in the range 2..941 (inclusive). These 3 numbers plus the numbers [0,1] together identify the 5 genes for which you will construct models. (For example, if you obtain random numbers 56, 452, and 593, then you want to compute on genes [0, 1, 56, 452, 593], i.e., the columns of the same number in the ``data`` array of ``Assignment-1.ipynb``.)

2. Make sure that you can run the code in ``Assignment-1.ipynb`` on Google Colaboratory. Use TensorBoard to study its progress.

3. For each of your 5 genes, experiment with different hyperparameters to find a set that generate a low ``val_losss``. 

4. Submit a file containing six lines:

   a. First, the URL for an ASCII text file containing a brief description of what you tried and what you learned. What hyperparameters did you vary? Which proved important? Did you find that the same model worked well for all genes?

   b. Then, five lines, one for each of your genes, each with the form

      <*gene-number*>, <*val-loss*>, <*URL-for-model*>, <*URL-for-history*>

      where:

      -  <*gene-number*> is an integer gene number

      -  <*val-loss*> is the best validation loss that you achievedd

      -  <*URL-for-model*> allows us to access a Google Drive file containing Python code for the model used to generate the <val-loss>. (You may name one model for all 5 genes, or a different model for each.)

      -  <*URL-for-history*> allows us to access a Google Drive file containing the execution trace for the run that achieved the reported val-loss

We will add an example of the desired output soon.
