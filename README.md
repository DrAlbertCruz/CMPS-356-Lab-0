# Lab 0: A simple reflex agent and performance metrics

CMPS 3560 - Artificial Intelligence

Alberto C. Cruz, Ph.D.

Department of Computer and Electrical Engineering and Computer Science

# Prelab

The following questions should be answered before the start of the lab. Read the entire lab first, and then answer the questions. Definitions should be answered in your own words. Cutting and pasting from any other source is considered plagiarism.

1. What is the difference between ground truth and a predicted label?
1. The rule given with this code is as follows: `IF 'sepal width' > 3.0 THEN 'prediction' is 'I. Versicolor'` Using this rule, what true positive rate do you expect? What accuracy?

# Introduction

## Goal

* Develop a program that implements a simple reflex agent
* Understand sensitivity, specificity, precision and accuracy

## Required Files

* This repository contains the lab manual and C++ code, but you are not required to use the code

## Background


In today’s lab, we will make a simple reflex agent that predicts the species of flower. The simple reflect agent uses an IF-THEN rule like an expert system. We will distinguish between flower species of Iris Virginica and Iris Virginica. The procedure follows:

1. Read in data measurements of 100 flowers from a comma separated value file (CSV)
1. Improve a simple reflex agent
1. Calculate the specificity, precision and accuracy

You must complete the lab with a partner. Collaboration with your lab partner is okay. Collaboration with other groups is also okay. Yet, sharing of code between groups is not okay and is cheating. I will assign a single grade to each group. If disputes arise you may switch partners. But, you must notify the instructor of any changes before any the start of the next lab. This repository contains base C++ code but you are not required to use it. I am familiar with C, C++, Java, MATLAB, Prolog, and Javascript. Refer to the syllabus for grading policies.

## Reflex agents

A reflex agent is an AI agent that acts only on the current stimulus. Reflex agents follow IF condition THEN action rules. This is like rule-based expert systems, except those systems have inference. Rule-based expert systems are discussed in Chapter 2. The reflex agent for today carries out a prediction using an IF-THEN rule. It does not use inference, consider the history of the data, or learn. An example: `IF 'fruit' is 'red' THEN 'fruit' is 'apple'`.  

As it turns out, there are red fruits out there that are not apples. Our agent can be wrong. This is an important concept. So, to measure the performance of our system, we will test it with many samples.

A sample consists of some data of the object. In the case of our apple, some relevant features are the weight, and color. It also has an associated correct prediction. For example:

1. 6 oz, yellow ... Bannana
1. 3 oz, red ... Strawberry

We will test the agent sample by sample, noting if it was correct. Noting the number of failures is absolute, and will vary based on how many samples you test on. A better metric is 
