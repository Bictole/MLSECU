# MLSECU [![Profile][title-img]][profile]

[title-img]:https://img.shields.io/badge/-SCIA--PRIME-red
[profile]:https://github.com/bictole

This project is about **Machine Learning and Cybersecurity**, we perform here the analysis of a large attacked netflow and the training of several machine learning algorithm, supervised and unsupervised, to compare them.

## Dataset

The dataset is not in the repository. It is the [UGR'16 dataset](https://nesg.ugr.es/nesg-ugr16/index.php) : A New Dataset for the Evaluation of
Cyclostationarity-Based Network IDSs.

The dataset is built with **real traffic** and **up-to-date attacks**. These data come from several netflow v9 collectors strategically located in the network of a spanish ISP. It is composed of two differentiated sets of data that are previously split in weeks.

A precise analysis of the dataset is available on [this](https://nesg.ugr.es/nesg-ugr16/dataset_AuthorVersionFinal.pdf) paper.

## Analysis

The analysis is made with python on the `MLSECU_SG_AL_VS.ipynb` notebook. We are going through the whole analysis process, with the **dataset exploration**, the **cleaning**, the **feature engineering**, **statistical analysis**, **visualization** and finally the **machine learning** part.

## Results

To compare our **supervised** classification model algorithms, we compared their f1_score to see which fit the data. We observed that the tree-based models, in particular the **RandomForest**, are those that obtains the best results.

<img src="https://github.com/Bictole/MLSECU/blob/master/bench.png" alt="Benchmarks_Results">

We also tested **XGBoost**, its results are excellent, with more than 94% of F1_score obtained for a test dataset with 1000 anomalies out of 10 000 network exchanges.