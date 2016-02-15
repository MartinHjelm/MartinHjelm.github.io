---
layout: post
title: How to generate a beep in Python using Numpy
---
It is a simple as this,

    import numpy as np
    import sounddevice as sd
    from scipy import signal
    Nt = 50000
    t = np.linspace(0, 1, Nt)
    sd.play(signal.square(75 * t))
    
There is a bunch of other signal generating functions that could be fun to play around with.
