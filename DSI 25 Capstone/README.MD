Project Title: Predicting Myocarditis/Pericarditis using VAERS dataset

This project aims to classify whether a patient is at risk of myocarditis or pericarditis
based on VAERS data.

Description

VAERS Dataset

The Vaccine Adverse Effect Reporting System (VAERS) is a early warning system to detect
possible safety problems in U.S.-licensed vaccines. VAERS accepts and analyzes reports of
adverse events (or side effects) after a person has received a vaccination.

VAERS is a passive reporting system, meaning it relies on individuals to send in r
eports of their experiences. As such, it is prone to biasness from self-reporting and therefore,
not designed for determining if a vaccine caused a health problem. Nonetheless, it can be
especially useful for detecting unusual or unexpected patterns of adverse event reporting that
might indicate a possible safety problem with a vaccine.

Problem Statement

There has been some concerns regarding the association between myocarditis and vaccination.
This has caused some uproar in social media. Some groups of people, particularly anti-vaccination
groups have used the VAERS dataset for analysis and concluded that COVID-19 vaccinations are associated
with myocarditis.

However, based on expert's advice, the VAERS dataset is not suitable for analysis as it is a passive
reporting system whereby any individuals can report their adverse events. This results in reporting
biasness which can lead to over-reporting of serious adverse events. In addition, the VAERS dataset do
not have a control group for baseline comparison and this can lead to erronous conclusion.

In this project, we will be attempting to create a predictive model using the VAERS dataset and base
on model results, decide whether if a suitable predictive model can be created using the VAERS dataset. The
outcome of interest for this project is myocarditis-related symptoms and pericarditis-related symptoms

Run the jupyter notebooks in this sequence:

1. Capstone VAERS
2. Capstone_VAERS_EDA
3. Capstone VAERS Modelling
4. Collect the data and presentation slides (pdf format) at https://drive.google.com/drive/folders/1FO3Ozak9MM1Aw4aNgClNr6PzcJV8zARR?usp=sharing

Data cleaning

1. Remove duplicates
2. Remove missing dataset
3. Impute missing data for column "VAX_SITE" using model
4. Remove redundant columns
5. Binarise all categorial features
6. Binarise all outcome variables and collapse them into a single columns

EDA

1. Distribution graph of all features
2. Biostatistics for all features between myocarditis/pericarditis patients and
non-myocarditis/pericarditis patients
3. Creating a simulated control group

Modelling

1. Preliminary modelling using pycaret
2. Optimization using Smote and Gridsearch CV
3. Neural Networks

Conclusion and Recommendation

The shortlisted models are XGBoost, XGBoost with ADASYN and a 2 layer NN models.
Expert's opinion is needed to determine which metric is important because consequences
can be dire. If precision is preferred over recall, XGBoost can be used. If recall
is preferred over precision, XGBoost with ADASYN and the 2 layer NN model can be used.

Model can be deployed but should not be solely relied on. It is recommended to be
complemented with more robust laboratory test to determine if patient is truly
at risk of myocarditis/pericarditis.

Authors:
Nixon
