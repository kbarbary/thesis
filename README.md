Thesis
======

My 2011 UC Berkeley PhD thesis on Type Ia supernova rates.

Thesis class
------------

This thesis is based on the widely available 'ucthesis' class.  It is
even in some package management systems. Here I'm using a version
updated by Kevin Young in March 2010 to follow the UC thesis
requirements as of November 2009. It is available here:

http://www.cchem.berkeley.edu/kbwgrp/index.php/People/KevinYoung

I've redistributed it here, with the following modifications made to 
`ucthesis.cls`:

* Remove the numbering from the reference list.
* Define `\abovecaptionskip` and `\belowcaptionskip`, necessary for the
  sidecap package.
* Define a `footnotesizetabular` environment for footnotesize tables.
* Redefine chapter heading font.


Bibliography
------------

For the bibliography, I use the Astrophysical Journal BibTeX style, 
included in `apj/apj.bst`. This style file uses abbrviations not defined in 
the file `apj.bst`. I've included the abbreviations in a stand-alone package
apjabbrev, included in `apj/apjabbrev.sty`. 


Configuring LaTeX
-----------------

To get LaTeX to look in these subdirectories (first) for the class
files, be sure to include `.//` in your `TEXINPUTS` and `BSTINPUTS`
environment variables. The `//` tells LaTeX to look in
subdirectories. For example, if your shell is BASH, include these
lines in your `.bashrc` file:

```
export TEXINPUTS=.//:$TEXINPUTS
export BSTINPUTS=.//:$BSTINPUTS
```

Additional packages
-------------------

Additionally, the following standard LaTeX packages are required:

* amssymb
* color
* graphicx
* natbib
* times
* hyperref
* fancyhdr
* ccaption
