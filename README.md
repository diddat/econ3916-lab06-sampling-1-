# econ3916-lab06-sampling-1-

# Sampling for Machine Learning — Train-Test Splits

## Objective

In this lab, I explored how the way data is split and prepared affects the accuracy of machine learning evaluations.

## Methodology

- I analyzed survival rates in a Titanic passenger dataset with 891 passengers.
- I compared a regular 80/20 train-test split with a split that keeps the survival proportions similar.
- I checked the passenger-class shares in the training and test sets.
- I corrected data leakage by fitting a StandardScaler and a SimpleImputer on the training data only.
- I wrote split_by_share() to make a train-test split using a chosen test percentage and random seed, and tested it with a 30% test share.
- In the optional extension, the lab models the Literary Digest polling problem to compare large biased samples with smaller random ones.

## Key Findings

- The overall Titanic survival rate was about **38.4%**: 342 of 891 passengers survived.
- The survival rates differed a lot by class: about **63.0%** in first class, **47.3%** in second class, and **24.2%** in third class.
- A stratified split kept the training and test survival rates closer to the overall survival rate than a regular split.
- I learned that test data should not be used to fit preprocessing steps, since that would give the training process information it is not supposed to have.
- **Sample design matters more than sample size.** A large biased sample can give a worse answer than a much smaller, well-chosen sample.
