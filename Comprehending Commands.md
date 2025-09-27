#1. cat: not the pet, but the command! 

In this challenge, I will copy the flag to the `flag` file in your home directory (where your shell starts). Go read it with `cat`!

**Flag:** `pwn.college{8J29JA2F-QC0sC6YGgwNJl33m2s.QXwITO0wSM0EzNzEzW}`

command used: `cat flag`

The `cat` command reads out whatever is present in a given file. Running `cat` with a file called `flag` gave out the required flag. 


#2. catting absolute paths

In this directory, I will not copy it to your home directory, but I will make it readable. You can read it with `cat` at its absolute path: `/flag`.

**Flag:** ``pwn.college{oSY5gwDL7EHOQpdqK-tKX1jhLf5.QX5ETO0wSM0EzNzEzW}

command used: `cat /flag`
```
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{oSY5gwDL7EHOQpdqK-tKX1jhLf5.QX5ETO0wSM0EzNzEzW}
```

By using my knowledge of absolute file paths and knowing the functionality of the `cat` command, I used the above mentioned command to get the flag. 


#3. more catting practice 

In this level, I'll put the flag in some crazy directory, and I will not allow you to change directories with `cd`, so no `cat flag` for you. You must retrieve the flag by absolute path, wherever it is.


**Flag:** `pwn.college{8J29JA2F-QC0sC6YGgwNJl33m2s.QXwITO0wSM0EzNzEzW}`

command used: `cat /usr/lib/php/flag`

The challenge told me to look for the flag at `cat /usr/lib/php/flag`, so I specified the absolute path of the flag and passed it as an argument to the `cat` command to obtain the flag.
```
hacker@commands~more-catting-practice:~$ cat /usr/lib/php/flag
pwn.college{8J29JA2F-QC0sC6YGgwNJl33m2s.QXwITO0wSM0EzNzEzW}
```

#### What I learnt

You can pass absolute path as an argument in the `cat` command to read the contents of the given file. 


#4. grepping for a needle in a haystack 

In this challenge, I've put a hundred thousand lines of text into the `/challenge/data.txt` file. Grep it for the flag!


**Flag:** `pwn.college{AlOIgm8fQ067me3PLlkAk9Zn6ad.QX3EDO0wSM0EzNzEzW}`

command used: `grep "pwn.college" /challenge/data.txt`

```
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{AlOIgm8fQ067me3PLlkAk9Zn6ad.QX3EDO0wSM0EzNzEzW}
```

### What I learnt from this: 

This is how the grep command works: 
`grep <stuff to look > <where to look >`


#5.comparing files 

Now for your challenge! There are two files in `/challenge`:

- `/challenge/decoys_only.txt` contains 100 fake flags
- `/challenge/decoys_and_real.txt` contains all 100 fake flags plus the one real flag

Use `diff` to find what's different between these files and get your flag!


**Flag:** `pwn.college{kpbN3f7WvQXUgrlfeUDsQ76XFP6.01MwMDOxwSM0EzNzEzW}`


Command used: `diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt`

The `diff` command finds the difference between two files. It works something like this: 
`diff <file1> <file2>`
That is what I did and obtained the flag. 


#6. listing files 

In this challenge, we've named `/challenge/run` with some random name! List the files in `/challenge` to find it.

**Flag:** `pwn.college{Ug4CLLDbzFPbqkPUBHGZBEYOdW5.QX4IDO0wSM0EzNzEzW}`

commands used: 
`cd /challenge`
`ls`
`11813-renamed-run-6057`

Considering `/challenge/run` was renamed, I had to go to the `/challenge` directory to look for the renamed file using the `cd` command as shown above. 
To actually view which file contained the run file, I used `ls` to view the contents of `/challenge`
I found out the renamed file and ran it using `11813-renamed-run-6057`.



#7. touching files

In this level, create two files: `/tmp/pwn` and `/tmp/college`, and run `/challenge/run` to get your flag!


**Flag:** `pwn.college{M10EPuxLG96G4m0MM2bwvh0pWk1.QXwMDO0wSM0EzNzEzW}`

commands used: 
`touch /tmp/pwn`
`touch /tmp/college`
`/challenge/run`

The `touch` command creates a file in the given directory. The challenge asked me to create two files in the `/tmp` directory and then run `/challenge/run` to get the file. I implemented the same using the commands given above.



#8. removing files 

Let's practice. This challenge will create a `delete_me` file in your home directory! Delete it, then run `/challenge/check`, which will make sure you've deleted it and then give you the flag!

