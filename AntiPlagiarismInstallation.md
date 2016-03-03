**_This page is obsolete. Latest version is at https://github.com/hit-moodle/anti_plagiarism/wiki_**

# Requirement #
  * Moodle 1.9.x
  * perl in Linux or cygwin in Windows

# DOWNLOAD #

Download from http://code.google.com/p/sunner-projects/downloads/list

# Installation #

  1. Untar downloaded file and put anti\_plagiarism/ into MOODLE\_HOME/blocks/
  1. Login moodle as admin
  1. Access http://site.domain.name/admin/index.php
  1. Follow the instructions shown by above url

# Configure #

Follow [MOSS's instruction](http://theory.stanford.edu/~aiken/moss/) to get the submission script and free account (the registration email must be sent in **PLAIN TEXT** format, otherwise moss won't reply).

## For Linux users ##
Save the script and make sure it is runnable and works (the script has plenty of comments tell the usage). Go to moodle's admin->Modules->Blocks->Anti-Plagiarism and Input the full path (include file name).

## For Windows users ##
First, you must install cygwin (http://www.cygwin.com/) and its perl packages which are required by moss.

Second, save the moss script somewhere and name it moss.pl

Third, create a text file named moss.bat and put the following code into it (change the upper case words into your correct path and do **NOT** change the direction of slashes):

`@C:\PATH\TO\CYGWIN\bin\perl.exe /cygdrive/DRIVE_LETTER/PATH/TO/MOSS_SCRIPT/moss.pl %*`

Finally, Go to moodle's admin->Modules->Blocks->Anti-Plagiarism and Input the full path of moss.bat (include file name).

## For Chinese users ##

moss脚本会检查源代码是否是文本，并把中文当作非文本，从而使提交失败。所以，需要打补丁。方法是在脚本中搜索"not a text file"，共两处。把这两行代码都注释掉。

Duplication是一个中文报告抄袭检测引擎，想了解或使用它的用户请联系Car(http://ir.hit.edu.cn/~car/)。

# Usage #

Add an instance of this block in your course page and click the assignment name (if any) in it. Follow the interface to trigger MOSS and judge plagiarism. If you have any question about the interface, just click the question mark icon and read the inline help.

# Debug #

Login as admin. Go to "site administration->server->debugging", set "debug messages" as "DEVELOPER", and enable "Display debug message". The block will output more details about its execution. Use these info to debug external script problem.