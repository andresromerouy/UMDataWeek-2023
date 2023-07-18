# [UM-02] Term deposits, 2nd round

## Introduction

This lecture is a continuation of the analysis performed in lecture [UM-02], in which we take a different approach to the problem of **class imbalance**. With a 11.7% **conversion rate**, the data from the Portuguese bank showed a moderate class imbalance, which was addressed using a **scoring** approach. For this second round, we plan to use a **resampling** approach, training our predictive models in a modified data set in which the class imbalance has been artificially corrected.

There are various resampling methods, but we can summarize them as: **undersampling**, in which we reduce the number of negative training units to match the number of positive training units, and **oversampling**, in which we increase the number of positive training units to match the number of negative training units. 

## Questions

Q1. Perform a **random split** of the data set, taking one half for training and the other half for testing. You will resample the training subset, but leaving the testing subset as it is, without correcting there the class imbalance. 

Q2. Undersample the training subset, by randomly dropping as many negative units as needed to match the positive units, so that you end up with a pefectly balanced data set. Train a **logistic regression model** on these data and evaluate it on the testing subset. Supposing that you are going to call 20% of your clients, how would you validate your model?

Q3. Oversample the training subset, by randomly adding as many duplicates of the positive units as needed to match the negative units, so that you end up with a pefectly balanced data set. Train a logistic regression model on these data and evaluate it on the testing subset. Supposing that you are going to call 20% of your clients, how would you validate your model?
