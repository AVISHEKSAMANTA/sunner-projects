**_This page is out of date. For latest info click https://github.com/hit-moodle/onlinejudge/wiki_**

# Installation #
## 1. Download Online Judge ##

Download from http://code.google.com/p/sunner-projects/downloads/list

Untar and put onlinejudge/ into mod/assignment/type/

## 2. Make sandbox ##
**_Only Linux users need to do this step. Windows users skip to next step._**

Requirement: Linux 2.6.x, gcc 4.x and make

In mod/assignment/type/onlinejudge/sandbox/, run:
```
make
```

## 3. Configure ##
**_Users who want to use ideone.com should do this step. Windows users must use ideone.com_**

Requirement: php with soap module

  1. register here: http://ideone.com/account/register
  1. After activation, login and set **API password** here: http://ideone.com/account/
  1. Open config.php and add the following lines:
```
$CFG->assignment_oj_ideone_username = 'change_me_to_ideone_username'; 
$CFG->assignment_oj_ideone_password = 'change_me_to_ideone_API_password'; 
```
## 4. Apply ##

  1. Login moodle as admin
  1. Access http://site.domain.name/admin/index.php
  1. Follow the instructions shown by above url

## 5. Make Judge Work ##

There are two recommended routines to make the judge work. The first is the most recommended but it works in Linux only.

### 5.1. Create Judge Daemon Through Cron ###

**_(Linux only)_**

Setup moodle's cron job to be called by php cli. In crontab, put a command which is similar with:

```
php -q /PATH/TO/MOODLE/admin/cron.php
```

That's all! Read http://docs.moodle.org/en/Cron for detail about how to setup moodle cron job triggered by **php cli** (Not wget, curl and etc.).

If it works, a judge daemon would be created. Use

```
ps -FC php
```

to ensure the daemon is running.

### 5.2. Create Judge Daemon in Command Line ###

If you can **NOT** trigger cron through php cli or are using Windows, then use this method.

#### In Linux ####

Run the following command to create judge daemon:

```
sudo -u APACHE-USER php /PATH/TO/MOODLE/mod/assignment/type/onlinejudge/judged.php
```

The APACHE-USER means the username of apache in your system. It is _www-data_ in debian, _apache_ in fedora. Perhaps _`ps aux|grep apache`_ or _`ps aux|grep httpd`_ can help you getting the correct username.

Use

```
ps -FC php
```

to ensure the daemon is running.

#### In Windows ####

Run the following command to create judge daemon:

```
C:\PHP\php.exe \PATH\TO\MOODLE\mod\assignment\type\onlinejudge\judged.php
```

Make sure the current user has the permission to access moodle code and files in moodledata.

# Upgrade #

  1. Overwrite the directory, onlinejudge/, with latest version.
  1. Repeat step 2-4 in Installation
  1. Routine 5.1 can apply the upgrade automatically.
  1. If you are using routine 5.2, kill the existing daemon and do the routine again.

# Usage #

The same as other standard assignment types. Follow its inline help.

# FAQ #

See [OnlineJudgeFAQ](OnlineJudgeFAQ.md)