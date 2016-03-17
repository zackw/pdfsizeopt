# Installation instructions for Windows #

## Installation ##

(For quick installation of pdfsizeopt to Linux and FreeBSD systems, please see [InstallationInstructionLinux](InstallationInstructionLinux.md), and for slow installation on any system, please see [InstallationInstructions](InstallationInstructions.md) instead.)

Please note that pdfsizeopt has many dependencies, but all these dependencies are conveniently bundled to a large .zip file (`pdfsizeopt_win32-v3.zip` below) for easy installation on Windows.

  1. Create directory `C:\pdfsizeopt` (If you wish, you can also create it on another drive or with a different name -- but it won't work if there is whitespace in any pathname component.)
  1. Download http://bin.pdfsizeopt.googlecode.com/git/pdfsizeopt_win32bin-v3.zip and extract its contents to `C:\pdfsizeopt`. This will create e.g. `C:\pdfsizeopt\pdfsizeopt.exe`, `C:\pdfsizeopt\sam2p.exe` etc.
  1. Download the latest `http://pdfsizeopt.googlecode.com/git/pdfsizeopt.single` and save it as `C:\pdfsizeopt\pdfsizeopt.py`.
  1. Optionally, add C:\pdfsizeopt to the (end of the) system path.

## Usage ##

pdfsizeopt is a command-line only application, there is no GUI. You can run pdfsizeopt by opening a command-prompt window (e.g. by Start menu / Run / `cmd.exe`), and typing commands there.

Since you have to type the input filename as a full pathname, it's recommended to create a directory with a short name (e.g. `C:\pdfs`), and copy the input PDF there.

To optimize a PDF, run the following command in a command-prompt window:

```
C:\pdfsizeopt\pdfsizeopt C:\pdfs\input.pdf
```

(Press **Tab** to get filename completion while typing.)

The optimized file will be saved as `C:\pdfs\input.psom.pdf` (or as `C:\pdfs\input.pso.pdf` is `pdfsizeopt --use-multivalent=no` is used).

To avoid typing `C:\pdfsizeopt\pdfsizeopt`, add `C:\pdfsizeopt` to the (end of the) system path, and open a new command-prompt window. You can type just `pdfsizeopt` instead there.

Please note that `pdfsizeopt` works perfectly in Wine (tested with wine-1.2 on Ubuntu Lucid), but it's a bit slower than running it natively (as a Linux or Unix program).