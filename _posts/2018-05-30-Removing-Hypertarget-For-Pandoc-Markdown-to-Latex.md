---
layout: post
title: Removing Hypertarget For Sections When Converting Markdown to Latex Using Pandoc
---
When converting Markdown to Latex using Pandoc 2 it puts hypertarget markers on each section like this,

    \hypertarget{my-chapter}{
    \section{My Chapter}\label{my-chapter}}

This can get annoying if you already defined a label or you have several sections named the same thing. For example, I have a document that have several input files each with the same section name and I convert them separately. This creates a lot of confusion and warnings when rendering to a pdf. Fortunatley it can be fixed by writing `markdown-auto_identifiers` instead of just `markdown`. The conversion becomes, 

    pandoc my_file.md -f markdown-auto_identifiers -t latex -o my_file.tex
