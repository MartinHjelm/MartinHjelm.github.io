---
layout: post
title: How to clear the terminal buffer
---
Sometimes you wan to start over in the terminal. On OSX on you Mac there is a convient shortcut: cmd+k. This will clear your scroll buffer. In Ubuntu there is no such short cut. What you can do clear and reset the scroll-back is to write

    clear && printf '\e[3J'

Of course we can add an alias to our .bashrc so that we can just write, for example, ccc

    alias ccc="clear && printf '\e[3J'"

