# Quick installation instructions #

To quickly install pdfsizeopt on Windows, see [InstallationInstructionWindows](InstallationInstructionWindows.md).

To quickly install pdfsizeopt on Linux or FreeBSD, see [InstallationInstructionLinux](InstallationInstructionLinux.md).

# Slow installation #

The remaining part of this page applies to Unix systems (e.g. Linux and Mac OS X).

Please note that not all the software mentioned in the instructions below is free software (if we consider freedom). Details:

  * pdfsizeopt: free
  * Python: free
  * Ghostscript: free version available
  * Java: free version available (OpenJDK)
  * sam2p: free
  * jbig2: free (http://github.com/agl/jbig2enc/tree/master)
  * png22pnm: free (http://sam2p.googlecode.com/files/tif22pnm-0.12.tar.gz)
  * pngtopnm: free (this is an replacement if you can't install png22pnm)
  * Multivalent.jar containing tool.pdf.Compress: not free software, don't use it if you don't have a license
  * PNGOUT: not free software, but you don't have to pay for using it, and you can download it from the official web site without having to pay

Necessary:

  1. A Unix system is needed, Linux is recommended, but it is reported to work on the Mac OS X as well. The following instructions have been tested on Debian Etch, Ubuntu Hardy and Ubuntu Lucid. See  also [InstallationInstructionWindows](InstallationInstructionWindows.md) for Windows (Win32).
  1. Install Python 2.4, Python 2.5, Python 2.6 or Python 2.7 from package. Earlier or later versions won't work.
  1. Install Ghostscript 8.61 or later (tested and found working with 8.61, 8.62, 8.63, 8.64, 8.71 and 9.06). Earlier versions won't work (You may try pdfsizeopt with Ghostscript 8.54 as well, but 8.54 has some known font conversion problems, so it will produce an error for some PDF files.) Make sure the command `gs` is on your `$PATH`.
  1. Create a directory named `pdfsizeopt`.
  1. Check out the source code at http://code.google.com/p/pdfsizeopt/source/checkout , or just download http://pdfsizeopt.googlecode.com/git/pdfsizeopt.py as `pdfsizeopt/pdfsizeopt.py`.
  1. Install a recent _sam2p_ and copy the binary to `pdfsizeopt/sam2p`. For Linux, the recommended binary is http://pdfsizeopt.googlecode.com/files/sam2p . For Mac OS X, the recommended binary is http://pdfsizeopt.googlecode.com/files/sam2p-darwin . Rename the downloaded file to _sam2p_, and move it to `pdfsizeopt/sam2p`. Please note that the sam2p in Ubuntu Intrepid and Debian Etch is too old. Either compile it yourself, or use the recommended download above.
  1. Install _png22pnm_ and copy the binary to `pdfsizeopt/png22pnm`. (As a replacement, you can install _pngtopnm_ instead from package. But please try installing _png22pnm_ first, because _sam2p_ works better with it.) For Linux, the recommended binary is http://pdfsizeopt.googlecode.com/files/png22pnm . For Mac OS X, the recommended binary is http://pdfsizeopt.googlecode.com/files/png22pnm-darwin . Rename the downloaded file to _png22pnm_, and move it to `pdfsizeopt/png22pnm`.

Optional, but strongly recommended:

  1. Download the official pdfsizeopt jbig2 binary (works on x86 and amd64, Linux version: http://pdfsizeopt.googlecode.com/files/jbig2.linux , Mac OS X version: http://pdfsizeopt.googlecode.com/files/jbig2.darwin) to `pdfsizeopt/jbig2`, or compile jbig2 for yourself.

Optional for Multivalent.jar (if in doubt, don't use it):

  1. Install Java 1.5 or newer from package. `javac` is not necessary. Sun's Java and OpenJDK are OK, gcj and gij and avian won't work. Make sure that `java -version` works and prints something at least 1.5.
  1. If you have a copy of `Multivalent*.jar` (e.g.  `Multivalent20060102.jar`), and you have a license to use it, then copy it to `pdfsizeopt/Multivalent.jar`.

Optional, but recommended:

  1. Download the PNGOUT binary for your system. Recommended for Linux: the http://static.jonof.id.au/dl/kenutils/pngout-20070430-linux-static.tar.gz archive on http://www.jonof.id.au/kenutils . For other PNGOUT downloads, visit http://advsys.net/ken/utils.htm . Copy the file `pngout-*-linux-static` to `pdfsizeopt/pngout`.

Try it:

  1. Create a file test.pdf, and run `pdfsizeopt.py --use-pngout=true --use-jbig2=true --use-multivalent=false test.pdf`. The output file will be `test.pso.pdf`.
  1. If you haven't installed some of the tools above, try changing `=true` to `=false` in the command line.