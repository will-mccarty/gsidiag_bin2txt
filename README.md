gsidiag_bin2txt
===============

THIS DISTRIBUTION HAS BEEN INCORPORATED INTO PyRadmon, [available here](https://github.com/alberthdev/pyradmon).  This repo is out-of-date.

Overview
--------
This is a simple tool for generating statistics table for Gridpoint Statistical Interpolation (GSI) radiance diagnostic (hereafter 'diag') files

Install
-------
First, you must run `./configure`.  This script will prompt you for your fortran compiler, fortran flags, and your GSI source directory.  You **really** should specify the GSI source directory, but by default, it will set the directory to `src/gsi_files` directory, which corresponds to GMAO GEOSadas 5.13. 

After running `./configure`, a `Makefile.inc` will be generated.  You can then simply type `make` to compile.

Execution
---------
Once you are compiled, you can simply type:
`./gsidiag_bin2txt.x diagfile.bin`
and it will return a diagfile.txt.  Some running options are available via the file's namelist, and you should read gsidiag_bin2txt.nl.README for information on that.

### Example 
Included with the package is one example file.  Once you have an executable, you can test it by running:

`./gsidiag_bin2txt.x example_data/x0014_so14.diag_amsua_n18_ges.20140201_00z.bin`

This should generate:

`example_data/x0014_so14.diag_amsua_n18_ges.20140201_00z.txt`

After this is generated, you can compare against:

`example_data/x0014_so14.diag_amsua_n18_ges.20140201_00z.txt.OUT`

and hopefully you should get a zero-diff result.  The .OUT file is included with the distribution.

Contact Info
------------
This was written by Will McCarty of the Global Modeling and Assimilation Office at NASA Goddard Space Flight Center.  If you have any questions, feel free to contact him via the information [available here](http://gmao.gsfc.nasa.gov/personnel.php).  

