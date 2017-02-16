---
layout: post
title: Concatenating files horizontally
---
Lets say you have a set of text files that contains column entry data, for example a set of csv files, or text files. Each row in each of the csv files contains data entries relating to the same instances. We would like to concatenate all the csv files into one csv file. We can do this in the terminal using the _paste_ command, like this,

    paste file1.csv file2.csv | column  > X.txt
    
If we want to remove the , ; \t or anuy other character that usually separates csv files we can tell _column_ to create a table separated by white space. Suppose the data in our csv files are separated by ; we can do 

     paste file1.csv file2.csv | column -s ';' -t > X.txt

Somtimes this generates an error since the paste command can only handle 512 character long lines(if I remember it correctly). A better approach is to use this script which I found on StackOverflow

    awk '{if ((getline a < "-") > 0) $0 = $0 ";" a; print}' f1.csv < f2.csv > fconcat.csv

where ; is the separator for the csv file. 