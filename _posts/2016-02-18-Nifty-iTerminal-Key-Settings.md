---
layout: post
title: i-Term Keyboard Shortcuts for Jumping Words 
---
In i-Term under preferences -> profiles -> keys we can set a number of useful key short cuts. 

To delete one word backwards using a non-alphanumeric character as the delimiter we set,

**alt+backspace:** Hexcode: 0x1B 0x08

That is, using alt+backspace on,

    /usr/bin/python

will remove,
    
    python
    bin
    usr
    /

For jumping one word backwards or forwards with the left and right arrowkeys  using a non-alphanumeric character as the delimiter, we use, 

**Alt + left:** Send Escape Sequence: Esc + b

**Alt + right:** Send Escape Sequence: Esc + f

That is, using alt + left on,

    /usr/bin/python

will jump,
    
    python
    bin
    usr
    /