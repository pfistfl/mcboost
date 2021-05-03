---
title: 'mcboost: Multi-Accuracy Boosting for R'
tags:
  - R
  - Multi-Accuracy
  - Boosting
  - Post-Processing
  - Fair ML
authors:
  - name: Florian Pfisterer^[Corresponding author]
    orcid: 0000-0001-8867-762X
    affiliation: 1
  - name: Christoph Kern
    orcid: 0000-0001-7363-4299
    affiliation: 2
  - name: Susanne Dandl
    orcid: 
    affiliation: 1
affiliations:
 - name: Ludwig Maximilian University of Munich
   index: 1
 - name: University of Mannheim
   index: 2
date: 20 April 2021
bibliography: paper.bib
---

# Summary

Given the increasing usage of automated prediction systems in the context of high-stakes decisions, a growing body of research focuses on methods for detecting and mitigating biases in algorithmic decision-making. `mcboost` implements Multi-Accuracy Boosting for R, a post-processing method which has been proposed by @kim2019, adapting the multicalibration framework of @hebert-johnson2018. The underlying fairness notion, Multi-Accuracy, promotes the idea of multigroup fairness and requires accurate predictions not only for marginal populations, but also for subpopulations that may be defined by complex intersections of many attributes. In contrast to other Fair ML approaches, Multi-Accuracy Boosting does not harm the overall utility of a prediction model by imposing a fairness constraint in the training process, but rather aims at improving prediction performance for a large set of subpopulations post training.

`mcboost` is model agnostic and allows the user to post-process any model that returns predictions. Post-processing would typically be run on a labeled auditing dataset after model training. `mcboost` includes two pre-defined learners for post-processing (ridge regression and decision trees), and allows to easily adjust the learner that is used for Multi-Accuracy Boosting. Users may also specify a fixed set of subgroups, instead of a learner, on which predictions should be audited.   

# Statement of need

Given the ubiquitous use of machine learning models in crucial areas and growing concerns of biased predictions for minority subpopulations, Multi-Accuracy Boosting should be widely accessible in form of a free and open-source software package. Previous to the development of `mcboost`, Multi-Accuracy Boosting has not been released as a software package.

# Acknowledgements

We acknowledge contributions from ...

# References