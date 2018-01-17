---
layout: post
title: How To Easily Find The Clipping Parameters For A Figure In Latex
---
You are in Latex setting up a figure and you want only part of it. Then you can use the clipping parameters of the `includegraphics` command. Like this,

    \begin{figure}
    % l b r t
    \centering
    \includegraphics[width=1.\linewidth,clip,trim=280 225 180 190]{mypic.png}
    \caption{Beautiful Picture.}
    \end{figure}

where `trim=280 225 180 190` is the clipping margins as `[left,bottom,right,top]` or `[l,b,r,t]`. 

This can be a tricky endavour since we have to do trial and error to see how much we should remove to get it right. It is often difficult to see the difference between the figure background and document if they have the same background color. However, if we put a fram around the figure we can better estimate how much space is left to the margin. This can be done by using the package,

    \usepackage[export]{adjustbox}

We can then do,

    \begin{figure}
    % l b r t
    \centering
    \includegraphics[width=1.\linewidth,clip,trim=280 225 180 190,frame]{mypic.png}
    \caption{Beautiful Picture.}
    \end{figure}

to see how much space is left. I have found this extremly useful for pdfs that are exported from Keynote since there is no clipping function in the program. 





