---
layout: post
title: Ubuntu Terminal Open Command
---
On OSX one can use the *open* command in the terminal to open a document using its associated program. Running open on a pdf file will open it using Preview. On Ubuntu the corresponding command is *xgd-open*. It is cumbersome to write that over and over again but we can add an alias in the .bashrc file 

    alias o="xdg-open"

If we, for example, want to open a pdf file we can write 
    
    o mydocument.pdf

