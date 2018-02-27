---
layout: post
title: Terminal Search For Non-Ascii Characters
---

Sometimes compilers of all sorts gives you trouble for non-ascii characters usually without no feedback as to where in the code they are located. One can then do a directory or file search for the pesky non-ascii characters. I found this discussion on [Stack Overflow](https://stackoverflow.com/questions/3001177/how-do-i-grep-for-all-non-ascii-characters-in-unix). What you do is a grep with regular expression that captures all non-ascii characters. To do this over for example your _site_ directory like this, 

    grep --color='auto' -P -n '[^\x00-\x7F]' _site/*

or on OSX

    pcregrep --color='auto' -n "[^\x00-\x7F]" _site/* 

Or you can just do a regular expression search for [^\x00-\x7F] in your favorite editor.