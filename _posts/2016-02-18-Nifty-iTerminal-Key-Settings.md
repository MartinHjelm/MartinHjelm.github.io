---
layout: post
title: Nifty i-Term Key Settings
---
This short-cut will delete one word backwards using a non-alphanumeric character as the delimiter.

    alt+backspace hex: 0x1B 0x08

That is, using alt+backspace on,

    /usr/bin/python

will remove,
    
    python
    bin
    usr
    /

For jumping one word backwards or forwards using a non-alphanumeric character as the delimiter, we can use, 

Alt + left: Send Escape Sequence, Esc + b
Alt + right: Send Escape Sequence, Esc + f

That is, using alt+left on,

    /usr/bin/python

will jump,
    
    python
    bin
    usr
    /