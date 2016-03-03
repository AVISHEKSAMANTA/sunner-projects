**_This page is out of date. For latest info click https://github.com/hit-moodle/onlinejudge/wiki_**

# Introduction #

This plugin is designed for courses involving programming. It can automatically grade programming assignments by testing the submissions by customizable test cases ([ACM-ICPC](http://en.wikipedia.org/wiki/ACM_International_Collegiate_Programming_Contest)/[Online Judge](http://en.wikipedia.org/wiki/Online_judge) style).
# Features #

This plugin inherent Moodle's standard assignment type, uploadsingle . So it gets all uploadsingle functions and has its own additional features:

  * Support both Linux and Windows.
  * Run C/C++ code locally in sophisticated [libsandbox](http://sourceforge.net/projects/libsandbox/) environment to prevent attacks (e.g. rebooting system, accessing files/network, consuming/occupying system resources). (Linux only)
  * Run C/C++, Java, C#, Python, php, schema and other 40+ languages remotely in http://ideone.com. It is safe and free. See http://ideone.com/faq for full list of supported languages.
  * Different results (e.g. Accept, Wrong Answer, Presentation Error, Compilation Error, Time/Memory/Output Limit Exceed) get different grade.
  * Support multiply test cases.
  * Grade test cases separately. E.g., there are four cases and max grade of each is 25. The student pass three of them can get 25+25+25 = 75.
  * Customized feedback/hint can be shown to who doesn't pass the test.
  * Compile only mode.
  * Teachers can trigger rejudge of all submissions and grade manually anytime.
  * Support resubmit many times and one time submit.
  * More details (program output and etc.) can be shown to teachers.
  * Highlight code preview (powered by [SyntaxHighlighter](http://alexgorbatchev.com/wiki/SyntaxHighlighter)).
  * Easy installation, no root required.
  * Translation: English and Simplified Chinese

# How to get/use #

See OnlineJudgeInstallation

# Credits #

This project is sponsored by [School of Computer Science and Techonolgy](http://www.cs.hit.edu.cn), and [School of Software](http://software.hit.edu.cn) in [HIT](http://www.hit.edu.cn).

This plugin learned and copied much from arkaitz.garro(AT gmail.com)'s [program (or called epaile) assignment type](http://cvs.moodle.org/contrib/plugins/mod/assignment/type/program/) which has stopped developing since 2007.

Other contributors:
  * 施兴 (paradisehit AT gmail.com) designed and implemented the prototype.
  * 刘禹 (pineapple.liu AT gmail.com）gave much help and advices.
  * 刘琦卿 (lqq0205 AT foxmail.com) contributed many codes.

# TODO #

  * Backup and restore. (Waiting for Moodle 2.0)
  * Better test case management UI

# Screenshot #

![http://sunner-projects.googlecode.com/svn/trunk/screenshots/online_judge.jpg](http://sunner-projects.googlecode.com/svn/trunk/screenshots/online_judge.jpg)