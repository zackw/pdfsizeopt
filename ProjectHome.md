_pdfsizeopt_ is a program for converting large PDF files to small ones. More specifically, pdfsizeopt is a free, cross-platform command-line application (for Linux, Mac OS X, Windows and Unix) and a collection of best practices to optimize the size of PDF files, with focus on PDFs created from TeX and LaTeX documents. pdfsizeopt is written in Python, so it is a bit slow, but it offloads some of the heavy work to its faster (C, C++ and Java) dependencies. pdfsizeopt was developed on a Linux system, and it depends on existing tools such as Python 2.4, Ghostscript 8.50, jbig2enc (optional), sam2p, pngtopnm, pngout (optional), and the Multivalent PDF compressor (optional) written in Java.

See the [InstallationInstructions](InstallationInstructions.md).

See PDF files _pdfsizeopt_ was tested with on [ExamplePDFsToOptimize](ExamplePDFsToOptimize.md).

A [white paper](https://dl.getdropbox.com/u/635918/pts_pdfsizeopt2009.psom.pdf) (and its [local copy](http://pdfsizeopt.googlecode.com/files/pts_pdfsizeopt2009.psom.pdf)) and some [talk slides](https://dl.getdropbox.com/u/635918/pts_pdfsizeopt2009_talk.psom.pdf) (and their [local copy](http://pdfsizeopt.googlecode.com/files/pts_pdfsizeopt2009_talk.psom.pdf)) have been prepared for EuroTeX 2009 about how _pdfsizeopt_ works, and how _pdfsizeopt.py_ can be customized.

Doesn't _pdfsizeopt_ work with your PDF? [Report the issue](http://code.google.com/p/pdfsizeopt/issues/entry?template=Cannot%20optimize%20PDF)