# Predicting Article Popularity in Online News Media

## 👉 [View the Full Analysis Here](https://mina-tj.github.io/news-popularity-ml/final_student.html)

## What is this project about?
Have you ever wondered why some news articles get shared thousands of times 
while others barely get noticed? This project tries to answer that question 
using machine learning.

I used a dataset of 39,644 articles published on Mashable to build models 
that predict how popular an article will be — before it even goes live.

## What I found
- The **keywords you use** matter more than anything else
- Articles published on **weekends** get significantly more shares
- **Social Media and Tech** topics consistently outperform other categories
- Writing **well-researched articles with lots of links** is associated with more shares

## Models I built
I compared four models for both predicting share counts and classifying 
articles as popular or not:

| Model | Result |
|-------|--------|
| Linear / Logistic Regression | Baseline benchmark |
| Random Forest | Good, but not the best |
| GBM | Slightly better than RF |
| **XGBoost** | **Best performer**  |

XGBoost achieved a test AUC of **0.7422** and RMSPE of **0.8462**, 
with a bootstrap stability of ± 0.0015 — meaning the results are 
very consistent and not just lucky.

## Dataset
- **Source:** Online News Popularity (UCI Machine Learning Repository)
- **Size:** ~40,000 articles, 59 features
- **Features include:** keywords, word counts, publishing day, topic channel, sentiment, links

##  Heads up on runtime
This project is seriously computationally heavy. Rendering the full QMD file 
from scratch takes around **7 hours** on an M4 MacBook Air. That's because of 
multiple grid searches, 100 bootstrap iterations, and stacked ensemble training 
across ~40,000 observations. The rendered HTML is provided so you don't have to wait!

## Tools used
- **Language:** R with Quarto
- **Libraries:** randomForest, gbm, xgboost, ROCR, pdp, tidyverse, doParallel

## Course
MBAN 5560 Final Project — Master of Business Analytics  
Saint Mary's University, 2026
