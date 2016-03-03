**_This page is obsolete. Latest version is at https://github.com/hit-moodle/anti_plagiarism/wiki_**

# Introduction #

This plugin works as a block. It can detect cheating in programming assignments. Also support html and plain text files. The core engine is [MOSS](http://theory.stanford.edu/~aiken/moss/).

It works in both Linux and Windows (cygwin with perl required).

中文用户还可以使用duplication做为评判核心，支持doc、pdf和txt文件的中文文本雷同检测。

# Features #

  * Support moodle assignment types include: upload, uploadsingle and onlinejudge
  * Support C, C++, Java, C#, Python, Visual Basic, Javascript, FORTRAN, ML, Haskell, Lisp, Scheme, Pascal, Modula2, Ada, Perl, TCL, Matlab, VHDL, Verilog, Spice, MIPS assembly, a8086 assembly, a8086 assembly, MIPS assembly, HCL2, HTML and ASCII text.
  * Unrar and unzip automatically
  * Use different parameters to detect the same assignment and merge results
  * Confirm manually by teacher
  * Students can see their own confirmed results only
  * Translation: English and Simplified Chinese

# How to get #

See AntiPlagiarismInstallation

# TODO #

  * Backup and restore. Now it can't backup the results
  * Show progress bar when using duplication
  * Better result view UI
  * online assignment type support
  * Code clean-up

# Screenshot #

![http://sunner-projects.googlecode.com/svn/trunk/screenshots/anti-plagiarism.jpg](http://sunner-projects.googlecode.com/svn/trunk/screenshots/anti-plagiarism.jpg)