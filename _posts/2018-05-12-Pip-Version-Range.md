---
layout: post
title: Pip Downgrading or Upgrading a Package to a Version Range
---

I was upgrading all Python packages and it turned out that the Flake8 package used for linting my Python code needed an older version of the PyCodeStyle package. To fix this, instead of downgrading, one can use the range requirement for pip.

    pip install 'pycodestyle<2.4.0,>=2.0.0'

That is, install a pycodestyle version lesser than version 2.4.0 but greater or equal to version 2.0.0. Pretty neat.