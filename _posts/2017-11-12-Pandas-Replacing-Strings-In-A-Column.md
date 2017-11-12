---
layout: post
title: Pandas: How to replace string values in a column with integer numbers
---
I found this nice solution on [StackOverflow](https://unix.stackexchange.com/questions/122795/long-line-wrapping-in-nano) to the problem of replacing strings in the columns of a dataframe. Lets assume that a column named _labels_ contains the label strings [A,B,C] and we want to replace them with [0,1,2]. Then we can do the following,

    mapping = {'A':0, 'B':1, 'C':2}
    df.replace({'Labels': mapping})