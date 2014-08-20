gsidiag_bin2txt
===============

Overview
--------
This is a simple tool for generating statistics table for Gridpoint Statistical Interpolation (GSI) radiance diagnostic (hereafter 'diag') files

Install
-------
First, you must run ./configure .  This script will prompt you for your fortran compiler, fortran flags, and your GSI source directory.  You **really** should specify the GSI source directory, but by default, it will set the directory to src/gsi_files directory, which corresponds to GMAO GEOSadas 5.13. 

After running ./configure, a Makefile.inc will be generated.  You can then simply type 'make' to compile.

Execution
---------
Once you are compiled, you can simply type:
`./gsidiag_bin2txt.x diagfile.bin`
and it will return a diagfile.txt.  Some running options are available via the file's namelist, and you should read gsidiag_bin2txt.nl.README for information on that.

Contact Info
------------
This was written by Will McCarty at the GMAO/GSFC.  If you have any questions, feel free to email at his NASA address ([available here](http://gmao.gsfc.nasa.gov/personnel.php)).  

