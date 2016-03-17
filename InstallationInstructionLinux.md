# Installation instructions for Linux #

## Installation ##

(For quick installation of pdfsizeopt to Windows systems, please see [InstallationInstructionWindows](InstallationInstructionWindows.md), and for slow installation on any system, please see [InstallationInstructions](InstallationInstructions.md) instead.)

Please note that pdfsizeopt has many binary dependencies, but all these dependencies are conveniently bundled to a ~14 MB .tar.gz file (` pdfsizeopt_libexec_linux-v1.tar.gz` below) for easy installation on Linux and FreeBSD.

Run these commands in a terminal window (without the leading `$`):

<pre>
$ mkdir pdfsizeopt.try<br>
$ cd pdfsizeopt.try<br>
$ wget -c \<br>
http://pdfsizeopt.googlecode.com/files/pdfsizeopt_libexec_linux-v1.tar.gz</pre><pre>
$ tar xzvf pdfsizeopt_libexec_linux-v1.tar.gz<br>
$ wget -O pdfsizeopt.py http://pdfsizeopt.googlecode.com/git/pdfsizeopt.single</pre>

Please note that `pdfsizeopt` works perfectly on any x86 and amd64 Linux system. There is no restriction on the libc, Linux distribution etc. because `pdfsizeopt` uses only its statically linked x86 executables, and it doesn't use any external commands (other than `pdfsizeopt` and `pdfsizeopt_libexec/*`) on the system. `pdfsizeopt` also works perfectly on x86 FreeBSD systems with the Linux emulation layer enabled.

## Usage ##

pdfsizeopt is a command-line only application, there is no GUI. You can run pdfsizeopt by opening a terminal window and typing commands there. The command includes the pathname to the `pdfsizeopt` binary and the input file name.

For example, to compress the sample lme\_v6.pdf file, run these commands in a terminal window (without the leading `$`):

<pre>
$ cd pdfsizeopt.try<br>
$ wget -c \<br>
http://pdfsizeopt.googlecode.com/files/lme_v6.pdf</pre><pre>
$ ./pdfsizeopt --use-pngout=no lme_v6.pdf<br>
$ ls -l lme_v6.pdf lme_v6.psom.pdf</pre>

Additional image compression is possible by removing `--use-pngout=no`, but that would make the whole process much slower, because _pngout_ is very slow.

It's possible to run `pdfsizeopt` from any directory. To do that, change the `./` in the command above to the name of the directory containing `pdfsizeopt` (and `pdfsizeopt_libexec`), or add the directory containing `pdfsizeopt` to your path. Please note that the `pdfsizeopt_libexec` directory and the `pdfsizeopt.py` file must be always next to the `pdfsizeopt` executable.

It's possible to optimize a PDF outside the current directory. To do that, specify the pathname (including the directory name) in the command-line.

`pdfsizeopt` creates lots of temporary files (`pso.*`) in the currect directory. As of now, you have to clean up those files manually.

The output file name for `DIR/INPUT.pdf` is `DIR/INPUT.psom.pdf` (or `DIR/INPUT.pso.pdf` if `pdfsizeopt --use-multivalent=no` is used).