#1. Learning from Documentation

Welcome to the documentation for `/challenge/challenge`! To properly run this program, you will need to pass it the argument of `--giveflag`. Good luck!

flag: `pwn.college{YXa0BseEDe0dnwWHIBwmWQ_2DZx.QX0ITO0wSM0EzNzEzW}`

Command used: 
`/challenge/challenge --giveflag`


#2. Learning Complex Usage 

Here is this level's documentation for `/challenge/challenge`:

> Welcome to the documentation for `/challenge/challenge`! This program allows you to print arbitrary files to the terminal, when given the `--printfile` argument. The argument to the `--printfile` argument is the path of the flag to read. For example, `/challenge/challenge --printfile /challenge/DESCRIPTION.md` will print out the description of the level!

Given that documentation, go get the flag!


flag: `pwn.college{EjTYniOjrsc_TF1ICRGRw84K5Do.QX1ITO0wSM0EzNzEzW}`

Command used: 
`/challenge/challenge --printfile /flag`

According to the documentation for `/challenge/challenge`, this program allows me to print the contents of the file to the terminal when the `--printfile` argument is passed. 

The `--printfile` should be followed by the absolute file path. 

I put that into practice and got the flag. 



#3. Reading Manuals 

The challenge in this level has a secret option that, when you use it, will cause the challenge to print the flag. You must learn this option through the man page for `challenge`!


flag: `pwn.college{gQgWH32ugkHVitFN96JYji564OW.QX0EDO0wSM0EzNzEzW}`

Commands used: 
`man challenge`
`/challenge/challenge --ggugki 329`

I looked up the manual page for the program `challenge`. 
This is what it gave me: 

In the manual page its written clearly that `/challenge/challenge` will only give out the flag if passed withe the argument `--ggugki 329`, I did that and got the flag. 



#4. Searching Manuals 

Find the option that will give you the flag by reading the `challenge` man page.

flag: ``pwn.college{sL5ZPLZfrXKtgTH7C-g1tizbBK9.QX1EDO0wSM0EzNzEzW}`

Commands used: 
`man challenge`
`search the man page using /flag`
`/challenge/challenge --nxhxfpz`

The challenge is pretty self explanatory, I looked up the `flag` keyword in the man page using `/<keyword>`. I found out you need to pass `--nxhxfpz` argument to `/challenge/challenge` and then I got the flag. 

#5. Searching For Manuals

This level is tricky: it hides the manpage for the challenge by randomizing its name. Luckily, all of the man pages are gathered in a searchable database, so you'll be able to search the man page database to find the hidden challenge man page! To figure out how to search for the right man page, read the `man` page manpage by doing: `man man`!

flag: ` pwn.college{wmrKlrY03o1PbtFcDkz8FzGHOJC.QX2EDO0wSM0EzNzEzW}`

Commands used: 
`man -k challenge`
`man wmrlrobtck  `
`/challenge/challenge --wmrlro 031`

By looking at the manual page for the `man` command, I found out that, you can search for manual entry keywords by passing `-k` argument followed by the keyword. 
That means, whichever manual entry contains that keyword will be shown. 

I used that knowledge to find out which manual entry contains the keyword. 

Looking at the man page for `wmrlrobtck ` , I saw what was needed to get the flag and I got the flag accordingly. 



#6. Helpful Programs: 

Some programs don't have a man page, but might tell you how to run them if invoked with a special argument. Usually, this argument is `--help`, but it can often be `-h` or, in rare cases, `-?`, `help`, or other esoteric values like `/?` (though that latter is more frequently encountered on Windows).

In this level, you will practice reading a program's documentation with `--help`. Try it out!

flag: `pwn.college{EZb80iAUYV09ftG0DnSLK57gxRN.QX3IDO0wSM0EzNzEzW}`

Commands used: 
`/challenge/challenge --help`
`/challenge/challenge -p #to print out the secret value`
`/challenge/challenge --give-the-flag  800`

Passed the `--help` argument to `/challenge/challenge` to look at the docs. This was my workflow: 
```
 hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 800
hacker@man~helpful-programs:~$ /challenge/challenge -g GIVE_THE_FLAG 800
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]
a challenge to make you ask for help: error: argument -g/--give-the-flag: invalid int value: 'GIVE_THE_FLAG'
hacker@man~helpful-programs:~$ /challenge/challenge --give-the-flag 800
Correct usage! Your flag: pwn.college{EZb80iAUYV09ftG0DnSLK57gxRN.QX3IDO0wSM0EzNzEzW}
```


#7. Help for Builtins 

Some good information! In this challenge, we'll practice using `help` to look up help for builtins. This challenge's `challenge` command is a shell builtin, rather than a program. Like before, you need to lookup its help to figure out the secret value to pass to it!

flag: `pwn.college{gdh2wzXAbw_HpYAVDfqLOZiKL9v.QX0ETO0wSM0EzNzEzW}`

Commands used: 
`help challenge`
`challenge --secret gdh2wzXA`

Used the `help` command to look at the docs for the builtin program `challenge`. 
Passed in required arguments to get the flag. 


