## Description

Quora is a place to gain and share knowledge—about anything. It’s a platform to ask questions and connect with people who contribute unique insights and quality answers. This empowers people to learn from each other and to better understand the world.

Over 100 million people visit Quora every month, so it's no surprise that many people ask similarly worded questions. Multiple questions with the same intent can cause seekers to spend more time finding the best answer to their question, and make writers feel they need to answer multiple versions of the same question. Quora values canonical questions because they provide a better experience to active seekers and writers, and offer more value to both of these groups in the long term.

Currently, Quora uses a Random Forest model to identify duplicate questions. Here challenge is to tackle this natural language processing problem by applying advanced techniques to classify whether question pairs are duplicates or not. Doing so will make it easier to find high quality answers to questions resulting in an improved experience for Quora writers, seekers, and readers.

## Task

The goal of this competition is to predict which of the provided pairs of questions contain two questions with the same meaning. The ground truth is the set of labels that have been supplied by human experts. The ground truth labels are inherently subjective, as the true meaning of sentences can never be known with certainty. Human labeling is also a 'noisy' process, and reasonable people will disagree. As a result, the ground truth labels on this dataset should be taken to be 'informed' but not 100% accurate, and may include incorrect labeling. We believe the labels, on the whole, to represent a reasonable consensus, but this may often not be true on a case by case basis for individual items in the dataset.


## Data fields
- __id__ - the id of a training set question pair
- __qid1, qid2__ - unique ids of each question (only available in train.csv)
- __question1__, __question2__ - the full text of each question
- __is_duplicate__ - the target variable, set to 1 if question1 and question2 have essentially the same meaning, and 0 otherwise.

## Approach

- Importing Dependencies
- Reading and Understanding Data
- Tokenization
- Tweaking Stepwords
- Removal of Stepwords and punctuation
- Lemmatization
- Feature Engineering
- Calculated cosine similarity
- Scaling
- Modelling : I. Logistic Regression II.Random Forest III.XGBoost
- Evalution Metric : Accuracy and Log Loss

## Final Outcome

- Random Forest outperformed all with __Accuracy:93%__ and __Log Loss:2.17__