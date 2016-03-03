**_This page is out of date. For latest info click https://github.com/hit-moodle/onlinejudge/wiki_**

# Why a simple program gets the result: restricted function #

In the installation step 2, make sandbox, use "make policy1" instead of "make" and resubmit the assignment.

If the problem is still there, use "make policy2" and resubmit.

If the problem is still there, do the following:

```
uname -a
gcc -v
cd /path/to/moodle/mod/assignment/type/onlinejudge/
./languages/c.sh simple.c a.out   #use ./languages/cpp.sh for C++ code
./sandbox/sand a.out              # Your program will run or be broken by sandbox
echo $?
```

Ensure that the last command output 2, run your program as:

```
strace ./a.out
```

Send simple.c, a.out and the output of all the above commands to sunner@gmail.com . I can make a special patch for your system.

# Why pending forever #
  1. Check whether the judge daemon is running. The process's name should be php or php.exe
  1. If the daemon quits by itself, check your PHP log (default to syslog or Windows NT events log) for detail error messages.


# What the difference between local sandbox and ideone.com #

OJ currently supports two kinds of judge engine: local sandbox and ideone.com. The following table describes the difference.

|**Judge**|**Supported OSes**|**Internet**|**Speed**|**Languages**|**Limits**|**Safe**|
|:--------|:-----------------|:-----------|:--------|:------------|:---------|:-------|
|Local sandbox|Linux only        |Not required|Depends on your server load. Normally faster than ideone.com|C/C++ only   |No        |Yes, but it depends on the sandbox|
|ideone.com|Linux & Windows   |Required    |Depends on the internet conection and ideone.com's load.|40+          |1000 submissions/month|Sure, no submissions will be executed on your server|

# What the difference between Linux and Windows for OJ #

Since the developers are using Linux, OJ supports Linux better. We did only a few testing under Windows.

And, Windows doesn't support all the features we provide. See [OnlineJudgeFAQ#What\_the\_difference\_between\_local\_sandbox\_and\_ideone.com](OnlineJudgeFAQ#What_the_difference_between_local_sandbox_and_ideone.com.md) for details.