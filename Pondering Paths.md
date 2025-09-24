# 1. THE ROOT
This module teaches about absolute path and how it is represented in a file system. Absolute path always begins with "/". followed by the directories name.

# Flag

**MY FLAG**  : `pwn.college{4obo98vHm_KZGne8Dm5VHGhYUEH.QX4cTO0wSM0EzNzEzW}`

# Solution

Type in the /pwn to execute function where /pwn is its absolute path.

``` 
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{4obo98vHm_KZGne8Dm5VHGhYUEH.QX4cTO0wSM0EzNzEzW}

```

# 2. PROGRAM AND ABSOLUTE PATH

The main objective of this module is to run the challenge program by invoking its absolute path.

# Flag

My flag: `pwn.college{g4oOYYX65xptjLNJjeB-0nUWQl6.QX1QTN0wSM0EzNzEzW}`

# Solution

The path to the challenge directory is  `/challenge`. The name of the challenge program in this level is run, and it lives in the `/challenge`] directory. Thus, the path to the `run` challenge program is `/challenge/run`.

```
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{g4oOYYX65xptjLNJjeB-0nUWQl6.QX1QTN0wSM0EzNzEzW}

```


# 3. POSITION THY SELF 

The major objective of this module is to explain about navigation through different directories in the Linux filesystem.

# FLAG

My flag ~ `pwn.college{MQcNoYjqeD1DKJVIqqEiQZgWHce.QX2QTN0wSM0EzNzEzW}`

# SOLUTION 

The challenge instructs you to execute /challenge/run.
This will give you an absolute path where you have to rerun the /challenge/run program. You can change directories using cd command.

```
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /usr/aarch64-linux-gnu/include/gnu directory.
Please use the cd utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /usr/aarch64-linux-gnu/include/gnu
hacker@paths~position-thy-self:/usr/aarch64-linux-gnu/include/gnu$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{MQcNoYjqeD1DKJVIqqEiQZgWHce.QX2QTN0wSM0EzNzEzW}

```
# What i learnt

You can change directories using command "cd"



# 4. POSITION ELSE WHERE

The major objective of this module is to explain about navigation through different directories  in Linux filesystem.


# FLAG

My flag ~ `pwn.college{MFbbZL_WKBDZ0oWJmyDR1qJTiv8.QX3QTN0wSM0EzNzEzW}`

# SOLUTION 

The challenge instructs you to execute /challenge/run.
This will give you an absolute path where you have to rerun the /challenge/run program. You can change directories using command cd.

```
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /usr/include directory.
Please use the cd utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /usr/include directory
bash: cd: too many arguments
hacker@paths~position-elsewhere:~$ cd /usr/include
hacker@paths~position-elsewhere:/usr/include$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{MFbbZL_WKBDZ0oWJmyDR1qJTiv8.QX3QTN0wSM0EzNzEzW}

```

# What I learnt.

You can change directories using command "cd"



# 5. POSITION YET ELSE WHERE

The major objective of this module is to explain about navigation through different directories in Linux filesystem.

# FLAG

My flag ~ `pwn.college{UCflrOaNMVHan6lvHdNBHXPjheX.QX4QTN0wSM0EzNzEzW}`

# SOLUTION 

The challenge instructs you to execute /challenge/run.
This will give you an absolute path where you have to rerun the /challenge/run program. You can change directories using command cd.


```
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /tmp directory.
Please use the cd utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /tmp
hacker@paths~position-yet-elsewhere:/tmp$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{UCflrOaNMVHan6lvHdNBHXPjheX.QX4QTN0wSM0EzNzEzW}

```

# What i learnt

You can change directories using command "cd"



# 6. IMPLICIT RELATIVE PATH FROM /

The major objective of  this challenge is to understand the concept of relative path

# FLAG

My flag ~ ` pwn.college{sxEJMAlxDlI8XFEs6HzVehQNc7k.QX5QTN0wSM0EzNzEzW}`

# SOLUTION

run `/challenge/run` using a relative path while having a current working directory of `/`

```
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{sxEJMAlxDlI8XFEs6HzVehQNc7k.QX5QTN0wSM0EzNzEzW}

```
# What i learnt.

A relative path is any path that does not start at root.
A relative path is interpreted relative to your current working directory.
Your cwd is the directory that your prompt is currently located at.



# 7. EXPLICIT RELATIVE PATH FROM /

This module teaches us about explicit relative paths.

# FLAG

My flag ~ `pwn.college{w_uPjjsixOfg12CBP_9Dy_lDW9U.QXwUTN0wSM0EzNzEzW}`

# SOLUTION 

Change your directory to '/' using cd command. And then execute ./challenge/run to obtain your flag.

```
hacker@paths~explicit-relative-paths-from-:/challenge$ cd ..
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{w_uPjjsixOfg12CBP_9Dy_lDW9U.QXwUTN0wSM0EzNzEzW}

```


# What i learnt 

In most operating systems, including Linux, every directory has two implicit entries that you can reference in paths: `.` and `..` 



# 8. IMPLICIT RELATIVE PATH

The major objective of this challenge is to teach you about implicit relative path.

# FLAG 

My flag ~ `pwn.college{8kSqvheV2rg_UAgZnn54Tliud4J.QXxUTN0wSM0EzNzEzW}`

# SOLUTION

change directory to  /challenge using cd command and execute run command using relative path '/run'

```
hacker@paths~implicit-relative-path:/challenge$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{8kSqvheV2rg_UAgZnn54Tliud4J.QXxUTN0wSM0EzNzEzW}

```


# WHAT I LEARNT

Linux searched the current directory for programs every time you entered a naked path, you could accidentally run programs in your current directory that happened to have the same names as core system utilities! As a result, the above commands will give the following error:

```
bash: run: command not found
```



# 9. HOME SWEET HOME


# FLAG

My flag ~ `pwn.college{sLidS6jLPcFedhizLatLqXGm1Ea.QXzMDO0wSM0EzNzEzW}`

# SOLUTION

```
hacker@paths~home-sweet-home:~$ /challenge/run ~/f
Writing the file to /home/hacker/f!
... and reading it back to you:
pwn.college{sLidS6jLPcFedhizLatLqXGm1Ea.QXzMDO0wSM0EzNzEzW}

```

# What i learnt 

```console
hacker@dojo:~$
```

Bash provides and uses this shorthand because, again, most of your time will be spent in your home directory. Thus, whenever bash sees `~` provided as the start of an argument in a way consistent with a path, it will expand it to your home directory.

echo LOOK: ~ command can be used to know your current directory.
