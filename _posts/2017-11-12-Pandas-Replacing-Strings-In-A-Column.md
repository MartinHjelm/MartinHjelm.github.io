---
layout: post
title: Pandas - How to replace string values in a column with integer numbers
---
I found this nice solution on [StackOverflow](https://unix.stackexchange.com/questions/122795/long-line-wrapping-in-nano) to the problem of replacing strings in the columns of a dataframe. Lets assume that a column named _labels_ contains the label strings [A,B,C] and we want to replace them with [0,1,2]. Then we can do the following,

    labels = df['labels'].unique().tolist()
    mapping = dict(zip(labels,range(len(labels))))
    df.replace({'labels': mapping},inplace=True)

This code first creates a list of the unique labels, creates a dictionary mapping from label value to a numeric value, and finally does a in place replacing of the label values with the numerical values. 