**Flag:** `pwn.college{gyesJ2cu_IXJgl9vJFKs6qMeOJL.QX2kDM1wSM0EzNzEzW}`

commands used: 
`rm delete_me`
`/challenge/check`

The challenge creates a file called `delete_me` in my home directory and my job is to delete it using the `rm` command, therefore I did the same. 
I checked if the file is removed or not using `/challenge/check` which also gave out the flag.



#9. moving files 

This challenge wants you to move the `/flag` file into `/tmp/hack-the-planet` (do it)! When you're done, run `/challenge/check`, which will check things out and give the flag to you.

**Flag:** `pwn.college{MaTyGobTUdUNL-qHVGrd4tJ2x9B.0VOxEzNxwSM0EzNzEzW}`

commands used: `mv /flag /tmp/hack-the-planet`

The challenge has asked me to move `/flag` to `/tmp/hack-the-planet`, I did just that using the `mv` command. 
Checked if the file is moved using the `/challenge/check` command which also gave out the flag. 

#### What I learnt: 

This is how the `mv` command works: 
- `mv <source> <destination>`

Moves the source to the destination, the source can either be a file or a folder.  


#10. hidden files 

Interestingly, `ls` doesn't list _all_ the files by default. Linux has a convention where files that start with a `.` don't show up by default in `ls` and in a few other contexts. To view them with `ls`, you need to invoke `ls` with the `-a` flag, as so:

```
hacker@commands~hidden-files:/$ ls -a
.  ..  .dockerenv  .flag-23427737212232  bin  boot  challenge  dev  etc  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@commands~hidden-files:/$ cat /.flag-23427737212232
pwn.college{McYpEKX7mPe5bXrAfCDrwscAflq.QXwUDO0wSM0EzNzEzW}
```

Now, it's your turn! Go find the flag, hidden as a dot-prepended file in `/`.

**Flag:** `pwn.college{McYpEKX7mPe5bXrAfCDrwscAflq.QXwUDO0wSM0EzNzEzW}`

commands used: 
`cd /`
`ls -a`
`cat /.flag-23427737212232`

Moved to the root directory using the `cd`  command and looked for the `.` prepended file using `ls -a` which lists all files in the present working directory along with the hidden files. 
Read the flag using the `cat` command. 



#11. ### An Epic Filesystem Quest

In this challenge, I have _hidden the flag_! Here, you will use `ls` and `cat` to follow my breadcrumbs and find it! Here's how it'll work:

