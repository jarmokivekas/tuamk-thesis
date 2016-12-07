

This repository contains material related to Jarmo Kivekäs' thesis work at Turku University of Applied Sciences.





# Compiling documentation

Much of the work is documented in either markdown (.md) files or Jupyter notebooks (.ipynb). Some parts of the manuscript are written in plain LaTeX (.tex) files. Browsing [this repository on github](https://github.com/jarmokivekas/tuas-thesis) will automatically render markdown files and jupyter notebooks in a fairly reasonable manner.

Use the Makefile in the `/doc` directory to compile a pdf version of the thesis manuscript:

    > cd doc
    > make



# Meta

This section contains cryptic notes that did not have a good place to be jotted down.

use the command

    \rule{\textwidth}{\textheight}

to make a text body sized box

## tools

All the tools that are needed are listed in .travis.yml.

The output of Travis is quite technical, but it does define an environment where the manuscript should be guaranteed to build.


## tool versions



 - os: Ubuntu 16.04

 - pandoc:
        pandoc 1.16.0.2
        Compiled with texmath 0.8.4.1, highlighting-kate 0.6.1

 - pdflatex:
        pdfTeX 3.14159265-2.6-1.40.16 (TeX Live 2015/Debian)
        kpathsea version 6.2.1
