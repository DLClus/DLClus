# DLClus

DLClus is an algorithm that uses free-text clustering techniques to segment structured (tabular) data

# Table of contents

- [General Info](#general-info)
- [Technologies](#technologies)
- [Files](#files)
  - [Datasets](#datasets)
  - [Data Cleaning](#data-cleaning)
  - [TF-IDF](#tf-idf)
  - [AvgW2V](#AvgW2V)


# General Info

[(Back to top)](#table-of-contents)

This algorithm was developed as part of a bachelor's thesis investigating the use of clustering in the topical segmentation of data lakes.

# Technologies

[(Back to top)](#table-of-contents)

- Python v 3.7
- IDE: Google Colab Jupyter Notebook 

# Files

### Datasets

This file contains links to the datasets used in this project, segmented by topics. 
All of the datasets were acquired from Kaggle.

### Data Cleaning

This file contains the algorithm used to clean and pre-process the data; 
The algorithm takes a tabular dataset as input, extracts its columns names, cleans them, and then removes stop words. After that, the algorithm stems the remaining words to get the final set of keywords that will be used to define the dataset. These keywords are then inserted as a row into a new dataframe.
The output of this algorithm is a dataframe that contains each dataset's keywords as a row.

### TF-IDF

This files contains the algorithm that clusters the datasets based on their TF-IDF similarity scores;
The algorithm takes the keywords dataset as input, calculates the TF-IDF score and produces a vector for each row, and then clustering is done using K-means to group similar rows.
Acurracy of the model is then calculated by comparing the lables assigned by the clustering model to an array of ground truths.

### AvgW2V

This files contains the algorithm that clusters the datasets based on their Average word2vec similarity scores;
The algorithm takes the keywords dataset as input, generatesand a vector for each row, and then clustering is done using K-means to group similar rows.
Acurracy of the model is then calculated by comparing the lables assigned by the clustering model to an array of ground truths.