0. Your first clue is in `/`. Head on over there.
1. Look around with `ls`. There'll be a file named HINT or CLUE or something along those lines!
2. `cat` that file to read the clue!
3. Depending on what the clue says, head on over to the next directory (or don't!).
4. Follow the clues to the flag!

Good luck!

**Flag:** `pwn.college{Q0OPpB8m1j5jlijsbMj23rmwXKz.QX5IDO0wSM0EzNzEzW}`

This is what I did: 

```
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
TRACE  challenge  flag  lib32   media  opt   run   sys  var
bin    dev        home  lib64   mnt    proc  sbin  tmp
boot   etc        lib   libx32  nix    root  srv   usr
hacker@commands~an-epic-filesystem-quest:/$ cat TRACE
Great sleuthing!
The next clue is in: /opt/linux/linux-5.4/Documentation/block

The next clue is *delayed* --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ cd /opt/linux/linux-5.4/Documentation/block
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/block$ ls
DOSSIER                data-integrity.rst    pr.rst
bfq-iosched.rst        deadline-iosched.rst  queue-sysfs.rst
biodoc.rst             index.rst             request.rst
biovecs.rst            ioprio.rst            stat.rst
capability.rst         kyber-iosched.rst     switching-sched.rst
cmdline-partition.rst  null_blk.rst          writeback_cache_control.rst
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/block$ cat DOSSIER
Lucky listing!
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/block$ cat DOSSIER
Lucky listing!
The next clue is in: /opt/linux/linux-5.4/arch/nds32/kernel/vdso
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/block$ cd /opt/linux/linux-5.4/arch/nds32/kernel/vdso
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/nds32/kernel/vdso$ ls
CLUE  Makefile  datapage.S  gen_vdso_offsets.sh  gettimeofday.c  note.S  sigreturn.S  vdso.S  vdso.lds.S
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/nds32/kernel/vdso$ cat CLUE
Congratulations, you found the clue!
The next clue is in: /usr/share/racket/pkgs/datalog/sexp

Watch out! The next clue is *trapped*. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/nds32/kernel/vdso$ ls /usr/share/racket/pkgs/datalog/sexp
INFO-TRAPPED  compiled  lang  lang.rkt
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/nds32/kernel/vdso$ cat ls /usr/share/racket/pkgs/datalog/sexp/INFO-TRAPPED
cat: ls: No such file or directory
Lucky listing!
The next clue is in: /usr/lib/python3/dist-packages/twisted/enterprise/_pycache_

Watch out! The next clue is *trapped*. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/nds32/kernel/vdso$ ls /usr/lib/python3/dist-packages/twisted/enterprise/_pycache_
ALERT-TRAPPED  _init_.cpython-38.pyc  adbapi.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/nds32/kernel/vdso$ cat /usr/lib/python3/dist-packages/twisted/enterprise/_pycache_/ALERT-TRAPPED
Congratulations, you found the clue!
The next clue is in: /opt/linux/linux-5.4/include/config/modules/tree

The next clue is *hidden* --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/nds32/kernel/vdso$ ls -a /opt/linux/linux-5.4/include/config/modules/tree
.  ..  .CUE  lookup.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/nds32/kernel/vdso$ cat /opt/linux/linux-5.4/include/config/modules/tree/.CUE
Great sleuthing!
The next clue is in: /usr/lib/python3/dist-packages/sphinx/transforms/_pycache_

The next clue is *hidden* --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/nds32/kernel/vdso$ ls -a /usr/lib/python3/dist-packages/sphinx/transforms/_pycache_
.  ..  .SPOILER  _init_.cpython-38.pyc  compact_bullet_list.cpython-38.pyc  i18n.cpython-38.pyc  references.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/nds32/kernel/vdso$ cat /usr/lib/python3/dist-packages/sphinx/transforms/_pycache_/.SPOILER
Lucky listing!
The next clue is in: /opt/linux/linux-5.4/drivers/clk/socfpga

The next clue is *hidden* --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/nds32/kernel/vdso$ ls -a /opt/linux/linux-5.4/drivers/clk/socfpga
.  ..  .DISPATCH  Makefile  clk-gate-a10.c  clk-gate-s10.c  clk-gate.c  clk-periph-a10.c  clk-periph-s10.c  clk-periph.c  clk-pll-a10.c  clk-pll-s10.c  clk-pll.c  clk-s10.c  clk.c  clk.h  stratix10-clk.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/nds32/kernel/vdso$ cat /opt/linux/linux-5.4/drivers/clk/socfpga/.DISPATCH
Congratulations, you found the clue!
The next clue is in: /usr/share/javascript/mathjax/jax/output/SVG/fonts/STIX-Web/Alphabets/BoldItalic
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/nds32/kernel/vdso$ ls /usr/share/javascript/mathjax/jax/output/SVG/fonts/STIX-Web/Alphabets/BoldItalic
Main.js  REVELATION
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/nds32/kernel/vdso$ cat /usr/share/javascript/mathjax/jax/output/SVG/fonts/STIX-Web/Alphabets/BoldItalic/REVELATION
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{Q0OPpB8m1j5jlijsbMj23rmwXKz.QX5IDO0wSM0EzNzEzW}
```


#12. making directories 

Now, go forth and create a `/tmp/pwn` directory and make a `college` file in it! Then run `/challenge/run`, which will check your solution and give you the flag!

**Flag:** `pwn.college{Ynnrupsj_ZorxPWNYWEObZ2XuJi.QXxMDO0wSM0EzNzEzW}`

commands used: 
`mkdir /tmp/pwn`
`cd /tmp/pwn`
`touch college`
`/challenge/run`

According to the challenge,  I had to make a directory in the `/tmp` directory called `/pwn`. I did that using the `mkdir` command. I changed my present working directory to `cd /tmp/pwn`. 
As per the challenge, I proceeded by making a file called `college` in the directory using `touch`. 
In the end, I ran `/challenge/run` to obtain the flag. 


#13. finding files 

Now it's your turn. I've hidden the flag in a random directory on the filesystem. It's still called `flag`. Go find it!

**Flag:** `pwn.college{QsxGEwiS2TM4eSQnL5I7T4Ml4xc.QXyMDO0wSM0EzNzEzW}`

Command used: `find / -name flag`

This is how my workflow looked like: 

```
 hacker@commands~finding-files:~$ find / -name flag
find: ‘/root’: Permission denied
find: ‘/proc/1/task/1/fd’: Permission denied
find: ‘/proc/1/task/1/fdinfo’: Permission denied
find: ‘/proc/1/task/1/ns’: Permission denied
find: ‘/proc/1/fd’: Permission denied
find: ‘/proc/1/map_files’: Permission denied
find: ‘/proc/1/fdinfo’: Permission denied
find: ‘/proc/1/ns’: Permission denied
find: ‘/proc/7/task/7/fd’: Permission denied
find: ‘/proc/7/task/7/fdinfo’: Permission denied
find: ‘/proc/7/task/7/ns’: Permission denied
find: ‘/proc/7/fd’: Permission denied
find: ‘/proc/7/map_files’: Permission denied
find: ‘/proc/7/fdinfo’: Permission denied
find: ‘/proc/7/ns’: Permission denied
/home/hacker/flag
find: ‘/var/log/private’: Permission denied
find: ‘/var/log/apache2’: Permission denied
find: ‘/var/log/mysql’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
find: ‘/var/cache/apt/archives/partial’: Permission denied
find: ‘/var/cache/private’: Permission denied
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/php/sessions’: Permission denied
find: ‘/var/lib/mysql-files’: Permission denied
find: ‘/var/lib/private’: Permission denied
find: ‘/var/lib/mysql-keyring’: Permission denied
find: ‘/var/lib/mysql’: Permission denied
find: ‘/tmp/tmp.4mK6TfTSUV’: Permission denied
find: ‘/run/mysqld’: Permission denied
find: ‘/run/sudo’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
/usr/local/lib/python3.8/dist-packages/pwnlib/flag
/usr/share/racket/pkgs/drracket/scribblings/drracket/flag
/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
/nix/store/7ns27apnvn4qj4q5c82x0z1lzixrz47p-radare2-5.9.8/share/radare2/5.9.8/flag
/nix/store/5z3sjp9r463i3siif58hq5wj5jmy5m98-python3.12-pwntools-4.13.1/lib/python3.12/site-packages/pwnlib/flag
/nix/store/5n5lp1m8gilgrsriv1f2z0jdjk50ypcn-rizin-0.7.3/share/rizin/flag
/nix/store/bnlabj2vsbljhp597ir29l51nrqhm89w-rizin-0.7.4/share/rizin/flag
/nix/store/s8b49lb0pqwvw0c6kgjbxdwxcv2bp0x4-radare2-5.9.8/share/radare2/5.9.8/flag
/nix/store/1hyxipvwpdpcxw90l5pq1nvd6s6jdi5m-python3.12-pwntools-4.14.1/lib/python3.12/site-packages/pwnlib/flag
/nix/store/h88mxp2mbgyj06vypwmqpy05idhwimnp-python3.13-pwntools-4.14.1/lib/python3.13/site-packages/pwnlib/flag
/nix/store/5qz6hgb1qzpvjrsw20wyiylx5zw8b9bk-pwntools-4.14.0/lib/python3.13/site-packages/pwnlib/flag
hacker@commands~finding-files:~$ cat /usr/local/lib/python3.8/dist-packages/pwnlib/flag
cat: /usr/local/lib/python3.8/dist-packages/pwnlib/flag: Is a directory
hacker@commands~finding-files:~$ cat /usr/share/racket/pkgs/drracket/scribblings/drracket/flag
pwn.college{QsxGEwiS2TM4eSQnL5I7T4Ml4xc.QXyMDO0wSM0EzNzEzW}
```

The command `find / -name flag` looked over every file in the root directory, whichever matches `flag` will be shown as output. 

I checked every file, finally found the flag at the above mentioned directory. 



#14. linking files 

Okay, now you try it! In this level the flag is, as always, in `/flag`, but `/challenge/catflag` will instead read out `/home/hacker/not-the-flag`. Use the symlink, and fool it into giving you the flag!


**Flag:** `wn.college{oMn_QjX3fqS8eZZJcI47a1bEOpm.QX5ETN1wSM0EzNzEzW}`

Command used: 
`ln -s /flag /home/hacker/not-the-flag`
`/challenge/catflag`


`ln -s` creates a symbolic link to a given source file
This is how it works: 
- `ln -s <source> <destination>`
Here, `/challenge/catflag` will only read out `/home/hacker/not-the-flag`, therefore I need to make a symlink to `/flag`. Using the above commands I did just that. I used `/challenge/catflag` to output me the required flag. 

#### What I learnt: 

In a filesystem, a file is, conceptually, an address at which the contents of that file live. A hard link is an alternate address that indexes that data --- accesses to the hard link and accesses to the original file are completely identical, in that they immediately yield the necessary data. A soft/symbolic link, instead, contains the original file name. When you access the symbolic link, Linux will realize that it is a symbolic link, read the original file name, and then (typically) automatically access that file. In most cases, both situations result in accessing the original data, but the mechanisms are different.
