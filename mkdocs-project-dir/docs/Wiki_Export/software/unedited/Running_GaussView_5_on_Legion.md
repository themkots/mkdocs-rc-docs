---
title: Running GaussView 5 on Legion
layout: docs
---
GaussView 5.0.8 is available on Legion and currently can be used on the
login nodes. GaussView is a graphical tool to help prepare input for
submission to Gaussian and to examine graphically the output from
Gaussian jobs. Job submission directly from GaussView is not possible,
instead save molecular structures as Gaussian input files and submit in
the normal way for Gaussian jobs.

Access to GaussView is enabled by a module file and being a member of
the appropriate reserved application group. Please email rc-support AT
ucl.ac.uk to get your userid added to the G09 group.

As GaussView uses the X Window System to display its graphical user
interface, the computer you are logging in to Legion from must be
running X and your ssh session must have X tunnelling enabled. From a
Linux/Unix workstation use an ssh command of the form: ```

`ssh -X your_userid@legion.rc.ucl.ac.uk`

``` If you use Windows then you can use the Exceed X server. UCL has
a site licence for Exceed and it's available for download from the [UCL
Software Database](http://swdb.ucl.ac.uk/).If you use a Mac then you can
either use Apple's supplied X11 application or the better open source
alternative [XQuartz](http://xquartz.macosforge.org/trac/wiki).

Before you can run GaussView interactively you need to load the G09
module and run an initialisation script using: ```

`module load gaussian/g09_a02/pgi`  
`. $g09root/g09/bsd/g09.profile`

``` You can use: ```

`module list`

``` to check that the module is loaded. Output should look similar
to this: ```

`Currently Loaded Modulefiles:`  
`  1) ucl                          6) nedit/5.6`  
`  2) compilers/intel/11.1/072     7) mrxvt/0.5.4`  
`  3) mkl/10.2.5/035               8) rcops/1.0`  
`  4) mpi/qlogic/1.2.7/intel       9) gaussian/g09_a02/pgi`  
`  5) sge/6.2u3`

``` You can now run GaussView using: ```

`gview &`

``` For more information about using GaussView see the [GaussView 5
Reference Manual](http://www.gaussian.com/g_tech/gv5ref/gv5ref_toc.htm)
on the Gaussian web site.

[Category:Bash script pages](Category:Bash_script_pages "wikilink")
[Category:Legion](Category:Legion "wikilink")