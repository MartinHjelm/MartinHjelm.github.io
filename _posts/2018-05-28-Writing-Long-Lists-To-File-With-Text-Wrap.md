---
layout: post
title: Writing Long Lists to File in Python With Enforced Line Length
---
I had a long array of numbers that I wanted to write to file such that the numbers would be comma separated and with a line break at 80 chars. I tried with numpy savetxt but there is always a problem with it so I resorted to the textwrap library.

    import numpy as np
    import textwrap
    long_arr = np.array([1, 2, 3, ...., n])
    long_str = 'long_arr = [' + ', '.join(long_arr.astype(str)) + ']'
    print(textwrap.fill(long_str, 80), file=open('long_arr.txt','w'))
